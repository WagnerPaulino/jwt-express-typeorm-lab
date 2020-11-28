# Lab jwt e typeorm

Steps to run this project:

1. Run `npm i` command
2. Insert the first admin user `npm run migration:run` command
3. Run `npm start` command

Create a migration
```bash 
`npx typeorm migration:create -n CreateAdminUser`
```

https://medium.com/javascript-in-plain-english/creating-a-rest-api-with-jwt-authentication-and-role-based-authorization-using-typescript-fbfa3cab22a4


For create a project like this
```bash
npx typeorm init --name jwt-express-typeorm --database sqlite --express
```