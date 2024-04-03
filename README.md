                               ** USER STORIES**

User stories typically describe a specific feature or functionality
from the perspective of an end-user. 
In Python, you can represent user stories using comments, docstrings, or even
custom classes/functions. 
Below is an example of how you can represent user stories in Python using comments:

# User Story 1: As a user, I want to be able to add two numbers together.

def add_numbers(num1, num2):
    """
    Function to add two numbers together.
    
    Args:
        num1 (int): The first number.
        num2 (int): The second number.
        
    Returns:
        int: The sum of num1 and num2.
    """
    return num1 + num2

# User Story 2: As a user, I want to be able to find the maximum number in a list.

def find_max(numbers):
    """
    Function to find the maximum number in a list.
    
    Args:
        numbers (list): A list of numbers.
        
    Returns:
        int: The maximum number in the list.
    """
    return max(numbers)

# User Story 3: As a user, I want to be able to calculate the square of a number.

def square_number(number):
    """
    Function to calculate the square of a number.
    
    Args:
        number (int): The number to be squared.
        
    Returns:
        int: The square of the number.
    """
    return number ** 2
In this example, each user story is represented by a comment that describes the
feature or functionality that needs to be implemented. 
Beneath each comment, there is a corresponding function that implements the described 
feature, along with docstrings that provide additional information about the function's 
purpose, arguments, and return value.

                                          **USE CASES**

In Python, a "use case" typically refers to a specific scenario or situation in which a
program or system is intended to be used. Use cases help in understanding the 
functionality and requirements of a system from an end-user perspective. 

Let's say we're building a simple library management system, and one of the use cases 
is to allow a librarian to add a new book to the library catalog.

class Library:
    def __init__(self):
        self.catalog = {}

    def add_book(self, book_id, title, author):
        if book_id not in self.catalog:
            self.catalog[book_id] = {'title': title, 'author': author}
            print(f"Book '{title}' by {author} added to catalog with ID: {book_id}")
        else:
            print(f"Book with ID {book_id} already exists in the catalog.")

# Example use case
if __name__ == "__main__":
    library = Library()
    
    # Librarian adds a new book
    library.add_book(101, "Harry Potter and the Philosopher's Stone", "J.K. Rowling")
    library.add_book(102, "To Kill a Mockingbird", "Harper Lee")
    library.add_book(101, "Harry Potter and the Philosopher's Stone", "J.K. Rowling")  


    # Output:
    # Book 'Harry Potter and the Philosopher's Stone' by J.K. Rowling added to catalog with ID: 101
    # Book 'To Kill a Mockingbird' by Harper Lee added to catalog with ID: 102
    # Book with ID 101 already exists in the catalog.

We define a Library class with an add_book method to add a new book to the
library catalog.
We create an instance of the Library class.
We demonstrate the use case by adding two books to the catalog and attempting to add one
of them again (which should fail because it already exists).
This is a basic example, but in a real-world scenario, use cases can involve more
complex interactions between different parts of the system, as well as interactions
with external systems or users.

                                      ** PROJECT REQUIREMENT**

class ProjectRequirements:
    def __init__(self, name, description, tasks):
        self.name = name
        self.description = description
        self.tasks = tasks
    
    def add_task(self, task):
        self.tasks.append(task)
    
    def remove_task(self, task):
        if task in self.tasks:
            self.tasks.remove(task)
    
    def display_requirements(self):
        print(f"Project: {self.name}")
        print(f"Description: {self.description}")
        print("Tasks:")
        for i, task in enumerate(self.tasks, start=1):
            print(f"{i}. {task}")

# Example usage
if __name__ == "__main__":
    # Create project requirements
    project_name = "Sample Project"
    project_description = "This is a sample project to demonstrate project requirements
in Python."
    tasks = ["Task 1: Implement feature A",
             "Task 2: Write unit tests for feature A",
             "Task 3: Review code for feature A"]
    project_requirements = ProjectRequirements(project_name, project_description, tasks)
    
    # Display project requirements
    project_requirements.display_requirements()
    
    # Add a new task
    new_task = "Task 4: Document feature A"
    project_requirements.add_task(new_task)
    
    # Display updated project requirements
    print("\nUpdated Project Requirements:")
    project_requirements.display_requirements()
    
    # Remove a task
    removed_task = "Task 2: Write unit tests for feature A"
    project_requirements.remove_task(removed_task)
    
    # Display final project requirements
    print("\nFinal Project Requirements:")
    project_requirements.display_requirements()
This code defines a ProjectRequirements class that represents the requirements for 
a project. It has attributes for the project name, description, and a list of tasks.
You can add and remove tasks as needed, and display the project requirements along 
with any updates made.
