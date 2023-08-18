# First-Steps-in-Angular-Building-a-Forum-App




# Backend Setup for Forum App

## Extract and Set Up Backend

1. Extract the backend files into the "backend" folder of your repository.
2. Place the Node.js backend files inside the "backend" folder along with the required resources.

## Installation

Use the following command to install dependencies:

```sh
npm install
```

## Update Dependencies

To update dependencies, run:

```sh
npm update
```

## Start the Backend

Start the Node.js backend with:

```sh
npm start
```

## MongoDB Setup with Docker

1. Run a Docker container with MongoDB, mapping ports and volumes:

```sh
docker run -d -p 27017:27017 -v /your/path/to/First-Steps-in-Angular-Building-a-Forum-App/backend/resources/forum:/data/db --name my-mongodb mongo
```

2. Enter the container and copy the resources into the database:

```sh
docker exec -it my-mongodb mongorestore -d forum /data/db/
```

3. Test the database connectivity:

Visit [http://localhost:3000/api/themes](http://localhost:3000/api/themes) to verify if everything is working correctly.
