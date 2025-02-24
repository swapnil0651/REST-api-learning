Here’s a `README.md` file for your repository:

```markdown
# REST API Learning - Flask Drinks API

This repository contains a Flask-based REST API to manage a collection of drinks. The API demonstrates basic CRUD operations (Create, Read, Update, Delete) with an SQLite database using SQLAlchemy as the ORM (Object Relational Mapper).

## Features

- **Retrieve all drinks**: GET `/drinks` – Returns a list of all available drinks.
- **Retrieve a specific drink**: GET `/drinks/<id>` – Returns a specific drink based on its ID.
- **Add a new drink**: POST `/drinks` – Adds a new drink to the collection.
- **Delete a drink**: DELETE `/drinks/<id>` – Removes a drink by its ID from the collection.

## Getting Started

### Prerequisites

- Python 3.x
- Flask
- SQLAlchemy

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/swapnil0651/REST-api-learning.git
   cd REST-api-learning
   ```

2. Set up a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Create the SQLite database:

   ```bash
   python
   >>> from application import db
   >>> db.create_all()
   >>> exit()
   ```

### Running the Application

To run the Flask app locally:

```bash
flask run
```

You should see output similar to:

```
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

### API Endpoints

#### Get All Drinks

```http
GET /drinks
```

Response:

```json
{
  "drinks": [
    {
      "name": "Coke",
      "description": "A refreshing soda"
    },
    {
      "name": "Pepsi",
      "description": "Another soda brand"
    }
  ]
}
```

#### Get a Specific Drink

```http
GET /drinks/<id>
```

Response:

```json
{
  "name": "Coke",
  "description": "A refreshing soda"
}
```

#### Add a New Drink

```http
POST /drinks
```

Request Body:

```json
{
  "name": "Sprite",
  "description": "A lemon-lime soda"
}
```

Response:

```json
{
  "id": 3
}
```

#### Delete a Drink

```http
DELETE /drinks/<id>
```

Response:

```json
{
  "message": "yeeted"
}
```

### Project Structure

```
REST-api-learning/
├── API/
│   ├── __pycache__/         # Python bytecode cache
│   ├── instance/            # Flask instance folder (includes SQLite database)
│   ├── application.py       # Main application file
│   └── requirements.txt     # Python dependencies
├── venv/                    # Virtual environment files
└── README.md                # Project documentation
```

### Technologies Used

- Python
- Flask
- SQLAlchemy
- SQLite

