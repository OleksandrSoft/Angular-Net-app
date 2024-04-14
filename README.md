# Angular + ASP.Net (Car Rent App)

![alt text](https://i.hizliresim.com/7TfAdR.png)


Welcome to the Car Rent App developed with Angular and ASP.Net. <br> <br>
This project has been developed based on Multi-Layered Architecture. 
SOLID software principles have been adopted in the project. 
Front-End part is coded with Angular, Back-End part is coded with C#. 
MSSQL Local Database is used for the database. 
<br>

<h2>
Database
</h2>
MSSQL Localdb was used for database in the project. 
To create the database, click "View > SQL Server Object Explorer" on Visual Studio 2019, a new panel will open on the left. 
From this panel, follow the path of "SQL Server > (localdb)\MSSQLLocalDB", right click on the "Databases" folder in the folders opened below, 
select "Add New Database" and create your database. (I have chosen "RentACarSystem" as database name) <br>
<br>


<h2>
Back-End
</h2>
C# was used in the back-end part of the project. Development was made on the basis of multi-layered architecture. I want to give information about what layers do; <br>
<b>1-Entities Layer:</b> It is where the classes of objects to be used throughout the program are defined. 
Each of the classes in this layer corresponds to a table in the database, in addition to these, it also contains DTO (Data Transfer Object) classes in which data from different tables are joined. <br>
<b>2-Data Access Layer:</b> It is the layer on which database connections and operations are made. Required configuration for database connection is done here. 
Also, operations such as data extraction, addition, deletion, and updating are encoded in this layer. <br>
<b>3-Business Layer:</b> It is the layer where business rules are defined and controlled. When a command comes to the program, 
what actions it should perform and which set of rules it should pass through are defined here. Cross-Cutting Concerns are triggered in this layer. <br>
<b>4-Core Layer:</b> It is the part where structures, cross-cutting concerns, aspects, extensions and tools to be used in common in all layers are coded. <br>
<b>5-Presentation Layer:</b> It is the layer that appears to the user, that the user interacts with and sends commands to the program. <br>
<b>6-Service Layer (Web API):</b> It is the part where the services that enable the Front-End part and other platforms to communicate with the program and perform operations are written. <br>


<h3>
Requirements for Back-End
</h3>

| Package Name  | Version |
| ------------- | ------------- |
| Autofac | 6.1.0  |
| Autofac.Extensions.DependencyInjection  | 7.1.0  |
| Autofac.Extras.DynamicProxy  | 6.0.0  |
| FluentValidation  | 9.5.1  |
| Microsoft.AspNetCore.Authentication.JwtBearer  | 3.1.12  |
| Microsoft.AspNetCore.Http  | 2.2.2 |
| Microsoft.AspNetCore.Http.Abstractions  | 2.2.0  |
| Microsoft.EntityFrameworkCore.SqlServer  | 3.1.12  |
| Microsoft.Extensions.Configuration  | 5.0.0  |
| Microsoft.IdentityModel.Tokens  | 6.8.0  |
| NETStandard.Library  | 2.0.3  |
| Newtonsoft.Json  | 12.0.3  |
| System.IdentityModel.Tokens.Jwt | 6.8.0 |

<br>
<h2>
Front-End
</h2>
Angular 11 was used in the front-end part of the project. Throughout the development, Visual Studio Code has been worked on as IDE. Bootstrap has been integrated to achieve a responsive design.
Also used Font-Awesome. BrowserModule, HttpClientModule, AppRoutingModule, FormsModule, ReactiveFormsModule, BrowserAnimationsModule and ToastrModule were used as modules in Angular. 
On the Front-End side, more attention was paid to whether the process is working correctly rather than the design. <br>
<br>

```
WARNING! For Front-End side to work, you need to set WebAPI as "Set as Startup Project" on Back-End side 
and start it with IIS Express. Then you have to follow the steps below.
```
1- First, you need to install the Node modules used in the project. <br>
```
npm install
```
2- Finally, we will open a new terminal and run the project on localhost. <br>
```
ng serve --open
```
