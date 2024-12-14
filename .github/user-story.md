**As a** developer of the account microservice 
**I need** REST API endpoints to read, update, delete, and list customer accounts 
**So that** microservices can manage customer data seamlessly on the e-commerce platform  
      
### Details and Assumptions
    * The database model and endpoint to create a customer account already exist.
    * The REST API is built using Python Flask.
    * The service should follow RESTful principles and return appropriate status codes.
    * The endpoints should handle potential errors (e.g., customer not found, invalid data).
    * The development will be done in an online lab environment.    

### Acceptance Criteria     
    gherkin 
    Given a customer account exists with a specific ID
    When a GET request is sent to /customers/{id}
    Then the customer details are returned with a 200 OK status

    Given a customer account exists with a specific ID
    When a PUT request is sent to /customers/{id} with valid updated data
    Then the account is updated, and a 200 OK status is returned with the updated account details

    Given a customer account exists with a specific ID
    When a DELETE request is sent to /customers/{id}
    Then the account is deleted, and a 204 No Content status is returned

    Given there are multiple customer accounts in the system
    When a GET request is sent to /customers
    Then a list of customer accounts is returned with a 200 OK status

    Given a customer account with a specific ID does not exist
    When a GET request is sent to /customers/{id}
    Then a 404 Not Found status is returned with an appropriate error message
