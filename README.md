## MiniBank

The purpose of this project was to learn .NET and C# while gaining experience developing a small backend application. The project also includes work with: database transactions, ACID principles, and thread safety using locks and handling race conditions

## Running the program
To run the program you need 
 - .NET SDK
 - Docker
 - Entity Framework Core CLI

1. Start the SQL Server Docker container (Replace <password> with your own SQL Server password):
```bash
docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=<password>" -p 1433:1433 -d mcr.microsoft.com/mssql/server:2022-latest
```

2. Configure the connection string (or the SQL_PASSWORD environment variable if required):
```bash
export SQL_PASSWORD=<password>
```

3. Apply the database migrations:
```bash
dotnet ef database update
```

4. Run the application:
```bash
dotnet run
```

## Features

- Create bank accounts
- Deposit and withdraw money
- Transfer money between accounts
- Store data in SQL Server




