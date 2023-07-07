# BlogAPI

About

A RESTful API adheres to the principles of the REST architectural style. REST (Representational State Transfer) is a standardized approach for facilitating communication between web-based computer systems. Within the REST architecture, clients initiate requests to retrieve or modify resources, and servers respond to these requests accordingly. The requests can involve data retrieval or modification on the server and typically include HTTP verbs, headers, source paths, and optional message bodies. The fundamental HTTP verbs employed in RESTful APIs are GET, POST, PUT, and DELETE.

Instructions

I have developed a straightforward blog post service that utilizes an H2 in-memory database to store the data. There are multiple ways to access and manipulate the data:

1) To view the data and execute queries, you can visit http://localhost:8080/h2-console/. Here, you will have the ability to interact with the data and examine the application.properties file for the JDBC URL.

2) Another option is to access the data through the endpoints: http://localhost:8080/posts or /posts/{id}. For testing purposes, I have hard-coded three sample posts, and you can retrieve them using these endpoints.

3) Currently, my preferred method is to run the application and open a terminal window. From there, you can enter the following command: curl -v localhost:8080/posts. This will allow you to retrieve the blog posts directly from the terminal.

These approaches provide different ways to view and manipulate the data in the blog post service.

Example CLI Commands:

View By Id	curl -v localhost:8080/posts/1
View All	curl -v localhost:8080/posts
Delete	curl -X DELETE localhost:8080/posts/4
Create	curl -X POST localhost:8080/posts -H 'Content-type:application/json' -d '{"title": "title 4", "content": "content 4", "author": "author 4"}'
Update	curl -X PUT localhost:8080/posts/4 -H 'Content-type:application/json' -d '{"title": "title 4", "content": "content 4", "author": "Emily"}'





