# 📦 Serverless Lambda API

This is a **REST API**  using the **Spring boot*****, featuring:


- ✅ Swagger documentation
- ✅ H2 Hibernate
- ✅ Map Struct
- ✅ Global Exeception
- ✅ Spring Security
- ✅ RSA JWT
- ✅ RESTful endpoints for `/api/v1/user`, `/login`, `/logout`

---

## 🌐 Swagger Documentation

Access the full interactive API documentations:

🔗 [Swagger UI](http://localhost:9090/swagger-ui.html#/)

---

## 📡 Deployed API Base URL

### Register User Endpoint

Use the following `curl` command to call the `POST /api/v1/user/` endpoint :

```bash
curl --location 'http://localhost:9090/api/v1/user/' \
--header 'Content-Type: application/json' \
--header 'Cookie: JSESSIONID=F0E5F93F65483E88EA0AA6569E8C9B84' \
--data-raw '    {
  "email": "hola@gmail.cl",
  "name": "hola",
  "password": "Hola123456.",
  "phones": [
    {
      "cityCode": "01",
      "countryCode": "lima",
      "number": "98765678"
    }
  ]
}'
```

### Get User Endpoint
Use the following `curl` command to call the `GET /api/v1/user/{id}` endpoint :

```bash
curl --location 'http://localhost:9090/api/v1/user/c9b3bfaf-24a1-4801-a7da-9ca97fcee9c4' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJzdWIiOiJob2xhQGdtYWlsLmNsIiwiaXNzIjoib2F0aCIsImV4cCI6MTc0NTk4MzY1MiwiaWF0IjoxNzQ1MDgzNjUyfQ.V3r4AG-NJFisJvzKj3mBdtj-wUcs5UaLFsvLbafZRgNDJNmPxkD6avNKZtkpxKp9XBSfocAnz8OUlEMonFZH835ZC3W4Q-a6Y3Ufu5erwIfyL_BcKgn76fsI4anhnCFOjTPaQCXX8efDxflqX6Bb__VoAZGPWf0_stmNSzVVAcf_o7X-DJfFc7mWIZ8dyBNqv-Mz5u1BSt2JaHktXzXsIHEhxiPWLq-q0IrezggVUMZFMfo7ILfomTpcoYXGaY7YPGRR5VxC5aZS6WkxISF7-PoQILM3n3UZZO66B2IsAeP-CBdSoESmRkSsmBdScyb6NUe143joC3tYL4_44R9bMA' \
--header 'Cookie: JSESSIONID=F0E5F93F65483E88EA0AA6569E8C9B84'
```
### Update State User Endpoint
Use the following `curl` command to call the `PACTH /api/v1/user/{id}` endpoint :

```bash
curl --location --request PATCH 'http://localhost:9090/api/v1/user/c9b3bfaf-24a1-4801-a7da-9ca97fcee9c4' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJzdWIiOiJob2xhQGdtYWlsLmNsIiwiaXNzIjoib2F0aCIsImV4cCI6MTc0NTk4MzY1MiwiaWF0IjoxNzQ1MDgzNjUyfQ.V3r4AG-NJFisJvzKj3mBdtj-wUcs5UaLFsvLbafZRgNDJNmPxkD6avNKZtkpxKp9XBSfocAnz8OUlEMonFZH835ZC3W4Q-a6Y3Ufu5erwIfyL_BcKgn76fsI4anhnCFOjTPaQCXX8efDxflqX6Bb__VoAZGPWf0_stmNSzVVAcf_o7X-DJfFc7mWIZ8dyBNqv-Mz5u1BSt2JaHktXzXsIHEhxiPWLq-q0IrezggVUMZFMfo7ILfomTpcoYXGaY7YPGRR5VxC5aZS6WkxISF7-PoQILM3n3UZZO66B2IsAeP-CBdSoESmRkSsmBdScyb6NUe143joC3tYL4_44R9bMA' \
--header 'Cookie: JSESSIONID=F0E5F93F65483E88EA0AA6569E8C9B84' \
--data '{
    "active" : false
}'
```

### Delete  User Endpoint
Use the following `curl` command to call the `DELETE /api/v1/user/{id}` endpoint: 

```bash
curl --location --request DELETE 'http://localhost:9090/api/v1/user/c9b3bfaf-24a1-4801-a7da-9ca97fcee9c4' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJzdWIiOiJob2xhQGdtYWlsLmNsIiwiaXNzIjoib2F0aCIsImV4cCI6MTc0NTk4MzY1MiwiaWF0IjoxNzQ1MDgzNjUyfQ.V3r4AG-NJFisJvzKj3mBdtj-wUcs5UaLFsvLbafZRgNDJNmPxkD6avNKZtkpxKp9XBSfocAnz8OUlEMonFZH835ZC3W4Q-a6Y3Ufu5erwIfyL_BcKgn76fsI4anhnCFOjTPaQCXX8efDxflqX6Bb__VoAZGPWf0_stmNSzVVAcf_o7X-DJfFc7mWIZ8dyBNqv-Mz5u1BSt2JaHktXzXsIHEhxiPWLq-q0IrezggVUMZFMfo7ILfomTpcoYXGaY7YPGRR5VxC5aZS6WkxISF7-PoQILM3n3UZZO66B2IsAeP-CBdSoESmRkSsmBdScyb6NUe143joC3tYL4_44R9bMA' \
--header 'Cookie: JSESSIONID=F0E5F93F65483E88EA0AA6569E8C9B84'
```
### Login Endpoint

Use the following `curl` command to call the `/login` endpoint:

```bash
curl --location 'http://localhost:9090/api/v1/login' \
--header 'Content-Type: application/json' \
--header 'Cookie: JSESSIONID=F0E5F93F65483E88EA0AA6569E8C9B84' \
--data-raw '{
  "email": "hola@gmail.cl",
  "password": "Hola123456."
}'
```

### Logout Endpoint

Use the following `curl` command to call the `/logout` endpoint:

```bash
curl --location --request POST 'http://localhost:9090/api/v1/logout' \
--header 'Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJzdWIiOiJob2xhQGdtYWlsLmNsIiwiaXNzIjoib2F0aCIsImV4cCI6MTc0NTkzMzAzMSwiaWF0IjoxNzQ1MDMzMDMxfQ.dcdr3wBYAzszht6fhKtVB2UMnshoVjz3jVSZHGEkrGcpzJcVz8zr8BELVQfs8Z3F2BXuoQl3w9XXzG455XpSj5_wid1fq527hFoanXCBLWEyvPcFpsxK4yEbNfB2mK5NSWaA9oam2O1-MI1FkVstLAeBaH7ZhHxonYOTOwk2HL6ceSYuRGMtS_NMaz6V35di-ONClyGw7uMEzVa486l5GLq6zm4vmRTxDevNs_x3agn-pN6WOGYjBu8BSy6w8e1YQXKiZwp-xPlrsoHdDdHy4qemXohtA34qPwD1uWo5u_lgrb0PWeDlksC8YRg3EpICgGKkWrO3Xp8E245y6J-5cw' \
--header 'Cookie: JSESSIONID=F0E5F93F65483E88EA0AA6569E8C9B84'
```

### DIAGRAM

       +-------------+         POST /api/v1/user/
           |             | <-------------------------------
           |             |                                  |
           |             |         GET /api/v1/user/{id}    |
           |  FRONTEND   | -------------------------------> |
           |             |                                  |
           |             |         PATCH /api/v1/user/{id}  |
           |             | -------------------------------> |
           |             |                                  |
           |             |         DELETE /api/v1/user/{id} |
           |             | -------------------------------> |
           |             |                                  |
           |             |         POST /api/v1/login       |
           |             | -------------------------------> |
           |             |                                  |
           |             |         POST /api/v1/logout      |
           |             | -------------------------------> |
           +-------------+
