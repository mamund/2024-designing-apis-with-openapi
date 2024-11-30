# Create Your OpenAPI Document

## Swagger Hub
We'll use the online Swagger Hub editor for this workshop. To do that, you need to have a Swagger Hub account.

### Create Your Swagger Hub Account
If you need a new account:

- Visit the swagger hub UI : https://app.swaggerhub.com/
- Click on "Log In"
- Select the "sign up" link
- Follow the prompts

### Log In to Swagger Hub Account
If you already have an account:

- Visit the swagger hub UI : https://app.swaggerhub.com/
- Click on "Log In"
- Follow the prompts

### Create a New API
After loggin in, do the following

- Visit the home page : https://app.swaggerhub.com/home
- select "Create API"
- Follow the prompts
  - Select OpenAPI 3.0
  - Select NONE for Template
  - Fill in name, version, title, description for the API (e.g. "simple-api")
  - Make sure Auto Mock API is turned ON



## Generated Code

openapi: 3.0.0

info:
  version: '1.0'
  title: Simple API
  description: a simple example
paths: {}
servers:
  # Added by API Auto Mocking Plugin
  - description: SwaggerHub API Auto Mocking
    url: https://virtserver.swaggerhub.com/amundsen/simple-api/1.0

## Edited Example
paths: {}
components: {}

openapi: 3.0.0

info:
  version: '1.0'
  title: Simple API
  description: a simple example

servers:
  # Added by API Auto Mocking Plugin
  - description: SwaggerHub API Auto Mocking
    url: https://virtserver.swaggerhub.com/amundsen/simple-api/1.0

paths: {}
components: {}

