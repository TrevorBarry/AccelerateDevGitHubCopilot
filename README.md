Collecting workspace information# Library App

## Description

Library App is a console application designed to manage a library system. It allows users to manage patrons, loans, books, and authors using JSON files for data storage.

## Project Structure

```
Library App/
├── AccelerateDevGitHubCopilot.sln
├── README.md
├── src/
│   ├── Library.ApplicationCore/
│   │   ├── Entities/
│   │   ├── Enums/
│   │   ├── Interfaces/
│   │   ├── Services/
│   │   ├── Library.ApplicationCore.csproj
│   ├── Library.Console/
│   │   ├── appSettings.json
│   │   ├── CommonActions.cs
│   │   ├── ConsoleApp.cs
│   │   ├── ConsoleState.cs
│   │   ├── Json/
│   │   ├── Library.Console.csproj
│   │   ├── Program.cs
│   ├── Library.Infrastructure/
│   │   ├── Data/
│   │   ├── Library.Infrastructure.csproj
├── tests/
│   ├── UnitTests/
│   │   ├── ApplicationCore/
│   │   ├── UnitTests.csproj
```

## Key Classes and Interfaces

- **`src/Library.ApplicationCore/`**
  - `Entities/`
    - `Author`: Represents an author in the library.
    - `Book`: Represents a book in the library.
    - `BookItem`: Represents a physical copy of a book.
    - `Patron`: Represents a library patron.
    - `Loan`: Represents a loan of a book item to a patron.
  - `Interfaces/`
    - `IPatronRepository`: Interface for patron data access.
    - `ILoanRepository`: Interface for loan data access.
    - `IPatronService`: Interface for patron-related operations.
    - `ILoanService`: Interface for loan-related operations.
  - `Services/`
    - `PatronService`: Implements `IPatronService`.
    - `LoanService`: Implements `ILoanService`.

- **`src/Library.Console/`**
  - `ConsoleApp`: Main console application class.
  - `CommonActions`: Enum for common actions in the console app.
  - `ConsoleState`: Represents the state of the console application.

- **`src/Library.Infrastructure/`**
  - `Data/`
    - `JsonData`: Handles loading and saving data to JSON files.
    - `JsonPatronRepository`: Implements `IPatronRepository` using JSON data.
    - `JsonLoanRepository`: Implements `ILoanRepository` using JSON data.

## Usage

1. **Build the project:**
   ```sh
   dotnet build
   ```

2. **Run the console application:**
   ```sh
   dotnet run --project src/Library.Console/Library.Console.csproj
   ```

3. **Unit tests:**
   ```sh
   dotnet test
   ```

## License

This project is licensed under the MIT License. See the LICENSE file for details.

