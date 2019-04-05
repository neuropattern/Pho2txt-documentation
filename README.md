# Pho2txt description
Pho2txt is a web application implemented as extension for Chrome browser. The application architecture represents client-server model. Text recognition can require high computer capacity so this architecture model lets transfer all computation to one high performance server and make our application more available.

---
## Application deployment
### Server
Server and database are going to be deployed on Heroku. Heroku is a platform as a service that enables developers to build, run, and operate applications entirely in the cloud.

### Client
Client part as extension can be downloaded from the [web-page](https://www.pho2txt.herokuapp.com/get-app) and installed to local Chrome extension market.

![](https://github.com/neuropattern/Pho2txt-documentation/blob/master/type_of_deployment.PNG)

---

## Technology justification
### Frontend
To implement client part we have chosen ReactJS - library for JavaScript. There are many reasons why:
1. React is easy to use. Unlike Angular and other libraries & frameworks for JavaScript, it’s not a complex tool.
2. It has a lot of easy-to-understand tutorials available on the Internet.
3. React lets you build rich user-interfaces easily.

### Backend
To implement server part we have chosen Flask - a micro web framework written in Python. It has no embedded database abstraction layer, form validation, or any other components that can be useless and load server work in vain. Reasons for Flask:
1. Speed. Flask can support hundreds of queries per second without any negative impact.
2. Simplicity. Flask being minimalistic provides the developer necessary features to build a prototype for a web application easily. It gives developers control as well as flexibility as to how they wish to develop their web apps.
3. Reach extension market. Numerous extensions provide database integration, form validation, upload handling, various open authentication technologies, and more.

### Recognition module
To implement recognition module we have chosen OpenCV. First reason why is because it's specific. It was created for image processing. All of the information and features of the system were fashioned with the Image Processing coder in mind. Second reason is its speed. In comparison with Matlab OpenCV can process in 6 times more frames per second. And the last reason is its efficient - it is less load on the productive capacity of computer.

---

## Quality indicators

- **Performance**: a user must receive recognized text in 10 seconds maximum or in 20 seconds if server is overloaded.
- **Compatibility**: the extension must be workable on most popular browsers like Chrome, Mozilla, Opera and Edge.
- **Security**: data must be transmitted in encrypted form between client and server.
- **Usability**: all fields and buttons must have description. A user must get access to the functionality consistently depending on the performed actions.

---

## Crosscutting concerns

- **Exception management**: ensure the stability of the application state after a crash.
- **Validation**: input validation.

---

## "To Be" VS "As Is" architecture

![](https://github.com/neuropattern/Pho2txt-documentation/blob/master/deployment_diagrams.jpg)
![](https://github.com/neuropattern/Pho2txt-documentation/blob/master/components.png)

---

## Conclusion

We should:
- **Define contacts**: define contracts for each component
- **Limit functionality**: component should perform defined functions/methods

According to deployment and component diagrams we have to change server framework. Flask is more lightweight, it does not need to be configured at the start and does not include special settings and middleware, which in our project will not be useful and will load the server in vain. We decided add web-page for more convenience.
