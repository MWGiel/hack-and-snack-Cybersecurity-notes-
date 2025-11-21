## Front End

The front end of a web application contains the user's components directly through their web browser (client-side). These components make up the source code of the web page we view when visiting a web application and usually include HTML, CSS, and JavaScript, which is then interpreted in real-time by our browsers.
Browser window displaying HTML, CSS, and JS code snippets for a webpage layout.
This includes everything that the user sees and interacts with, like the page's main elements such as the title and text HTML, the design and animation of all elements CSS, and what function each part of a page performs JavaScript.
---
### Back End

The back end of a web application drives all of the core web application functionalities, all of which is executed at the back end server, which processes everything required for the web application to run correctly.
It is the part we may never see or directly interact with, but a website is just a collection of static web pages without a back end.
Some of the main jobs performed by back end components include:

 - Develop the main logic and services of the back end of the web application
 - Develop the main code and functionalities of the web application
 - Develop and maintain the back end database
 - Develop and implement libraries to be used by the web application
 - Implement technical/business needs for the web application
 - Implement the main APIs for front end component communications
 - Integrate remote servers and cloud services into the web application
---
### Securing Front/Back End

Even though in most cases, we will not have access to the back end code to analyze the individual functions and the structure of the code, it does not make the application invulnerable. It could still be exploited by various injection attacks, for example.
Suppose we have a search function in a web application that mistakenly does not process our search queries correctly. In that case, we could use specific techniques to manipulate the queries in such a way that we gain unauthorized access to specific database data SQL injections or even execute operating system commands via the web application, 
also known as Command Injections.
We will later discuss how to secure each component used on the front and back ends. When we have full access to the source code of front end components, we can perform a code review to find vulnerabilities, which is part of what is referred to as Whitebox Pentesting.
On the other hand, back end components' source code is stored on the back end server, so we do not have access to it by default, which forces us only to perform what is known as Blackbox Pentesting. However, as we will see, some web applications are open source, meaning we likely have access to their source code.
Furthermore, some vulnerabilities such as Local File Inclusion could allow us to obtain the source code from the back end server.
With this source code in hand, we can then perform a code review on back end components to further understand how the application works, potentially find sensitive data in the source code (such as passwords), and even find vulnerabilities that would be difficult or impossible to find without access to the source code.
---
> The W3C Document Object Model (DOM) is a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document.
