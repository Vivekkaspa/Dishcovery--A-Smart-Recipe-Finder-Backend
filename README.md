# 🍽️ Dishcovery – A Smart Recipe Finder Backend  

**Dishcovery** is a Spring Boot-powered backend designed to help users search, manage, and discover recipes based on ingredients, difficulty level, and personal preferences. It provides secure authentication, efficient recipe retrieval, and seamless data management through a well-structured RESTful API.

## 🚀 Features  

- ✅ **Advanced Recipe Search** – Find recipes by name, difficulty level, and specific ingredients.  
- ✅ **Ingredient Management** – Add, update, and retrieve ingredient details (name, availability, quantity, measurement).  
- ✅ **User Authentication & Access Control** – Secure login system with role-based access (users can only modify their own recipes).  
- ✅ **CRUD Operations** – Create, update, delete, and fetch recipes and ingredients.  
- ✅ **Optimized Query Performance** – Efficient data retrieval, reducing query response time.  
- ✅ **Global CORS Policy** – Ensures smooth communication between frontend and backend.  

## 🛠️ Tech Stack  

- **Backend:** Spring Boot, Java  
- **Database:** PostgreSQL
- **Security:** Spring Security, JWT Authentication  
- **Deployment:** Docker, AWS  

## 🔧 Installation & Setup  

### 1️⃣ Clone the Repository  
```sh
git clone https://github.com/yourusername/Dishcovery.git
cd Dishcovery
```

### 2️⃣ Configure Database

Ensure PostgreSQL is installed and running. Then, create a database:
```sql
CREATE DATABASE dishcovery;
```

Edit ```application.properties``` to configure PostgreSQL:

```properties
# Database Configuration
spring.datasource.url=jdbc:postgresql://localhost:5432/dishcovery
spring.datasource.username=your_pg_username
spring.datasource.password=your_pg_password

# Hibernate Configuration
spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.format_sql=true
```

### 3️⃣ Run the Application

```sh
mvn spring-boot:run
```

### 📌 API Endpoints
#### 🔑 Authentication

| **Method** | **Endpoint**        | **Description**                        |
|------------|--------------------|----------------------------------------|
| `POST`     | `/auth/register`    | Register a new user                   |
| `POST`     | `/auth/login`       | Authenticate user & get JWT token     |

#### 📖 Recipe Management  
| **Method**  | **Endpoint**        | **Description**                       |
|------------|--------------------|----------------------------------------|
| `GET`      | `/recipes`          | Get all recipes                       |
| `GET`      | `/recipes/{id}`     | Get recipe by ID                      |
| `POST`     | `/recipes`          | Add a new recipe                      |
| `PUT`      | `/recipes/{id}`     | Update a recipe (owner only)          |
| `DELETE`   | `/recipes/{id}`     | Delete a recipe (owner only)          |

#### 🥦 Ingredient Management  
| **Method**  | **Endpoint**       | **Description**                       |
|------------|-------------------|----------------------------------------|
| `GET`      | `/ingredients`     | Get all ingredients                   |
| `POST`     | `/ingredients`     | Add a new ingredient                  |


### 🛡️ Security & Access Control

🔒 JWT Authentication – Secure token-based authentication for API access.
👤 Role-Based Access Control – Users can only modify their own recipes.
🌍 Global CORS Policies – Enables smooth frontend-backend communication.

---
### 🎯 Contribution Guidelines

Contributions are welcome! Follow these steps to contribute:

1. **Fork** the repository
2. **Create a feature branch**
```sh
git checkout -b feature-name
```
3. **Commit your changes**
```sh
git commit -m "Add new feature"
```
4.**Push to the branch**
```sh
git push origin feature-name
```
5.**Open a Pull Request**






