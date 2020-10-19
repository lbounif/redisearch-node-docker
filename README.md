Run the Sample Application
The application and all the services, including RediSearch, are available as a Docker Compose application.

If you have not already downloaded the project, clone it:

> git clone https://github.com/lbounif/redis-search-node-sample.git

> cd redis-search-node-sample

> To run the application:

> docker-compose up --force-recreate --build -d

This Docker Compose will start:

RediSearch instance on port 6380, and import all movies, actors and create indexes
The Node REST Service available on port 8086

Once started you can access the application and its services using the following URLs:

http://localhost:8086/api/1.0/movies/search?q=star&offset=0&limit=10

Stop and Delete Everything
Run the following command to delete the containers & images:

> docker-compose down -v --rmi local --remove-orphans
