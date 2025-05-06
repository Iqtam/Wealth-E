# <div align="center">Wealth-E API Documentation</div>

### <div align="center"> Group 6 (A1) </div>

<div align="center">1. 2005015 - Adibah Mahmud </div>
<div align="center">2. 2005028 - Md. Tamim Iqbal </div>
<div align="center">3. 2005029 - Md. Minhajul Islam Fuad </div>

----------------------------------------------

## Index

---

## Register/Login Module

### Login

| API Endpoint              | HTTP Method | Description |
| ------------------------- | :---------: | :---------: |
| [api/login]()                |   `POST`     | Authenticates a user and returns an access token |


>### Request
>
>#### Request Body
>
>```json
>{
>
>    "id": "jarin@gmail.com",
>    "password": "12345678"
>}
>```
>

>### Response - Success
>
>#### Response Code: 200 (`OK`)
>
>#### Response Body
>
>```json
>{
>    "success": true,
>    "role": "user",
>    "token": "123123"
>}
>```
>
<br>

> [!NOTE]
> Subsequent requests while logged in must contain this token.
<br>

>### Response - Wrong ID or Password
>
>#### Response Code: 401 (`Unauthorized`)
>
>#### Response Body
>
>```json
>{
>    "success": false,
>    "error": "Invalid ID or password"
>}
>```
>
-------------

### Register


#### Get Tax Zone List

| API Endpoint              | HTTP Method | Description |
| ------------------------- | :---------: | :---------: |
| [api/register/zones]()                |   `GET`     |Retrieves the list of available tax zones for user registration|

>#### Request
>
>##### Request Body
>
>```json
>{
>
>}
>```
>
<br>

>#### Response : Success
>
>##### Response Code: 200 (`OK`)
>
>##### Response Body
>
>```json
>{
>    "taxZones": [
>                        "Tax Zone 1", 
>                        "Tax Zone 2",
>                        "Tax Zone 15"
>                 ]
>}
>```
>

#### Get Tax Circle List

| API Endpoint              | HTTP Method | Description |
| ------------------------- | :---------: | :---------: |
| [api/register/circle]()                |   `GET`     | Retrieves the list of available tax circles for user registration|

>### Request
>
>#### Request Body
>
>```json
>{
>   "taxZone" : "Tax Zone 2"
>}
>```
>

>### Response
>
>#### Response Code: 200 (`OK`)
>
>#### Response Body
>
>```json
>{
>    "taxCircles": [
>                        "Tax Circle 75", 
>                        "Tax Circle 76",
>                        "Tax Circle 78"
>                   ]
>}
>```
>


### Submit Registration Request

| API Endpoint              | HTTP Method | Description |
| ------------------------- | :---------: | :---------: |
| [api/register/submit]()                |   `POST`     |Submits a new user registration with personal and tax information|

>### Request
>
>#### Request Body
>
>```json
>{
>    "email": "jarin@gmail.com",
>    "name": "Jarin Tasneem",
>    "nid": 1234567890,
>    "tin": 232345456767,
>    "mobile": 0123456789,
>    "taxZone": 15,
>    "taxCircle": 78,
>    "dob": "02-02-1990",
>    "spouse": "",
>    "spouseTIN": null,
>    "isResidential": true,
>    "benefittedPerson": {
>           "isFF": false,
>           "isFemale": true,
>           "isDisabled": false               
>       }  
>}
>```
>


>### Response - Success
>
>#### Response Code: 201 (`Created`)
>
>#### Response Body
>
>```json
>{
>    "success": true,
>    "token": "1234cdb32"
>}
>```


>### Response - Invalid Input
>
>#### Response Code: 422 (`Unprocessable Entity`)
>
>#### Response Body
>
>```json
>{
>    "success": false,
>    "error": "Invalid {field}"
>}
>```
>

<br>

### Personal Info

| API Endpoint              | HTTP Method | Description |
| ------------------------- | :---------: | :---------: |
| [api/profile]()                |   `GET`     | Returns profile information of the user|

>### Request
>
>#### Request Body
>
>```json
>{
>   
>    
>}
>```
>
<br>

<br>

>### Response - Success
>
>#### Response Code: 200 (`OK`)
>
>#### Response Body
>
>```json
>{
>    "email": "jarin@gmail.com",
>    "name": "Jarin Tasneem",
>    "nid": 1234567890,
>    "tin": 232345456767,
>    "mobile": 0123456789,
>    "taxZone": 15,
>    "taxCircle": 78,
>    "dob": "02-02-1990",
>    "spouse": "",
>    "spouseTIN": null,
>    "isResidential": true,
>    "benefittedPerson": {
>           "isFF": false,
>           "isFemale": true,
>           "isDisabled": false               
>   }    
>}
>````
>
<br>

### Update Personal Info

| API Endpoint              | HTTP Method | Description |
| ------------------------- | :---------: | :---------: |
| [api/update_profile]()                |   `POST`     |Updates profile of the user|

>### Request
>
>#### Request Body
>
>```json
>{
>   "email": "jarin@gmail.com",
>   "name": "Jarin Tasneem",
>   "nid": 1234567890,
>   "tin": 232345456767,
>   "mobile": "0123456789",
>   "taxZone": 15,
>   "taxCircle": 76,
>   "dob": "1990-02-02",
>   "spouse": "",
>   "spouseTIN": null,
>   "isResidential": true,
>   "benefittedPerson": {
>       "isFF": true,
>       "isFemale": true,
>       "isDisabled": false
>   }
> }
>```
>

>### Response - Success
>
>#### Response Code: 200 (`OK`)
>
>#### Response Body
>
>```json
>{
>   "message": "Profile updated successfully",
>   "profile": {
>   "email": "jarin@gmail.com",
>   "name": "Jarin Tasneem",
>   "nid": 1234567890,
>   "tin": 232345456767,
>   "mobile": "0123456789",
>   "taxZone": 15,
>   "taxCircle": 76,
>   "dob": "1990-02-02",
>   "spouse": "",
>   "spouseTIN": null,
>   "isResidential": true,
>   "benefittedPerson": {
>       "isFF": true,
>       "isFemale": true,
>       "isDisabled": false
>   }
>   }
> }
>```
>
<br>

-----------

## Income Module

### Empoyment Income

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/employment]() |    `POST`    | Add new employment income        |

 ### Request

 #### Request Body

```json
    {
    "employmentType": "Basic pay",
    "incomeType": "Government Pay scale",
    "amount": 50000,
    "exemptedAmount": 4000,
    "date": "05-11-2024"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "income/employment"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/employment]() |    `GET`    | List all employment incomes        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "employment_incomes": [
>           {
>               "id": 123456789,
>               "employmentType": "Government Pay scale",
>               "incomeType": "Basic pay",
>               "amount": 50000,
>               "exemptedAmount": 4000,
>               "date": "05-11-2024"
>           },
>           {
>               "id": 123456789,
>               "employmentType": "Non-Government Pay scale",
>               "incomeType": "Transportation",
>               "amount": 5000,
>               "exemptedAmount": 4000,
>               "date": "05-11-2024"
>           },
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/employment/:id]() |    `GET`    | Returns requested employment income      |


> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>         "id": 123456789,
>         "employmentType": "Government Pay scale",
>         "incomeType": "Basic pay",
>         "amount": 50000,
>         "exemptedAmount": 4000,
>         "date": "05-11-2024"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/employment]() |    `POST`    | Update employment income       |

> ### Request
>
> #### Request Body

```json
    {
    "id": 123456789,
    "employmentType": "Government Pay scale",
    "incomeType": "Basic pay",
    "amount": 50000,
    "exemptedAmount": 4000,
    "date": "05-11-2024"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Employment income updated successfully",
    "employment_income": {
        "id": 123456789,
        "employmentType": "Government Pay scale",
        "incomeType": "Basic pay",
        "amount": 52000,
        "exemptedAmount": 4000,
        "date": "2024-11-05"
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/employment/:id]() |    `DELETE`    | Delete employment income with specific id     |

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Employment income deleted successfully"
    }

```

---

### Rental Income

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/rent]() |    `POST`    | Add new rental income        |

> ### Request
>
> #### Request Body

```json
    {
    "incomeType": "Rent received",
    "amount": 50000,
    "allowable_deduction": 4000,
    "date": "05-11-2024"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "income/rent"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/rent]() |    `GET`    | List all rent incomes        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "rent_incomes": [
> 
>            {
>            "incomeType": "Rent received for flat 2/A",
>            "amount": 10000,
>            "allowable_deduction": 4000,
>            "date": "05-11-2024"
>            },
>            {
>            "incomeType": "Rent received",
>            "amount": 50000,
>            "allowable_deduction": 5000,
>            "date": "05-11-2024"
>            }
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/rent/:id]() |    `GET`    | Returns requested rent income      |


> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>               "id": 123456789,
>               "incomeType": "Rental Income",
>               "amount": 50000,
>               "exemptedAmount": 4000,
>               "date": "05-11-2024"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/rent]() |    `POST`    | Update rent income       |

> ### Request
>
> #### Request Body

```json
    {
    "id": 123456789,
    "incomeType": "Basic pay",
    "amount": 50000,
    "allowable_deduction": 4000,
    "date": "05-11-2024"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Employment income updated successfully",
    "rent_income": {
        "id": 123456789,
        "incomeType": "Government Pay scale",
        "amount": 52000,
        "allowable_deduction": 4000,
        "date": "2024-11-05"
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/rent/:id]() |    `DELETE`    | Delete rent income  with specific id     |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Rent income deleted successfully"
    }

```

---

### Agricultural Income

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/agriculture]() |    `POST`    | Add new agriculture income        |

 ### Request

 #### Request Body

```json
    {
    "incomeType": "Government Pay scale",
    "sellingPrice": 50000,
    "profit": 4000,
    "date": "05-11-2024"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "income/agriculture"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/agriculture]() |    `GET`    | List all agriculture incomes        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "agriculture_incomes": [
>           {
>               "id": 123456789,
>               "incomeType": "Basic pay",
>               "sellingPrice": 50000,
>               "profit": 4000,
>               "date": "05-11-2024"
>           },
>           {
>               "id": 123456789,
>               "incomeType": "Transportation",
>               "sellingPrice": 50000,
>               "profit": 4000,
>               "date": "05-11-2024"
>           },
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/agriculture/:id]() |    `GET`    | Returns requested agriculture income      |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>               "id": 123456789,
>               "incomeType": "Basic pay",
>               "sellingPrice": 50000,
>               "profit": 4000,
>               "date": "05-11-2024"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/agriculture]() |    `POST`    | Update agriculture income       |

> ### Request
>
> #### Request Body

```json
    {
    "id": 123456789,
    "incomeType": "Basic pay",
    "sellingPrice": 50000,
    "profit": 4000,
    "date": "05-11-2024"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Agriculture income updated successfully",
    "employment_income": {
        "id": 123456789,
        "incomeType": "Basic pay",
        "sellingPrice": 52000,
        "profit": 4000,
        "date": "2024-11-05"
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/income/agriculture/:id]() |    `DELETE`    | Delete agriculture income       |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Agriculture income deleted successfully"
    }

```

---

## Expense Module


| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/expense]() |    `POST`    | Add expenditure       |

 ### Request

 #### Request Body

```json
    {
    "expenseType": "Basic pay",
    "description": "Government Pay scale",
    "amount": 50000,
    "date": "05-11-2024"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "expense"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/expense]() |    `GET`    | List all expenses        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "expenses": [
>           {
>               "id": 123456789,
>               "expenseType": "Government Pay scale",
>               "description": "Basic pay",
>               "amount": 50000,
>               "date": "05-11-2024"
>           },
>           {
>               "id": 123456789,
>               "expenseType": "Non-Government Pay scale",
>               "description": "Transportation",
>               "amount": 5000,
>               "date": "05-11-2024"
>           },
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/expense/:id]() |    `GET`    | Returns requested expense      |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>               "id": 123456789,
>               "expenseType": "Government Pay scale",
>               "description": "Basic pay",
>               "amount": 50000,
>               "date": "05-11-2024"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/expense]() |    `POST`    | Update expense     |

> ### Request
>
> #### Request Body

```json
    {
            "id": 123456789,
            "expenseType": "Government Pay scale",
            "description": "Basic pay",
            "amount": 50000,
            "date": "05-11-2024"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Expense updated successfully",
    "expenses":    {
            "id": 123456789,
            "expenseType": "Government Pay scale",
            "description": "Basic pay",
            "amount": 50000,
            "date": "05-11-2024"
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/expense/:id]() |    `DELETE`    | Delete expense      |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Expense deleted successfully"
    }

```

---

-----------

## Asset Module

### Agricultural Property

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/agriculture]() |    `POST`    | Add new agricultural property        |

 ### Request

 #### Request Body

```json
    {
    "name": "Farm",
    "costValue": 50000,
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "asset/agriculture"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/agriculture]() |    `GET`    | List all agricultural property        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "agricultural_property ": [
>           {
>               "id": 123456789,
>               "name": "Farm",
>               "costValue": 50000,
>               "location": "Mirpur",
>               "aquisitionType": "Inheritance",
>               "date": "05-11-2024",
>               "description": "demo"
>           },
>           {
>               "id": 123456788,
>               "name": "Pond",
>               "costValue": 50000,
>               "location": "Mirpur",
>               "aquisitionType": "Inheritance",
>               "date": "05-11-2024",
>               "description": "demo"
>           }
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/agriculture/:id]() |    `GET`    | Returns requested agricultural property      |


> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>           {
>               "id": 123456788,
>               "name": "Pond",
>               "costValue": 50000,
>               "location": "Mirpur",
>               "aquisitionType": "Inheritance",
>               "date": "05-11-2024",
>               "description": "demo"
>           }
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/agriculture]() |    `POST`    | Update agricultural property       |

> ### Request
>
> #### Request Body

```json
    {
    "id": 123456789,
    "name": "Pond",
    "costValue": 50000,
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Agricultural property updated successfully",
    "agricultural_property": {
    "id": 123456789,
    "name": "Pond",
    "costValue": 50000,
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```


| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/agriculture/sell]() |    `POST`    | Sell an agricultural property       |

> ### Request
>
> #### Request Body

```json
    {
    "id": 123456789,
    "name": "Pond",
    "costValue": 50000,
    "sellAmount": 60000,
    "depositAccount": "Cash",
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Agricultural property sell recorded successfully",
    "agricultural_property": {
    "id": 123456789,
    "name": "Pond",
    "costValue": 50000,
    "sellAmount": 60000,
    "depositAccount": "Cash",
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/agriculture/:id]() |    `DELETE`    | Delete agricultural property       |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Agricultural property deleted successfully"
    }

```

---

### Non-Agricultural Property

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/non_agriculture]() |    `POST`    | Add non-agricultural property        |

 ### Request

 #### Request Body

```json
    {
    "name": "Plot",
    "costValue": 50000,
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "asset/non_agriculture"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/non_agriculture]() |    `GET`    | List all non-agricultural property        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "non_agricultural_property ": [
>           {
>               "id": 123456789,
>               "name": "Plot",
>               "costValue": 50000,
>               "location": "Mirpur",
>               "aquisitionType": "Inheritance",
>               "date": "05-11-2024",
>               "description": "demo"
>           },
>           {
>               "id": 123456788,
>               "name": "Plot-1",
>               "costValue": 50000,
>               "location": "Mirpur",
>               "aquisitionType": "Inheritance",
>               "date": "05-11-2024",
>               "description": "demo"
>           }
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/non_agriculture/:id]() |    `GET`    | Returns requested non-agricultural property      |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>               "id": 123456788,
>               "name": "Plot",
>               "costValue": 50000,
>               "location": "Mirpur",
>               "aquisitionType": "Inheritance",
>               "date": "05-11-2024",
>               "description": "demo"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/non_agriculture]() |    `POST`    | Update non-agricultural property       |

> ### Request
>
> #### Request Body

```json
    {
    "id": 123456789,
    "name": "Plot",
    "costValue": 50000,
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Non-Agricultural property updated successfully",
    "non_agricultural_property": {
    "id": 123456789,
    "name": "Plot",
    "costValue": 50000,
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```


| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/non_agriculture/sell]() |    `POST`    | Sell an non_agricultural property       |

> ### Request
>
> #### Request Body

```json
    {
    "id": 123456789,
    "name": "Plot",
    "costValue": 50000,
    "sellAmount": 60000,
    "depositAccount": "Cash",
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Non-Agricultural property sell recorded successfully",
    "agricultural_property": {
    "id": 123456789,
    "name": "Plot",
    "costValue": 50000,
    "sellAmount": 60000,
    "depositAccount": "Cash",
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/non_agriculture/:id]() |    `DELETE`    | Delete non-agricultural property       |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Non-Agricultural property deleted successfully"
    }

```
---

### Motor Vehicle

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/motor_vehicle]() |    `POST`    | Add momor vehicle        |

 ### Request

 #### Request Body

```json
    {
    "name": "Toyota",
    "type": "Car",
    "costValue": 50000,
    "reg_number": "Ka-12345",
    "engine_capacity": "2000 cc",
    "date": "05-11-2024",
    "description": "demo"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "asset/motor_vehicle"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/motor_vehicle]() |    `GET`    | List all motor vehicle property        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "motor_vehicles": [
>           {
>               "id": 123456789,
>               "name": "Toyota",
>               "type": "Car",
>               "costValue": 50000,
>               "reg_number": "Ka-12345",
>               "engine_capacity": "2000 cc",
>               "date": "05-11-2024",
>               "description": "demo"
>           },
>           {
>               "id": 123456786,
>               "name": "Toyota",
>               "type": "Car",
>               "costValue": 50000,
>               "reg_number": "Ka-12345",
>               "engine_capacity": "2000 cc",
>               "date": "05-11-2024",
>               "description": "demo"
>           }
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/motor_vehicle/:id]() |    `GET`    | Returns requested motor vehicle property      |


> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>               "id": 123456789,
>               "name": "Toyota",
>               "type": "Car",
>               "costValue": 50000,
>               "reg_number": "Ka-12345",
>               "engine_capacity": "2000 cc",
>               "date": "05-11-2024",
>               "description": "demo"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/motor_vehicle]() |    `POST`    | Update motor_vehicle property       |

> ### Request
>
> #### Request Body

```json
    {
    "name": "Toyota",
    "type": "Car",
    "costValue": 50000,
    "reg_number": "Ka-12345",
    "engine_capacity": "2000 cc",
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Motor vehicles property updated successfully",
    "motor_vehicles":     {
    "name": "Toyota",
    "type": "Car",
    "costValue": 50000,
    "reg_number": "Ka-12345",
    "engine_capacity": "2000 cc",
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```


| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/motor_vehicle/sell]() |    `POST`    | Sell an non_agricultural property       |

> ### Request
>
> #### Request Body

```json
    {
    "id": 123456789,
    "name": "Toyota",
    "type": "Car",
    "costValue": 50000,
    "sellAmount": 60000,
    "depositAccount": "Cash",
    "reg_number": "Ka-12345",
    "engine_capacity": "2000 cc",
    "date": "05-11-2024"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Motor vehicle property sell recorded successfully",
    "motor_vehicles": {
    "id": 123456789,
    "name": "Plot",
    "costValue": 50000,
    "sellAmount": 60000,
    "depositAccount": "Cash",
    "location": "Mirpur",
    "aquisitionType": "Inheritance",
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/motor_vehicle/:id]() |    `DELETE`    | Delete motor_vehicle property       |

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Motor_vehicle property deleted successfully"
    }

```

### Ornaments

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/ornament]() |    `POST`    | Add new ornament       |

 ### Request

 #### Request Body

```json
    {
    "name": "Gold",
    "aquisitionType": "Inheritance",
    "costValue": 50000,
    "unit": 2,
    "quantity": 3,
    "date": "05-11-2024",
    "description": "demo"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "asset/ornament"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/ornament]() |    `GET`    | List all ornaments        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "ornament": [
>           {
>               "id": 123456789,
>               "name": "Gold",
>               "aquisitionType": "Inheritance",
>               "costValue": 50000,
>               "unit": 2,
>               "quantity": 3,
>               "date": "05-11-2024",
>               "description": "demo"
>           },
>           {
>               "id": 123456788,
>               "name": "Diamond",
>               "aquisitionType": "Inheritance",
>               "costValue": 500000,
>               "unit": 2,
>               "quantity": 3,
>               "date": "05-11-2024",
>               "description": "demo"
>           }
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/ornament/:id]() |    `GET`    | Returns requested ornament      |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
>           {
>               "id": 123456788,
>               "name": "Diamond",
>               "aquisitionType": "Inheritance",
>               "costValue": 500000,
>               "unit": 2,
>               "quantity": 3,
>               "date": "05-11-2024",
>               "description": "demo"
>           }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/ornament]() |    `POST`    | Update ornament       |

> ### Request
>
> #### Request Body
```json
    {
    "name": "Gold",
    "aquisitionType": "Inheritance",
    "costValue": 50000,
    "unit": 2,
    "quantity": 3,
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Ornament updated successfully",
    "ornament":     {
    "name": "Gold",
    "aquisitionType": "Inheritance",
    "costValue": 50000,
    "unit": 2,
    "quantity": 3,
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```


| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/ornament/sell]() |    `POST`    | Sell an ornament       |

> ### Request
>
> #### Request Body

```json
    {
    "id": 123456789,
    "sellAmount": 60000,
    "depositAccount": "Cash",
    "bank_account": 4404001111111
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Ornament sell recorded successfully",
    "ornament": {
    "id": 123456789,
    "name": "Gold",
    "costValue": 50000,
    "sellAmount": 60000,
    "depositAccount": "Cash",
    "aquisitionType": "Inheritance",
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/ornament/:id]() |    `DELETE`    | Delete ornament       |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Ornament deleted successfully"
    }

```

---

### Sanchaypatra

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/sanchaypatra]() |    `POST`    | Add new sanchaypatra       |

 ### Request

 #### Request Body

```json
    {
    "name": "Family Sanchaypatra",
    "aquisitionType": "Inheritance",
    "costValue": 50000,
    "bank_account": 440400111111,
    "date": "05-11-2024",
    "description": "demo"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "asset/sanchaypatra"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/sanchaypatra]() |    `GET`    | List all sanchaypatra        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "sanchaypatra": [
>           {
>               "id": 123456789,
>               "name": "10 Year Sanchaypatra",
>               "aquisitionType": "Inheritance",
>               "costValue": 50000,
>               "bank_account": 440400111111,
>               "date": "05-11-2024",
>               "description": "demo"
>           },
>           {
>               "id": 123456788,
>               "name": "5 Year Sanchaypatra",
>               "aquisitionType": "Inheritance",
>               "costValue": 500000,
>               "bank_account": 440400111111,
>               "date": "05-11-2024",
>               "description": "demo"
>           }
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/sanchaypatra/:id]() |    `GET`    | Returns requested sanchaypatra      |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
>           {
>               "id": 123456788,
>               "name": "5 Year Sanchaypatra",
>               "aquisitionType": "Inheritance",
>               "costValue": 500000,
>               "bank_account": 440400111111,
>               "date": "05-11-2024",
>               "description": "demo"
>           }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/sanchaypatra]() |    `POST`    | Update sanchaypatra       |

> ### Request
>
> #### Request Body
```json
    {
    "name": "Gold",
    "aquisitionType": "Inheritance",
    "costValue": 50000,
    "bank_account": 440400111111,
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Sanchaypatra updated successfully",
    "sanchaypatra":     {
    "name": "5 Year Sanchaypatra",
    "aquisitionType": "Inheritance",
    "costValue": 50000,
    "bank_account": 440400111111,
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```


| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/asset/sanchaypatra/:id]() |    `DELETE`    | Delete sanchaypatra       |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Sanchaypatra deleted successfully"
    }

```


-----------

## Liability Module

### Bank Loan

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/bank_loan]() |    `POST`    | Add new bank loan        |

 ### Request

 #### Request Body

```json
    {
    "name": "Brac Bank",
    "amount": 50000,
    "paid_amount": 1000,
    "interest_rate": 15,
    "date": "05-11-2024",
    "description": "demo"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "liability/bank_loan"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/bank_loan]() |    `GET`    | List all bank loans        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "liabilities ": [
>           {
>               "id": 123456789,
>               "name": "Brac Bank",
>               "amount": 50000,
>               "paid_amount": 1000,
>               "interest_rate": 15,
>               "date": "05-11-2024",
>               "description": "demo"
>           },
>           {
>               "id": 123456788,
>               "name": "Brac Bank",
>               "amount": 50000,
>               "paid_amount": 1000,
>               "interest_rate": 15,
>               "date": "05-11-2024",
>               "description": "demo"
>           }
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/bank_loan/:id]() |    `GET`    | Returns requested bank loan     |


> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>           {
>               "id": 123456789,
>               "name": "Brac Bank",
>               "amount": 50000,
>               "paid_amount": 1000,
>               "interest_rate": 15,
>               "date": "05-11-2024",
>               "description": "demo"
>           }
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/bank_loan]() |    `POST`    | Update bank loan       |

> ### Request
>
> #### Request Body


```json
    {
    "name": "Brac Bank",
    "amount": 50000,
    "paid_amount": 1000,
    "interest_rate": 15,
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Bank loan updated successfully",
    "liabilities": {
    "name": "Brac Bank",
    "amount": 50000,
    "paid_amount": 1000,
    "interest_rate": 15,
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/bank_loan/credit]() |    `POST`    | Update bank loan       |

> ### Request
>
> #### Request Body


```json
    {
        "loanId": "L1011",
        "name": "Brac bank",
        "creditAmount": 20000,
        "date": "2024-10-24"
    }

```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
{
  "status": "success",
  "message": "Loan credited successfully",
  "loanId": "L1011"
}

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/bank_loan/:id]() |    `DELETE`    | Delete bank loan       |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Bank loan deleted successfully"
    }

```

---

### Personal Loan

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/personal_loan]() |    `POST`    | Add new personal loan        |

 ### Request

 #### Request Body

```json
    {
    "name": "Personal loan-1",
    "amount": 50000,
    "paid_amount": 1000,
    "interest_rate": 15,
    "date": "05-11-2024",
    "description": "demo"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "liability/personal_loan"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/personal_loan]() |    `GET`    | List all personal loans        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "liabilities ": [
>           {
>               "id": 123456789,
>               "name": "Brac Bank",
>               "amount": 50000,
>               "paid_amount": 1000,
>               "interest_rate": 15,
>               "date": "05-11-2024",
>               "description": "demo"
>           },
>           {
>               "id": 123456788,
>               "name": "Brac Bank",
>               "amount": 50000,
>               "paid_amount": 1000,
>               "interest_rate": 15,
>               "date": "05-11-2024",
>               "description": "demo"
>           }
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/personal_loan/:id]() |    `GET`    | Returns requested personal loan     |


> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>           {
>               "id": 123456789,
>               "name": "Brac Bank",
>               "amount": 50000,
>               "paid_amount": 1000,
>               "interest_rate": 15,
>               "date": "05-11-2024",
>               "description": "demo"
>           }
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/personal_loan]() |    `POST`    | Update personal loan       |

> ### Request
>
> #### Request Body


```json
    {
    "name": "Brac Bank",
    "amount": 50000,
    "paid_amount": 1000,
    "interest_rate": 15,
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Personal loan updated successfully",
    "liabilities": {
    "name": "Brac Bank",
    "amount": 50000,
    "paid_amount": 1000,
    "interest_rate": 15,
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/personal_loan/credit]() |    `POST`    | Credit personal loan       |

> ### Request
>
> #### Request Body


```json
    {
        "loanId": "L1011",
        "name": "PL-1",
        "creditAmount": 20000,
        "date": "2024-10-24"
    }

```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
{
  "status": "success",
  "message": "Loan credited successfully",
  "loanId": "L1011"
}

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/liability/personal_loan/:id]() |    `DELETE`    | Delete personal loan       |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Personal loan deleted successfully"
    }

```

-----------

## Investment Module

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/investment]() |    `POST`    | Add new Investment      |

 ### Request

 #### Request Body

```json
    {
    "type": "Fixed Deposit",
    "amount": 50000,
    "duration": "2 years",
    "date": "05-11-2024",
    "description": "demo"
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
>   ```json
>   {
>       "success": true,
>       "redirectURL": "investment"
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/investment]() |    `GET`    | List all Investments        |

> ### Request
>
> #### Request Body

```json
    {
    
    }
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>       "investments": [
>           {
>               "id": 123456789,
>               "type": "Fixed Deposit",
>               "amount": 50000,
>               "duration": "2 years",
>               "date": "05-11-2024",
>               "description": "demo"
>           },
>           {
>               "id": 123456789,
>               "type": "Fixed Deposit",
>               "amount": 50000,
>               "duration": "2 years",
>               "date": "05-11-2024",
>               "description": "demo"
>           }
>       ],
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/investment/:id]() |    `GET`    | Returns requested Investment     |


> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>           {
>               "id": 123456789,
>               "type": "Fixed Deposit",
>               "amount": 50000,
>               "duration": "2 years",
>               "date": "05-11-2024",
>               "description": "demo"
>           }
> }
> ```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/investment]() |    `POST`    | Update Investment       |

> ### Request
>
> #### Request Body


```json
    {
    "id": 123456789,
    "type": "Fixed Deposit",
    "amount": 50000,
    "duration": "2 years",
    "date": "05-11-2024",
    "description": "demo"
    }
```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Investment updated successfully",
    "investments": {
    "id": 123456789,
    "type": "Fixed Deposit",
    "amount": 50000,
    "duration": "2 years",
    "date": "05-11-2024",
    "description": "demo"
    }
    }

```


| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/investment/:id]() |    `DELETE`    | Delete Investment       |


 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Investment deleted successfully"
    }

```

| API Endpoint         | HTTP Method | Description |
| -------------------- | :---------: | :---------: |
| [/api/investment/liquidate/:id]() |    `POST`    | Liquidate Investment       |

> ### Request
>
> #### Request Body
>```json
>    {
>    "amount": 50000,
>    "bank_account": 4404001234567
>    }
>```

 ### Response - Success

 #### Response Code : 200 (`OK`)

 #### Response Body

```json
    {
    "message": "Investment liquidated successfully",
    "investment": {
    "id": 123456789,
    "type": "Fixed Deposit",
    "amount": 50000,
    "bank_account": 4404001234567,
    "transferred_amount": 10000,
    "account_balance": 150000
    }
    }

```
-----------------

