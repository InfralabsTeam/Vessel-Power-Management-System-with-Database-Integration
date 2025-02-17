# **Task 1: Vessel Power Management System with Database Integration**

## **Objective**

Develop a C# console application that allows users to manage vessel records and their power calculations, with data stored in a relational database (SQL Server).

## **Requirements**

### **1. Database Schema**

- Create a database named `VesselDB`.
- Create a table `Vessels` with the following fields:
  - `Id` (INT, Primary Key, Identity(1,1))
  - `Name` (NVARCHAR(100), NOT NULL)
  - `Type` (NVARCHAR(50), NOT NULL)
- Create a table `PowerCalculations` with the following fields:
  - `Id` (INT, Primary Key, Identity(1,1))
  - `VesselId` (INT, Foreign Key referencing `Vessels(Id)`, NOT NULL)
  - `EnginePower` (DECIMAL(10,2), NOT NULL)
  - `FuelConsumption` (DECIMAL(10,2), NOT NULL)
  - `Speed` (DECIMAL(10,2), NOT NULL)

### **2. Functional Requirements**

- **Add a new vessel**: Users should be able to input a vessel's name and type, which gets stored in the database.
- **Add power calculations to a vessel**: Users should select a vessel by ID and enter engine power, fuel consumption, and speed, which will be stored in the `PowerCalculations` table.
- **Display all vessels with average power efficiency**: The system should fetch all vessels and their corresponding power efficiency (efficiency = Speed / FuelConsumption) from the database.
- **Find a vessel by ID**: Users should be able to input a vessel ID and retrieve its details, including power calculations and efficiency.
- **Exit the program**: Allow the user to terminate the program gracefully.

### **3. Implementation Guidelines**

- Use **C# (.NET 8) Console Application**.
- Use **raw SQL queries** for database interactions.
- Implement **exception handling** for database connectivity and invalid inputs.
- Use **LINQ** for data manipulation (sorting, filtering, and averaging).
- Ensure **data validation** (e.g., preventing duplicate entries, validating input data).

### **4. Expected Features**

- **Menu-driven console application** with user prompts.
- **CRUD operations** on vessels and power calculations.
- **Data persistence** using a SQL Server database instead of in-memory storage.
- **Well-structured code** with object-oriented principles (e.g., separate data access layer).

### **5. Bonus Features (Optional)**

- Implement a **search feature** that allows filtering vessels by name or type.
- Allow **updating and deleting vessels and power calculations**.
- Implement **unit tests** for database operations.

### **6. Submission Requirements**

- **Source code** in a GitHub repository.
- **README.md** with setup instructions (including database creation scripts).
- Brief documentation on how to run the application.

---

### **Example User Flow**

```
1. Add new vessel
2. Add power calculations to vessel
3. Display all vessels
4. Find vessel by ID
5. Exit

Enter your choice: 1
Enter Vessel Name: Ocean Explorer
Enter Vessel Type: Cargo
Vessel added successfully!

Enter your choice: 2
Enter Vessel ID: 1
Enter Engine Power (kW): 5000
Enter Fuel Consumption (tons/hour): 10
Enter Speed (knots): 20
Power calculations added successfully!

Enter your choice: 3
ID: 1, Name: Ocean Explorer, Type: Cargo, Efficiency: 2.00 knots per ton of fuel

Enter your choice: 5
Exiting program...
```

