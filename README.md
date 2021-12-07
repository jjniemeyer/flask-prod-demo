## Flask, SQLAlchemy, Postgresql, Gunicorn, Nginx

This was created by following the tutorial [here](https://testdriven.io/blog/dockerizing-flask-with-postgres-gunicorn-and-nginx/#nginx)
The only modifications that I made were using more recent versions of several packages.

### Build and Test for Development

`docker-compose up -d --build`

This uses the development environment variable and Docker run on port 5000. 
Bring down the containers in the usual way `docker-compose down -v`

### Build and Test for Production

`docker-compose -f docker-compose.prod.yml up -d --build`

This uses nginx and gunicorn running port 1337 (hahahaha...blame testdriven.io for that bad joke)

take down `docker-compose -f docker-compose.prod.yml down -v`

###### note:

The env folders have been committed to versioning because there isn't really anything sensitive there and I have no plans to deploy this.