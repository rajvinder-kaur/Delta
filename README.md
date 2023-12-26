 # Delta API

This is a simple Express.js API that connects to a MongoDB database.

## Prerequisites

- Node.js and npm installed
- MongoDB installed and running

## Installation

Clone the repository:

```
git clone https://github.com/delta/api.git
```

Install the dependencies:

```
npm install
```

## Configuration

Edit the `connectionString` variable in the `main` function to point to your MongoDB database.

## Running the API

Start the API by running the following command:

```
npm start
```

The API will listen on port 3001.

## API Routes

The API has two routes:

- `/`: Returns a simple message indicating that the API is running.
- `/api/todos`: Returns a list of all todos in the database.

## Code Explanation

### Connecting to the Database

The `main` function connects to the MongoDB database using the `mongoose` library.

```javascript
async function main(){
    await mongoose.connect(connectionString);
}
```

The `connectionString` variable is defined at the top of the file.

```javascript
const connectionString = `mongodb://127.0.0.1:27017/delta`;
```

### API Routes

The API has two routes:

- `/`: Returns a simple message indicating that the API is running.
- `/api/todos`: Returns a list of all todos in the database.

The `/` route is defined as follows:

```javascript
app.get("/",(req,res)=>{
res.send("started")
})
```

The `/api/todos` route is defined as follows:

```javascript
app.get("/api/todos",(req,res)=>{
res.send("started")
})
```

## Conclusion

This is a simple Express.js API that connects to a MongoDB database. It can be used as a starting point for building more complex APIs.

