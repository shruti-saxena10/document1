# document1

# 🛍️ Product Catalog Microservice

A Product Catalog Microservice for a retail company that will manage product
information and publish events when products are added or updated. The service can be deployed in a cloud-native environment.

## Features

- Create, update, and retrieve products via REST APIs
- Persist product data in PostgreSQL using JPA
- Publish events to GCP Pub/Sub when products are created or updated
- Optionally support RabbitMQ for event publishing
- Ready for cloud deployment (Docker + Cloud Run compatible)

## Tech Stack

- Java 21
- Spring Boot
- PostgreSQL
- Maven
- GitLab (for version control)
- Optional: RabbitMQ, PL/SQL, Docker
- GCP Pub/Sub (local emulator or mock library)(Can be added later on in production)

## Typical setup:
Local dev: Use RabbitMQ for event messaging.

Production: Connect to GCP Pub/Sub.

## API Endpoints
| Method | Endpoint | Description |
| :----- | :------: | ----------: |
| POST   | /products | Add a new product |
| PUT | /products/{id} | Update an existing product |
| GET | /products | List all products |
| GET | /products/{id} | Get product by ID |

          


## Product Entity
| Field | Type | Description |
| :---- | :--: | ---------: |
| productId | UUID | Unique product identifier |
| name | String | Product name |
| description | String | Product description |
| category | String | Product category |
| price | BigDecimal | Product price |
| availableStock | Integer | Available stock quantity |
| lastUpdated | Timestamp | Last updated timestamp |

## Event-Driven Design
1. On create/update:

## Cloud & Deployment
1. Dockerize the application and prepare for deployment on Cloud Run.


Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install foobar
```

## Usage

```python
import foobar

# returns 'words'
foobar.pluralize('word')

# returns 'geese'
foobar.pluralize('goose')

# returns 'phenomenon'
foobar.singularize('phenomena')
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.


## Setup instructions (local DB)
```
brew install postgresql
brew services start postgresql
# Switch to postgres user
sudo -i -u postgres
# Open PostgreSQL prompt
psql
# Create a new database
CREATE DATABASE your_database_name;
# Create a new user with a password
CREATE USER your_username WITH PASSWORD 'your_password';
# Grant privileges to the user
GRANT ALL PRIVILEGES ON DATABASE your_database_name TO your_username;
```
## For connecting a Spring Boot app to PostgreSQL
application.yml
```
spring:
  datasource:
    url: jdbc:postgresql://localhost:5432/database_name
    username: your_username
    password: your_password
    driver-class-name: org.postgresql.Driver

  jpa:
    hibernate:
      ddl-auto: update  # Or validate / create / create-drop based on your needs
    show-sql: true
    properties:
      hibernate:
        dialect: org.hibernate.dialect.PostgreSQLDialect
```

Also add PostgreSQL driver dependency in your pom.xml:

Pub/Sub setup (mock or emulator)
API usage examples (curl/Postman)
(Bonus) Dockerfile and sample docker-compose.yml
(Bonus) Unit tests (JUnit + Mockito)

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
