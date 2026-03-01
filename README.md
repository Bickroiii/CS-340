# CS-340
Ricky Suarez 
Grazioso Salvare Rescue Dog Dashboard 
Description 
The Grazioso Salvare Rescue Dog Dashboard is a full stack client server application 
designed to help an international rescue animal training company identify dogs suitable for 
specialized search and rescue training. The application connects to a MongoDB database 
containing Austin Animal Center outcomes data and provides an interactive dashboard 
that allows users to filter, visualize, and explore potential rescue dog candidates. 
The dashboard applies database concepts, client side interaction, and the MVC design 
pattern to provide a user friendly decision support system. Users can filter animals by 
rescue specialization and dynamically view updates through a data table, geolocation map, 
and outcome frequency chart. 

Features 
• MongoDB database integration using a custom Python CRUD module 
• Interactive dashboard built with Dash and JupyterDash 
• Radio button filtering for rescue categories 
• Dynamic data table with sorting, filtering, and pagination 
• Geolocation map visualization using Leaflet 
• Outcome type frequency chart for data insights 
• Reset functionality to restore unfiltered dataset 
• MVC architecture separating model, view, and controller logic 
Rescue Filter Categories 
The dashboard supports filtering dogs suitable for the following rescue types: 
• Water Rescue 
• Wilderness Rescue 
• Disaster or Individual Tracking 
• Reset to view all animals 
Each filter dynamically updates the table, map, and chart widgets. 
Installation 
Requirements 
• Python 3.x 
• MongoDB running locally 
• Jupyter Lab environment 
• Required Python libraries: 
pip install pandas numpy matplotlib plotly dash jupyter-dash dash-leaflet pymongo 
Usage 
Step 1 
Import the Austin Animal Center dataset into MongoDB and create the animals collection. 
Step 2 
Run the CRUD Python module to verify database connectivity. 
Step 3 
Launch the dashboard notebook: 
Run all cells in ProjectTwoDashboard.ipynb 
Step 4 
Interact with the dashboard using radio filters to explore rescue candidate dogs. 
Screenshots 
Include the following screenshots in the repository: 
• Initial dashboard state with all widgets visible 
• Water rescue filter applied 
• Wilderness rescue filter applied 
• Disaster or tracking filter applied 
• Reset filter returning to original dataset 
MVC Architecture 
Model 
MongoDB database storing Austin Animal Center outcomes data 
View 
Dashboard widgets including data table, map, and chart 
Controller 
Python CRUD module and Dash callbacks handling filtering and visualization logic 
Tools and Technologies 
• Python 
• MongoDB 
• PyMongo 
• Pandas 
• Plotly 
• Dash and JupyterDash 
• Dash Leaflet 
• Jupyter Lab 
Contributing 
This project was created as part of an academic software engineering assignment. 
Contributions are not required, but suggestions for improvements are welcome. 
Author 
Ricky Suarez 
SNHU Computer Science Program 
Project Status 
Completed as part of the Grazioso Salvare dashboard development project for SNHU CS 
340. 
License 
This project is intended for educational use. 


All Queries display a bar graph and map 




Reflection
How do you write programs that are maintainable, readable, and adaptable?

Writing maintainable and readable programs starts with structure and separation of responsibility. In this project, the most important design decision was separating the database logic into a standalone CRUD Python module in Project One. Instead of embedding database queries directly inside the dashboard code, I created reusable methods that handled create, read, update, and delete operations independently from the user interface. This separation made the code significantly easier to manage, test, and modify.

By organizing the project using an MVC style pattern, the model remained in MongoDB, the controller logic handled filtering and queries through the CRUD module, and the view was responsible only for presentation through Dash widgets. This approach improved adaptability because if the database schema changes, I only need to update the CRUD module rather than rewrite the dashboard. It also improved readability because each component has a clear purpose.

The advantage of building the CRUD module first was reusability. The same module could be reused for other dashboards, APIs, reporting tools, or administrative systems that need access to the animal database. In the future, this module could be expanded into a REST API service, integrated into a mobile application, or connected to a machine learning pipeline for predictive rescue candidate identification. Designing with modularity in mind makes software scalable and flexible over time.

How do you approach a problem as a computer scientist?

I approach problems by breaking them into layers and identifying system components before writing code. For this project, I first analyzed the client requirements from Grazioso Salvare and identified key elements: database design, filtering logic, visualization requirements, and user interaction. Instead of jumping directly into dashboard development, I ensured the database was structured correctly and that efficient queries could retrieve the correct subsets of dogs for each rescue category.

This approach differed from earlier assignments in other courses where the focus was often on solving isolated problems or writing standalone programs. Here, the project required systems thinking. I had to consider database indexing, query performance, user experience design, and interaction between multiple components simultaneously.

In the future, I would continue using strategies such as:
• Defining requirements clearly before implementation
• Designing schemas that reflect real world constraints
• Using indexing to optimize performance
• Building modular components that can be reused
• Testing small pieces incrementally before integrating them

Approaching database projects from a systems perspective ensures that the final solution is not only functional but also efficient and scalable.

What do computer scientists do, and why does it matter?

Computer scientists design systems that transform data into meaningful and actionable information. In this project, the raw animal shelter dataset by itself is just structured data. By building a database interface and an interactive dashboard, that data becomes a decision support tool.

For a company like Grazioso Salvare, this system allows them to quickly identify dogs that meet very specific rescue training criteria. Instead of manually sorting through records, the dashboard automatically filters candidates and visualizes relevant characteristics. This saves time, reduces human error, and supports more informed decision making.

Computer scientists create tools that improve efficiency, accuracy, and insight. In real world applications, systems like this can directly impact organizational effectiveness. For rescue organizations, that can ultimately affect lives by accelerating the identification and training of rescue dogs.

This project demonstrates how software engineering principles, database systems, and user centered design combine to produce practical solutions that help organizations operate more effectively.
