# todolistrazor
To-do-List app with Razor Pages

## About the App
The Todolist App will be a simple webapp that allows individual users add, edit, or delete tasks. They can also add their own categories. The tasks can have a category, date and time, and can be checked off.

## Entities
The entities I will be using for the webapp are the following:
- Account: represents the users
  - AccountId / int primary key identity
  - DisplayName / string(1-50) : Display name
  - UserName / string (1-100) : for login
  - Password / string (1 - 200) : for login
  - AccountPhoto ***
- Category:
  - CategoryId / int primary key identity : there will default categories but they can add their own
  - CategoryName / string(1-50)
  - Description / string(1-500)
  - CategoryIcon ***
- Task
  - TaskId / int primary key identity
  - CategoryId / int foreign key to Category
  - Description / string(1-500)
  - DateTime / datetime (>= currentdatetime)