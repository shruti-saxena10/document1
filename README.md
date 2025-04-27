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
| Item              | In Stock | Price |
| :---------------- | :------: | ----: |
| Python Hat        |   True   | 23.99 |
| SQL Hat           |   True   | 23.99 |
| Codecademy Tee    |  False   | 19.99 |
| Codecademy Hoodie |  False   | 42.99 |
          


## Installation

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

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
