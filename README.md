# 訂餐系統

## swagger like this  http://localhost:8080/swagger-ui.html#

後端API
---
#### 1.註冊 api/signup
postman
```
{
    "username":"adimin",
    "email":"adimin@bezkoder.com",
    "password":"12345678",
    "role":["mod","user"]
}

```
return
```
{
    "message": "User registered successfully!"
}
```
#### 2.登入 api/signin
postman
```
{
       "username":"auth",
     "password":"12345678"
}
```
return
```
{
    "id": 1,
    "username": "auth",
    "email": "auth@bezkoder.com",
    "roles": [
        "ROLE_USER",
        "ROLE_MODERATOR"
    ],
    "tokenType": "Bearer",
    "accessToken": "eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJhdXRoIiwiaWF0IjoxNjA2MTEyNTkzLCJleHAiOjE2MDYxOTg5OTN9.SFzBhbS9CPe_3RtOuh-9jj6flBZyTilMEwzs9c7TaBe2RgS2Ifera-8Yl63nlZ7NhD49EWo36MJCskE7AFN2Cg"
}
```

##### 3. api/getSupplier

postman 

@RequestParam("org") String org

header Bearer token

ex:Bearer eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiJhdXRoIiwiaWF0IjoxNjA2MTEyNTkzLCJleHAiOjE2MDYxOTg5OTN9.SFzBhbS9CPe_3RtOuh-9jj6flBZyTilMEwzs9c7TaBe2RgS2Ifera-8Yl63nlZ7NhD49EWo36MJCskE7AFN2Cg

#### 4. api/postSupplier
header Bearer token
```
{
    "suppId":19,
    "suppName":"aufffffffffffffff",
    "tel":"q2",
    "fax":"qqqqqqqqqqq",
    "address":"cccaaaaaacccc",
    "org":"1",
    "status":true,
    "createDate":"",
    "createPerson":"ee",
    "updateDate":null,
    "updatePerson":""
}
```

#### 5. api/putSupplier
header Bearer token
```
{
    "suppId":19,
    "suppName":"aufffffffffffffff",
    "tel":"q2",
    "fax":"qqqqqqqqqqq",
    "address":"cccaaaaaacccc",
    "org":"1",
    "status":true,
    "createDate":"",
    "createPerson":"ee",
    "updateDate":null,
    "updatePerson":""
}
```

#### 6. api/deleteSupplier/{id}
header Bearer token
@PathVariable(value="id") long id

#### 7.api/getSuppByCondi
header Bearer token
@RequestParam("org") String org, @RequestParam("suppNM") String suppNM

此為模糊搜尋

#### 8. api/getSupplierBySuppId
header Bearer token
@RequestParam("suppId") long suppId





未完成
---
### 後端:登出 + swagger api



