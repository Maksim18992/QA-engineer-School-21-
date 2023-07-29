> # Раздел 1. Activities

## 1) Activities: запрос на получение ресурсов GET ​/api​/v1​/Activities
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities 
- **Ожидаемый результат:** код ответа: 200 Success - успешное получениe ответа со списком активностей
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 429badef-86ff-4496-950e-12b56fbb0aba
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:** 
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 16:43:03 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
[
    {
        "id": 1,
        "title": "Activity 1",
        "dueDate": "2023-06-18T17:43:04.3123323+00:00",
        "completed": false
        ...
        {
        "id": 30,
        "title": "Activity 30",
        "dueDate": "2023-06-19T22:43:04.3123419+00:00",
        "completed": true
    }
]
```

## 2) Activities: запрос на создание ресурсов POST ​/api​/v1​/Activities

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities
- **Ожидаемый результат:** код ответа: 200 Success  - данные в теле запроса, успешно отправлены на сервер
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 07aa95ef-8e90-4f8c-89aa-586910aeb490
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-17T16:37:01.064Z",
  "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 16:54:54 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-17T16:37:01.064Z",
    "completed": true
}
```

## 3) Activities: запрос на создание несуществующего ресурса POST ​/api​/v1​/Activities

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities
- **Ожидаемый результат:** код ответа: 201 - Created ("cоздано") - данные в теле запроса, успешно отправлены на сервер
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 06ba1cb8-7220-444e-84ff-88a23508c249
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 31,
  "title": "string",
  "dueDate": "2023-06-17T16:37:01.064Z",
  "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 17:01:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "id": 31,
    "title": "string",
    "dueDate": "2023-06-17T16:37:01.064Z",
    "completed": true
}
```

## 4) Activities: запрос на извлечение ресурсов GET ​/api​/v1​/Activities​/{id} с корректным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{id_ok}}
- **Ожидаемый результат:**  НТТР статус 200 ОК. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: db41283f-34ad-4aec-a123-6b789bb43d0e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 17:04:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-06-18T18:06:20.1347477+00:00",
    "completed": false
}
```

## 5) Activities: запрос на обновление ресурсов PUT ​/api​/v1​/Activities/{id} с корректным id
 
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Activities/{{id_ok}}
- **Ожидаемый результат:** НТТР статус 200 ОK. Запрос на обновление ресурсов прошёл успешно
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: c5cce673-7060-496e-a835-38e333d45da2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-17T16:53:15.454Z",
  "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 17:08:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа**
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-17T16:53:15.454Z",
    "completed": true
}
```

## 6) Activities: запрос на удаление ресурсов DELETE ​/api​/v1​/Activities​/{id} с корректным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities/1
- **Ожидаемый результат:** НТТР статус 200 ОК. Удаление ресурса прошло успешно
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 0b81dac1-2152-4a67-9e50-23ea1b383f36
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Length: 0
Date: Sun, 18 Jun 2023 17:10:52 GMT
Server: Kestrel
api-supported-versions: 1.0

***

## 7) Activities: запрос на извлечение ресурсов GET ​/api​/v1​/Activities​ с отрицательным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{negative_id}}
- **Ожидаемый результат:** НТТР статус 404. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b4b19d10-a4be-48f2-a780-de6e6329f0d0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 17:13:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-a246861882dea743821302a5a8eba385-4d38cc7185489f4b-00"
}
```

## 8) Activities: запрос на извлечение ресурсов с несуществующим id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities/31
- **Ожидаемый результат:** НТТР статус 404. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 101620e5-e07e-4112-b8ba-03876e2c2e9c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 17:15:21 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-063a60ac83e2b74390f695dd8fcc2053-37ab1ef3a75d0f47-00"
}
```

## 9) Activities: запрос на извлечение ресурсов с невалидным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{not_valid}}
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 182ca438-f268-49e7-9355-e0b4b29f3462
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 17:15:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-997c56888be5b04f935de1096874912d-d8a31bee4237c946-00",
    "errors": {
        "id": [
            "The value '9999999999' is not valid."
        ]
    }
}
```

## 10) Activities: запрос на обновление ресурсов с отрицательным id

- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Activities/{{negative_id}}
- **Ожидаемый результат:**  НТТР статус 405 Method Not Allowed или 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 656aca3e-12c9-42eb-af79-569debe5c70c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-17T16:53:15.454Z",
    "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 17:17:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "id": 0,
    "title": "string",
    "dueDate": "2023-06-17T16:53:15.454Z",
    "completed": true
}
```

## 11) Activities: запрос на обновление ресурсов с несуществующим id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{Activities_bad}}
- **Ожидаемый результат:** НТТР статус 201 ОК. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:**  
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 38caed34-3c5e-4ee1-899f-49b10d51bf13
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

- **Тело запроса:**
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-17T16:53:15.454Z",
  "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 17:20:08 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

- **Тело ответа** 
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-17T16:53:15.454Z",
  "completed": true
}
```

## 12) Activities: запрос на обновление ресурсов с невалидным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{not_valid}}
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6e14e8ef-ea32-4cec-99b0-59cfb32a3b8b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-17T16:53:15.454Z",
  "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 17:22:05 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1d532ec6cf04d243b844443cfc2fb318-b34aa096c1034143-00",
    "errors": {
        "id": [
            "The value '9999999999' is not valid."
        ]
    }
}
```

## 13) Activities: запрос на обновление ресурсов с пустым телом запроса

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities/1
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 49a34f09-4261-445f-b39f-37b9dd4447ae
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 17:23:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-767cd2e2086d86409db6a9d7644acc71-8a14cca4e783764b-00",
    "errors": {
        "": [
            "A non-empty request body is required."
        ],
        "id": [
            "The value ' ' is invalid."
        ]
    }
}
```

## 14) Activities: запрос на обновление ресурсов с некорректным телом запроса

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{id_ok}}
- **Ожидаемый результат:** НТТР статус 400.Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6a7f6f8b-ad83-41c3-a1e3-e949d2a6423f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
    "id": 1,
    "title": S,
    "dueDate": "",
    "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 17:25:25 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-39af2ceb0d47264aa172ba6dd1146f66-04b5601ecf49c64e-00",
    "errors": {
        "$.title": [
            "'S' is an invalid start of a value. Path: $.title | LineNumber: 4 | BytePositionInLine: 10."
        ]
    }
}
```
## 15) Activities: запрос на удаление несуществующих ресурсов 

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{negative_id}}
- **Ожидаемый результат:** НТТР статус 404 или 410 Gone
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: cade5897-9413-4a45-b235-77b430863c5d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
- **Заголовки ответа:**
Content-Length: 0
Date: Sun, 18 Jun 2023 17:28:07 GMT
Server: Kestrel
api-supported-versions: 1.0
- **Тело ответа** 

## 16) Activities: запрос на создание ресурсов с пустым телом запроса

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: d4003743-1cec-47f7-9d08-9dc25110f9ce
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 17:30:44 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-89314f91109a6a4a8b5202853209e818-5dca9442f6f3ed46-00",
    "errors": {
        "": [
            "A non-empty request body is required."
        ]
    }
}

## 17) Activities: запрос на создание ресурса с некорректным телом запроса

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Activities
- **Ожидаемый результат:**  НТТР статус 400.Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: d32cb495-9ecd-4994-bb8f-37e3f80e86f8
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
 "id": 1,
 "title": S,
 "dueDate": "",
 "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 17:31:43 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-be41d644f596484f99ed86a508bbf3e4-e87e4c5aad8b7b40-00",
    "errors": {
        "$.title": [
            "'S' is an invalid start of a value. Path: $.title | LineNumber: 2 | BytePositionInLine: 10."
        ]
    }
}
```

> # Раздел 2. Authors

## 1) Authors: запрос на получение ресурсов GET ​/api​/v1​/Authors

- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Authors
- **Ожидаемый результат:** НТТР код статуса 200 ОК. - успешное получениe ответа со списком авторов
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 8d3c8c38-5c43-4313-a6fd-eaead09bfd76
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 04:30:41 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
[
    {
        "id": 1,
        "idBook": 1,
        "firstName": "First Name 1",
        "lastName": "Last Name 1"
    },
    ...
]
```

## 2) Authors: запрос на создание ресурсов POST ​/api​/v1​/Authors

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors
- **Ожидаемый результат:** НТТР статус 200 ОК. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 317b1160-a4a4-43f8-85db-b0fa0cc95066
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 04:33:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

## 3) Authors: запрос на извлечение ресурсов GET ​/api/v1/Authors/authors/books/{idBook} с корректным id

- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/1
- **Ожидаемый результат:** НТТР статус 200 ОК. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 024e9fe0-9800-4d2e-af8b-f6c3277c7de4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 04:36:00 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
[
    {
        "id": 1,
        "idBook": 1,
        "firstName": "First Name 1",
        "lastName": "Last Name 1"
    },
    {
        "id": 2,
        "idBook": 1,
        "firstName": "First Name 2",
        "lastName": "Last Name 2"
    },
    {
        "id": 3,
        "idBook": 1,
        "firstName": "First Name 3",
        "lastName": "Last Name 3"
    }
]
```

## 4) Authors: запрос на извлечение ресурсов GET ​/api​/v1​/Authors​/{id} с корректным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{id_ok}}
- **Ожидаемый результат:** НТТР статус 200 ОК. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 23c3b781-1d8f-4eb1-9454-50e1c68c7516
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 05:41:54 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
}
```
## 5) Authors: запрос на обновление ресурсов PUT ​/api​/v1​/Authors/{id} с корректным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/1
- **Ожидаемый результат:** НТТР статус 200 ОК. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 12ad78c7-9dc5-4fdd-ba8a-a1f764007d23
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 05:45:04 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "id": 0,
    "idBook": 0,
    "firstName": "string",
    "lastName": "string"
}
```

## 6) Authors: запрос на удаление ресурсов DELETE ​/api​/v1​/Authors​/{id} с корректным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{id_ok}}
- **Ожидаемый результат:** НТТР код статус 200 ОК
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 288c562e-0249-4946-8365-32092894d972
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Length: 0
Date: Mon, 19 Jun 2023 05:46:18 GMT
Server: Kestrel
api-supported-versions: 1.0

## 7) Authors: запрос на создание несуществующего ресурса POST ​/api​/v1​/Authors

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors
- **Ожидаемый результат:** код ответа: 201 - Created ("cоздано") - данные в теле запроса, успешно отправлены на сервер
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7bc1e417-04ec-4113-8e25-d4f54e9608ef
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 800,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 05:48:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
  "id": 800,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

***

## 8) Authors: запрос на получение ресурсов GET ​/api​/v1​/Authors​ с отрицательным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{negative_id}}
- **Ожидаемый результат:** НТТР статус 404. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b0cd790f-1cd7-4c55-85d4-11437f43d18e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 05:50:08 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-b7f29cd26645a84f9e97d06a4629d899-13ef459c31cef846-00"
}
```

## 9) Authors: запрос на извлечение ресурсов GET ​/api​/v1​/Authors​/{id} с несуществующим id

- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Authors/600
- **Ожидаемый результат:**  НТТР код статус 404. Запрос на получение несуществующего ресурса провален
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a91cee91-97cf-4c23-88db-e0a36c0b3ed1
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 05:51:58 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "id": 600,
    "idBook": 199,
    "firstName": "First Name 600",
    "lastName": "Last Name 600"
}
```

## 10) Authors: запрос на извлечение ресурсов GET ​/api​/v1​/Authors​/{id} с невалидным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{not_valid}}
- **Ожидаемый результат:** НТТР код статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 9384c1e0-c3ef-473c-a91c-3fb2d578a8cd
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 19 Jun 2023 05:54:58 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-fb27e6450f118742a6a537d7395d887b-de59c90612df5344-00",
    "errors": {
        "id": [
            "The value '9999999999' is not valid."
        ]
    }
}
```

## 11) Authors: запрос на получение ресурсов GET ​/api​/v1​/Authors​/authors​/books​/{idBook} с отрицательным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/-1
- **Ожидаемый результат:** НТТР статус 404. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 724faaa0-ea1f-456e-813c-25006a50ce9c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 05:56:17 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
[]
```
## 12) Authors: запрос на извлечение ресурсов GET ​/api​/v1​/Authors​/authors​/books​/{idBook} с несуществующим id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/250
- **Ожидаемый результат:** НТТР статус 404. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: f17b114c-b9af-4b70-b5db-94aa98546a46
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 05:57:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
[]
```

## 13) Authors: запрос на извлечение ресурсов GET ​/api​/v1​/Authors​/authors​/books​/{idBook} с невалидным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{not_valid}}
- **Ожидаемый результат:** НТТР статус 400.Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3 
Accept: */*
Cache-Control: no-cache
Postman-Token: 26e97929-35de-4ad6-a1bf-4ee339021fcc
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 19 Jun 2023 05:58:22 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-f346808584f35847829927ea53e13247-7fdf0977bdd7d443-00",
    "errors": {
        "idBook": [
            "The value '9999999999' is not valid."
        ]
    }
}
```

## 14) Authors: запрос на обновление ресурсов с отрицательным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{negative_id}}
- **Ожидаемый результат:**  НТТР статус 405 Method Not Allowed или 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: bcbd8dfc-1139-41bc-9764-851b66a90ce0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 05:59:16 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

## 15) Authors: запрос на обновление ресурсов с несуществующим id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/1000
- **Ожидаемый результат:** НТТР код статус 201 ОК. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 048685ae-2931-4709-a565-d62344251536
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- **Заголовки ответа:**
Content-Type: application/json; charset=utf-8; v=1.0
Date: Mon, 19 Jun 2023 06:01:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
- **Тело ответа** 
```
{
    "id": 0,
    "idBook": 0,
    "firstName": "string",
    "lastName": "string"
}
```

## 16) Authors: запрос на обновление ресурсов с невалидным id

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{not_valid}}
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 49aa51bd-29d4-4ad5-8810-2661961e7815
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 19 Jun 2023 06:02:32 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1df0f76e16f31c458de4c8b16039887d-6983f4d91409554c-00",
    "errors": {
        "id": [
            "The value '9999999999' is not valid."
        ]
    }
}
```

## 17) Authors: запрос на обновление ресурсов с некорректным телом запроса
 
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/1
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 24a7a015-7af0-4f4c-948e-273acecccd56
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:**
```
{
 "id": 1,
 "title": S,
 "dueDate": "",
 "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 19 Jun 2023 06:03:56 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-7caf075396326a4c894c952548dfa3f2-0ee5e2b4ef0adb4b-00",
    "errors": {
        "$.title": [
            "'S' is an invalid start of a value. Path: $.title | LineNumber: 2 | BytePositionInLine: 10."
        ]
    }
}
```

## 18) Authors: запрос на обновление ресурсов с пустым телом запроса

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/1
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6c2a9ceb-cdf9-46b1-8a1c-62b01178ce1d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 19 Jun 2023 06:04:58 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-110694765c8d284c91dd2254eac8307e-b00885d0b7da0245-00",
    "errors": {
        "": [
            "A non-empty request body is required."
        ]
    }
}
```

## 19) Authors: запрос на удаление несуществующих ресурсов 

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors/1000
- **Ожидаемый результат:** НТТР код статус 404 или 410
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 25dd0ecf-7397-49fb-8149-fd4c56cb5043
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Length: 0
Date: Mon, 19 Jun 2023 06:05:52 GMT
Server: Kestrel
api-supported-versions: 1.0

## 20) Authors: запрос на удаление ресурсов с невалидным id

- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Authors/{{not_valid}}
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 40239648-f108-4223-bcfa-4ce4b1398faa
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 19 Jun 2023 06:06:59 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-9eccc20a7e69114d9fb61a8e46b9e0ce-6b3c326c9d9ae74a-00",
    "errors": {
        "id": [
            "The value '9999999999' is not valid."
        ]
    }
}
```

## 21) Authors: запрос на создание ресурсов с пустым телом запроса

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:** 
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 54365c30-2825-48ad-830c-c06b8963e8ec
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 19 Jun 2023 06:08:26 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-1d659c4c96158e4fbed1608aee6e4e15-5a215c247a20f541-00",
    "errors": {
        "": [
            "A non-empty request body is required."
        ]
    }
}
```

## 22) Authors: запрос на создание ресурса с некорректным телом запроса

- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Authors
- **Ожидаемый результат:** НТТР статус 400. Тело ответа в формате JSON возвращается от сервера
- **Заголовки запроса:**
Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: cce500c7-be3d-49a7-985d-c57a8a0762fe
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive 
- **Тело запроса:**
```
{
 "id": 1,
 "title": S,
 "dueDate": "",
 "completed": true
}
```
- **Заголовки ответа:**
Content-Type: application/problem+json; charset=utf-8
Date: Mon, 19 Jun 2023 06:09:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
- **Тело ответа** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-24ea50655bf35d44897291ea3f29c517-db0b0b4db5a34a48-00",
    "errors": {
        "$.title": [
            "'S' is an invalid start of a value. Path: $.title | LineNumber: 2 | BytePositionInLine: 10."
        ]
    }
}
```
 
> # Раздел 3. Books

## 1) Books : получение списка книг * GET ​/api​/v1​/Books 200 OK
- **URL** https://fakerestapi.azurewebsites.net/api/v1/Books
- **Ожидаемый результат:** код HTTPS ответа: `200 Success` - успешное получениe ответа со списком книг
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7d34d116-789b-44b4-af6a-0a2c86b16908
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса** `-`
- **Заголовки ответа**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:42:48 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа** 
```
[
    {
    "id": 1,
    "title": "Book 1",
    "description": "Dolores ullamcorper amet no ipsum dolor. Et at adipiscing wisi. Kasd congue lorem sit consequat nulla. In nonumy invidunt voluptua ut nonumy. Nonumy nonumy et. Erat ipsum et gubergren dolore accusam accusam justo amet vulputate nibh sed molestie ut nulla dolores lorem hendrerit sea. Dolores no lorem dolor vero consequat dolore amet.\n",
    "pageCount": 100,
    "excerpt": "Clita justo dolores luptatum nam aliquyam at illum vero consequat sed duo sed. Dolor sed commodo ullamcorper sadipscing accusam dolore dolore duis ut consetetur et duo at velit at diam. Lorem ea feugiat at vero est. Ea elitr zzril illum gubergren ut. Magna dolor amet sed dolor accusam ut et sit. Eirmod exerci eos. Magna amet gubergren lorem ullamcorper ea ipsum dolor augue voluptua accumsan sadipscing. Sed erat justo vel ipsum. At labore accusam at voluptua et et et et ea commodo nam erat et gubergren ipsum elitr eos labore. Sea eum nisl sit quis ipsum elitr vero at lorem eu ut. Tation dolor ea diam in sea voluptua diam diam molestie. Et adipiscing kasd nibh lobortis nulla eirmod dignissim congue sit sadipscing dolor justo aliquip clita lobortis. Erat sit sit et dolore eos aliquip et clita elitr et sed takimata ut justo gubergren est dolores erat. Dolores in ad et stet duo kasd et dolor erat facer dolor duo sit sea eirmod diam ea. Exerci sanctus suscipit sadipscing aliquip lorem enim vulputate dolore et tempor amet lorem et consectetuer. Vulputate lorem delenit lorem rebum in tempor. Et volutpat justo takimata clita diam aliquyam justo nonumy ut dolore ipsum erat amet ea sed ut dolor. No gubergren sit tempor ea ut dolores dolor dolores diam elit tempor invidunt justo magna nonummy magna.\nAt est dolor qui consetetur clita wisi. Amet facilisis est dolore eirmod consectetuer et facilisis ea justo consequat est accusam consetetur feugait stet. No magna amet et. Consequat duo hendrerit no blandit amet ipsum at sit sit erat lorem. Iusto stet magna facilisi ipsum nonumy sed et facilisi et et dolor amet aliquyam minim. Et in ea aliquyam aliquip sadipscing. Sed erat dolore elit lorem suscipit sit. Invidunt ea duis tempor duo tempor dolor rebum et sea. Aliquyam dolor consetetur takimata duo elit ad option lorem illum ipsum voluptua amet facilisis elitr kasd quis cum. Voluptua nulla accusam labore sit erat.\nEt facilisi dolore voluptua sadipscing nisl amet rebum qui ut et ea sit. No dolor sit dolor labore diam sadipscing. Facilisis tation feugait takimata et sed et dolores dolor lorem eum et dolores sed labore. Gubergren eirmod justo rebum sanctus tempor placerat possim sit consetetur dolore eum illum consetetur et. Amet vero dolore hendrerit ex aliquip invidunt et sed lorem lobortis sit ipsum. Et duo quod erat sed ut nulla feugiat invidunt lorem. Est est justo. Ipsum dolores lorem et ut elitr sed. Veniam sanctus est rebum dolor. Justo et lorem stet aliquyam iriure ut lorem est ipsum. Sit lorem tempor dolore ut amet labore dolor sanctus diam et aliquip aliquyam dolores. Nonumy sed erat vero tempor et magna et duo kasd consetetur duo at. Dolor lorem minim dolor facer molestie justo sed. Tempor eu possim stet. Nulla elit accusam et ipsum magna sed takimata et dolore et erat accusam invidunt justo vulputate dolores nulla at. Ea eum et ex no dolor erat ipsum stet elitr duis minim takimata sit.\nAccusam aliquam consequat sadipscing est eirmod nonumy nulla ut amet quis dolore. Voluptua assum ipsum ea accumsan. Labore no diam duo dolor ipsum consetetur amet diam diam ut nonumy et imperdiet consectetuer qui dolor sadipscing dolore. Diam sit amet magna ea esse rebum voluptua sea et te dolores nobis voluptua invidunt consetetur magna ut. Sed sed sadipscing duo tempor amet voluptua ipsum tempor accusam erat vulputate. Et dolore sadipscing commodo stet quod invidunt dolor nisl dolor eirmod esse at labore ullamcorper elit vero voluptua eirmod. Sed elitr at labore lorem sit magna. Ut sed accusam est eu. Ipsum magna et nisl magna nisl lorem ut ipsum gubergren. Stet congue amet amet eirmod rebum sed gubergren sadipscing commodo takimata doming no ut consetetur. Diam clita stet zzril dolor takimata clita eu at commodo vel sit eu augue. Lobortis illum nulla qui nonumy ea elitr zzril ad voluptua eirmod eirmod ipsum amet. Vero lorem invidunt tempor vulputate takimata diam dolor invidunt sanctus tempor. Sadipscing odio stet enim sit magna lorem erat gubergren rebum autem. Ipsum dolores sit lorem nonumy no justo no tempor accusam vero illum sadipscing vero takimata.\nSanctus consetetur erat vel et eu consetetur sit feugait. In ipsum amet quod iriure nonumy congue erat accusam. Sed facer facer eirmod. Nonummy et sadipscing zzril sea kasd vero vel amet est justo esse dolore magna. Dolor volutpat enim laoreet imperdiet gubergren gubergren dolor ipsum sadipscing. Id sit eros diam duo et consetetur. Consequat erat dolor vel justo minim volutpat eos vel in amet ipsum. Ipsum molestie no facilisi voluptua ea laoreet ut lorem vero amet lobortis augue sit takimata no mazim lorem dolor. Dolor erat vero sit magna amet rebum erat clita et no et nonumy. Eum ea erat ut ut tation invidunt.\n",
    "publishDate": "2023-06-17T12:20:36.2047691+00:00"
  }
]
```

## 2)  Books : обновление данных книги под id:7 * POST ​/api​/v1​/Books 200 OK
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Books
- **Ожидаемый результат:** код HTTPS ответа: `200 - Success` - успешное обновление данных книги 
- **Заголовки запроса:** 
` User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: abe9ddf9-d13a-4ed5-a724-57e9969ebb11
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-18T11:29:30.336Z"
}
```
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 10:54:57 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
отсутсвует
```

## 3) Books : получение данных книги под id:1 * GET ​/api​/v1​/Books​/{id} 200 OK
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Books/{{activity_id}}
- **Ожидаемый результат:** код HTTPS ответа: `200 Success` - успешное получениe ответа с данными книги под id:1
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7e4a7651-8eed-4f44-be86-fc77def65696
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:55:41 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
отсутсвует
```

## 4) Books : получение данных книги под {{activitynegative_id}} *GET ​/api​/v1​/Books​/{id} 400 surpass
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Books/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное 
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 033e991d-1fe0-4790-9896-1ef946cc5238
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Length: 0
Date: Sun, 18 Jun 2023 11:10:30 GMT
Server: Kestrel`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0e7807c2db36cf49bd41660a6c13c10d-36cc6afabe479343-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```

## 5)  Books : получение данных книги под id:0 * GET ​/api​/v1​/Books​/{id} 404 none 
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Books/{{activity_null}}
- **Ожидаемый результат:** код HTTPS ответа: `404 - Error: Not Found` - пользователь под id:0 не найден  
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7e4a7651-8eed-4f44-be86-fc77def65696
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:55:41 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-8b4fe036dab3444499dc7edfed8646d6-ce9b72f616a1894c-00"
}
```

## 6)  Books : изменение данных  книги под id:1 *PUT ​/api​/v1​/Books​/{id} 200 OK
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Books/{{activity_id}}
- **Ожидаемый результат:** код HTTPS ответа: `200 - Success` - успешное обновление данных книги под id:7
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 040e47b1-4762-4c7a-aabe-4e1a1e0702c2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
   {
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-18T10:57:20.480Z"
}
}
```
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 10:59:11 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-18T10:57:20.480Z"
}
```

## 7)  Books : изменение данных книги под {{activitynegative_id}} *PUT ​/api​/v1​/Books​/{id} 400 surpass
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Books/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-18T10:57:20.480Z"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e44e9436bedd8c429047fc39e78a2408-6e937e3a40eaf246-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```

## 8)  Books : изменение данных книги под {{activitynegative_id}} *PUT ​/api​/v1​/Books​/{id} 400 surpass
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Books/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-18T10:57:20.480Z"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e44e9436bedd8c429047fc39e78a2408-6e937e3a40eaf246-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```

## 9)  Books : внесение данных книги с пустым полем * PUT ​/api​/v1​/Books​/{id} 400 null body
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Books/
- **Ожидаемый результат:** код HTTPS ответа -> `400 - Error: Bad Request` - изменение данных с пустым полем
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
отсуствует
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
отсутсвует 
```

## 10)  Books : удаление книги под id:1 * DELETE ​/api​/v1​/Books​/{id} 200 OK 
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Books/{{activity_id}}
- **Ожидаемый результат:** код HTTPS ответа: `200 - Success` - успешное удаление книги под id:1
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3e121446-aa7d-4c96-b744-bde1e92369c4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Length: 0
Date: Sun, 18 Jun 2023 11:02:15 GMT
Server: Kestrel
api-supported-versions: 1.0`
- **Тело ответа:** `-`

## 11)  Books : удаление книги под {{activitynegative_id}} * DELETE ​/api​/v1​/Books​/{id} 400 surpass 
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Books/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ed9d6dc4-8ea9-423e-a7d2-06d113830591
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:** `-`
- **Заголовки ответа:**
Content-Length: 0
Date: Sun, 18 Jun 2023 11:03:04 GMT
Server: Kestrel
api-supported-versions: 1.0
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-44cf97c208271f439a2dd44f3ad6f167-a26e32fbbe2ff148-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```

## 12)  Books : изменение данных книги под {{activity_null}} *PUT ​/api​/v1​/Books​/{id} 400 surpass
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Books/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-18T10:57:20.480Z"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e44e9436bedd8c429047fc39e78a2408-6e937e3a40eaf246-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
} 
```

> # Раздел 4. CoverPhotos

## 1) CoverPhotos : получение списка обложки * GET ​/api​/v1​/CoverPhotos 200 OK
- **URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
- **Ожидаемый результат:** код HTTPS ответа: `200 Success` - успешное получениe ответа со списком обложки
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3afe40f9-7759-430a-9218-d31e398500e2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса** 
  ```
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }
  ```
- **Заголовки ответа**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:08:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа** 
```
[
    {
        "id": 1,
        "idBook": 1,
        "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
    }
]
```

## 2)  CoverPhotos : создание данных обложки  * POST ​/api​/v1​/CoverPhotos 200 OK
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
- **Ожидаемый результат:** код HTTPS ответа: `200 - Success` - успешное обновление данных обложкии 
- **Заголовки запроса:** 
` User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: abe9ddf9-d13a-4ed5-a724-57e9969ebb11
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 10:54:57 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
    "id": 0,
    "idBook": 0,
    "url": "string"
}
```


## 3) CoverPhotos : получение данных обложки под id:1 * GET ​/api​/v1​/CoverPhotos/books​/{id} 200 OK
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}
- **Ожидаемый результат:** код HTTPS ответа: `200 Success` - успешное получениe ответа с данными обложкии под id:1
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7e4a7651-8eed-4f44-be86-fc77def65696
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:55:41 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
отсутствует
```
## 4) CoverPhotos : получение данных обложки под {{activitynegative_id}} *GET ​/api​/v1​/CoverPhotos/books​/{id} 400 surpass
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное 
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 033e991d-1fe0-4790-9896-1ef946cc5238
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
  ```
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  }
  ```
- **Заголовки ответа:**
`Content-Length: 0
Date: Sun, 18 Jun 2023 11:10:30 GMT
Server: Kestrel`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0e7807c2db36cf49bd41660a6c13c10d-36cc6afabe479343-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```
## 5)  CoverPhotos : получение данных обложки под id:0 * GET ​/api​/v1​/CoverPhotos/books​/{id} 404 none 
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_null}}
- **Ожидаемый результат:** код HTTPS ответа: `404 - Error: Not Found` - пользователь под id:0 не найден  
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7e4a7651-8eed-4f44-be86-fc77def65696
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:55:41 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-8b4fe036dab3444499dc7edfed8646d6-ce9b72f616a1894c-00"
}
```

## 6)  CoverPhotos : получение данных обложки с пустым полем * GET ​/api​/v1​/CoverPhotos/books​/{id} 400 null body
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа -> `400 - Error: Bad Request` - получение данных с пустым полем
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
отсутствует
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
отсутствует
```

## 7) CoverPhotos : получение данных фото под {{activitynegative_id}} *GET ​/api​/v1​/CoverPhotos​/{id} 400 surpass
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное 
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 033e991d-1fe0-4790-9896-1ef946cc5238
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
  {
  "id": 1,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
} 
```
- **Заголовки ответа:**
`Content-Length: 0
Date: Sun, 18 Jun 2023 11:10:30 GMT
Server: Kestrel`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0e7807c2db36cf49bd41660a6c13c10d-36cc6afabe479343-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
} 
```

## 8)  CoverPhotos : получение данных фото под id:0 * GET ​/api​/v1​/CoverPhotos​/{id} 404 none 
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_null}}
- **Ожидаемый результат:** код HTTPS ответа: `404 - Error: Not Found` - пользователь под id:0 не найден  
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7e4a7651-8eed-4f44-be86-fc77def65696
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
  {
  "id": 1,
  "idBook": 1,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:55:41 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-8b4fe036dab3444499dc7edfed8646d6-ce9b72f616a1894c-00"
} 
```

## 9)  CoverPhotos : получение данных фото с пустым полем * GET ​/api​/v1​/CoverPhotos/books​/{id} 400 null body
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}
- **Ожидаемый результат:** код HTTPS ответа -> `400 - Error: Bad Request` - получение данных с пустым полем
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
отсутствует
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
отсутствует
```

## 10)  CoverPhotos : внесение данных обложкии с пустым полем * PUT ​/api​/v1​/CoverPhotos​/{id} 400 null body
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}
- **Ожидаемый результат:** код HTTPS ответа -> `400 - Error: Bad Request` - изменение данных с пустым полем
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
отсутствует
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
отсутствует
```

## 11)  CoverPhotos : изменение данных  обложки под id:1 *PUT ​/api​/v1​/CoverPhotos​/{id} 200 OK
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}
- **Ожидаемый результат:** код HTTPS ответа: `200 - Success` - успешное обновление данных обложки под id:7
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 040e47b1-4762-4c7a-aabe-4e1a1e0702c2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "idBook": 0,
  "url": "string"
}
```
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 10:59:11 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-18T10:57:20.480Z"
}
```

## 12)  CoverPhotos : изменение данных обложки под {{activitynegative_id}} *PUT ​/api​/v1​/CoverPhotos​/{id} 400 surpass
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  {
  "id": 0,
  "idBook": 0,
  "url": "string"
}
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e44e9436bedd8c429047fc39e78a2408-6e937e3a40eaf246-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```

## 13)  CoverPhotos : внесение данных обложки с пустым полем * PUT ​/api​/v1​/CoverPhotos​/{id} 400 null body
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}
- **Ожидаемый результат:** код HTTPS ответа -> `400 - Error: Bad Request` - изменение данных с пустым полем
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
отсутствует
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
отсутствует
```

## 14)  CoverPhotos : удаление обложки под id:1 * DELETE ​/api​/v1​/CoverPhotos​/{id} 200 OK 
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}
- **Ожидаемый результат:** код HTTPS ответа: `200 - Success` - успешное удаление обложкии под id:1
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3e121446-aa7d-4c96-b744-bde1e92369c4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Length: 0
Date: Sun, 18 Jun 2023 11:02:15 GMT
Server: Kestrel
api-supported-versions: 1.0`
- **Тело ответа:** `-`

## 15)  CoverPhotos : удаление обложки под {{activitynegative_id}} * DELETE ​/api​/v1​/CoverPhotos​/{id} 400 surpass 
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное
- **Заголовки запроса:** 
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: ed9d6dc4-8ea9-423e-a7d2-06d113830591
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive
- **Тело запроса:** `-`
- **Заголовки ответа:**
Content-Length: 0
Date: Sun, 18 Jun 2023 11:03:04 GMT
Server: Kestrel
api-supported-versions: 1.0
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-44cf97c208271f439a2dd44f3ad6f167-a26e32fbbe2ff148-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```

## 16)  CoverPhotos : изменение данных обложки под {{activity_null}} *PUT ​/api​/v1​/CoverPhotos​/{id} 400 surpass
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activitynegative_id}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 299a1ed7-e94d-4e60-b2f2-d9a448b8dd8c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-18T10:57:20.480Z"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 10:59:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.4.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e44e9436bedd8c429047fc39e78a2408-6e937e3a40eaf246-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
} 
```

> # Раздел 5. Users 

## 1) 5.1 Users : получение списка пользователей * GET ​/api​/v1​/Users 200 OK
- **URL** https://fakerestapi.azurewebsites.net/api/v1/Users
- **Ожидаемый результат:** код HTTPS ответа: `200 Success` - успешное получениe ответа со списком пользователей
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 9bee2a61-3e76-47db-a991-62abe1c8bade
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса** `-`
- **Заголовки ответа**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 11:30:45 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа** 
```
[
    {
        "id": 1, 
        "userName": "User 1", 
        "password": "Password1"
    },
                  ...
    {
        "id": 10, 
        "userName": "User 10", 
        "password": "Password10"
    }
]
```

## 2) 5.2 Users : обновление данных пользователя под id:7 * POST ​/api​/v1​/Users 200 OK
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users
- **Ожидаемый результат:** код HTTPS ответа: `200 - Success` - успешное обновление данных пользователя под id:7
- **Заголовки запроса:** 
` Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 545210f2-1162-48a0-8c2c-1109ece6abd4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive `
- **Тело запроса:** 
```
{
  "id": 7,
  "userName": "7",
  "password": "7"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 14:47:30 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
  "id": 7,
  "userName": "7",
  "password": "7"
}
```
## 3) 5.2 Users : обновление данных пользователя под invalid id * POST ​/api​/v1​/Users 400 surpass
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - данные не могут быть обработаны
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 2be5e535-bb8f-4ab8-b15a-4f9fc87a791d
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 14:48:27 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-3cb5da0bde6cde4899f8548891a6268f-3c3ba4ee2f0c8744-00",
    "errors": {
        "$.id": [
            "The JSON value could not be converted to System.Int32. Path: $.id | LineNumber: 1 | BytePositionInLine: 18."
        ]
    }
}
```
## 4) 5.2. Users : создание данных пользователя под id:11 * POST ​/api​/v1​/Users 201 none (bug)
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users
- **Ожидаемый результат:** код HTTPS ответа -> `201 - Created` - создание данных пользователя под id:11
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: bbdf14be-97ce-46a2-8dfe-951c93182e3e
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 11,
  "userName": "11",
  "password": "11"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 14:46:40 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
  "id": 11,
  "userName": "11",
  "password": "11"
}
```
## 5) 5.2 Users : обновление данных пользователя под id в теле * POST ​/api​/v1​/Users 400 symbol
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение не может быть обработано, а обновления не могут быть применены
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 11ab20ac-0c61-4f30-8830-c5908e048e83
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 14:51:12 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e90de062d7dcae4e81f2a8dca0e3d995-c9970ef29138d04b-00",
    "errors": {
        "$.id": [
            "'@' is invalid within a number, immediately after a sign character ('+' or '-'). Expected a digit ('0'-'9'). Path: $.id | LineNumber: 1 | BytePositionInLine: 9."
        ]
    }
}
```
## 6) 5.2 Users : обновление данных пользователя без тела * POST ​/api​/v1​/Users 400 null body 
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - нет (содержания) тела запроса
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e9471683-e95a-4176-b26d-3d26b399a57f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `удалено`
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 14:52:47 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4f7056506dc7ca42b0168eb284622e94-d8a53404856c2e40-00",
    "errors": {
        "": [
            "A non-empty request body is required."
        ]
    }
}
```
## 7) 5.2. Users : обновление данных пользователя под id:-7 * POST ​/api​/v1​/Users 400 neg. (bug)
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - запрос с отрицательным значением id пользователя не обрабатывается сервером
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: a007d7ae-cfb4-41e8-bc84-0070d72880f0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
    "id": -7,
    "userName": "string",
    "password": "string"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 20:38:27 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "id": -7,
    "userName": "string",
    "password": "string"
}
```

## 8) 5.3 Users : получение данных пользователя под id:7 * GET ​/api​/v1​/Users​/{id} 200 OK
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_ok}}
- **Ожидаемый результат:** код HTTPS ответа: `200 Success` - успешное получениe ответа с данными пользователя под id:7 (username, password) 
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 1f9bd674-6397-4418-bb24-b62f1f4c227f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 13:52:13 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
    "id": 7,
    "userName": "User 7",
    "password": "Password7"
}
```
## 9) 5.3 Users : получение данных пользователя под invalid id *GET ​/api​/v1​/Users​/{id} 400 surpass
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_surpass}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное 
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 8caa2fa3-49be-4e57-8e38-2d0c1fdb1685
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 13:46:50 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-0e7807c2db36cf49bd41660a6c13c10d-36cc6afabe579343-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```
## 10) 5.3 Users : получение данных пользователя под id:11 * GET ​/api​/v1​/Users​/{id} 404 none 
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_none}}
- **Ожидаемый результат:** код HTTPS ответа: `404 - Error: Not Found` - пользователь под id:11 не найден  
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e6ceee64-34f0-483a-af49-1da888e3739b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 13:47:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-8b4fe036dab3444499dc7edfed8646d6-ce9b72f616a1894c-00"
}
```
## 11) 5.3 Users : получение данных пользователя под id:-7 * GET ​/api​/v1​/Users​/{id} 404 neg.  
- **URL:** https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_neg.}}
- **Ожидаемый результат:** код HTTPS ответа: `404 - Error: Not Found` - неприемлиемое значение параметра
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e6ceee64-34f0-483a-af49-1da888e3739b
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 13:47:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
    "title": "Not Found",
    "status": 404,
    "traceId": "00-8b4fe036dab3444499dc7edfed8646d6-ce9b72f616a1894c-00"
}
```

## 12) 5.4 Users : изменение данных старого пользователя под id:7 *PUT ​/api​/v1​/Users​/{id} 200 OK
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_ok}}
- **Ожидаемый результат:** код HTTPS ответа: `200 - Success` - успешное обновление данных пользователя под id:7
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 050e57b1-4762-4c7a-aabe-5e1a1e0702c2
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
    "id": 7,
    "userName": "7",
    "password": "7"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 13:50:54 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "id": 7,
    "userName": "7",
    "password": "7"
}
```
## 13) 5.4 Users : изменение данных пользователя под invalid id *PUT ​/api​/v1​/Users​/{id} 400 surpass
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_surpass}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 1f9bd674-6397-4418-bb24-b62f1f4c227f
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 13:52:13 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e54e9536bedd8c429057fc39e78a2408-6e937e3a50eaf246-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```
## 14) 5.4. Users : внесение данных нового пользователя под id:11 * PUT ​/api​/v1​/Users​/{id} 201 none (bug)
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_none}}
- **Ожидаемый результат:** код HTTPS ответа -> `201 - Created` - изменение данных пользователя под id:11
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 545210f2-1162-48a0-8c2c-1109ece6abd4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
    "id": 11,
    "userName": "11",
    "password": "11"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 13:50:54 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "id": 11,
    "userName": "11",
    "password": "11"
}
```
## 15) 5.4 Users : изменение данных пользователя под id в теле * PUT ​/api​/v1​/Users​/{id} 400 symbol
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_symbol}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение не может быть обработано, а изменения не могут быть внесены
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: cbd6bbb0-004a-47fb-add0-7b0e320090be
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- **Заголовки ответа:**
`Content-Type: application/problem+json; charset=utf-8
Date: Thu, 15 Jun 2023 13:56:02 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-4df5c669c891e64db00883572bd33b0a-24e6630ee074a54f-00",
    "errors": {
        "id": [
            "The value '-@' is not valid."
        ]
    }
}
```
## 16) 5.4 Users : изменение данных пользователя без тела * PUT ​/api​/v1​/Users​/{id} 400 null body
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_null}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - нет (содержания) тела запроса
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 81372e41-54d1-4e03-bb3d-62ef99ad4549
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `удалено`
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 13:57:15 GMT
Server: Kestrel
Transfer-Encoding: chunked`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-e9248a587d79674aa4c21edbcabd6a82-c4cd664a33103049-00",
    "errors": {
        "": [
            "A non-empty request body is required."
        ]
    }
}
```
## 17) 5.4. Users : изменение данных пользователя под id:-7 * PUT ​/api​/v1​/Users​/{id} 400 neg. (bug)
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_neg.}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - запрос с отрицательным значением id пользователя не обрабатывается сервером 
- **Заголовки запроса:** 
`Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: e7e6cba9-cabb-4d5d-b756-6d18a8ca0d0c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** 
```
{
    "id": -7,
    "userName": "string",
    "password": "string"
}
```
- **Заголовки ответа:**
`Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 13:58:07 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "id": -7,
    "userName": "string",
    "password": "string"
}
```

## 18) 5.5 Users : удаление пользователя под id:7 * DELETE ​/api​/v1​/Users​/{id} 200 OK 
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_ok}}
- **Ожидаемый результат:** код HTTPS ответа: `200 - Success` - успешное удаление пользователя под id:7
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 3e121546-aa7d-4c96-b745-bde1e92369c4
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Length: 0
Date: Thu, 15 Jun 2023 14:00:14 GMT
Server: Kestrel
api-supported-versions: 1.0`
- **Тело ответа:** `-`
## 19) 5.5 Users : удаление пользователя под invalid id * DELETE ​/api​/v1​/Users​/{id} 400 surpass 
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_surpass}}
- **Ожидаемый результат:** код HTTPS ответа: `400 - Error: Bad Request` - введенное значение id невалидное
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7c541dd3-39cf-470a-8912-423adbfd9f30
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Length: 0
Date: Thu, 15 Jun 2023 14:02:34 GMT
Server: Kestrel
api-supported-versions: 1.0`
- **Тело ответа:** 
```
{
    "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
    "title": "One or more validation errors occurred.",
    "status": 400,
    "traceId": "00-55cf97c208271f439a2dd54f3ad6f167-a26e32fbbe2ff148-00",
    "errors": {
        "id": [
            "The value '2147483648' is not valid."
        ]
    }
}
```
## 20) 5.5. Users : удаление пользователя под id:11 * DELETE ​/api​/v1​/Users​/{id} 404 none (bug)
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_none}}
- **Ожидаемый результат:** код HTTPS ответа -> `404 - Error: Not Found` - пользователь под id:11 не найден
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7c541dd3-39cf-470a-8912-423adbfd9f30
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Length: 0
Date: Thu, 15 Jun 2023 14:20:36 GMT
Server: Kestrel
api-supported-versions: 1.0`
- **Тело ответа:** `-`
## 21) 5.5. Users : удаление пользователя под id:-7 * DELETE ​/api​/v1​/Users​/{id} 400 neg. (bug)
- **URL:**  https://fakerestapi.azurewebsites.net/api/v1/Users/{{user_neg.}}
- **Ожидаемый результат:** код HTTPS ответа -> `400 - Error: Bad Request` - запрос с отрицательным значением id пользователя не обрабатывается сервером 
- **Заголовки запроса:** 
`User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 7c541dd3-39cf-470a-8912-423adbfd9f30
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive`
- **Тело запроса:** `-`
- **Заголовки ответа:**
`Content-Length: 0
Date: Thu, 15 Jun 2023 14:20:36 GMT
Server: Kestrel
api-supported-versions: 1.0`
- **Тело ответа:** `-`

