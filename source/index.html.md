--- 

title: Ashwins-Auth 

language_tabs: 
   - HTTP 

toc_footers: 
   - <a href='#'>Sign Up for a Developer Key</a> 
   - <a href='https://github.com/lavkumarv'>Documentation Powered by lav</a> 

includes: 
   - errors 

search: true 

--- 

# Introduction 

This is the API for every Auth functionality for Ashwins Pharmacy. There are three different unique flows :

**Login:** Login is the most basic functionality where it is used for Signup, Login & Forgot password flows. <br />
**Groups:** Groups is the higher level functionality where once a pharmacist has logged in to the account , he can create groups, add users, delete users, set password etc <br />
**Admin:** This provides all the admin functionalities

**URL:**  https://api.dev.ashwins.com.au <br/>

**Version:** 0.1 


# User

## Signup 

> Sample Request object

```json 
{
    "fullName" : "FirstName LastName",
    "email" : "email@dragatron.com.au",
    "password" : "testing1234" 
  }
```

**Description:** Signup of a new users. This method is from the user perspective. Whenever a new users wants to signup on the platform. Refer the url from top level description

### HTTP Request 
`***POST*** /dev/user/signup` 

| field | Description |
| ---- | ----------- |
| fullName | full name |
| email | email |
| password | password |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Invalid input |



## login 

> Sample Request object

```json 
{
    "email" : "email@dragatron.com.au",
    "password" : "testing1234" 
  }
```
> Sample Response object

```json 
{
    "message": "Success",
    "token": "eyJraWQiOiJkclh2eE5sZ3NvMmVjRGt4QlVGTzh3b3lsemgzU25GT3VydzZhSkw0WTlnPSIsImFsZyI6IlJTMjU2In0.eyJzdWIiOiI1YWEyMDQ4ZS0xNzJkLTRhNmEtYmRmMS1hMGQwZGFmNDAxNmMiLCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAuYXAtc291dGhlYXN0LTIuYW1hem9uYXdzLmNvbVwvYXAtc291dGhlYXN0LTJfVUppbG11eGVZIiwiY2xpZW50X2lkIjoiNzR1bWxvNnVyM2k1YnAzZzI0NDdycDh0MXQiLCJvcmlnaW5fanRpIjoiN2I5ZmVjYjAtM2QwNC00YWMzLTg4ZDYtYTEwNzAwZTYxOGFkIiwiZXZlbnRfaWQiOiIxZDI2NjcxMi04NzZiLTQ0YWEtOTU2NC1kNWI2YWM2MjVhNzkiLCJ0b2tlbl91c2UiOiJhY2Nlc3MiLCJzY29wZSI6ImF3cy5jb2duaXRvLnNpZ25pbi51c2VyLmFkbWluIiwiYXV0aF90aW1lIjoxNjU2NTY4MzUxLCJleHAiOjE2NTY1ODYzNTEsImlhdCI6MTY1NjU2ODM1MSwianRpIjoiZWFmYjBlZGUtZjM4Mi00N2Q4LThlZDUtZGExYTI3ZDQ1MDg1IiwidXNlcm5hbWUiOiJha2hpbEBkcmFnYXRyb24uY29tLmF1In0.DzKsnQSRAWMxj6RxiKiUCQQK71fCKi-69b9jOieqDzFd6y4OwkEbrJfBDmNRSMvBiTlwGfgdPSYOBbWeUtp2AredNDcupph9njpty3BGpU56yK2JOSb-6Y1msF81Kft3L2eWS-KwtIg88-BbE9wVKLeG3RNrYUGNpv3r4CgeUvZxx-6OADvjXfSpLpJLyqkCF1d23D5YDRLoVi0MY74wYV3rh_a6T_2dAuoYd0B9RR1w6v8FFzaTRg-nmpEIKYDc41hMuMpPEkpY08oYIBmW4dvSvT_8jkFj-q1uir1kSRimUco2FFgjl1WykM3vKuD_FTgg4eRNpXXofd_5n2eZgA"
}
```

**Description:** Login of a new users. This method is from the user perspective. Whenever a new users wants to login on the platform. Refer the url from top level description

### HTTP Request 
`***POST*** /dev/user/login` 

| field | Description |
| ---- | ----------- |
| email | email |
| password | password |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Invalid input |
| token | Returns a JWT token which can be used to check the validity of the session |


## Forgot


> Sample Request object

```json 
{
    "email" : "email@dragatron.com.au"
  }
```

**Description:** Forgot Password Functionality. Takes it email address as an input and sends an email to the user with a link on clicking of that the user is directed to the password reset screen where user will add his password and re-enter the password 

### HTTP Request 
`***POST*** /dev/user/forgot` 

| field | Description |
| ---- | ----------- |
| email | email |

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 400 | Invalid input |

# /DEV/USER/CONFIRMCODEPWD
## ***POST*** 

**Description:** Auto generated using Swagger Inspector

### HTTP Request 
`***POST*** /dev/user/confirmCodePwd` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |

# /DEV/GROUPS
## ***GET*** 

**Description:** Auto generated using Swagger Inspector

### HTTP Request 
`***GET*** /dev/groups` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |

# /DEV/GROUPS/USERS
## ***POST*** 

**Description:** Auto generated using Swagger Inspector

### HTTP Request 
`***POST*** /dev/groups/users` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |

# /DEV/USER/LOGIN
## ***POST*** 

**Description:** Auto generated using Swagger Inspector

### HTTP Request 
`***POST*** /dev/user/login` 

**Responses**

| Code | Description |
| ---- | ----------- |
| 200 | Auto generated using Swagger Inspector |

<!-- Converted with the swagger-to-slate https://github.com/lavkumarv/swagger-to-slate -->
