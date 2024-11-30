# Populate Your OpenAPI Components


Update your OpenAPI document component section with:
* At least one query parameter (e.g. ?id=)
* At least one schema item/collection pair of objects
* At least one response item (e.g. HomeResponse)
* At least one requestBodies item (e.g. addItem)


## Examples:
Below are OpenAPI Component section examples.

### parameters
```
parameters:
    nameParam:
      name: name
      in: query
      description: "Used to filter the list of persons"
      required: false
      schema:
        type: string
        example: "fred" 
```

### schemas
```
  schemas:
    PersonItem:
      type: object
      properties:
        id:
          type: string
          description: "Unique identifier for each record"
          example: "q1w2e3r4"
        name:
          type: string
          description: "Name of the person"
          example: "Morton Muffley"
        email:
          type: string
          description: "Default email for this person"
          example: "morton.muffley@example.org"
    PersonCollection:
      type: array
      items:
        $ref: '#/components/schemas/PersonItem'
```

### responses
```
    GenericError:
      description: "generic error occured"
      content:
        application/json:
          schema:
            $ref: "#/components/schemas/Error"
```

### requestBodies
```
    AddPerson:
      description: "body for a new Person record"
      required: true
      content:
        application/json:
          schema:
            $ref: "#/components/schemas/PersonItem"
        application/x-www-urlencoded:
          schema:
            $ref: "#/components/schemas/PersonItem"
```

