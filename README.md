# Employee Management Backend

## Overview
A Spring Boot application providing a RESTful API for managing employees with CRUD operations.

## Technologies
- **Java 11+**
- **Spring Boot**
- **Maven**
- **MySQL**

## Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/employee-management-backend.git
   ```

2. **Navigate to the Project Directory:**
   ```bash
   cd employee-management-backend
   ```

3. **Install Dependencies:**
   ```bash
   mvn install
   ```

4. **Configure Database Connection:**
   Create a `.env` file with:
   ```dotenv
   SPRING_DATASOURCE_URL=jdbc:mysql://localhost:3306/your_database
   SPRING_DATASOURCE_USERNAME=your_username
   SPRING_DATASOURCE_PASSWORD=your_password
   ```

5. **Configure Application Settings:**
   Update `src/main/resources/application.properties`:
   ```properties
   spring.application.name=spring-boot-crud-api

   # MySQL Configuration
   spring.datasource.url=${SPRING_DATASOURCE_URL}
   spring.datasource.username=${SPRING_DATASOURCE_USERNAME}
   spring.datasource.password=${SPRING_DATASOURCE_PASSWORD}

   # JPA/Hibernate Configuration
   spring.jpa.show-sql=true
   spring.jpa.hibernate.ddl-auto=update
   spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
   ```

6. **Run the Application:**
   ```bash
   mvn spring-boot:run
   ```

## API Endpoints

- **Get All Employees:** `GET /employee/all`
- **Get Employee by ID:** `GET /employee/find/{id}`
- **Add New Employee:** `POST /employee/add`
- **Update Employee:** `PUT /employee/update`
- **Delete Employee:** `DELETE /employee/delete/{id}`

## Model: Employee
- `id` (Long)
- `name` (String)
- `email` (String)
- `jobTitle` (String)
- `phone` (String)
- `imageUrl` (String)
- `employeeCode` (String)

## Running Tests
```bash
mvn test
```

## License
MIT License
