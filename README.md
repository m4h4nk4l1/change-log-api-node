# change-log-api-node

# INTRO
#### This is an api developed for changes that be released with different versions of any product to keep track of those internally with a postgresql database storing all the information regarding it. This api is developed using express.js and nodejs as runtime, coded in typescript.

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

The API accepts and returns data in JSON format.
