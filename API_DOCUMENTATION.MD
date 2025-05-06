# <div align="center">Wealth-E API Documentation</div>

### <div align="center"> Group 6 (A1) </div>

<div align="center">1. 2005015 - Adibah Mahmud </div>
<div align="center">2. 2005028 - Md. Tamim Iqbal </div>
<div align="center">3. 2005029 - Md. Minhajul Islam Fuad </div>

---

## Index

- [Wealth-E API Documentation](#wealth-e-api-documentation)
    - [ Group 6 (A1) ](#-group-6-a1-)
  - [Index](#index)
  - [Modules](#modules)
  - [Register/Login Module](#registerlogin-module)
    - [Login](#login)
    - [Register](#register)
      - [Get Tax Zone List](#get-tax-zone-list)
    - [Get Tax Circle List](#get-tax-circle-list)
    - [Submit Registration Request](#submit-registration-request)
    - [Personal Info](#personal-info)
    - [Update Personal Info](#update-personal-info)
  - [Income Module](#income-module)
    - [Employment Income](#employment-income)
  - [](#)
    - [Response - Success](#response---success)
      - [Response Code : 200 (`OK`)](#response-code--200-ok)
      - [Response Body](#response-body)
    - [Response - Success](#response---success-1)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-1)
      - [Response Body](#response-body-1)
    - [Rental Income](#rental-income)
    - [Response - Success](#response---success-2)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-2)
      - [Response Body](#response-body-2)
    - [Response - Success](#response---success-3)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-3)
      - [Response Body](#response-body-3)
    - [Agricultural Income](#agricultural-income)
    - [Request](#request)
      - [Request Body](#request-body)
    - [Response - Success](#response---success-4)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-4)
      - [Response Body](#response-body-4)
    - [Response - Success](#response---success-5)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-5)
      - [Response Body](#response-body-5)
  - [Expense Module](#expense-module)
    - [Request](#request-1)
      - [Request Body](#request-body-1)
    - [Response - Success](#response---success-6)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-6)
      - [Response Body](#response-body-6)
    - [Response - Success](#response---success-7)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-7)
      - [Response Body](#response-body-7)
  - [Asset Module](#asset-module)
    - [Agricultural Property](#agricultural-property)
    - [Request](#request-2)
      - [Request Body](#request-body-2)
    - [Response - Success](#response---success-8)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-8)
      - [Response Body](#response-body-8)
    - [Response - Success](#response---success-9)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-9)
      - [Response Body](#response-body-9)
    - [Response - Success](#response---success-10)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-10)
      - [Response Body](#response-body-10)
    - [Non-Agricultural Property](#non-agricultural-property)
    - [Request](#request-3)
      - [Request Body](#request-body-3)
    - [Response - Success](#response---success-11)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-11)
      - [Response Body](#response-body-11)
    - [Response - Success](#response---success-12)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-12)
      - [Response Body](#response-body-12)
    - [Response - Success](#response---success-13)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-13)
      - [Response Body](#response-body-13)
    - [Motor Vehicle](#motor-vehicle)
    - [Request](#request-4)
      - [Request Body](#request-body-4)
    - [Response - Success](#response---success-14)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-14)
      - [Response Body](#response-body-14)
    - [Response - Success](#response---success-15)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-15)
      - [Response Body](#response-body-15)
    - [Response - Success](#response---success-16)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-16)
      - [Response Body](#response-body-16)
    - [Ornaments](#ornaments)
    - [Request](#request-5)
      - [Request Body](#request-body-5)
    - [Response - Success](#response---success-17)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-17)
      - [Response Body](#response-body-17)
    - [Response - Success](#response---success-18)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-18)
      - [Response Body](#response-body-18)
    - [Response - Success](#response---success-19)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-19)
      - [Response Body](#response-body-19)
    - [Sanchaypatra](#sanchaypatra)
    - [Request](#request-6)
      - [Request Body](#request-body-6)
    - [Response - Success](#response---success-20)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-20)
      - [Response Body](#response-body-20)
    - [Response - Success](#response---success-21)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-21)
      - [Response Body](#response-body-21)
  - [Liability Module](#liability-module)
    - [Bank Loan](#bank-loan)
    - [Request](#request-7)
      - [Request Body](#request-body-7)
    - [Response - Success](#response---success-22)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-22)
      - [Response Body](#response-body-22)
    - [Response - Success](#response---success-23)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-23)
      - [Response Body](#response-body-23)
    - [Response - Success](#response---success-24)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-24)
      - [Response Body](#response-body-24)
    - [Personal Loan](#personal-loan)
    - [Request](#request-8)
      - [Request Body](#request-body-8)
    - [Response - Success](#response---success-25)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-25)
      - [Response Body](#response-body-25)
    - [Response - Success](#response---success-26)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-26)
      - [Response Body](#response-body-26)
    - [Response - Success](#response---success-27)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-27)
      - [Response Body](#response-body-27)
  - [Investment Module](#investment-module)
    - [Request](#request-9)
      - [Request Body](#request-body-9)
    - [Response - Success](#response---success-28)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-28)
      - [Response Body](#response-body-28)
    - [Response - Success](#response---success-29)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-29)
      - [Response Body](#response-body-29)
    - [Response - Success](#response---success-30)
      - [Response Code : 200 (`OK`)](#response-code--200-ok-30)
      - [Response Body](#response-body-30)
  - [Tax Module](#tax-module)
    - [Tax estimation](#tax-estimation)
    - [Rebate Plans](#rebate-plans)
    - [Respond to Selected Rebate Plans](#respond-to-selected-rebate-plans)
    - [All tax returns](#all-tax-returns)
    - [Employment Income APIs](#employment-income-apis)
    - [Agricultural income APIs](#agricultural-income-apis)
    - [Tax Exempted Income](#tax-exempted-income)
    - [Investment related APIs](#investment-related-apis)
    - [Get Total Income Overview](#get-total-income-overview)
    - [Get Tax Computation](#get-tax-computation)
    - [Generate Return PDF Preview (Before Submission)](#generate-return-pdf-preview-before-submission)
    - [Finalize Submission](#finalize-submission)
    - [Download Finalized Return PDF](#download-finalized-return-pdf)
    - [Check Submission Status](#check-submission-status)
  - [AI features](#ai-features)
    - [AI Chatbot- Tax Q\&A](#ai-chatbot--tax-qa)
    - [Tax Breakdown Explanation](#tax-breakdown-explanation)
    - [Rebate Investment Optimizer](#rebate-investment-optimizer)
  - [Admin Module](#admin-module)
    - [Tax Rules on Income](#tax-rules-on-income)
      - [Show Income Slabs](#show-income-slabs)
      - [Edit No Tax Threshold](#edit-no-tax-threshold)
      - [Edit Common Slabs](#edit-common-slabs)
      - [Get Categories](#get-categories)
      - [Edit Categories](#edit-categories)
    - [Investment Sectors](#investment-sectors)
      - [Get Investment options](#get-investment-options)
      - [Add Investment Option](#add-investment-option)
      - [Edit Investment Option](#edit-investment-option)
    - [Tax Zone Rules](#tax-zone-rules)
      - [Get Tax Zone Rules](#get-tax-zone-rules)
      - [Edit Tax Zone Rules](#edit-tax-zone-rules)
    - [Rebate Rules](#rebate-rules)
      - [Get Rebate Rules](#get-rebate-rules)
      - [Edit Rebate Rules](#edit-rebate-rules)
    - [Admin File Section](#admin-file-section)
      - [Get Return List](#get-return-list)
      - [View a Return](#view-a-return)
      - [Get Individual Return](#get-individual-return)
      - [Update Tax Return Status](#update-tax-return-status)

---

## Modules

## Register/Login Module

### Login

| API Endpoint  | HTTP Method |                   Description                    |
| ------------- | :---------: | :----------------------------------------------: |
| [api/login]() |   `POST`    | Authenticates a user and returns an access token |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "id": "jarin@gmail.com",
>   "password": "12345678"
> }
> ```
>
 </br>

> ### Response - Success
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "success": true,
>   "role": "user",
>   "token": "123123"
> }
> ```
>
> <br>

---

> [!NOTE]
> Subsequent requests while logged in must contain this token.
> <br>

> ### Response - Wrong ID or Password
>
> #### Response Code: 401 (`Unauthorized`)
>
> #### Response Body
>
> ```json
> {
>   "success": false,
>   "error": "Invalid ID or password"
> }
> ```

---

### Register

#### Get Tax Zone List

| API Endpoint           | HTTP Method |                           Description                           |
| ---------------------- | :---------: | :-------------------------------------------------------------: |
| [api/register/zones]() |    `GET`    | Retrieves the list of available tax zones for user registration |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>

> ### Response : Success
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "taxZones": ["Tax Zone 1", "Tax Zone 2", "Tax Zone 15"]
> }
> ```
</br>

---
### Get Tax Circle List

| API Endpoint            | HTTP Method |                            Description                            |
| ----------------------- | :---------: | :---------------------------------------------------------------: |
| [api/register/circle]() |    `GET`    | Retrieves the list of available tax circles for user registration |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "taxZone": "Tax Zone 2"
> }
> ```
</br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "taxCircles": ["Tax Circle 75", "Tax Circle 76", "Tax Circle 78"]
> }
> ```
</br>

---

### Submit Registration Request

| API Endpoint            | HTTP Method |                            Description                            |
| ----------------------- | :---------: | :---------------------------------------------------------------: |
| [api/register/submit]() |   `POST`    | Submits a new user registration with personal and tax information |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "email": "jarin@gmail.com",
>   "name": "Jarin Tasneem",
>   "nid": 1234567890,
>   "tin": 232345456767,
>   "mobile": 0123456789,
>   "taxZone": 15,
>   "taxCircle": 78,
>   "dob": "02-02-1990",
>   "spouse": "",
>   "spouseTIN": null,
>   "isResidential": true,
>   "benefittedPerson": {
>     "isFF": false,
>     "isFemale": true,
>     "isDisabled": false
>   }
> }
> ```

</br>

> ### Response - Success
>
> #### Response Code: 201 (`Created`)
>
> #### Response Body
>
> ```json
> {
>   "success": true,
>   "token": "1234cdb32"
> }
> ```

</br>

> ### Response - Invalid Input
>
> #### Response Code: 422 (`Unprocessable Entity`)
>
> #### Response Body
>
> ```json
> {
>   "success": false,
>   "error": "Invalid {field}"
> }
> ```

<br>

----

### Personal Info

| API Endpoint    | HTTP Method |               Description               |
| --------------- | :---------: | :-------------------------------------: |
| [api/profile]() |    `GET`    | Returns profile information of the user |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>



> ### Response - Success
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "email": "jarin@gmail.com",
>   "name": "Jarin Tasneem",
>   "nid": 1234567890,
>   "tin": 232345456767,
>   "mobile": 0123456789,
>   "taxZone": 15,
>   "taxCircle": 78,
>   "dob": "02-02-1990",
>   "spouse": "",
>   "spouseTIN": null,
>   "isResidential": true,
>   "benefittedPerson": {
>     "isFF": false,
>     "isFemale": true,
>     "isDisabled": false
>   }
> }
> ```
>
> <br>
> ----

### Update Personal Info

| API Endpoint           | HTTP Method |         Description         |
| ---------------------- | :---------: | :-------------------------: |
| [api/update_profile]() |   `POST`    | Updates profile of the user |

> ### Request
>
> #### Request Body
>
> ```json
> {
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
>     "isFF": true,
>     "isFemale": true,
>     "isDisabled": false
>   }
> }
> ```
</br>

> ### Response - Success
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Profile updated successfully",
>   "profile": {
>     "email": "jarin@gmail.com",
>     "name": "Jarin Tasneem",
>     "nid": 1234567890,
>     "tin": 232345456767,
>     "mobile": "0123456789",
>     "taxZone": 15,
>     "taxCircle": 76,
>     "dob": "1990-02-02",
>     "spouse": "",
>     "spouseTIN": null,
>     "isResidential": true,
>     "benefittedPerson": {
>       "isFF": true,
>       "isFemale": true,
>       "isDisabled": false
>     }
>   }
> }
> ```
>
> <br>

---

## Income Module

### Employment Income

| API Endpoint               | HTTP Method |        Description        |
| -------------------------- | :---------: | :-----------------------: |
| [/api/income/employment]() |   `POST`    | Add new employment income |

>### Request
>
>#### Request Body
>
>```json
>{
>  "employmentType": "Basic pay",
>  "incomeType": "Government Pay scale",
>  "amount": 50000,
>  "exemptedAmount": 4000,
>  "date": "05-11-2024"
>}
>```

</br>

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "success": true,
>   "redirectURL": "income/employment"
> }
> ```

</br>
---

| API Endpoint               | HTTP Method |         Description         |
| -------------------------- | :---------: | :-------------------------: |
| [/api/income/employment]() |    `GET`    | List all employment incomes |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "employment_incomes": [
>     {
>       "id": 123456789,
>       "employmentType": "Government Pay scale",
>       "incomeType": "Basic pay",
>       "amount": 50000,
>       "exemptedAmount": 4000,
>       "date": "05-11-2024"
>     },
>     {
>       "id": 123456789,
>       "employmentType": "Non-Government Pay scale",
>       "incomeType": "Transportation",
>       "amount": 5000,
>       "exemptedAmount": 4000,
>       "date": "05-11-2024"
>     }
>   ]
> }
> ```

</br>

----
| API Endpoint                   | HTTP Method |             Description             |
| ------------------------------ | :---------: | :---------------------------------: |
| [/api/income/employment/:id]() |    `GET`    | Returns requested employment income |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "id": 123456789,
>   "employmentType": "Government Pay scale",
>   "incomeType": "Basic pay",
>   "amount": 50000,
>   "exemptedAmount": 4000,
>   "date": "05-11-2024"
> }
> ```

| API Endpoint               | HTTP Method |       Description        |
| -------------------------- | :---------: | :----------------------: |
| [/api/income/employment]() |   `POST`    | Update employment income |

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

| API Endpoint                   | HTTP Method |                Description                |
| ------------------------------ | :---------: | :---------------------------------------: |
| [/api/income/employment/:id]() |  `DELETE`   | Delete employment income with specific id |

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

| API Endpoint         | HTTP Method |      Description      |
| -------------------- | :---------: | :-------------------: |
| [/api/income/rent]() |   `POST`    | Add new rental income |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "income/rent"
> }
> ```

| API Endpoint         | HTTP Method |      Description      |
| -------------------- | :---------: | :-------------------: |
| [/api/income/rent]() |    `GET`    | List all rent incomes |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "rent_incomes": [
>     {
>       "incomeType": "Rent received for flat 2/A",
>       "amount": 10000,
>       "allowable_deduction": 4000,
>       "date": "05-11-2024"
>     },
>     {
>       "incomeType": "Rent received",
>       "amount": 50000,
>       "allowable_deduction": 5000,
>       "date": "05-11-2024"
>     }
>   ]
> }
> ```

| API Endpoint             | HTTP Method |          Description          |
| ------------------------ | :---------: | :---------------------------: |
| [/api/income/rent/:id]() |    `GET`    | Returns requested rent income |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "id": 123456789,
>   "incomeType": "Rental Income",
>   "amount": 50000,
>   "exemptedAmount": 4000,
>   "date": "05-11-2024"
> }
> ```

| API Endpoint         | HTTP Method |    Description     |
| -------------------- | :---------: | :----------------: |
| [/api/income/rent]() |   `POST`    | Update rent income |

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

| API Endpoint             | HTTP Method |             Description             |
| ------------------------ | :---------: | :---------------------------------: |
| [/api/income/rent/:id]() |  `DELETE`   | Delete rent income with specific id |

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

| API Endpoint                | HTTP Method |        Description         |
| --------------------------- | :---------: | :------------------------: |
| [/api/income/agriculture]() |   `POST`    | Add new agriculture income |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "income/agriculture"
> }
> ```

| API Endpoint                | HTTP Method |         Description          |
| --------------------------- | :---------: | :--------------------------: |
| [/api/income/agriculture]() |    `GET`    | List all agriculture incomes |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "agriculture_incomes": [
>     {
>       "id": 123456789,
>       "incomeType": "Basic pay",
>       "sellingPrice": 50000,
>       "profit": 4000,
>       "date": "05-11-2024"
>     },
>     {
>       "id": 123456789,
>       "incomeType": "Transportation",
>       "sellingPrice": 50000,
>       "profit": 4000,
>       "date": "05-11-2024"
>     }
>   ]
> }
> ```

| API Endpoint                    | HTTP Method |             Description              |
| ------------------------------- | :---------: | :----------------------------------: |
| [/api/income/agriculture/:id]() |    `GET`    | Returns requested agriculture income |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "id": 123456789,
>   "incomeType": "Basic pay",
>   "sellingPrice": 50000,
>   "profit": 4000,
>   "date": "05-11-2024"
> }
> ```

| API Endpoint                | HTTP Method |        Description        |
| --------------------------- | :---------: | :-----------------------: |
| [/api/income/agriculture]() |   `POST`    | Update agriculture income |

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

| API Endpoint                    | HTTP Method |        Description        |
| ------------------------------- | :---------: | :-----------------------: |
| [/api/income/agriculture/:id]() |  `DELETE`   | Delete agriculture income |

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

| API Endpoint     | HTTP Method |   Description   |
| ---------------- | :---------: | :-------------: |
| [/api/expense]() |   `POST`    | Add expenditure |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "expense"
> }
> ```

| API Endpoint     | HTTP Method |    Description    |
| ---------------- | :---------: | :---------------: |
| [/api/expense]() |    `GET`    | List all expenses |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "expenses": [
>     {
>       "id": 123456789,
>       "expenseType": "Government Pay scale",
>       "description": "Basic pay",
>       "amount": 50000,
>       "date": "05-11-2024"
>     },
>     {
>       "id": 123456789,
>       "expenseType": "Non-Government Pay scale",
>       "description": "Transportation",
>       "amount": 5000,
>       "date": "05-11-2024"
>     }
>   ]
> }
> ```

| API Endpoint         | HTTP Method |        Description        |
| -------------------- | :---------: | :-----------------------: |
| [/api/expense/:id]() |    `GET`    | Returns requested expense |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "id": 123456789,
>   "expenseType": "Government Pay scale",
>   "description": "Basic pay",
>   "amount": 50000,
>   "date": "05-11-2024"
> }
> ```

| API Endpoint     | HTTP Method |  Description   |
| ---------------- | :---------: | :------------: |
| [/api/expense]() |   `POST`    | Update expense |

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
  "expenses": {
    "id": 123456789,
    "expenseType": "Government Pay scale",
    "description": "Basic pay",
    "amount": 50000,
    "date": "05-11-2024"
  }
}
```

| API Endpoint         | HTTP Method |  Description   |
| -------------------- | :---------: | :------------: |
| [/api/expense/:id]() |  `DELETE`   | Delete expense |

### Response - Success

#### Response Code : 200 (`OK`)

#### Response Body

```json
{
  "message": "Expense deleted successfully"
}
```

---

---

## Asset Module

### Agricultural Property

| API Endpoint               | HTTP Method |          Description          |
| -------------------------- | :---------: | :---------------------------: |
| [/api/asset/agriculture]() |   `POST`    | Add new agricultural property |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "asset/agriculture"
> }
> ```

| API Endpoint               | HTTP Method |          Description           |
| -------------------------- | :---------: | :----------------------------: |
| [/api/asset/agriculture]() |    `GET`    | List all agricultural property |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "agricultural_property ": [
>     {
>       "id": 123456789,
>       "name": "Farm",
>       "costValue": 50000,
>       "location": "Mirpur",
>       "aquisitionType": "Inheritance",
>       "date": "05-11-2024",
>       "description": "demo"
>     },
>     {
>       "id": 123456788,
>       "name": "Pond",
>       "costValue": 50000,
>       "location": "Mirpur",
>       "aquisitionType": "Inheritance",
>       "date": "05-11-2024",
>       "description": "demo"
>     }
>   ]
> }
> ```

| API Endpoint                   | HTTP Method |               Description               |
| ------------------------------ | :---------: | :-------------------------------------: |
| [/api/asset/agriculture/:id]() |    `GET`    | Returns requested agricultural property |

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

| API Endpoint               | HTTP Method |         Description          |
| -------------------------- | :---------: | :--------------------------: |
| [/api/asset/agriculture]() |   `POST`    | Update agricultural property |

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

| API Endpoint                    | HTTP Method |          Description          |
| ------------------------------- | :---------: | :---------------------------: |
| [/api/asset/agriculture/sell]() |   `POST`    | Sell an agricultural property |

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

| API Endpoint                   | HTTP Method |         Description          |
| ------------------------------ | :---------: | :--------------------------: |
| [/api/asset/agriculture/:id]() |  `DELETE`   | Delete agricultural property |

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

| API Endpoint                   | HTTP Method |          Description          |
| ------------------------------ | :---------: | :---------------------------: |
| [/api/asset/non_agriculture]() |   `POST`    | Add non-agricultural property |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "asset/non_agriculture"
> }
> ```

| API Endpoint                   | HTTP Method |            Description             |
| ------------------------------ | :---------: | :--------------------------------: |
| [/api/asset/non_agriculture]() |    `GET`    | List all non-agricultural property |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "non_agricultural_property ": [
>     {
>       "id": 123456789,
>       "name": "Plot",
>       "costValue": 50000,
>       "location": "Mirpur",
>       "aquisitionType": "Inheritance",
>       "date": "05-11-2024",
>       "description": "demo"
>     },
>     {
>       "id": 123456788,
>       "name": "Plot-1",
>       "costValue": 50000,
>       "location": "Mirpur",
>       "aquisitionType": "Inheritance",
>       "date": "05-11-2024",
>       "description": "demo"
>     }
>   ]
> }
> ```

| API Endpoint                       | HTTP Method |                 Description                 |
| ---------------------------------- | :---------: | :-----------------------------------------: |
| [/api/asset/non_agriculture/:id]() |    `GET`    | Returns requested non-agricultural property |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "id": 123456788,
>   "name": "Plot",
>   "costValue": 50000,
>   "location": "Mirpur",
>   "aquisitionType": "Inheritance",
>   "date": "05-11-2024",
>   "description": "demo"
> }
> ```

| API Endpoint                   | HTTP Method |           Description            |
| ------------------------------ | :---------: | :------------------------------: |
| [/api/asset/non_agriculture]() |   `POST`    | Update non-agricultural property |

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

| API Endpoint                        | HTTP Method |            Description            |
| ----------------------------------- | :---------: | :-------------------------------: |
| [/api/asset/non_agriculture/sell]() |   `POST`    | Sell an non_agricultural property |

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

| API Endpoint                       | HTTP Method |           Description            |
| ---------------------------------- | :---------: | :------------------------------: |
| [/api/asset/non_agriculture/:id]() |  `DELETE`   | Delete non-agricultural property |

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

| API Endpoint                 | HTTP Method |    Description    |
| ---------------------------- | :---------: | :---------------: |
| [/api/asset/motor_vehicle]() |   `POST`    | Add momor vehicle |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "asset/motor_vehicle"
> }
> ```

| API Endpoint                 | HTTP Method |           Description           |
| ---------------------------- | :---------: | :-----------------------------: |
| [/api/asset/motor_vehicle]() |    `GET`    | List all motor vehicle property |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "motor_vehicles": [
>     {
>       "id": 123456789,
>       "name": "Toyota",
>       "type": "Car",
>       "costValue": 50000,
>       "reg_number": "Ka-12345",
>       "engine_capacity": "2000 cc",
>       "date": "05-11-2024",
>       "description": "demo"
>     },
>     {
>       "id": 123456786,
>       "name": "Toyota",
>       "type": "Car",
>       "costValue": 50000,
>       "reg_number": "Ka-12345",
>       "engine_capacity": "2000 cc",
>       "date": "05-11-2024",
>       "description": "demo"
>     }
>   ]
> }
> ```

| API Endpoint                     | HTTP Method |               Description                |
| -------------------------------- | :---------: | :--------------------------------------: |
| [/api/asset/motor_vehicle/:id]() |    `GET`    | Returns requested motor vehicle property |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "id": 123456789,
>   "name": "Toyota",
>   "type": "Car",
>   "costValue": 50000,
>   "reg_number": "Ka-12345",
>   "engine_capacity": "2000 cc",
>   "date": "05-11-2024",
>   "description": "demo"
> }
> ```

| API Endpoint                 | HTTP Method |          Description          |
| ---------------------------- | :---------: | :---------------------------: |
| [/api/asset/motor_vehicle]() |   `POST`    | Update motor_vehicle property |

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
  "motor_vehicles": {
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

| API Endpoint                      | HTTP Method |            Description            |
| --------------------------------- | :---------: | :-------------------------------: |
| [/api/asset/motor_vehicle/sell]() |   `POST`    | Sell an non_agricultural property |

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

| API Endpoint                     | HTTP Method |          Description          |
| -------------------------------- | :---------: | :---------------------------: |
| [/api/asset/motor_vehicle/:id]() |  `DELETE`   | Delete motor_vehicle property |

### Response - Success

#### Response Code : 200 (`OK`)

#### Response Body

```json
{
  "message": "Motor_vehicle property deleted successfully"
}
```

### Ornaments

| API Endpoint            | HTTP Method |   Description    |
| ----------------------- | :---------: | :--------------: |
| [/api/asset/ornament]() |   `POST`    | Add new ornament |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "asset/ornament"
> }
> ```

| API Endpoint            | HTTP Method |    Description     |
| ----------------------- | :---------: | :----------------: |
| [/api/asset/ornament]() |    `GET`    | List all ornaments |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "ornament": [
>     {
>       "id": 123456789,
>       "name": "Gold",
>       "aquisitionType": "Inheritance",
>       "costValue": 50000,
>       "unit": 2,
>       "quantity": 3,
>       "date": "05-11-2024",
>       "description": "demo"
>     },
>     {
>       "id": 123456788,
>       "name": "Diamond",
>       "aquisitionType": "Inheritance",
>       "costValue": 500000,
>       "unit": 2,
>       "quantity": 3,
>       "date": "05-11-2024",
>       "description": "demo"
>     }
>   ]
> }
> ```

| API Endpoint                | HTTP Method |        Description         |
| --------------------------- | :---------: | :------------------------: |
| [/api/asset/ornament/:id]() |    `GET`    | Returns requested ornament |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "id": 123456788,
>   "name": "Diamond",
>   "aquisitionType": "Inheritance",
>   "costValue": 500000,
>   "unit": 2,
>   "quantity": 3,
>   "date": "05-11-2024",
>   "description": "demo"
> }
> ```

| API Endpoint            | HTTP Method |   Description   |
| ----------------------- | :---------: | :-------------: |
| [/api/asset/ornament]() |   `POST`    | Update ornament |

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
  "ornament": {
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

| API Endpoint                 | HTTP Method |   Description    |
| ---------------------------- | :---------: | :--------------: |
| [/api/asset/ornament/sell]() |   `POST`    | Sell an ornament |

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
    "aquisitionType": "Inheritance"
  }
}
```

| API Endpoint                | HTTP Method |   Description   |
| --------------------------- | :---------: | :-------------: |
| [/api/asset/ornament/:id]() |  `DELETE`   | Delete ornament |

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

| API Endpoint                | HTTP Method |     Description      |
| --------------------------- | :---------: | :------------------: |
| [/api/asset/sanchaypatra]() |   `POST`    | Add new sanchaypatra |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "asset/sanchaypatra"
> }
> ```

| API Endpoint                | HTTP Method |      Description      |
| --------------------------- | :---------: | :-------------------: |
| [/api/asset/sanchaypatra]() |    `GET`    | List all sanchaypatra |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "sanchaypatra": [
>     {
>       "id": 123456789,
>       "name": "10 Year Sanchaypatra",
>       "aquisitionType": "Inheritance",
>       "costValue": 50000,
>       "bank_account": 440400111111,
>       "date": "05-11-2024",
>       "description": "demo"
>     },
>     {
>       "id": 123456788,
>       "name": "5 Year Sanchaypatra",
>       "aquisitionType": "Inheritance",
>       "costValue": 500000,
>       "bank_account": 440400111111,
>       "date": "05-11-2024",
>       "description": "demo"
>     }
>   ]
> }
> ```

| API Endpoint                    | HTTP Method |          Description           |
| ------------------------------- | :---------: | :----------------------------: |
| [/api/asset/sanchaypatra/:id]() |    `GET`    | Returns requested sanchaypatra |

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "id": 123456788,
>   "name": "5 Year Sanchaypatra",
>   "aquisitionType": "Inheritance",
>   "costValue": 500000,
>   "bank_account": 440400111111,
>   "date": "05-11-2024",
>   "description": "demo"
> }
> ```

| API Endpoint                | HTTP Method |     Description     |
| --------------------------- | :---------: | :-----------------: |
| [/api/asset/sanchaypatra]() |   `POST`    | Update sanchaypatra |

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
  "sanchaypatra": {
    "name": "5 Year Sanchaypatra",
    "aquisitionType": "Inheritance",
    "costValue": 50000,
    "bank_account": 440400111111,
    "date": "05-11-2024",
    "description": "demo"
  }
}
```

| API Endpoint                    | HTTP Method |     Description     |
| ------------------------------- | :---------: | :-----------------: |
| [/api/asset/sanchaypatra/:id]() |  `DELETE`   | Delete sanchaypatra |

### Response - Success

#### Response Code : 200 (`OK`)

#### Response Body

```json
{
  "message": "Sanchaypatra deleted successfully"
}
```

---

## Liability Module

### Bank Loan

| API Endpoint                 | HTTP Method |    Description    |
| ---------------------------- | :---------: | :---------------: |
| [/api/liability/bank_loan]() |   `POST`    | Add new bank loan |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "liability/bank_loan"
> }
> ```

| API Endpoint                 | HTTP Method |     Description     |
| ---------------------------- | :---------: | :-----------------: |
| [/api/liability/bank_loan]() |    `GET`    | List all bank loans |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "liabilities ": [
>     {
>       "id": 123456789,
>       "name": "Brac Bank",
>       "amount": 50000,
>       "paid_amount": 1000,
>       "interest_rate": 15,
>       "date": "05-11-2024",
>       "description": "demo"
>     },
>     {
>       "id": 123456788,
>       "name": "Brac Bank",
>       "amount": 50000,
>       "paid_amount": 1000,
>       "interest_rate": 15,
>       "date": "05-11-2024",
>       "description": "demo"
>     }
>   ]
> }
> ```

| API Endpoint                     | HTTP Method |         Description         |
| -------------------------------- | :---------: | :-------------------------: |
| [/api/liability/bank_loan/:id]() |    `GET`    | Returns requested bank loan |

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

| API Endpoint                 | HTTP Method |   Description    |
| ---------------------------- | :---------: | :--------------: |
| [/api/liability/bank_loan]() |   `POST`    | Update bank loan |

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

| API Endpoint                        | HTTP Method |   Description    |
| ----------------------------------- | :---------: | :--------------: |
| [/api/liability/bank_loan/credit]() |   `POST`    | Update bank loan |

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

| API Endpoint                     | HTTP Method |   Description    |
| -------------------------------- | :---------: | :--------------: |
| [/api/liability/bank_loan/:id]() |  `DELETE`   | Delete bank loan |

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

| API Endpoint                     | HTTP Method |      Description      |
| -------------------------------- | :---------: | :-------------------: |
| [/api/liability/personal_loan]() |   `POST`    | Add new personal loan |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "liability/personal_loan"
> }
> ```

| API Endpoint                     | HTTP Method |       Description       |
| -------------------------------- | :---------: | :---------------------: |
| [/api/liability/personal_loan]() |    `GET`    | List all personal loans |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "liabilities ": [
>     {
>       "id": 123456789,
>       "name": "Brac Bank",
>       "amount": 50000,
>       "paid_amount": 1000,
>       "interest_rate": 15,
>       "date": "05-11-2024",
>       "description": "demo"
>     },
>     {
>       "id": 123456788,
>       "name": "Brac Bank",
>       "amount": 50000,
>       "paid_amount": 1000,
>       "interest_rate": 15,
>       "date": "05-11-2024",
>       "description": "demo"
>     }
>   ]
> }
> ```

| API Endpoint                         | HTTP Method |           Description           |
| ------------------------------------ | :---------: | :-----------------------------: |
| [/api/liability/personal_loan/:id]() |    `GET`    | Returns requested personal loan |

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

| API Endpoint                     | HTTP Method |     Description      |
| -------------------------------- | :---------: | :------------------: |
| [/api/liability/personal_loan]() |   `POST`    | Update personal loan |

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

| API Endpoint                            | HTTP Method |     Description      |
| --------------------------------------- | :---------: | :------------------: |
| [/api/liability/personal_loan/credit]() |   `POST`    | Credit personal loan |

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

| API Endpoint                         | HTTP Method |     Description      |
| ------------------------------------ | :---------: | :------------------: |
| [/api/liability/personal_loan/:id]() |  `DELETE`   | Delete personal loan |

### Response - Success

#### Response Code : 200 (`OK`)

#### Response Body

```json
{
  "message": "Personal loan deleted successfully"
}
```

---

## Investment Module

| API Endpoint        | HTTP Method |    Description     |
| ------------------- | :---------: | :----------------: |
| [/api/investment]() |   `POST`    | Add new Investment |

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
> ```json
> {
>   "success": true,
>   "redirectURL": "investment"
> }
> ```

| API Endpoint        | HTTP Method |     Description      |
| ------------------- | :---------: | :------------------: |
| [/api/investment]() |    `GET`    | List all Investments |

> ### Request
>
> #### Request Body

```json
{}
```

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "investments": [
>     {
>       "id": 123456789,
>       "type": "Fixed Deposit",
>       "amount": 50000,
>       "duration": "2 years",
>       "date": "05-11-2024",
>       "description": "demo"
>     },
>     {
>       "id": 123456789,
>       "type": "Fixed Deposit",
>       "amount": 50000,
>       "duration": "2 years",
>       "date": "05-11-2024",
>       "description": "demo"
>     }
>   ]
> }
> ```

| API Endpoint            | HTTP Method |         Description          |
| ----------------------- | :---------: | :--------------------------: |
| [/api/investment/:id]() |    `GET`    | Returns requested Investment |

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

| API Endpoint        | HTTP Method |    Description    |
| ------------------- | :---------: | :---------------: |
| [/api/investment]() |   `POST`    | Update Investment |

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

| API Endpoint            | HTTP Method |    Description    |
| ----------------------- | :---------: | :---------------: |
| [/api/investment/:id]() |  `DELETE`   | Delete Investment |

### Response - Success

#### Response Code : 200 (`OK`)

#### Response Body

```json
{
  "message": "Investment deleted successfully"
}
```

| API Endpoint                      | HTTP Method |     Description      |
| --------------------------------- | :---------: | :------------------: |
| [/api/investment/liquidate/:id]() |   `POST`    | Liquidate Investment |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "amount": 50000,
>   "bank_account": 4404001234567
> }
> ```

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

</br>

---

## Tax Module

### Tax estimation

| API Endpoint      | HTTP Method | Description                                                                                                           |
| ----------------- | :---------: | --------------------------------------------------------------------------------------------------------------------- |
| [/tax/estimate]() |    `GET`    | Estimates the user's income tax for current tax year and based on submitted income, assets, investments, and rebates. |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "totalIncome": 1000000,
>   "taxableIncome": 600000,
>   "totalInvestments": 500000,
>   "rebateOnInvestments": 30000,
>   "netIncomeTax": 12000
> }
> ```

---

### Rebate Plans

| API Endpoint          | HTTP Method | Description                                                                                                                                        |
| --------------------- | :---------: | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| [/tax/rebate/plans]() |    `GET`    | Retrieve all investment types that are eligible for tax rebates along with their default attributes like mak rebate % or amount and interest rates |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```

</br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "plans": [
>     {
>       "type": "Sanchayapatra",
>       "interestRate": 7.5,
>       "maxRebateRate": 15,
>       "maxRebateAmount": 75000
>     },
>     {
>       "type": "Fixed Deposit",
>       "interestRate": 8.0,
>       "maxRebateRate": 10,
>       "maxRebateAmount": 100000
>     },
>     {
>       "type": "Zakat Fund",
>       "interestRate": 0.0,
>       "maxRebateRate": 15,
>       "maxRebateAmount": 7500
>     }
>   ]
> }
> ```

---

### Respond to Selected Rebate Plans

| API Endpoint             | HTTP Method | Description                                                                                         |
| ------------------------ | :---------: | --------------------------------------------------------------------------------------------------- |
| [/tax/rebate/estimate]() |   `POST`    | Receive selected investment plans with user-inputted amounts and return the computed rebate summary |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "investments": [
>     {
>       "type": "Sanchayapatra",
>       "amount": 500000
>     },
>     {
>       "type": "Zakat Fund",
>       "amount": 50000
>     }
>   ]
> }
> ```

</br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "rebates": [
>     {
>       "type": "Sanchayapatra",
>       "rebateAmount": 75000
>     },
>     {
>       "type": "Zakat Fund",
>       "rebateAmount": 7500
>     }
>   ],
>   "totalInvestment": 550000,
>   "maximumRebate": 82500
> }
> ```

---

</br>

### All tax returns

| API Endpoint        | HTTP Method | Description                                         |
| ------------------- | :---------: | --------------------------------------------------- |
| [/tax/return/all]() |    `GET`    | Get all tax return ids and their status of the user |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```

</br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "returns": [
>     { "id": "trn_2024_user123", "year": 2024, "status": "in-progress" },
>     { "id": "trn_2023_user123", "year": 2023, "status": "submitted" }
>   ]
> }
> ```

</br>

---

### Employment Income APIs

| API Endpoint                                    | HTTP Method | Description                                                                                             |
| ----------------------------------------------- | :---------: | ------------------------------------------------------------------------------------------------------- |
| [/tax/return/{taxReturnId}/employment-income]() |    `GET`    | Retrieve the previously submitted employment income — useful for pre-filling form fields during editing |

> ## Request
>
> ### Request Body
>
> ```json
> {}
> ```

</br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "employmentType": "Government Pay Scale",
>   "designation": "Senior Officer",
>   "particulars": {
>     "basicPay": 600000,
>     "specialAllowance": 100000,
>     "houseRentAllowance": 200000,
>     "medicalAllowance": 30000,
>     "banglaNoboborshoAllowance": 15000,
>     "conveyanceAllowance": 12000,
>     "overtimeAllowance": 30000,
>     "supportStaffAllowance": 20000,
>     "festivalAllowance": 30000,
>     "leaveAllowance": 25000,
>     "gratuity": 40000,
>     "others": 10000
>   },
>   "total": 1082000
> }
> ```
>
> </br>

---

| API Endpoint                                   | HTTP Method | Description                                                      |
| ---------------------------------------------- | :---------: | ---------------------------------------------------------------- |
| [/tax/return/{taxReturnId}employment-income]() |   `POST`    | Submit or create the employment income breakdown for tax return. |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "employmentType": "Government Pay Scale",
>   "designation": "Senior Officer",
>   "particulars": {
>     "basicPay": 600000,
>     "specialAllowance": 100000,
>     "houseRentAllowance": 200000,
>     "medicalAllowance": 30000,
>     "banglaNoboborshoAllowance": 15000,
>     "conveyanceAllowance": 12000,
>     "overtimeAllowance": 30000,
>     "supportStaffAllowance": 20000,
>     "festivalAllowance": 30000,
>     "leaveAllowance": 25000,
>     "gratuity": 40000,
>     "others": 10000
>   }
> }
> ```
>
> </br>

> ### Response- Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Employment income saved successfully",
>   "totalIncome": 1082000
> }
> ```
>
> </br>

---

### Agricultural income APIs

| API Endpoint                                     | HTTP Method | Description                                                                                              |
| ------------------------------------------------ | :---------: | -------------------------------------------------------------------------------------------------------- |
| [/tax/return/{taxReturnId}/agriculture-income]() |    `GET`    | Retrieve the previously submitted agriculture income — useful for pre-filling form fields during editing |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> </br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "agricultureType": "Agricultural Land",
>   "cultivationArea": 3,
>   "areaUnit": "Decimal",
>   "produces": "Rice",
>   "salesProceed": 200000,
>   "profit": 50000,
>   "totalIncome": 50000
> }
> ```

</br>

---

| API Endpoint                                     | HTTP Method | Description                                                                                      |
| ------------------------------------------------ | :---------: | ------------------------------------------------------------------------------------------------ |
| [/tax/return/{taxReturnId}/agriculture-income]() |   `POST`    | Submit details of income generated from agricultural activities for inclusion in the tax return. |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "agricultureType": "Agricultural Land",
>   "cultivationArea": 3,
>   "areaUnit": "Decimal",
>   "produces": "Rice",
>   "salesProceed": 200000,
>   "profit": 50000
> }
> ```

</br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Agricultural income saved successfully",
>   "totalIncome": 50000
> }
> ```

</br>

### Tax Exempted Income

| API Endpoint                                      | HTTP Method | Description                                                                                  |
| ------------------------------------------------- | :---------: | -------------------------------------------------------------------------------------------- |
| [/tax/return/{taxReturnId}/tax-exempted-income]() |   `POST`    | Submit details of income that is exempted from tax under specific provisions of the tax law. |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "exemptedIncomeType": "Other Exemption Under 6th Schedule Part-1",
>   "paragraphNo": "AB-12/0123",
>   "particulars": "Educational scholarship",
>   "amountOfIncome": 150000,
>   "relatedExpense": 20000
> }
> ```

</br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Tax exempted income saved successfully",
>   "taxExemptedIncome": 130000
> }
> ```
>
> </br>

---

### Investment related APIs

| API Endpoint                          | HTTP Method | Description                                                                      |
| ------------------------------------- | :---------: | -------------------------------------------------------------------------------- |
| [/tax/return/{taxReturnId}/rebates]() |   `POST`    | Submit investment entries for a given tax return to claim tax rebate eligibility |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "depositPensionSchemes": [
>     {
>       "bank": "Sonali Bank",
>       "accountNumber": "10200039485",
>       "depositAmount": 20000
>     },
>     {
>       "bank": "Pubali Bank",
>       "accountNumber": "400038484545",
>       "depositAmount": 35000
>     }
>   ],
>   "sanchayapatras": [
>     {
>       "name": "Family",
>       "registrationNumber": "ADR-123445",
>       "issueDate": "2023-10-13",
>       "investmentAmount": 300000
>     }
>   ]
> }
> ```

</br>

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Rebate data submitted successfully",
>   "allowableAmountForDPS": 60000,
>   "allowableAmountForShanchayportro": 50000,
>   "totalActualInvestment": 355000,
>   "totalAllowableRebateInvestment": 30000
> }
> ```

</br>

---

| API Endpoint                          | HTTP Method | Description                         |
| ------------------------------------- | :---------: | ----------------------------------- |
| [/tax/return/{taxReturnId}/rebates]() |    `GET`    | Retrieve previous investments data. |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```

</br>

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "depositPensionSchemes": [
>     {
>       "bank": "Sonali Bank",
>       "accountNumber": "10200039485",
>       "depositAmount": 20000
>     },
>     {
>       "bank": "Pubali Bank",
>       "accountNumber": "400038484545",
>       "depositAmount": 35000
>     }
>   ],
>   "sanchayapatras": [
>     {
>       "name": "Family",
>       "registrationNumber": "ADR-123445",
>       "issueDate": "2023-10-13",
>       "investmentAmount": 300000
>     }
>   ],
>   "allowableAmountForDPS": 60000,
>   "allowableAmountForShanchayportro": 50000,
>   "totalActualInvestment": 355000,
>   "totalAllowableRebateInvestment": 30000
> }
> ```

</br>

---

### Get Total Income Overview

| API Endpoint                                 | HTTP Method | Description                                                                                                                               |
| -------------------------------------------- | :---------: | ----------------------------------------------------------------------------------------------------------------------------------------- |
| [/tax/return/{taxReturnId}/summary/income]() |    `GET`    | Fetch a computed breakdown of the user's income from various categories, total income, and tax-exempt income — for a specific tax return. |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```

</br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "incomeFromEmployment": 1015000,
>   "incomeFromFinancialAssets": 50000,
>   "incomeFromRent": 479500,
>   "incomeFromAgriculture": 0,
>   "incomeFromBusiness": 0,
>   "capitalGains": 0,
>   "incomeFromOtherSources": 0,
>   "totalIncome": 1535000,
>   "taxExemptedIncome": 230000
> }
> ```
>
> </br>

---

### Get Tax Computation

| API Endpoint                                   | HTTP Method | Description                                                                 |
| ---------------------------------------------- | :---------: | --------------------------------------------------------------------------- |
| [/taxx/return/{taxReturnId}/tax-computation]() |    `GET`    | Return the full breakdown of computed tax liability for a given tax return. |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```

</br>

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "grossTaxBeforeRebate": 153900,
>   "regularIncomeTax": 148900,
>   "taxUnderSection163": 5000,
>
>   "rebates": {
>     "onInvestment": 44835,
>     "otherRebate": 0
>   },
>
>   "netTaxAfterRebate": 109065,
>
>   "minimumTax": {
>     "tdsSection163": 0,
>     "locationOfIncome": 5000
>   },
>
>   "surcharge": {
>     "netWealth": 0
>   },
>
>   "totalPayableTax": 109065
> }
> ```

</br>

> ### Response - Failure
>
> #### Response Code : 400 (`Bad Request`)
>
> #### Response Body
>
> ```json
> {
>   "success": false,
>   "message": "Income data is required before tax computation"
> }
> ```
>
> </br>

---

### Generate Return PDF Preview (Before Submission)

| API Endpoint                                | HTTP Method | Description                                                       |
| ------------------------------------------- | :---------: | ----------------------------------------------------------------- |
| [/tax/return/{taxReturnId}/form/generate]() |   `POST`    | Generate a preview version of the tax return PDF (not finalized). |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```

</br>

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "pdfUrl": "https://cdn.wealthe.dev/returns/previews/trn_2024_user123.pdf",
>   "status": "preview",
>   "generatedAt": "2024-05-06T14:00:00Z"
> }
> ```

</br>

---

### Finalize Submission

| API Endpoint                              | HTTP Method | Description                                                  |
| ----------------------------------------- | :---------: | ------------------------------------------------------------ |
| [/tax/return/{taxReturnId}/form/submit]() |   `POST`    | Confirm and finalize the return after user approves the PDF. |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "confirmDeclaration": true
> }
> ```
>
> </br>

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Return submitted successfully",
>   "adminValidation": "True",
>   "submissionId": "SUB-2024-TRN001",
>   "status": "submitted",
>   "finalPdfUrl": "https://cdn.wealthe.dev/returns/final/trn_2024_user123.pdf"
> }
> ```
>
> </br>

> ### Response - Failure
>
> #### Response Code : 400 (`Bad Request`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Return submission failed,Necessary documnents needed",
>   "adminValidation": "False",
>   "status": "preview"
> }
> ```

</br>

---

### Download Finalized Return PDF

| API Endpoint                                | HTTP Method | Description                  |
| ------------------------------------------- | :---------: | ---------------------------- |
| [/tax/return/{taxRetunrId}/form/download]() |    `GET`    | Get downloadable return form |

> ### Request
>
> #### Request Headers
>
> ```
> Authorization: Bearer <jwt_token>
> Accept: application/pdf
>
> ```

</br>

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "pdfUrl": "https://cdn.wealthe.dev/returns/final/trn_2024_user123.pdf"
> }
> ```

</br>

---

### Check Submission Status

| API Endpoint                              | HTTP Method | Description                                            |
| ----------------------------------------- | :---------: | ------------------------------------------------------ |
| [/tax/return/{taxReturnId}/form/status]() |   `POST`    | Get the submission status of the tax return from admin |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```

</br>

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "status": "submitted",
>   "finalPdfAvailable": true,
>   "submittedAt": "2024-05-06T14:05:00Z"
> }
> ```

</br>

---

## AI features

### AI Chatbot- Tax Q&A

| API Endpoint | HTTP Method | Description                                                           |
| ------------ | :---------: | --------------------------------------------------------------------- |
| [/ai/chat]() |    `GET`    | Get answer for tax-related queries from the user in natural language. |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "message": "What is the tax slab for income above 10 lakhs?",
>   "context": {
>     "taxReturnId": "trn_2024_user123"
>   }
> }
> ```

</br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "answer": "If your income exceeds BDT 10,00,000, the slab rate is 20% on the amount above that threshold."
> }
> ```
>
> </br>

---

### Tax Breakdown Explanation

| API Endpoint                   | HTTP Method | Description                                                   |
| ------------------------------ | :---------: | ------------------------------------------------------------- |
| [/ai/explain-tax-breakdown/]() |    `GET`    | Get a human-readable explanation of how the tax was computed. |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "taxReturnId": "trn_usr_123"
> }
> ```

</br>

> ### Response - Success
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "success": true,
>
>   "explanation": "You earned BDT 12,00,000. Based on your age and gender, you're taxed under the 2024–25 slab. Total rebate from investment was BDT 60,000. Final tax payable is BDT 22,000 after applying Section 44."
> }
> ```
>
> </br>

---

### Rebate Investment Optimizer

| API Endpoint             | HTTP Method | Description                                               |
| ------------------------ | :---------: | --------------------------------------------------------- |
| [/ai/rebate-optimizer]() |   `POST`    | Suggest ideal investment mix to maximize rebate benefits. |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "goal": "maximize short-term returns",
>   "preferences": {
>     "liquidity": "high",
>     "riskTolerance": "medium",
>     "investmentPeriod": "1 year"
>   }
> }
> ```

</br>

> ### Response
>
> #### Response Code : 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "success": "True",
>   "goal": "maximize short-term returns",
>   "maxEligibleInvestment": 300000,
>   "remaining": 120000,
>   "strategy": "balanced",
>   "recommended": [
>     { "type": "Mutual Fund", "amount": 70000, "liquidity": "high" },
>     { "type": "Shariah Fund", "amount": 50000, "liquidity": "medium" }
>   ],
>   "reasoning": "Chosen for short lock-in period and medium risk with rebate eligibility."
> }
> ```

</br>

---

## Admin Module

### Tax Rules on Income

#### Show Income Slabs

| API Endpoint           | HTTP Method |   Description    |
| ---------------------- | :---------: | :--------------: |
| [/admin/rule/income]() |    `GET`    | Get income slabs |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "0% tax": [
>     {
>       "no_tax_id": "z0-1",
>       "category": "regular",
>       "threshold_amount": 350000
>     },
>     {
>       "no_tax_id": "z0-2",
>       "category": "female & senior citizen",
>       "threshold_amount": 400000
>     },
>     {
>       "no_tax_id": "z0-3",
>       "category": "physically challenged & 3rd gender",
>       "threshold_amount": 475000
>     },
>     {
>       "no_tax_id": "z0-4",
>       "category": "freedom fighter with war casualties",
>       "threshold_amount": 500000
>     }
>   ],
>   "common_slabs": [
>     { "common_slab_id": "cs-1", "slab_no": 2, "amount": 100000, "rate": 5 },
>     { "common_slab_id": "cs-2", "slab_no": 3, "amount": 400000, "rate": 10 },
>     { "common_slab_id": "cs-3", "slab_no": 4, "amount": 500000, "rate": 15 },
>     { "common_slab_id": "cs-4", "slab_no": 5, "amount": 500000, "rate": 20 },
>     {
>       "common_slab_id": "cs-5",
>       "slab_no": 6,
>       "amount": "infinity",
>       "rate": 25
>     }
>   ]
> }
> ```

#### Edit No Tax Threshold

| API Endpoint                              | HTTP Method |                 Description                  |
| ----------------------------------------- | :---------: | :------------------------------------------: |
| [/admin/rule/income/no-tax/{no_tax_id}]() |   `POST`    | Edit 0% tax threshold for different category |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "threshold amount": 420000
> }
> ```

> ```
>
> <br>
> ```

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "0% tax threshold updated successfully."
> }
> ```

> ### Response - Invalid ID
>
> #### Response Code: 400 (`Not Found`)
>
> #### Response Body
>
> ```json
> {
>   "success": false,
>   "message": "Invalid rule ID"
> }
> ```

#### Edit Common Slabs

| API Endpoint                                        | HTTP Method |    Description    |
| --------------------------------------------------- | :---------: | :---------------: |
| [/admin/rule/income/common-slab/{common_slab_id}]() |   `POST`    | Edit common slabs |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "amount": 550000,
>   "rate": 22
> }
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Common slab updated successfully."
> }
> ```

#### Get Categories

| API Endpoint                      | HTTP Method |     Description     |
| --------------------------------- | :---------: | :-----------------: |
| [/admin/rule/income/categories]() |    `GET`    | Get user categories |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "categories": [
>     "regular",
>     "female & senior citizen",
>     "physically challenged & 3rd gender",
>     "freedom fighter with war casualties"
>   ]
> }
> ```

#### Edit Categories

| API Endpoint                      | HTTP Method |     Description      |
| --------------------------------- | :---------: | :------------------: |
| [/admin/rule/income/categories]() |   `POST`    | Edit user categories |

> ### Request
>
> #### Request Body
>
> ```json
> {
>
>   "categories" : [
>                    "regular",
>                    "female & senior citizen",
>                    "physically challenged & 3rd gender",
>                    "freedom fighter with war casualties"
>                  ]
> }
>
> <br>
> ```

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Category updated successfully."
> }
> ```

### Investment Sectors

#### Get Investment options

| API Endpoint               | HTTP Method |                    Description                    |
| -------------------------- | :---------: | :-----------------------------------------------: |
| [/admin/rule/investment]() |    `GET`    | Sectors of investment and donation for tax rebate |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "investment_options": [
>     { "invest_id": "inv-1", "name": "Insurance Premium", "rebate_rate": 15 },
>     { "invest_id": "inv-2", "name": "Deferred Annuity", "rebate_rate": 15 },
>     {
>       "invest_id": "inv-3",
>       "name": "Contribution to Recognized Provident Fund",
>       "rebate_rate": 15
>     },
>     {
>       "invest_id": "inv-4",
>       "name": "Investment in Government Savings Certificates",
>       "rebate_rate": 15
>     },
>     {
>       "invest_id": "inv-5",
>       "name": "Investment in Mutual Funds",
>       "rebate_rate": 15
>     },
>     {
>       "invest_id": "inv-6",
>       "name": "Government Unit Certificate",
>       "rebate_rate": 15
>     },
>     {
>       "invest_id": "inv-7",
>       "name": "Donation in Welfare Fund)",
>       "rebate_rate": 15
>     },
>     { "invest_id": "inv-8", "name": "Zakat Donation", "rebate_rate": 15 },
>     {
>       "invest_id": "inv-9",
>       "name": "Donation to an approved charitable or educational institution",
>       "rebate_rate": 15
>     },
>     {
>       "invest_id": "inv-10",
>       "name": "Charitable Donations to Approved Institutions",
>       "rebate_rate": 15
>     },
>     {
>       "invest_id": "inv-11",
>       "name": "Donation to the Disability Welfare Fund",
>       "rebate_rate": 15
>     },
>     {
>       "invest_id": "inv-12",
>       "name": "Contribution to an approved Old Age Fund",
>       "rebate_rate": 15
>     }
>   ]
> }
> ```

#### Add Investment Option

| API Endpoint               | HTTP Method |              Description              |
| -------------------------- | :---------: | :-----------------------------------: |
| [/admin/rule/investment]() |   `POST`    | Add investment options for tax rebate |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "name": "Donation to Cancer Treatment Fund",
>   "rebate_rate": 15
> }
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "invest_id": "inv-13",
>   "name": "Donation to Cancer Treatment Fund",
>   "rebate_rate": 15
> }
> ```

#### Edit Investment Option

| API Endpoint                           | HTTP Method |              Description               |
| -------------------------------------- | :---------: | :------------------------------------: |
| [/admin/rule/investment/{invest_id}]() |   `POST`    | Edit investment options for tax rebate |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "name": "Donation to Cancer Treatment Fund",
>   "rebate_rate": 10
> }
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Investment option updated successfully."
> }
> ```

### Tax Zone Rules

#### Get Tax Zone Rules

| API Endpoint            | HTTP Method |                      Description                       |
| ----------------------- | :---------: | :----------------------------------------------------: |
| [/admin/rule/taxZone]() |    `GET`    | Get rules for minimum amount of tax in different zones |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "zone_rules": [
>     {
>       "zone_rule_id": "zr-1",
>       "zone_type": "specific_city_corporation",
>       "zones": [
>         "Dhaka North City Corporation",
>         "Dhaka South City Corporation",
>         "Chattogram City Corporation"
>       ],
>       "minimumTax": 5000
>     },
>     {
>       "zone_rule_id": "zr-2",
>       "Zone_type": "other_city_corporation",
>       "zones": ["others"],
>       "minimumTax": 4000
>     },
>     {
>       "zone_rule_id": "zr-3",
>       "Zone_type": "non_city_corporation",
>       "zones": ["other than city corporation"],
>       "minimumTax": 3000
>     }
>   ]
> }
> ```

#### Edit Tax Zone Rules

| API Endpoint                           | HTTP Method |                       Description                       |
| -------------------------------------- | :---------: | :-----------------------------------------------------: |
| [/admin/rule/taxZone/{zone_rule_id}]() |   `POST`    | Edit rules for minimum amount of tax in different zones |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "minimumTax": 4500
> }
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Minimum amount of tax for a zone updated successfully."
> }
> ```

### Rebate Rules

#### Get Rebate Rules

| API Endpoint           | HTTP Method |                Description                 |
| ---------------------- | :---------: | :----------------------------------------: |
| [/admin/rule/rebate]() |    `GET`    | Get rules for maximum amount of tax rebate |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "tax_rebate_rules": [
>     {
>       "rebate_rule_id": "tr-1",
>       "description": "Rebate percentage of actual investment amount",
>       "value": 15
>     },
>     {
>       "rebate_rule_id": "tr-2",
>       "description": "Rebate percentage of total taxable income",
>       "value": 3
>     },
>     {
>       "rebate_rule_id": "tr-3",
>       "description": "Maximum allowable rebate amount",
>       "value": 1000000
>     }
>   ]
> }
> ```

#### Edit Rebate Rules

| API Endpoint                            | HTTP Method |                 Description                 |
| --------------------------------------- | :---------: | :-----------------------------------------: |
| [/admin/rule/rebate/{rebate_rule_id}]() |   `POST`    | Edit rules for maximum amount of tax rebate |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "value": 20
> }
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "Tax Rebate Rule updated successfully."
> }
> ```

### Admin File Section

#### Get Return List

| API Endpoint           | HTTP Method |       Description       |
| ---------------------- | :---------: | :---------------------: |
| [/admin/return-list]() |    `GET`    | Get list of tax returns |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "tax_returns": [
>     {
>       "return_id": 443223455,
>       "TIN": 123456789,
>       "tax_amount": 15000,
>       "date": "2024-06-30",
>       "return_pdf_url": "https://example.com/returns/123456789_2024.pdf"
>     },
>     {
>       "return_id": 441232455,
>       "TIN": 987654321,
>       "tax_amount": 22000,
>       "date": "2024-09-15",
>       "return_pdf_url": "https://example.com/returns/987654321_2024.pdf"
>     },
>     {
>       "return_id": 123323121,
>       "TIN": 456789123,
>       "tax_amount": 18500,
>       "date": "2025-03-20",
>       "return_pdf_url": "https://example.com/returns/456789123_2025.pdf"
>     }
>   ]
> }
> ```

> ```
>
> ```

#### View a Return

| API Endpoint                       | HTTP Method |        Description         |
| ---------------------------------- | :---------: | :------------------------: |
| [/admin/return-list/{return_id}]() |    `GET`    | View a specific tax return |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "id": 443223455,
>   "TIN": 123456789,
>   "tax_amount": 15000,
>   "date": "2024-06-30",
>   "return_pdf_url": "https://example.com/returns/123456789_2024.pdf"
> }
> ```

#### Get Individual Return

| API Endpoint                 | HTTP Method |             Description             |
| ---------------------------- | :---------: | :---------------------------------: |
| [/admin/return-list/{TIN}]() |    `GET`    | Get an individual's tax return list |

> ### Request
>
> #### Request Body
>
> ```json
> {}
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "tax_returns": [
>     {
>       "return_id": 443223455,
>       "TIN": 123456568,
>       "tax_amount": 15000,
>       "date": "2024-06-30",
>       "return_pdf_url": "https://example.com/returns/123456789_2024.pdf"
>     },
>     {
>       "return_id": 441232455,
>       "TIN": 123456568,
>       "tax_amount": 12000,
>       "date": "2023-09-15",
>       "return_pdf_url": "https://example.com/returns/987654321_2023.pdf"
>     },
>     {
>       "return_id": 123323121,
>       "TIN": 123456568,
>       "tax_amount": 8500,
>       "date": "2022-08-20",
>       "return_pdf_url": "https://example.com/returns/456789123_2022.pdf"
>     }
>   ]
> }
> ```

#### Update Tax Return Status

| API Endpoint                      | HTTP Method |          Description          |
| --------------------------------- | :---------: | :---------------------------: |
| [/admin/return-list/tax-status]() |   `POST`    | Update tax status of a return |

> ### Request
>
> #### Request Body
>
> ```json
> {
>   "id": 123323121,
>   "isApproved": false,
>   "report": "Asset is not compatible with previous year's data."
> }
> ```
>
> <br>

> ### Response
>
> #### Response Code: 200 (`OK`)
>
> #### Response Body
>
> ```json
> {
>   "message": "feedback sent successfully"
> }
> ```

---
