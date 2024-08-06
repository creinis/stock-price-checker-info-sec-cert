## Stock Price Checker

###### Technologies:
<p align="center">
<img src="https://img.icons8.com/color/75/000000/javascript.png" width="50" height="50" alt="JavaScript" style="margin: 10px 15px 0 15px;" />
<img src="https://nodejs.org/static/images/logo.svg" height="35" alt="Node.js" style="margin: 10px 15px 0 15px;" />
<img src="https://expressjs.com/images/express-facebook-share.png" height="35" alt="Express" style="margin: 10px 15px 0 15px;" />
<img src="https://mongoosejs.com/docs/images/mongoose5_62x30_transparent.png" height="50" alt="Mongoose" style="margin: 10px 15px 0 15px;" />
<img src="https://axios-http.com/assets/logo.svg" height="35" alt="Axios" style="margin: 10px 15px 0 15px;" />
</p>

### Try it!

To run the Stock Price Checker application, follow the instructions in the Setup section below.
https://stock-price-checker.freecodecamp.rocks/.

## Project Structure

- `server.js`: Main server file that sets up the Express server and routes.
- `routes/api.js`: Contains the API routes and logic for fetching and storing stock data.
- `tests/2_functional-tests.js`: Contains functional tests for validating the implementation.
- `db-connection.js`: Manages the connection to the MongoDB database.
- `public/script.js`: Contains client-side JavaScript.
- `public/style.css`: Contains styles for the application.
- `views/index.html`: Main HTML file for the application.

## Setup

### Prerequisites

- Node.js installed
- MongoDB installed

### Installation Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/creinis/stock-price-checker-info-sec-cert.git
   cd stock-price-checker
   ```

2. Install the required libraries:
   ```bash
   npm install
   ```

3. Run the Stock Price Checker script:
   ```bash
   npm start
   ```

## Stock Price Checker

### Functionality

The Stock Price Checker allows users to check the latest stock prices and compare them. Users can also like a stock, with the number of likes being limited to one per IP address. The application ensures compliance with data privacy laws by anonymizing IP addresses before storing them.

### Functions

#### Stock Data Retrieval

The application uses a proxy API to fetch up-to-date stock price information, which is then displayed to the user.

#### Like Feature

Users can like a stock, and the application ensures that only one like per IP address is counted. This is achieved by storing anonymized IP addresses in the database.

#### Comparison of Two Stocks

Users can compare two stocks, and the application will display the relative likes between the two.

### Practical Use Case

This application is useful for individuals and investors who want to check current stock prices and compare the popularity of different stocks based on the number of likes.

### Benefits

- **Real-Time Data:** Provides up-to-date stock price information.
- **User Interaction:** Allows users to like stocks and see relative likes for comparisons.
- **Privacy Compliance:** Anonymizes IP addresses to comply with data privacy laws.

## How to Use

1. Start the server using `npm start`.
2. Access the application in your web browser at `http://localhost:3000`.
3. Use the input fields to enter stock symbols and check prices.
4. Like stocks and compare their popularity.

### Example Usage

```javascript
// To view the price of a single stock
fetch('/api/stock-prices?stock=GOOG')
  .then(response => response.json())
  .then(data => console.log(data));

// To view and like a single stock
fetch('/api/stock-prices?stock=GOOG&like=true')
  .then(response => response.json())
  .then(data => console.log(data));

// To view and compare two stocks
fetch('/api/stock-prices?stock=GOOG&stock=MSFT')
  .then(response => response.json())
  .then(data => console.log(data));
```

### Additional Information

- **Dataset:** The stock data is fetched from a proxy API provided by freeCodeCamp.
- **Comprehensive Analysis:** The application allows users to view stock prices, like stocks, and compare likes between two stocks.

---
#### This is a FreeCodeCamp Challenge for Information Security Certification.
<p align="center">
<img src="https://cdn.freecodecamp.org/platform/universal/fcc_primary.svg" width="250" height="75" alt="freeCodeCamp" style="margin: 0 15px; opacity: 0.6" />
</p>