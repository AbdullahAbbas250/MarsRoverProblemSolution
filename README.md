There are five projects in which three are class library projects, one is a console application project and one is a Unit Test project. Let’s see each project mapping with onion architecture layers.

MarsRoverProblemSolution.Data
It is a class library project. It holds business related entities and enum related to the application. It represents the Domain Entities layer of the onion architecture. It’s a core and central part of the application.

2. MarsRoverProblemSolution.Repository

It is a second class library project. Generally this layer contains all the database related activities like CRUD operations, but in this application layer I have used command design pattern to execute rover movement according to the command passed from service layer which I will talk about in the next point.

3. MarsRoverProblemSolution.Service

It is a third class library project. It holds business logic and interfaces. These interfaces communicate between UI and data access logic. As it communicates via interfaces, it builds applications that are loosely coupled. This project represents the Service layer of the onion architecture.

4. MarsRoverProblemSolution

It is a .NET Core 3.1 Console Application. It is the most external part of an application by which the end-user can interact with the application. It represents the UI layer of the onion architecture.

5. MarsRoverProblemSolution.Tests

It is a .NET Core Test project which contains the unit tests for the application using xUnit framework.


