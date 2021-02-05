# SES HR Department

## Introduction:
This project is created for a master course using 12-factors in PHP. 
You can find our project in a folder called "SES-HR-Department". 
In the "php - services" folder, you can find the same services but in pure php. 
And in folder called "related_files" you can find ( MySQL Database , Postman json file )

SES HR department is a project containing (add / edit / delete / search / show list / show info) for employees, where those services are an API. The main aim is to walk through 12-factor and implement them in our project. Implement "SES HR Department.postman_collection.json" file to Postman to view API services & results. We start by creating an Online Google Document to find all information. And then learn about Git vs Github with differences between them, important keywords in GitHuh, create an account in GitHub, interact with it.deal with Desktop GitHub.


## Technical used in SES HR Department
The techniques used to develop the API are Codeigniter framework using PHP script Language with RESTFUL API. Connecting it with PHPMyAdmin Database (MySQL) and using the kanban project of GitHub. In addition, using Docker.
| Technical                 | Description                                          |
| ------------------------- | -----------------------------------------------------|
| CodeIgniter 4 Framework   | It powerful PHP framework with a very small footprint. It supports REST APIs and we create 1 class containing 5 functions, where each function is represented as a service (This is a way to define services if they are related to the same object as an employee).  Link : https://codeigniter.com/                  |
| MySQL Database            | PHPMyAdmin, put in code we use MySQLi & PDO          |
| Postman                   | Used to view APIs services & results                 |
| Kanban Project            | To manage services between team members and also manage work on repo.         |
| GitHub                    | To Upload our work on it and create a repository (first factor)               |
| Desktop GitHub            | To help us to upload, send pull request, see any changes on the code          |
| Docker                    | Helps to implement many factors with our project                              |
| Docker Compose            | It is a tool for defining and running multi-container Docker applications     |
| Yamel                     |         |
| Kubernetus                |         |


## Our Services
1. Show Employee List service
2. Show Employee Details service
3. Search For Employee service
4. Add New Employee service
5. Edit employee Information service
6. Delete Employee service

## APIs
| Service             | Method        | Link                      |
| ------------------- |:-------------:| :-------------------------|
| Add Employee        |   /POST       | /employee/add             |
| Edit Employee       |   /POST       | /employee/update          |
| Employee Info       |   /POST       | /employee/show  + param.  |
| Search for Employee |   /POST       | /employee/search          |
| Delete Employee     |   /POST       | /employee/delete          |
| All Employee        |   /GET        | /employee/show            |

## Context Diagram
![Context Diagram](context_diagram.png)


## 12-Factor:
**1. Codebase**
>One codebase tracked in revision control, many deploys ✔
>We have no particular problems here, it’s just a matter of development workflow. 
>We can track our app code in Git: the master branch is deployed to production, while 
>all the development and testing is made under separate branches.


**2. Dependencies**
>* Explicitly declare and isolate dependencies
>* We got this too, we have Composer for PHP dependencies.
>* In PHP you can use composer, which basically allows you to create a list of dependencies that needs to be downloaded and installed during the deployment of the application.
>* We create composer.json for codeigniter or file docker (DockerFile).
>* Dockerfile used to help and applied docker commands 


**3. Config**
> In Codeigniter, the rest of the api is added as a system library.
> There is a file named Konfig that works on the connection with the Databases, which is MySQL
With the new version of the web we will be working on using





**4. Backing services**
>* We create 6 services as shown in the previous topic and it is APIs. 
>* Also we add some dependencies with is as backig services to the docker.
>* As example of third parity (adding some commands and files to Codeigniter project).



**5. Build, release, Run**
>Deployment tools typically offer release management tools, most notably the ability to roll back to a previous release.
>An approach is to store releases in a subdirectory named releases, where the current release is a symlink to the latest release binary. This makes it easy to quickly roll back to a previous release.
>`ouer code command line`


**6. Processes**
>Twelve-factor processes are stateless and share-nothing. Any data that needs to persist must be stored in a stateful backing service, typically a database.

>A twelve-factor app never assumes that anything cached in memory or on disk will be available on a future request, because chances are high that a future request will be served by a different process


**7. Port binding**
 >IP sockets (especially TCP/IP sockets) are a mechanism allowing communication between processes over the network. In some cases, you can use TCP/IP sockets to talk with >processes running on the same computer (by using the loopback interface, a.k.a. 127.0.0.1).

 >A Unix socket is an inter-process communication mechanism that allows bidirectional data exchange between processes running on the same machine


**8. Concurrency**
>They should rely on the operating system's process manager (such as systemd) to manage output streams, respond to crashed processes, and handle user initiated restarts and shutdowns.

> This makes adding more concurrency a simple and reliable operation.


**9. Disposability**
> By using Docker and K8s this allows the system to be fast startup & graceful shutdown. 

>  **Fast Startup:** 
>  The time starts from executing the launch command until the process is up and ready to receive requests (Minimize processes startup time).

>  **Graceful Shutdown:**
>    * **For Web Process:** Stop listening to the service port (refusing any new requests & finish it, then exiting). This means HTTP requests should be short.
>    * **For Worker Process:** Return the current job to a work queue manually. When a worker disconnects, queuing systems return the job automatically to the queue. Jobs can be reentrant, by wrapping the results in a transaction (to allow rollbacks)


**10. Dev/prod parity**
>"Keep all deploys similar as you can"
>It helps to minimize the gap in time, employee, tool, and deploys (between development and production).


**11. Logs**



**12. Admin processes**



