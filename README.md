# CRUD Server with Express and MongoDB

This project is a CRUD server built using Express and MongoDB. It provides API endpoints to perform Create, Read, Update, and Delete operations on a MongoDB database.

## Prerequisites

- Node.js
- npm (Node Package Manager)
- MongoDB Atlas account (or a local MongoDB instance)

## Installation

1. Clone the repository:

   ```sh
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Install the dependencies:

   ```sh
   npm install
   ```

3. Create a `.env` file in the root directory and add your MongoDB connection string and database name:
   ```env
   connectionStringAtlas=<your-mongodb-connection-string>
   dbName=<your-database-name>
   ```

## Running the Server

Start the server using the following command:

```sh
npm start
```

The server will start listening on port 3000.

## API Endpoints

### Get All Collections

- **URL:** `/api/getCollection`
- **Method:** `GET`
- **Description:** Retrieves all collections in the database.

### Get Documents from a Collection

- **URL:** `/api/:collection`
- **Method:** `GET`
- **Description:** Retrieves documents from the specified collection. You can pass query parameters to filter the results.

### Get a Document by ID

- **URL:** `/api/:collection/:id`
- **Method:** `GET`
- **Description:** Retrieves a document by its ID from the specified collection.

### Insert a New Document

- **URL:** `/api/:collection`
- **Method:** `POST`
- **Description:** Inserts a new document into the specified collection. The document data should be sent in the request body.

### Update a Document by ID

- **URL:** `/api/:collection/:id`
- **Method:** `PUT`
- **Description:** Updates a document by its ID in the specified collection. The update data should be sent in the request body.

### Delete a Document by ID

- **URL:** `/api/:collection/:id`
- **Method:** `DELETE`
- **Description:** Deletes a document by its ID from the specified collection.

## Error Handling

- **404 Not Found:** If a requested resource is not found, the server will respond with a 404 status code and an error message.
- **500 Internal Server Error:** If an error occurs during the execution of a request, the server will respond with a 500 status code and an error message.

## License

This project is licensed under the MIT License.
