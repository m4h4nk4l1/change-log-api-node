# change-log-api-node

### This is an api developed for changes that be released with different versions of any product to keep track of those internally with a postgresql database storing all the information regarding it. This api is developed using express.js and nodejs as runtime, coded in typescript.

## Technologies & libraries used

1. Express.js
2. jwt tokens
3. render for deployment
4. bycrypt and express-validator
5. prisma orm
6. postgresql for data storage

## Testing

Testing of api is done while creating this api is tested using thunder-client which is an vscode extension that can be used to test in over IDE.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)


## Installation

1. Clone the repository: `git clone https://github.com/m4h4nk4l1/change-log-api-node.git`
2. Navigate to the project folder: `cd change-log-api-node`
3. Install dependencies: `npm install`

## Usage

To run the API, execute the following command:

``` npm run dev  ```


The API will be available at `http://localhost:3000` by default. You can change the port in the configuration if needed.

## API Endpoints

The API provides the following endpoints:

- `POST /api/product` - Create a new product entry and log the version change.
- `GET /api/product/:id` - Retrieve the details of a specific product by ID.
- `PUT /api/product/:id` - Update the product details and log the version change.
- `GET /api/product` - Get a list of all products with their latest versions.
- `GET /api/log/:productId` - Retrieve the update log for a specific product.
- `DELETE /api/product/:id` - Deletes the update log for a specific product with given id.
  
- `GET /api/update` - Get all updates.
- `GET /api/update/:id` - Get a specific update by ID.
- `PUT /api/update/:id` - Update an existing update entry. 
  - Request body parameters (optional):
    - `title` (string)
    - `body` (string)
    - `status` (string, valid values: "IN_PROGRESS", "SHIPPED", "DEPRECATED")
    - `version` (string)
- `POST /api/update` - Create a new update entry.
  - Request body parameters (required):
    - `title` (string)
    - `body` (string)
    - `productId` (string)
- `DELETE /api/update/:id` - Delete a specific update by ID.
  
- `GET /api/updatepoint` - Get all update points.
- `GET /api/updatepoint/:id` - Get a specific update point by ID.
- `PUT /api/updatepoint/:id` - Update an existing update point entry.
  - Request body parameters (optional):
    - `name` (string)
    - `description` (string)
- `POST /api/updatepoint` - Create a new update point entry.
  - Request body parameters (required):
    - `name` (string)
    - `description` (string)
    - `updateId` (string)
- `DELETE /api/updatepoint/:id` - Delete a specific update point by ID.



The API accepts and returns data in JSON format.
