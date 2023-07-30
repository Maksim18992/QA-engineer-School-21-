# 1. GET ​/api​/v1​/Activities

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии): 
- Статус-код ответа: 200
- Тело ответа (при наличии): 
```
[
  {
    "id": 1,
    "title": "Activity 1",
    "dueDate": "2023-06-11T13:38:23.8865017+00:00",
    "completed": false
  },
  {
    "id": 2,
    "title": "Activity 2",
    "dueDate": "2023-06-11T14:38:23.8865038+00:00",
    "completed": true
  },
```
# 2. POST ​/api​/v1​/Activities 

- HTTP-метод: POST
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии): 
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-11T12:42:43.046Z",
  "completed": true
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-11T12:42:43.046Z",
  "completed": true
}
```
# 3. GET ​/api​/v1​/Activities​/29
  
- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/29
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии): 
- Статус-код ответа: 200
- Тело ответа (при наличии): 
```
{
  "id": 29,
  "title": "Activity 29",
  "dueDate": "2023-06-12T17:48:28.2660672+00:00",
  "completed": false
}
```

# 4. GET ​/api​/v1​/Activities​/35

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/35
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 404
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-15717012f0c9064a9ddcdea444215d49-84f83928617cbe4b-00"
}
```

# 5. PUT ​/api​/v1​/Activities​/15

- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/15
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии):
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-11T11:29:46.157Z",
  "completed": true
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-11T11:29:46.157Z",
  "completed": true
}
```
 
# 6. PUT ​/api​/v1​/Activities​/45948594454354

- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/45948594454354
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии):
```
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-11T11:29:46.157Z",
  "completed": true
}
```
- Статус-код ответа: 400
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-705e6a0e63ff734bbf78e93ed98f1a2c-a7eb9525b9ec7544-00",
  "errors": {
    "id": [
      "The value '45948594454354' is not valid."
    ]
  }
}
```

# 7. DELETE ​/api​/v1​/Activities​/3

- HTTP-метод: DELETE
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/3
- Заголовки запроса: `-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):



# 8. DELETE ​/api​/v1​/Activities​/54645645645654645654
- HTTP-метод: DELETE
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Activities/54645645645654645654
- Заголовки запроса: `-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 400
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-15289e8e4444754597ad3d65fae67e27-884f765db03f7c4a-00",
  "errors": {
    "id": [
      "The value '54645645645654645654' is not valid."
    ]
  }
}
```

***

# 9. GET ​/api​/v1​/Authors

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
```

# 10. POST /api​/v1​/Authors

- HTTP-метод: POST
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии):
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

# 11. GET ​/api​/v1​/Authors​/authors​/books​/1

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/1
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
[
  {
    "id": 1,
    "idBook": 1,
    "firstName": "First Name 1",
    "lastName": "Last Name 1"
  },
```

# 12. GET ​/api​/v1​/Authors​/authors​/books​/34343434343

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/34343434343
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 404
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-df91a148bd8e864dbefce6451d5d8335-bc057f6de83e064c-00",
  "errors": {
    "idBook": [
      "The value '34343434343' is not valid."
    ]
  }
}
```

# 13. GET ​/api​/v1​/Authors​/1

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/1
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 1,
  "idBook": 1,
  "firstName": "First Name 1",
  "lastName": "Last Name 1"
}
```
# 14 GET ​/api​/v1​/Authors​/0

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/0
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 404
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-b8a1f0349bcead46bfdc60020db932e2-83bb91d38ddd534c-00"
}
```

# 15. PUT ​/api​/v1​/Authors​/1

- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/1
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии):
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
```

# 16. PUT ​/api​/v1​/Authors​/2
- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/2
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии):
```
{
  "id": 0,
  "idBook": 0,
  "firstName": S,
  "lastName": "string"
}
```
- Статус-код ответа: 400
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b3409f043dd6414e83a58173e9dc434f-092b67df3bda7e42-00",
  "errors": {
    "$.firstName": [
      "'S' is an invalid start of a value. Path: $.firstName | LineNumber: 3 | BytePositionInLine: 15."
    ]
  }
}
```

# 17. DELETE ​/api​/v1​/Authors​/1

- HTTP-метод: DELETE 
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/1
- Заголовки запроса: ` -H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):

# 18. DELETE ​/api​/v1​/Authors​/564564565454
- HTTP-метод: DELETE 
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Authors/564564565454
- Заголовки запроса: `-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 404
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-1e75102095912441b10f2f77ad4026f7-d8f289d5d39fdf49-00",
  "errors": {
    "id": [
      "The value '564564565454' is not valid."
    ]
  }
}
```

***

# 19. GET /api​/v1​/Books

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
[
  {
    "id": 1,
    "title": "Book 1",
    "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "pageCount": 100,
    "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
    "publishDate": "2023-06-10T13:40:59.4943696+00:00"
  },
```

# 20. POST ​/api​/v1​/Books

- HTTP-метод: POST
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books
- Заголовки запроса: `-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"`
- Тело запроса (при наличии):
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-11T13:41:36.616Z"
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-11T13:41:36.616Z"
}
```

# 21. GET ​/api​/v1​/Books​/60

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/60
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 60,
  "title": "Book 60",
  "description": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "pageCount": 6000,
  "excerpt": "Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\nLorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n",
  "publishDate": "2023-04-12T13:42:59.5476803+00:00"
}
```

# 22. GET ​/api​/v1​/Books​/0
- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/0
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 404
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-fab3596254009c4caf4128f9b93c6350-ec2e6f32d367e840-00"
}
```

# 23. PUT /api​/v1​/Books​/70

- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/70
- Заголовки запроса: `-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"`
- Тело запроса (при наличии): 
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-11T13:47:20.444Z"
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-11T13:47:20.444Z"
}
```

# 24. PUT /api​/v1​/Books​/1

- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/1
- Заголовки запроса: -H  "accept: */*" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии):
```
{
  "id": 0,
  "title": CAT CAT CAT,
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-11T13:48:48.057Z"
}
```
- Статус-код ответа: 400
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-046eaf1a9938d241b1605476e08c5f3a-2eb1a7a891223c45-00",
  "errors": {
    "$.title": [
      "'C' is an invalid start of a value. Path: $.title | LineNumber: 2 | BytePositionInLine: 11."
    ]
  }
}
```

# 25. DELETE /api​/v1​/Books​/45

- HTTP-метод: DELETE
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/45
- Заголовки запроса: `-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):

# 26. DELETE /api​/v1​/Books​/9999999999999999

- HTTP-метод: DELETE
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Books/9999999999999999
- Заголовки запроса: `-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 400
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-be715b3e50dba84aac547de1f3f7b113-a6ccb29ace9f9344-00",
  "errors": {
    "id": [
      "The value '9999999999999999' is not valid."
    ]
  }
}
```

***

# 27. GET /api​/v1​/CoverPhotos

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
- Заголовки запроса:  -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии): 
```
[
  {
    "id": 1,
    "idBook": 1,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"
  },
```

# 28. POST /api​/v1​/CoverPhotos

- HTTP-метод: POST
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии):
```
{
  "id": 0,
  "idBook": 0,
  "url": "MRX"
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 0,
  "idBook": 0,
  "url": "MRX"
}
```

# 29. GET /api​/v1​/CoverPhotos​/books​/covers​/69

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/69
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
[
  {
    "id": 69,
    "idBook": 69,
    "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 69&w=250&h=350"
  }
]
```

# 30. GET /api​/v1​/CoverPhotos​/books​/covers​/4565645654

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/4565645654
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 400
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-8d16441dc39c724ca1f48875bafdc4e6-9d73df2a66dc0245-00",
  "errors": {
    "idBook": [
      "The value '4565645654' is not valid."
    ]
  }
}
```

# 31. GET ​/api​/v1​/CoverPhotos​/2

- HTTP-метод: GET 
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/2
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 2,
  "idBook": 2,
  "url": "https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"
}
```

# 32. GET ​/api​/v1​/CoverPhotos​/0

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/0
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 404
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-d9e4822710432a46bba19001c38f4899-86b920814a10de45-00"
}
```

# 33. PUT /api​/v1​/CoverPhotos​/3

- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/3
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии):
```
{
  "id": 3,
  "idBook": 3,
  "url": "string"
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 3,
  "idBook": 3,
  "url": "string"
}
```

# 34. PUT /api​/v1​/CoverPhotos​/3

- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/3
- Заголовки запроса: -H  "accept: text/plain; v=1.0" -H  "Content-Type: application/json; v=1.0"
- Тело запроса (при наличии):
```
{
  MRX
}
```
- Статус-код ответа: 400
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-b1d54ca1779f2641b4b730a8d66623ed-d6606a14606ddf4b-00",
  "errors": {
    "$": [
      "'M' is an invalid start of a property name. Expected a '\"'. Path: $ | LineNumber: 1 | BytePositionInLine: 2."
    ]
  }
}
```

# 35. DELETE /api​/v1​/CoverPhotos​/1

- HTTP-метод: DELETE 
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/1
- Заголовки запроса:`-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):


# 36. DELETE /api​/v1​/CoverPhotos​/90987078965

- HTTP-метод: DELETE 
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/90987078965
- Заголовки запроса:`-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-3304982f112c2343bc12437809019c74-b31471f337329048-00",
  "errors": {
    "id": [
      "The value '90987078965' is not valid."
    ]
  }
}
```

***

# 37. GET ​/api​/v1​/Users

- HTTP-метод: GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users
- Заголовки запроса: -H  "accept: text/plain; v=1.0"
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
[
  {
    "id": 1,
    "userName": "User 1",
    "password": "Password1"
  },
```

# 38. POST /api​/v1​/Users

- HTTP-метод: POST
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users
- Заголовки запроса: `-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"`
- Тело запроса (при наличии):
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```

# 39. GET /api​/v1​/Users​/10

- HTTP-метод:GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/10
- Заголовки запроса: `-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 10,
  "userName": "User 10",
  "password": "Password10"
}
```

# 40. GET /api​/v1​/Users​/0

- HTTP-метод:GET
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/0
- Заголовки запроса: `-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 404
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.4",
  "title": "Not Found",
  "status": 404,
  "traceId": "00-0041e22de0d9d44f97a0b8fa979fc476-07a08bbdacc2da42-00"
}
```

# 41. PUT /api​/v1​/Users​/5

- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/5
- Заголовки запроса: `-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"`
- Тело запроса (при наличии):
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Статус-код ответа: 200
- Тело ответа (при наличии):
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```


# 42. PUT /api​/v1​/Users​/0097807907998

- HTTP-метод: PUT
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/0097807907998
- Заголовки запроса: `-H  "accept: */*" -H  "Content-Type: application/json; v=1.0"`
- Тело запроса (при наличии):
```
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
```
- Статус-код ответа: 404
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-5155976be34ee34d8f1de0e928c9a47f-241d131bfc354c43-00",
  "errors": {
    "id": [
      "The value '0097807907998' is not valid."
    ]
  }
}
```
# 43. DELETE /api​/v1​/Users​/1

- HTTP-метод: DELETE
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/1
- Заголовки запроса: `-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 200
- Тело ответа (при наличии):

# 44. DELETE /api​/v1​/Users​/3546346345635463

- HTTP-метод: DELETE
- Полный URL запроса: https://fakerestapi.azurewebsites.net/api/v1/Users/3546346345635463
- Заголовки запроса: `-H  "accept: */*"`
- Тело запроса (при наличии):
- Статус-код ответа: 400
- Тело ответа (при наличии):
```
{
  "type": "https://tools.ietf.org/html/rfc7231#section-6.5.1",
  "title": "One or more validation errors occurred.",
  "status": 400,
  "traceId": "00-8ddd2e4fac81bf4fb52a6dd80d62aebc-03c640c5f2195a40-00",
  "errors": {
    "id": [
      "The value '3546346345635463' is not valid."
    ]
  }
}
```