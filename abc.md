# Introduction to Web Development Using Python 
# Introduction 
 Importance of Web Development The backbone of our online experience is based on web creation Web sites, web applications help businesses run smoothly, ease education processes, facilitate communication and enhance entertainment. On these grounds, we use them to share information, carry out electronic transactions and other related tasks; thus, they should be part of every organization’s endeavors. In addition, when people are seeking friends or life partners, they build new relationships through the social services they subscribe into. For these reasons, more of us will need good professionals who can make relevant pages with different engines or networks despite a growing addiction to information technology that human beings all over the world seem to experience.
# Overview of the Tutorial
The tutorial will introduce the most basic concepts of developing tools and technologies for the Web using Python. 
This includes the following:
- Base concepts of web development.
- Differentiating between front-end development and back-end development.
- The role of Python in web development.
- How to set up a development environment
- Creating a simple web application
- Understanding HTTP and URLs
- Handling requests and responses
- Templating and rendering dynamic content.
- Database and its working
- Deploying and hosting your web application
- References for additional topics
# What is Web Development?
## Definition and Role
Web development is the process of creating and maintaining websites and web applications. It involves independent works on -
 **Frontend Development:** User interface creation with HTML, CSS, and JavaScript.
 **Backend Development:** Management of the server, application, and database.
 **Full-Stack Development:** Both frontend and backend development tasks are handled.
The functionality, usability, and efficiency of websites are ensured through web development, which has become quite important for the visibility and functioning of any business.
# Client-Server Architecture
Web development adopts a client server architecture.
## Client
Its the web browser-like Chrome, Firefox-that:
- **Renders Content:** Shows HTML, CSS, and JavaScript.
- **Manages Interaction:** Collects the user inputs and submits to the server.
- **Local Storage:** Saves data locally for performance and offline use.
## Server
A powerful computer does;
- **Storage of data:** It does the handling of databases.
- **Business logic:** Does the server-side code.
- **Security:** Ensures the security of data and applications.
## Client-Server Interaction
HTTP protocol is used for:
1. **Request:** HTTP request made by the client.
2. **Processing:** Server processes the request.
3. **Response:** HTTP response made by the server.
4. **Rendering:** Content is rendered to the client.
This design is to enable webs in and around the network so that servers do the work, which is resource-intensive, with the client giving a user-friendly look.
# Frontend vs. Backend Development
## Frontend Development
It deals with the user interface and user experience of a website—directly connected to the user. This involves creating visual and interactive features that users will view and interact with in their web browser.
- **Technologies:** HTML, CSS, JavaScript
- **Tools:** Some of these are frameworks like React, Angular, and Vue.js.
- **Responsibilities:** Designing layout, implementing responsive design, handling user interactions
## Backend development
Backend development concerns the server side of a web application. It deals with the management of the server and database with application logic responsible for powering the frontend.
- **Technologies:** Python, Ruby, Java, Node.js
- **Frameworks:** Django, Flask, Express.js
- **Roles and Responsibilities:** Handling data storage/retrieval, user authentication, business logic, and server configuration.
## Full-Stack Development
Full-stack development involves the combination of frontend and backend development; a developer has the skills to handle the architecture of a web application at all levels. Thus, full-stack developers can handle everything from designing user interfaces to constructing server-side logic and databases.
![Add a subheading](https://github.com/anuja19103/Articles/assets/125860363/53999c56-c1fd-4304-b753-37ea0e1053d8)
# Introduction of Python for Web Development
## Reasons to Use Python
Python is well-suited for web development because of its:
- **Readability:** The language has very easy-to-understand syntax.
- **Productivity:** Fast coding with fewer lines.
- **Libraries:** Tremendous libraries available for a variety of functionalities.
- **Community:** Large community, support, and resources are widely available. 
- **Versatility:** Used in Web Development, Data Science, etc.
## Some Popular Python Web Frameworks
**Django** — Full-stack framework. This is an ideal framework with an inbuilt admin interface, ORM, and robust security features for very complex data-driven applications. 
**Flask** — A lightweight microframework. This framework lays great emphasis on simplicity and flexibility, hence very well suited for small to medium applications and even prototyping. 
**Pyramid** — General-purpose framework. Highly flexible and scalable. It has a lot of configuration options and hence is suitable for any size of projects.
# Setting Up Your Development Environment
## Installing Python and a Web Framework
You start web development with Python by installing the Python programming language, choosing a web framework that you prefer, and setting up a virtual environment.
## Step 1: Install Python
**Download Python:**
 Go to [python.org](https://www.python.org/).
 Select the installer for your OS.
**Install Python**
 Run the installer and make sure to check "Add Python to PATH".
 Roll on through the prompts.
## Step 2: Installing Django
**Open Terminal/Command Line:**
 `pip install django`
![The Command to install django](https://github.com/anuja19103/Articles/assets/125860363/7dabe068-5567-4f4f-8934-0e9068f5cd33)
## Virtual Environments
Virtual environments are a way to manage dependencies and to keep things neat and connected to our projects.
## Creating and Activating a Virtual Environment
**Create Environment:**
**macOS/Linux:** `source myenv/bin/activate`
![Screenshot 2024-06-09 233009](https://github.com/anuja19103/Articles/assets/125860363/18b7e2c6-ea41-4fad-b5ee-2eeb6fa60c62)
## Environment check
**Python Version Check:**
   ```bash
   python --version
   ```
**Packages list:**
   ```bash
   pip list
   ```
   ![Screenshot 2024-06-09 233025](https://github.com/anuja19103/Articles/assets/125860363/abc1a403-1072-486c-b84d-9e756f984dd0)
## Example workflow
1. **Change into Project Directory:**
   ```bash
   cd path/to/your/project
   ```
2. **Create and Activate Virtual Environment:**
   ```bash
   python -m venv myenv
   source myenv/bin/activate  # On Windows: myenv\\\\Scripts\\\\activate
   ```
3. **Install Django:**
   ```bash
   pip install django
   ```
4. **Start a Django Project:**
   ```bash
   django-admin startproject my_project
   ```
5. **Run the Server:**
   ```bash
   cd my_project
   python manage.py runserver
   ```
This setup provides you with an isolated functional environment to get started building your web application.
![Starting Server](https://github.com/anuja19103/Articles/assets/125860363/aad005c7-bb60-42a7-8e22-1b4d6891fd31)
## Creating Your First Web Application
Creating your very first web application with Django requires several steps:
1. Start a New Project
Open your terminal and run:
```bash
django-admin startproject myproject
cd myproject
```
This will now create a directory structure as follows:
```
myproject/
├── manage.py
└── myproject/
├── __init__.py
       ├── asgi.py
       ├── settings.py
       ├── urls.py
       └── wsgi.py
   ``` 
2. Run the Server
 Run the development server:
```bash
   python manage.py runserver
```
3. Follow `http://127.0.0.1:8000/` in your web browser and you should get the Django default welcome page.
#### 3. Create an App
1. The following will create a new Django app called myapp.
   ```bash
   python manage.py startapp myapp
   ```
2. It will create the following directory structure:
```
   myapp/
   ├── __init__.py
   ├── admin.py
   ├── apps.py
   ├── migrations/
   │   └── __init__.py
   └── models.py
   ├── tests.py
   └── views.py 
```
## Basic Structure
## I.Routes
1. Inside `myproject/urls.py`, add the routes for your project.

```python
   from django.contrib import admin
   from django.urls import path, include

   urlpatterns = [
      path('admin/', admin.site.urls),
      path('', include('myapp.urls')),
   ]
```
2. Open/create `myapp/urls.py`. 

```python
   from django.urls import path
   from. import views
   urlpatterns = [
  	
       path('', views.home, name='home'),
   ]
```
## II.Views

1. Create a simple view in `myapp/views.py`:

```python
   from django.http import HttpResponse
   def home(request):

         return HttpResponse("Hello, World!")
```
## III.Templates

1. Create a templates directory inside `myapp`, then add inside it an index.html file:
```
   myapp/
      ├── templates/
         └── index.html
```
2. Example `index.html`:

```html
   <!DOCTYPE html>
   <html>
   <head>
        <title>My First Django App</title>
   </head>
   <body>
       <h1>{{ message }}</h1>
   </body>
   </html>
```
3. Update the `home` view to use this template:
```python
   from django.shortcuts import render
   def home(request):

       context = {'message': 'hello This is my first Django Application'}
       return render(request, 'index.html', context)
```
   ![Output](https://github.com/anuja19103/Articles/assets/125860363/c7cb0cac-2f40-4e42-8bf7-f749761fdc6f)

The steps above create a very basic Django web application with just one basic homepage view. Make this structure more sophisticated by adding more views, templates, and routes to get bigger applications.
# Understanding HTTP and URLs
## HTTP Protocol
HTTP stands for HyperText Transfer Protocol. It is the basis of communication on the web that allows for the transfer of data between clients, typically browsers, and servers, typically websites. This is a request–response protocol; the client requests resources, and the server responds to the request.

Some of its main components are:

- **Request:** This is sent by the client in order to request a resource from the server.
- **Response:** This is what is sent in reply by the server, carrying either the requested resource or the outcome of that request.
- **Methods:** define actions like GET or POST.
- **Status Codes:** define the result, like 200 OK or 404 Not Found.
- **Headers:** This is metadata for requests and responses. For example, Content-Type.
- **Body:** The actual data being sent, for example, HTML or JSON.
## URLs (Uniform Resource Locators)
A URL is an address by which web resources are accessed. It consists of a number of parts.
**Components of a URL**
1. **Scheme:** Protocol, for instance, `http` or `https`.
2. **Host:** Domain name or IP address, say, `www.example.com`.
3. **Port:** Optional, port number, for example`:80` or `:443`.
4. **Path:** Particular resource, such as `/about`.
5. **Query:** Optional: Parameters of the resource, such as `?id=123`.
6. **Fragment:** Optional, which part of the resource, like `#section2`.
For instance, an URL could look as follows: `https://www.example.com:8080/path/to/resource?query=value#fragment`
### HTTP Methods and Status Codes
HTTP methods define an intent to do action on a resource:
- **GET :** to retrieve data from an origin server.
- **POST :** to submit data.
- **PUT :** to replace resource.
- **DELETE :** to remove data.
- **PATCH :**  to modify data.
- **HEAD :** to retrieve header only.

**HTTP status codes are to represent the final result of the request:**
- **1xx Informational:** Request received, continuing process (e.g., 100 Continue).

- **2xx Success:** The action was successfully received, understood, and accepted.
- **4xx Client Error:** Bad request example, 404 Not Found .
- **5xx Server Error:** Server failure example, 500 Internal Server Error .
### HTTP Request/Response Cycle

**1. Client sends request:** Lines of the request, headers and optionally a body.
**2. Server processes request:** Steps like the query of a database.
**3. Server sends response:** Line of the status, headers and optionally a body.
**4. Client renders response:** The content is displayed to the user.
Understanding of HTTP and URLs by a web developer enables one to manage web resources and facilitate smooth operation during client-server communications.
# Request and Response Handling
## HTTP Requests and Methods
These are client manipulations on a server. Major methods include:
- **GET**: Fetch data.
- **POST**: Send data.
- **PUT**: Modify data.
- **DELETE**: Remove data.
### HTTP Status Codes
These are responses to a request:
- **200 OK**: Success.
- **201 Created**: New resource created.
- **204 No Content**: Successful request with no content.
- **400 Bad Request**: Request that does not meet the validation criterion.
- **401 Unauthorized**: Authentication is required.
- **404 Not Found**: Resource is unavailable or disguised at that URI.
- **500 Internal Server Error**: Server error.
## Handling in Python (Django Example)
1. Create a Django project and app:

```bash
   django-admin startproject myproject
   cd myproject
   python manage.py startapp myapp
```
2. Define a view in `myapp/views.py`:

```python
   from django.http import HttpResponse

   def hello_world(request):
       return HttpResponse("Hello, World!")
```
3. Configure URL routing in `myproject/urls.py`:
```python
   from django.contrib import admin
   from django.urls import path

   from myapp.views import hello_world

   urlpatterns = [

       path('admin/', admin.site.urls),
       path('hello/', hello_world),
   ]
```
4. **Now run the development server**:
```bash
python manage.py runserver
```
5. **Access the view in a browser**: Open a browser and type the URL `http://127.0.0.1:8000`. 

Below is the output.

![Output - portno](https://github.com/anuja19103/Articles/assets/125860363/e8ad7ec5-d715-4129-8767-23ace5ec19a8)

# Templating and Rendering
## Templating Engines
**What are Templating Engines?**

- Templating engine should be able to process the template files within the application.
- The engine replaces variables in a template file with actual values that are passed by the application through
```
from django.shortcuts import render
def hello_name(request, name):

    return render(request, 'template.html', {'name': name})
```
It will render `template.html` and replace `{{name}}` with the given `name`. It works as dynamic html output.
### Advantages Of Templating Engines -
1. **Separation of Concerns**: Allows us to separate the presentation from the business logic.
2. **Code Reusability:** Reduces DRY violation and code duplication by providing reusability of HTML structure in multipe pages.
 3. **Dynamic Content:** It is easy to generate dynamic content in templates.
It offers dynamic, maintainable web applications, hence enhancing web development. In this regard, templating engines similar to that of Django become significantly valuable in their field.
# Working with Databases
## Role
Databases are at the heart of any web application, for they help to store and recover this data in a safe and effective way.
## Interacting with Databases
Interactions with the database can be enabled through frameworks like Django using the Object-Relational Mapping approach that maps database tables to Python classes.
## What's ORM?
ORM advertises itself as a middleware application or tool between a web application and a database.
## Example in Django
In Django, models are used to represent database tables, where every attribute corresponds to a column in the table. For example:
```python
   from django.db import models
   class Person(models.Model):
      name = models.CharField(max_length=100)
      age = models.IntegerField()
```
## Key Features of ORM
ORM gives a number of advantages including but not limited to: abstraction, portability, security against SQL injection, flexibility in querying and code organization and many other python and web developments projects.
It implies that with ORM, they efficiently handle databases and focus on developing great user experience.
# Deployment and Hosting
## The Process of Deployment
The process of deploying a web application involves preparing your code, choosing a hosting service, and configuring the server.
## Web Hosting Services
Heroku, AWS, and DigitalOcean are some great options; in fact, each of these services comes with their different features and plans.
## Choosing the Right Service for Hosting
Consider scalability, reliability, performance, security, and cost in your choice of a hosting service.
# Further Learning

On areas such as RESTful APIs, Authentication, Web Security, and Frontend Frameworks. Practical building projects applications.

# Resources

-**[Django Official Documentation](https://docs.djangoproject.com/)**: The official Django documentation is the best place to start. It provides comprehensive guides, tutorials, and references for all Django functionalities.
-**[Simple is Better Than Complex](https://simpleisbetterthancomplex.com/)**: A blog with tutorials and articles on Django and Python web development.
-**[Django Stars Blog](https://djangostars.com/blog/)**: Articles and case studies related to Django development and best practices.
-**"Django for Beginners" by William S. Vincent**: This book is perfect for those who are new to Django and web development.
-**"Django Unleashed" by Andrew Pinkham**: A more in-depth book that covers advanced topics and best practices.
-**"Two Scoops of Django" by Audrey Roy Greenfeld and Daniel Roy Greenfeld**: This book offers best practices and tips from Django experts.

# Conclusion

This tutorial was an introduction to Web Development with Python, including the frontend and backend of development, setting up a development environment, creating Web applications, understanding of HTTP, templating, working with Databases, and deployment of applications.
