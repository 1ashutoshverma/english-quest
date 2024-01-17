# Book Library Management System

### Important Links

- [Frontend deployed Link](https://english-quest-frontend.vercel.app/)

```bash
https://english-quest-frontend.vercel.app/
```

- [Frontend deployed Repo Link](https://github.com/1ashutoshverma/english-quest-frontend) :

```bash
https://github.com/1ashutoshverma/english-quest-frontend
```

- [Backend deployed Link](https://cyan-rich-katydid.cyclic.app/) :

```bash
https://cyan-rich-katydid.cyclic.app/
```

- [Backend deployed Repo Link](https://github.com/1ashutoshverma/english-quest-backend) :

```bash
https://github.com/1ashutoshverma/english-quest-backend
```

- ### [Watch Demo Video](https://drive.google.com/file/d/1r205q8K6x6tlOwoRy23JJ-mKMHvcU_u1/view?usp=drive_link)

## Table of Contents

- [Routes and Methods](#routes-and-methods)
  - [User Routes](#user-routes)
    - [Signup](#signup)
    - [Login](#login)
  - [Book Routes](#book-routes)
    - [Get Books](#get-books)
    - [Add Book](#add-book)
    - [Update Book](#update-book)
    - [Delete Book](#delete-book)

## Routes and Methods

### User Routes

### **Signup**

- Method: POST
- Endpoint: /api/signup
- Request Body:

```json
{
  "email": "user@example.com",
  "name": "John Doe",
  "password": "password123",
  "role": "[\"VIEWER\"]"
}
```

- response

```json
{
  "message": "User signed up successfully"
}
```

### **Login**

- Method: POST
- Endpoint: /api/login
- Request Body:

```json
{
  "email": "user@example.com",
  "password": "password123"
}
```

- response

```json
{
  "message": "login successful",
  "userData": {
    "token": "jwtTokenHere",
    "name": "John Doe",
    "role": ["VIEWER"],
    "userId": "userIdHere"
  }
}
```

### Book Routes

### **Get Books**

- Method: GET
- Endpoint: /books
- Query Parameters:

  - page (optional): Page number for pagination (default: 1)
  - pageSize (optional): Number of items per page (default: 10)

  ```bash
  /books?page=1&pageSize=10
  ```

  - genre (optional): Filter by book genre

  ```bash
  /books?genre=Fiction
  ```

  - old (optional): Show books created 10 minutes ago or earlier

  ```bash
  /books?old=1
  ```

  - new (optional): Show books created less than 10 minutes ago

  ```bash
  /books?new=1
  ```

  - sort (optional): Sort field (e.g., title)
  - order (optional): Sort order (asc or desc)

  ```bash
  /books?sort=title&order=asc
  ```

  - title (optional): Search by title (case-insensitive)

  ```bash
  /books?title=""
  ```

  - author (optional): Search by author (case-insensitive)

  ```bash
  /books?author=""
  ```

- Response:

```json
{
  "data": [...],
  "page": 1,
  "totalPages": 3,
  "totalItems": 25
}
```

### **Add Book**

- Method: POST
- Endpoint: /books
- Request Body:

```json
{
  "title": "The Great Gatsby",
  "author": "F. Scott Fitzgerald",
  "genre": "Classic"
}
```

- response

```json
{
  "message": "Book added successfully"
}
```

### **Update Book**

- Method: PATCH
- Endpoint: /books/update/:id
- Request Body:

```json
{
  "title": "Updated Title",
  "author": "Updated Author",
  "genre": "Updated Genre"
}
```

- response

```json
{
  "message": "Book updated successfully"
}
```

### **Delete Book**

- Method: DELETE
- Endpoint: /books/delete/:id
- response

```json
{
  "message": "Book deleted successfully"
}
```

# Created by Ashutosh Verma

- [LinkedIn](https://www.linkedin.com/in/1ashutoshverma/)
- [Portfolio](https://1ashutoshverma.github.io/)
- [GitHub](https://github.com/1ashutoshverma)
