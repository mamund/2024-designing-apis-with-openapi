# Document Your OpenAPI Paths

Add path elements to your OpenAPI document

 * One or more URLs (/, /collection, /collection/{identifier}, etc.)
 * One or more methods per URL (GET, PUT, DELETE, etc.)
 * Add parameters, requestBody, and response as needed


_NOTE: Update your components section when appropriate_

## Examples
Below are some path examples.

### Root/Home 
```
  /:
    get:
      operationId: home
      summary: Use this to retrieve the home page for the onboarding API
      tags:
      - onboarding
      
      parameters:
        - $ref: "#/components/parameters/eTag"

      responses:
        '200':
          $ref: "#/components/responses/reply"
          
        default:
          $ref: "#/components/responses/error"
```

### Filtered List
```
  /wip:
    get:
      operationId: wipList
      summary: Use this to get a list of onboarding records
      tags:
      - onboarding
    
      parameters:
        - $ref: "#/components/parameters/status" <-- query param
        - $ref: "#/components/parameters/eTag"   <-- header
          
      responses:
        '200':
          $ref: "#/components/responses/reply"
          
        default:
          $ref: "#/components/responses/error"
```     

### Single Item with GET and PUT
```
  /wip/{identifier}/status:
    get:
      operationId: getStatus
      summary: Use this to get the status for this WIP recxord
      tags:
      - onboarding
    
      parameters:
        - $ref: "#/components/parameters/identifier"
        - $ref: "#/components/parameters/eTag"
            
      responses:
        '200':
              $ref: "#/components/responses/reply"
          
        default:
          $ref: "#/components/responses/error"

    put:
      operationId: updateStatus
      summary: Use this to update the status for this WIP record
      tags:
      - onboarding
    
      parameters:
        - $ref: "#/components/parameters/identifier"

      requestBody:
        $ref: "#/components/requestBodies/status"

      responses:    
        '200':
          $ref: "#/components/responses/reply"
          
        default:
          $ref: "#/components/responses/error"
```

