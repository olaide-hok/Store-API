# Store API

The Store API is designed to provide advanced filtering, sorting, and dynamic database population capabilities for an online store. This API handles all the heavy lifting on the backend, allowing the frontend to make simple HTTP calls to retrieve product data. Whether users need to search by product name, filter by price, or sort by category, the Store API manages these operations efficiently.

## Table of Contents

-   [Overview](#overview)
-   [Features](#features)
-   [Technologies Used](#technologies-used)
-   [Installation](#installation)
-   [Usage](#usage)
-   [API Endpoints](#api-endpoints)
-   [Contributing](#contributing)
-   [License](#license)

## Overview

Imagine you’re in charge of a store's API, and you need to offer a wide range of search and filtering options for users. This API allows users to:

-   Search for products by name.
-   Filter products based on price, category, and company.
-   Sort results according to various parameters.

Inspired by the [Hacker News API](https://hn.algolia.com/api), the Store API shifts the burden of processing from the frontend to the backend. The frontend only needs to make HTTP requests, and the backend handles all the complex queries and returns the relevant data.

## Features

-   **Search by Name**: Easily search for products by their name.
-   **Filter by Price**: Filter products based on price ranges.
-   **Filter by Category and Company**: Narrow down search results by selecting specific categories or companies.
-   **Sorting**: Sort products by price, popularity, or other criteria.
-   **Dynamic Database Population**: Efficiently populate and update the MongoDB database.

## Technologies Used

-   **Node.js**: JavaScript runtime environment.
-   **Express**: Web framework for Node.js.
-   **MongoDB**: Non-relational database used for storing product data.
-   **Mongoose**: Object Data Modeling (ODM) library for MongoDB and Node.js.
-   **dotenv**: Module to load environment variables from a `.env` file.

## Installation

To install and run the Store API locally, follow these steps:

1. Clone the repository:

    ```bash
    git clone https://github.com/olaide-hok/store-api.git
    cd store-api
    ```

2. Install the dependencies:

    ```bash
    npm install
    ```

3. Create a .env file in the root directory and add your MongoDB URI:

    ```bash
    MONGO_URI=your_mongodb_connection_string
    ```

4. Start the development server:

    ```bash
    npm start
    ```

## Usage

Once the server is running, you can interact with the API using HTTP requests. The frontend application can make these requests to search, filter, and sort products.

### Example Request

```bash
GET /products?name=ikea&price[lte]=500&sort=price
```

This request fetches products with "phone" in their name, priced at $500 or less, and sorts the results by price.

## API Endpoints

```bash
GET /products: Retrieve a list of products with various search, filter, and sort options.
```

## Contributing

If you'd like to contribute to this project, please fork the repository and submit a pull request. All contributions are welcome!
