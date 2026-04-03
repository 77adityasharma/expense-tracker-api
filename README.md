# Personal Expense Tracker API

A REST API to log expenses, categorize them, and get spending summaries. Built with Node.js, Express.js, and MongoDB.

## Setup

1. Clone the repo
2. Install dependencies
   ```
   npm install
   ```
3. Create a `.env` file in the root
   ```
   PORT=5000
   MONGO_URI=your_mongodb_atlas_connection_string
   ```
4. Start the server
   ```
   npm start
   ```

## API Endpoints

| Method   | Endpoint                      | Description                     |
| -------- | ----------------------------- | ------------------------------- |
| `GET`    | `/api/expenses`               | Get all expenses                |
| `GET`    | `/api/expenses?category=food` | Filter expenses by category     |
| `GET`    | `/api/expenses/summary`       | Get category-wise spending totals |
| `GET`    | `/api/expenses/:id`           | Get a single expense            |
| `POST`   | `/api/expenses`               | Create a new expense            |
| `PUT`    | `/api/expenses/:id`           | Update an expense               |
| `DELETE` | `/api/expenses/:id`           | Delete an expense               |

## Request Body Example (POST / PUT)

```json
{
  "title": "Lunch",
  "amount": 150,
  "category": "food"
}
```

### Categories

`food` · `travel` · `shopping` · `bills` · `entertainment` · `other`

## Tech Stack

- **Node.js** — Runtime
- **Express.js** — Web framework
- **MongoDB Atlas** — Cloud database
- **Mongoose** — ODM for MongoDB
- **dotenv** — Environment variables
