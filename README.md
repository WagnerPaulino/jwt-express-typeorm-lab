# Lab jwt e typeorm

Steps to run this project:

1. Run `npm i` command
2. Run `npm start` command
3. Insert the first admin user `npm run migration:run` command

Create a migration
```bash 
$ `npx typeorm migration:create -n CreateAdminUser`
```


Login
```bash 
$ curl -X POST http://localhost:3000/auth/login --header "Content-Type: application/json" --data '{"username": "admin", "password": "admin" }'
```

List Users
```bash 
$ curl -X GET http://localhost:3000/user --header "Content-Type: application/json" --header "auth: <TOKEN>"
```

Create User
```bash
curl -X POST http://localhost:3000/user --header "Content-Type: application/json" --header "auth: <TOKEN>" --data '{"username": "wagner", "password": "1234", "role":"user" }'
```

For create a project like this
```bash
npx typeorm init --name jwt-express-typeorm --database sqlite --express
```

Reference:
https://medium.com/javascript-in-plain-english/creating-a-rest-api-with-jwt-authentication-and-role-based-authorization-using-typescript-fbfa3cab22a4