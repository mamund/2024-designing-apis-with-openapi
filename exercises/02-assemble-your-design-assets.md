# Assemble Your Design Assets

Create an API Story for your API

1. Purpose
2. Actions
3. Properties (Data)
4. Rules
5. Processing


_Items 1-3 are required, 4 & 5 are optional_

## Example
Here is anme example API Story asset:

### Assigning Sales Reps to New Clients API

#### Purpose
This API is a solution for accurately and quickly 
assigning sales representatives to new clients.

#### Actions
This API has the following actions:
 
 * ListSalesReps - List SalesReps accepting new clients.
 * ListClientsWithNoSalesReps - List clients without an active-status assignment.
 * AssignSalesRepToClient - Assign a SalesRep to a client.
 * RemoveSalesRepFromClient - Remove a SalesRep assignment from a client.

#### Data

 * Each assignment record has the following properties/data:
   * `assignmentId, salesRepId, clientId, status[active,removed] dateCreated, DateUpdated`
 * Each record in the SalesRepList has the following properties/data:
   * `salesRepId, salesRepName, dateCreated, dateUpdated`
 * Each record in the ClientList has the following properties/data:
   * `clientId, clientName, dateCreated, dateUpdated`
   
#### Rules
 * When assigning a SalesRep to a Client, an Assingment record is created.
 * You cannot assign two SalesReps to the same Client
 * The returned SalesRepList will only include SalesReps that are available for assignment
