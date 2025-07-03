# Library App

## Description
Library App is a .NET-based console application for managing a library's books, patrons, and loans. It demonstrates clean architecture principles, separating core logic, infrastructure, and user interface layers. Data is stored in JSON files for easy portability and testing.

## Project Structure
- AccelerateDevGitHubCopilot.sln
- src/
  - Library.ApplicationCore/
    - Entities/
    - Enums/
    - Interfaces/
    - Services/
    - Library.ApplicationCore.csproj
  - Library.Console/
    - ConsoleApp.cs
    - ConsoleState.cs
    - CommonActions.cs
    - Json/
    - appSettings.json
    - Library.Console.csproj
  - Library.Infrastructure/
    - Data/
      - JsonData.cs
      - JsonLoanRepository.cs
      - JsonPatronRepository.cs
    - Library.Infrastructure.csproj
- tests/
  - UnitTests/
    - ApplicationCore/
    - LoanFactory.cs
    - PatronFactory.cs
    - UnitTests.csproj

## Key Classes and Interfaces
- **ConsoleApp**: Main controller for the console UI, manages user interaction and state transitions.
- **JsonData**: Handles loading, saving, and populating data from JSON files.
- **ILoanService, IPatronService**: Service interfaces for business logic related to loans and patrons.
- **ILoanRepository, IPatronRepository**: Repository interfaces for data access.
- **Entities**: Domain models such as `Patron`, `Book`, `Loan`, `Author`, etc.

## Usage
1. Ensure you have .NET 8.0 SDK installed.
2. Build the solution:
   ```sh
   dotnet build AccelerateDevGitHubCopilot.sln
   ```
3. Run the console application:
   ```sh
   dotnet run --project src/Library.Console/Library.Console.csproj
   ```
4. Follow the on-screen prompts to search for patrons, view loans, and manage library operations.

## License
This project is licensed under the MIT License.
