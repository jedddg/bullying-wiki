# bullying.wiki

[![License](https://img.shields.io/badge/license-GPL--3.0-blue)](LICENSE)

> This is the offical repository of the non-profit anti bullying.wiki website. The aim of this project is to raise awareness about bullying in a modern way.

# Table of Contents

- [Introduction](#introduction)
- [Documentation](#documentation)
- [License](#license)
- [Acknowledgements](#acknowledgements)

##### Disclaimer: Some content on this documentation may be generated by and sourced from ChatGPT, an AI language model.

## Introduction

Bullying, in forms of verbal abuse, physical abuse or tall poppy syndrome is now extremely common amongst teens in schools or public places and has now increased due to the form of cyberbullying taking place. A survey conducted by the National Centre Against Bullying (NCAB) found 1 in 4 Australian students have reported being bullied. Imagine the amount of other kids who have stayed silent through their teenage years.

Unfortunately, issues like these are not being properly raised.

## Documentation

### Explanation[^1]

### Technologies

#### EJS
EJS (Embedded JavaScript) is a JavaScript templating engine widely used in web development to create dynamic web pages and applications. It functions similar to HTML (Hyper Text Markup Language), but allows seamless integration of JavaScript code within HTML, enabling the creation of more dynamic and fluent web applications.

EJS also supports the use of partials, which allows developers to nest .ejs files to create reusable components that assemble into complete HTML files at runtime. Unlike React, EJS is more user-friendly as it follows the HTML syntax and is lightweight. In this project, EJS was mainly used for the navigation bar, reducing code duplication and separate rendering on each page.

#### Node.js
Node.js is an open-source, cross-platform JavaScript runtime environment built on Google Chrome's V8 JavaScript engine. It enables JavaScript to run outside the web development environment, powering server-side (backend), mobile apps, and non-web applications with JavaScript.

JavaScript is essential in a web developer's toolkit, mainly due to its Node Package Manager (NPM), which allows installation of community-built packages such as Express.js or EJS, adding additional functionality. Node.js is considered one of the most significant projects in JavaScript development history.

Major organizations like Netflix, NASA, Trello, PayPal, LinkedIn, Walmart, Uber, Twitter, eBay, GoDaddy, and Citibank utilize Node.js for its versatility and efficiency.

#### Express.js
Express.js, commonly referred to as Express, is a versatile framework for Node.js that simplifies the web development process. It provides developers with a powerful API (Application Programming Interface) that simplifies complex tasks like routing, logging, authentication, and handling HTTP requests.

Companies like Twitter and Trustpilot include Express.js in their tech stack due to its versatility. In this project, Express was used for routing, allowing the setup of different routes for various pages in a secure and modern way without the need for the .html extension.

#### GitHub
GitHub is a centralized version control, code management, and hosting platform that facilitates collaboration on software projects and tracks changes to codebases. It utilizes Git, an open-source version control system that links the developer's local repository with the cloud-based repository on GitHub.

GitHub also serves as a social platform where developers can share their coding journey and showcase their activity, which interests companies in search of hiring opportunities. Among the tens of thousands of companies that use GitHub in their tech stack, popular ones include Netflix, Airbnb, Shopify, Udemy, and Reddit.

In this project, GitHub was used for collaboration, change tracking, and documentation.

#### Visual Studio Code
Visual Studio Code is an open-source Integrated Development Environment (IDE) created by Microsoft. It is a lightweight version of Microsoft Visual Studio. While Visual Studio Code lacks low-level programming capabilities for languages like C++ or Assembly, it is well-suited for web development.

Developers benefit from its simple user interface, shortcuts, and extensions. Visual Studio Code is widely used in the industry by companies like Google and is also popular in many universities.

#### ./src/index.js
The `index.js` code sets up a web server using the Express.js framework, applies security and performance enhancements, and defines routes for different pages.

The code imports the necessary modules: express, helmet, and compression.
> These modules are required for creating the web server, enhancing security, and improving performance.

The code initializes an instance of the Express application by calling `express()`.
> The created instance is assigned to the variable app.

The code sets the view engine to EJS (Embedded JavaScript) using `app.set("view engine", "ejs")`.
> It specifies the directory where the EJS views are located by setting `app.set("views", "./src/views")`.

The code uses express.static middleware to serve static files (such as CSS, images) from the "public" directory.
> The `__dirname` variable represents the current directory.

The code applies the Helmet middleware using `app.use(helmet())`.
> Helmet is a collection of security-related middleware functions that enhance the security of the web application.
> It helps protect the application from various attacks and vulnerabilities.
> The code also disables the "x-powered-by" header using `app.disable("x-powered-by")`.
> Disabling this header removes server information from the response, providing an additional layer of security.

The code applies the Compression middleware using `app.use(compression())`.
> Compression is a middleware that enables gzip compression for the responses sent by the server.
> This helps reduce the size of the responses and improves the overall performance of the web application.

The code defines routes for different pages using `app.get()`.
> For example, when a GET request is made to the root URL ("/"), the server renders the "index" template using `res.render("index")`.
> Similarly, when requests are made to `"/aboutUs"`, `"/mission"`, and `"/events"`, the corresponding EJS templates are rendered.

The code starts the server and makes it listen on port 3001 using `app.listen(3001)`.
> This means the web application will be accessible at `http://localhost:3001`.

#### ./src/views/index.ejs
The `index.ejs` file represents the home page of the Bullying Wiki website. It contains the HTML structure and content for the home page, including the page title, favicon, CSS stylesheets, and JavaScript file references. Here's a breakdown of the code:
> The **head** section includes the necessary metadata, such as character encoding, viewport settings, and page title.

> External resources, such as the website logo and CSS stylesheets, are linked using the **link** tags.

> The **body** section contains the main content of the home page.

> The **fold** div represents the top section of the page, which includes the website name "Bullying.wiki" and a tagline about creating a safer web.

> The **bullying-definition** div provides a definition of bullying, including the pronunciation and a description of its meaning.

> The **our-mission-button-container** div contains a button with a link to the "Our Mission" page.

> The **script** tag at the end references a JavaScript file named `nav.js` for any additional functionality related to navigation.

#### ./src/views/aboutUs.ejs

The `aboutUs.ejs` file represents the "About Us" page of the Bullying Wiki website. It contains the HTML structure and content for the about us page, including the page title, favicon, CSS stylesheets, and JavaScript file references. Here's a breakdown of the code:

> The **head** section includes the necessary metadata, such as character encoding, viewport settings, and page title.

> External resources, such as the website logo and CSS stylesheets, are linked using the **link** tags.

> The **body** section contains the main content of the about us page.

> The **include** statement includes the navigation section from a partial file named `nav.ejs`.

> The **p** tag contains a paragraph describing the creators of the website and their motivation behind creating it.

> The **h2** tag represents the heading "Meet the team," which likely introduces information about the individuals involved in the project.

#### ./src/views/events.ejs

The `events.ejs` file represents the "Events" page of the Bullying Wiki website. It contains the HTML structure and content for the events page, including the page title, favicon, CSS stylesheets, and JavaScript file references. Here's a breakdown of the code:

> The **head** section includes the necessary metadata, such as character encoding, viewport settings, and page title.

> External resources, such as the website logo and CSS stylesheets, are linked using the **link** tags.

> The **body** section contains the main content of the events page.

> The **include** statement includes the navigation section from a partial file named `nav.ejs`.

#### ./src/views/mission.ejs

The `mission.ejs` file represents the "Our Mission" page of the Bullying Wiki website. It contains the HTML structure and content for the mission page, including the page title, favicon, CSS stylesheets, and JavaScript file references. Here's a breakdown of the code:
> The **head** section includes the necessary metadata, such as character encoding, viewport settings, and page title.

> External resources, such as the website logo and CSS stylesheets, are linked using the **link** tags.

> The **body** section contains the main content of the mission page.

> The **incldue** statement includes the navigation section from a partial file named `nav.ejs`.

> The **p** tag contains a paragraph describing the mission of the Bullying Wiki website, which is to bring awareness to the issue of bullying and cyber-bullying in a fun and informative way.

### The Future

For the rest of the term I would love to get this website finished with Hannes to have a site that clearly emphazises the problem of bullying and how to combat it.

I plan to host the site by the end of the term with my Raspberry Pi, using Cloudflare Tunnels to securely host it to the internet without needing to open ports on my router.

The site should hopefully be indexed high on Google so people can access and view the website, I may need to look into SEO if it is low in Google results.

### Usage
1. Install and set up Git. A guide by GitHub (https://github.com/git-guides/install-git).
2. Clone the GitHub repository. 
```bash
git clone https://github.com/jedddg/bullying-wiki.git
```
3. Open the terminal and navigate to the folder using `cd`.
4. Check if npm is installed by running `npm` in the terminal. If not, install Node.js and NPM (https://docs.npmjs.com/downloading-and-installing-node-js-and-npm).
5. To make sure that all dependencies are installed, run 
```bash
npm i
````
6. Run 
```bash
npm run dev
```
7. Visit `https://localhost:3001`.

### License

We love improvements, so we use the GPL-3.0 license to ensure that our work being used is used in good favour.

### Acknowledgements

Shoutout Hannes for doing the styling and base JavaScript and HTML. Cool guy.

[^1]: Documentation was partially written by ChatGPT.
