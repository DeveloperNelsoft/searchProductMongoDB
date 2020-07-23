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