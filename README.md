#  Документация API для сервиса по работе с пользователями
Данный сайт позволяет получить представление о  документации API для сервиса по работе  с пользователями
##  Содержание
1.[Overview-Что это за API, кому он нужен, краткое описание возможностей](##Overview)

2.[Quickstart-Шаги от регистрации до первого успешного запроса](##Quickstart)

3.[Authentication-Как авторизоваться в API](##Authentication)

4.[API Reference-Отрендеренный справочник по openapi.yaml](##API_Reference)


## Overview 
Что это за API - API для создания, получения, обновления и удаления пользователей. 

Кому он нужен - предназначен для разработчиков, которые не хотят тратить время на разработку интерфейса работы с пользователями. 

Краткое описание возможностей - позволяет создавать, удалять пользователей, выполнять обновление информации о пользователях как полное так и частичное.

[Содержание](##__Содержание)


## Quickstart 
Шаги от регистрации до первого успешного запроса.
Для работы необходимо автризоваться, получив токен через форму запроса.

#### Основной сервер

> url: https://api.documentat.io/api/prod

#### Тестовый сервер

> url: https://api.documentat.io/api/dev


### Операции с пользователями, описание методов

#### GET /users
Получить список всех пользователей

```
get:
      summary: Получить список всех пользователей
      operationId: usersGET
      tags:
        - users
      parameters:
        - name: limit
          in: query
          required: false
          description: Максимальное количество элементов на странице
          schema:
            type: integer
            default: 10
```

#### Ошибки метода

##### 200

```
{
    "id": 0,
    "username": "string",
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "address": {
      "country": "string",
      "city": "string",
      "street": "string",
      "house": "string"
    },
    "age": 0,
    "isEmployee": true,
    "accountStatus": "active"
  }
```

##### 401

```
{
  "code": 0,
  "message": "string"
}
```

##### 500

```
{
  "code": 0,
  "message": "string"
}
```

#### POST /users
Создать нового пользователя

```
 post:
      summary: Создать нового пользователя
      operationId: usersPOST
      tags:
        - users
      requestBody:
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/CreateUser'
```

#### Ошибки метода

##### 201

```
{
    "id": 0,
    "username": "string",
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "address": {
      "country": "string",
      "city": "string",
      "street": "string",
      "house": "string"
    },
    "age": 0,
    "isEmployee": true,
    "accountStatus": "active"
  }
```

##### 401

```
{
  "code": 0,
  "message": "string"
}
```

##### 500

```
{
  "code": 0,
  "message": "string"
}
```







[Содержание](https://github.com/VeronikaSukhareva/API-documentation-for-the-user-management-service/edit/main/README.md#%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5)


## Authentication 
Как авторизоваться в API.

[Содержание](https://github.com/VeronikaSukhareva/API-documentation-for-the-user-management-service/edit/main/README.md#%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5)


## API Reference
Отрендеренный справочник по openapi.yaml

[Содержание](https://github.com/VeronikaSukhareva/API-documentation-for-the-user-management-service/edit/main/README.md#%D1%81%D0%BE%D0%B4%D0%B5%D1%80%D0%B6%D0%B0%D0%BD%D0%B8%D0%B5)

