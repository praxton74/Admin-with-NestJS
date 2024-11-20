# Admin Panel Project

# Assumptions

- User can have only 1 role.
- 3 Roles: Admin, Editor, User (Authorizations of roles are described down below)
- There are 3 data types. Users, Courses and Contents.
- Courses can have multiple contents.

**Admin**

| Table    | Read | Write | Update | Delete |
| -------- | ---- | ----- | ------ | ------ |
| Users    | ✓    | ✓     | ✓      | ✓      |
| Courses  | ✓    | ✓     | ✓      | ✓      |
| Contents | ✓    | ✓     | ✓      | ✓      |

**Editor**

| Table    | Read   | Write | Update | Delete |
| -------- | ------ | ----- | ------ | ------ |
| Users    | itself |       | itself |        |
| Courses  | ✓      | ✓     | ✓      |        |
| Contents | ✓      | ✓     | ✓      |        |

**User**

| Table    | Read   | Write | Update | Delete |
| -------- | ------ | ----- | ------ | ------ |
| Users    | itself |       | itself |        |
| Courses  | ✓      |       |        |        |
| Contents | ✓      |       |        |        |

# Tech Stack

1. **Backend**: NestJS
2. **Frontend**: React
3. **Database**: PostgreSQL
4. **Testing**: Jest for unit testing. Postman for e2e testing.

# Features

- Swagger Documentation
- JWT authentication with refresh & access token
- Role based authorization
- Data filtering
- Fully responsive design


# First Login

On the first run, application inserts a new admin to the database.

- **username**: admin
- **password**: admin123

