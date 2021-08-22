---
layout: project
title: savetimewithus
subtitle: A todo list with a twist
---

Savetimewithus is a simple todo list application. however the completion has to be signed off with a picture of the completed task. Users can also see the memories of the tasks they completed in a scrapbook type UI. 

This project was built in a hackathon by me and my teammates ([Vijay](https://www.linkedin.com/in/vijay-jaisankar/) and [Prasanna](https://www.linkedin.com/in/prasannavenkatesh-ramkumar-6b91241a0/)), where we were declared as one of the winners!

#### Inspiration

Our inspiration came from the single fact that by seeing their previous completed tasks, people get a rush of seratonin which in turn aids them in completing new tasks. Hence we added the picture component to the to do list. Also, a simple plain todo-list more often than not is unable to make people interested in doing their work. People may just strike off their work as done even if they haven't actually done it. We take care of this loophole in traditional task management by using the picture component, that is, people have to actually upload a picture of the completed task to strike it off.

#### What it does

Savetime is a to do list application where user can add a bunch of tasks to be completed. The tasks are marked as completed when the user adds a picture of the completed task. The users can also see the tasks they completed on a specific day in a scrapbook UI which is integrated with the site. There is also a discord bot through which users can state their tasks for the day and can also see what tasks others are doing on that particular day providing inspiration to complete their tasks on time.

#### How we built it

We built the project using django and django-rest-framework for the backend. The frontend is primarily HTML,CSS and JS. The discord bot was built using the discord.py package. For local development environment we used DataStax Astra’s Cassandra service as the database. We went with postgreSQL as database for deployment since we deployed on heroku.

#### What we learned

We learnt a lot about django-rest-framework and how django handles media files. We also learnt about DataStax Astra’s Cassandra-made-easy service.


#### Implementation:

[GitHub Repository](https://github.com/shrey27tri01/savetimewithus)   
[Live Demo](https://savetimewithus.herokuapp.com/)




