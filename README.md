# Contents Of Table

-[API Reference](#api-reference)
-[Demo](#demo)

## API Reference

#### Create User

```http
  POST /Account/v1/User
```

| Object    | Type     | Description                 |
| :-------- | :------- | :-------------------------- |
| `userName`| `string` | **Required**. User name     |
| `password`| `string` | **Required**. User password |

#### Authorize Account

```http
  POST /Account/v1/Authorized
```

| Object    | Type     | Description                 |
| :-------- | :------- | :-------------------------- |
| `userName`| `string` | **Required**. User name     |
| `password`| `string` | **Required**. User password |

#### Genetarate Token

```http
  POST /Account/v1/GenerateToken
```

| Object    | Type     | Description                 |
| :-------- | :------- | :-------------------------- |
| `userName`| `string` | **Required**. User name     |
| `password`| `string` | **Required**. User password |

#### Delete User

```http
  DELETE /Account/v1/User/{UUID}
```
| Parameters  | Type     | Description                                   |
| :---------- | :------- | :-------------------------------------------- |
| `UserId`    | `string` | **Required**. Valid user id to delete account |

#### Get Account Information

```http
  GET /Account/v1/User/{UUID}
```

| Parameters  | Type     | Description                                     |
| :---------- | :------- | :---------------------------------------------- |
| `UserId`    | `string` | **Required**. Valid user id to get account info |

#### Get All Books Information

```http
  GET /Bookstore/v1/Books
```

| Bearer Token | Type     | Description                      |
| :----------- | :------- | :------------------------------- |
| `Token`      | `string` | **Required**. Valid Bearer Token |

#### Add List Of Books To User Account

```http
  POST /Bookstore/v1/Books
```

| Bearer Token | Type     | Description                      |
| :----------- | :------- | :------------------------------- |
| `Token`      | `string` | **Required**. Valid Bearer Token |

| Object    | Type     | Description                                  |
| :-------- | :------- | :------------------------------------------- |
| `useId`   | `string` | **Required**. Valid user ID is required      |
| `isbn`    | `string` | **Required**. Valid book ISBN to update book |

#### Delete Books 

````http
  DELETE /BookStore/v1/Books
````
 
| Bearer Token | Type     | Description                      |
| :----------- | :------- | :------------------------------- |
| `Token`      | `string` | **Required**. Valid Bearer Token |

| Parameters | Type     | Description                                   |
| :--------- | :------- | :-------------------------------------------- |
| `UserId`   | `string` | **Required**. Valid user id to delete account |

#### Get Specific Book Information

````https
  GET /BookStore/v1/Book
````

| Bearer Token | Type     | Description                      |
| :----------- | :------- | :------------------------------- |
| `Token`      | `string` | **Required**. Valid Bearer Token |

| Parameters  | Type     | Description                                  |
| :---------- | :------- | :------------------------------------------- |
| `UserId`    | `string` | **Required**. Valid book ISBN to lookup book |

#### Delete Specific Book User Has

````http
  DELETE /BookStore/v1/Book
````

| Bearer Token | Type     | Description                      |
| :----------- | :------- | :------------------------------- |
| `Token`      | `string` | **Required**. Valid Bearer Token |

| Object    | Type     | Description                                  |
| :-------- | :------- | :------------------------------------------- |
| `isbn`    | `string` | **Required**. Valid book ISBN to delete book |
| `useId`   | `string` | **Required**. Valid user ID is required      |

#### Update One Book

```http 
  PUT /BookStore/v1/Books/{ISBN}
```

Authentification Bearer token

| Bearer Token | Type     | Description                      |
| :----------- | :------- | :------------------------------- |
| `Token`      | `string` | **Required**. Valid Bearer Token |

| Parameters | Type     | Description                                  |
| :--------- | :------- | :------------------------------------------- |
| `isbn`     | `string` | **Required**. Valid book ISBN to update book |

| Object    | Type     | Description                                  |
| :-------- | :------- | :------------------------------------------- |
| `useId`   | `string` | **Required**. Valid user ID is required      |
| `isbn`    | `string` | **Required**. Valid book ISBN to update book |
  

## Demo 

- [Docs: BookstoreAPI](https://bookstore.toolsqa.com/swagger)
