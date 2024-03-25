
# User Service

This is a C# project that uses Entity Framework Core and MySQL for data persistence. The project is containerized using Docker.

## Prerequisites

- .NET Core 3.1 or later
- Docker
- MySQL

## Installation and Setup

1. Clone the repository:

```bash
git clone https://github.com/ramonfounder/user-service.git
cd user-service
```

2. Build the Docker image:

```bash
docker-compose build
```

3. Run the Docker containers:

```bash
docker-compose up
```

The application will be available at `http://localhost:5000`.

## Database Migrations

To create a new migration, run:

```bash
dotnet ef migrations add <MigrationName>
```

To update the database with the latest migration, run:

```bash
dotnet ef database update
```

## API Endpoints

### Users API

- `GET /api/users`: Retrieves a list of all users.
- `GET /api/users/{id}`: Retrieves a specific user by their ID.
- `POST /api/users`: Creates a new user. The request body should include `firstName`, `lastName`, and `email`.
- `PUT /api/users/{id}`: Updates a specific user. The request body should include `firstName`, `lastName`, and `email`.
- `DELETE /api/users/{id}`: Deletes a specific user.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
