# Learning FastAPI with Strawberry GraphQL, SQLModel and Postgres

Welcome to the **Learning FastAPI with Strawberry GraphQL** project! This project is designed to showcase a robust implementation of FastAPI integrated with Strawberry GraphQL, providing a seamless experience for building high-performance web applications with asynchronous capabilities.

## Project Overview
This project demonstrates the integration of FastAPI with Strawberry GraphQL to create a modern, scalable, and efficient web application. The application includes a sample GraphQL schema with queries and mutations, database management, and a simple FastAPI endpoint. The project also includes a PostgreSQL database for storing data and SQLModel for defining database models.

## Features
- **FastAPI**: A modern, fast (high-performance) web framework for building APIs with Python 3.7+ based on standard Python type hints.
- **Strawberry GraphQL**: A new GraphQL library for Python 3, inspired by dataclasses.
- **Asynchronous Database Operations**: Leveraging SQLAlchemy and async/await for high-performance database interactions.
- **Structured Project Layout**: A well-organized project structure with separate modules for models, schemas, and routes.
- **SQLModel**: A library for interacting with databases using Python type hints.
- **PostgreSQL Database**: A PostgreSQL database for storing data with SQLAlchemy as the ORM.

## Technologies Used
- **Python**: The core programming language used for development.
- **FastAPI**: The web framework used to create the API.
- **Strawberry GraphQL**: The GraphQL library used for defining and serving the GraphQL schema.
- **SQLAlchemy**: The ORM used for database interactions.
- **uvicorn**: The ASGI server used for running the FastAPI application.
- **PostgreSQL**: The relational database used for data storage.

## Getting Started

### Prerequisites
- Python 3.8+
- PostgreSQL
- pgAdmin4 (optional)

### Installation
1. Create and activate virtual environment
```bash
python -m venv venv
```
```bash
cd venv/Scripts
```
```bash
activate
```

2. Install dependencies
```bash
pip install -r requirements.txt
```
or 
```bash
pip install fastapi uvicorn sqlmodel sqlalchemy psycopg2 python-dotenv strawberry-graphql[fastapi]
```

3. Create a `.env` file in the root directory and add the following environment variables:
```bash
DATABASE_URL=postgresql://username:password@localhost/dbname
```
> The Database can be created using the pgadmin4 or any other database management tool.
> The `DATABASE_URL` should be in the format `postgresql://username:password@localhost/dbname`

## Running the Application
To run the FastAPI application, use the following command:
```bash
python main.py
```

The application will start running on `[http://localhost:8888](http://localhost:8888)

## Accessing the GraphQL Playground
To access the GraphQL Playground, navigate to `[http://localhost:8888/graphql](http://localhost:8888/graphql) in your browser.

## Sample Queries and Mutations
Here are some sample queries and mutations that you can try in the GraphQL Playground:

#### GET
1. Query to get all Notes
```graphql
query GetAllNotes{
  getAll{
    id
    name
  }
}
```

#### POST
2. Mutation to create a new Note:
mutation {
  createNote(noteData: { name: "Lets start coding today", descripiton: "Coding makes you enterpreneur" }) {
    id
    description
    content
  }
}

## PUT
3. Update a Note:
mutation {
  updateNote(noteId: 1, noteData: { name: "Lets start coding today", descripiton: "Coding makes you enterpreneur" }) {
    id
    description
    content
  }
}

## DELETE
4. Delete a Note:
mutation {
  deleteNote(noteId: 1) {
    id
    description
    content
  }
}

## Conclusion
This project provides a solid foundation for building web applications with FastAPI and Strawberry GraphQL. By leveraging the power of Python's type hints and asynchronous capabilities, developers can create high-performance APIs with ease. The integration of SQLModel and PostgreSQL further enhances the application's database interactions, making it a robust solution for modern web development.

## Contributing
Contributions are welcome! If you have any ideas, enhancements, or bug fixes, feel free to submit a pull request.

# License
This project is licensed under the MIT License. 

## About Me
I am a passionate Full Stack Developer with over 3 years of experience in web development. I specialize in creating robust and scalable web applications using modern technologies. My expertise includes FastAPI, GraphQL, PostgreSQL. I am dedicated to writing clean, maintainable code and following industry best practices.

**GitHub**: https://github.com/bilalmohib
**LinkedIn**: https://www.linkedin.com/in/bilalmohib

I am always eager to take on new challenges and collaborate with innovative teams. Let's build something amazing together!