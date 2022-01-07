## MONGO CONNECTION 

### example

- mongodb://<USERNAME>:<PASSWORD>@<MONGO-SERVICE>:<PORT>/<DATABASE>

| name | description |
|------|-------------|
| DATABASE | The name of your database |
| MONGO-SERVICE | The service of mongo, do kubectl get service |
| PORT | The mongo service port, usually 27017 |
| USERNAME | The username of the DATABASE |
| PASSWORD | The password of the USERNAME |

### NOTE: You need to create a user in the database, for example in your mongo cli with the admin user

```
use gamesDB
db.games.createUser(
{
  user: 'hencor2019',
  pwd: 'hencor2019',
  roles: [{ role: 'read', db: 'gamesDB'}]
})
```
#### Your uri connection can be: mongodb://hencor2019:hencor2019@mongo-service:27017/gamesDB

### NOTE: Before to apply another service, verify if the user exists in your database
