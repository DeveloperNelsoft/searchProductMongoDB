# Search product Mongo DB

data source for Search product back end app.

### Installation

If you want to set the mongodb and import the products to start to consume, use this command:
```sh
$ make database-up
```
If you only want to run the mongodb image, use this one:
```sh
$ make database-docker-up

```

In mongo db, we must consider:

Go to docker container: mongodb-local db admin, and create role to promotions db user

docker ps (get container id hash)

docker exec -it "container id de container mongodb-local" bash

mongo --port 27017 -u productListUser -p productListPassword --authenticationDatabase admin

db.createUser({user:'productListUser',pwd:'productListPassword',roles:[{role:'readWrite',db:'promotions'}]})

```


If you only want to import the products in the running mongodb image, use this:
```sh
$ make database-provision
```
### Something went wrong?

If something went wrong, you can stop and remove the container with this:
```sh
$ make database-down
```

If you want to reset the container:
```sh
$ make database-reset
```