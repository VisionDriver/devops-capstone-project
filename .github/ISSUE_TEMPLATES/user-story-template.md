**As a** Developer
**I need** to implement REST APIs to read, update, delete, and list customer accounts
**So that** the customer account microservice has full CRUD capabilities
      
### Details and Assumptions
    * A Flask-based REST API with a create customer endpoint already exists
    * The database model for customers already exists
    * I will be working in an online development environment that needs configuring    
### Acceptance Criteria     
    gherkin 
    Given a valid customer ID
    When a GET request is made to the /customers/{id} endpoint
    Then the API returns the customer details associated with the given ID
    And the response status code is 200


    Given a valid customer ID and updated customer data
    When a PUT request is made to the /customers/{id} endpoint with the updated data
    Then the API updates the customer details associated with the given ID
    And the response status code is 200


    Given a valid customer ID
    When a DELETE request is made to the /customers/{id} endpoint
    Then the API deletes the customer account associated with the given ID
    And the response status code is 204


    Given there are existing customer accounts in the database
    When a GET request is made to the /customers endpoint
    Then the API returns a list of all customer accounts
    And the response status code is 200

    Given an invalid customer ID
    When a GET, PUT, or DELETE request is made to the /customers/{id} endpoint
    Then the API returns an error response indicating that the customer account does not exist
    And the response status code is 404
