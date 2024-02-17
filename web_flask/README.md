#ALX Software Engineering Program

Write a script that starts a Flask web application:

    Your web application must be listening on 0.0.0.0, port 5000
    Routes:
        /: display “Hello HBNB!”
    You must use the option strict_slashes=False in your route definition

Before using Flask to display our HBNB data, you will need to update some part of our engine:

Update FileStorage: (models/engine/file_storage.py)

    Add a public method def close(self):: call reload() method for deserializing the JSON file to objects

Update DBStorage: (models/engine/db_storage.py)

    Add a public method def close(self):: call remove() method on the private session attribute (self.__session) tips or close() on the class Session tips

Update State: (models/state.py) - If it’s not already present

    If your storage engine is not DBStorage, add a public getter method cities to return the list of City objects from storage linked to the current State

