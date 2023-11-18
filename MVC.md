## MVC - Design Pattern
    - Model: Logic & Data
      - Sends data to the Controller    
    - View: User Interface 
      - View send the input events to the Controller    
    - Controller: Mediator
      - Makes the request to the Model
      - Modifies the View    
    - View and Model will never talk to each other
    - View and Model will always use Controller to communicate with either one
