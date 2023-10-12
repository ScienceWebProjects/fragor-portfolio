# Contents

- [Summary](#summary)
- [Project creators](#project-creators)
- [How do we work](#how-do-we-work)
- [Technologies used](#technologies-used)
- [Functionalities](#functionalities)
- [Awards](#awards)
- [Future of this project](#future-of-this-project)

# Summary

The subject matter of the project is of an interdisciplinary nature. Creating a management and data acquisition system required a combination of issues from the fields of web development, microcontroller programming and rapid prototyping in the form of three-dimensional design. The visual part of the website was created using the React framework for Java Script. The part supporting the server and analyzing and handling the data was written in python with the use of the django framework. For the process of data analysis and acquisition, the example of measuring the amount of filament used and the working time of the device in the 3D printing process was used. For this purpose, ESP8266 microcontrollers were used to communicate with the server. RFID technology allowed to assign tags to individual spools of filaments. Encoders were also used to measure the material used.

# Project creators

Piotr Goraj
`Front-End developer`

[GitHub account](https://github.com/Piotr-Goraj) /
[LinkedIn](https://www.linkedin.com/in/piotr-goraj-154a79225/?locale=en_US)

>I am a master's student of AWSB Merito, majoring in computer science, specializing in artificial intelligence management. I am a graduate of the Krakow University of Technology, majoring in electrical engineering. I belonged to research groups dealing with microprocessor programming and 3D graphics. Thanks to my professional experience, I have gained the ability to work in a team and organize this work into individual tasks.

Dawid Franczak
`Back-End developer`

[GitHub account](https://github.com/DawidFranczak) /
[LinkedIn](https://www.linkedin.com/in/dawid-franczak-3b20a9262/?locale=en_US)

> I have been involved in non-commercial programming for 1.5 years. I am proficient in Python version 3.x, Django framework version 4.x, as well as Django REST Framework. I provide a project that confirms my qualifications on Github (https://github.com/DawidFranczak/Smart-home-main-server) and a link to a website presenting the project described on Github: https://dawidfranczak.pythonanywhere.com/. My knowledge of JavaScript and CSS/HTML helped me create the basic UI of the website. Participation in scientific circles allowed me to gain experience working in a group.
>
> My goal: Back-End (Python-Django) Developer
>
> Currently learning: React

# How do we work

## Git & GitHub

- [Frontend repository](https://github.com/ScienceWebProjects/fragor-frontend)
- [Backend repository](https://github.com/ScienceWebProjects/fragor-backend)

## Jira software

- [Jira board](https://dataprocessing.atlassian.net/jira/software/projects/DPA/boards/1/roadmap)
- Confluence

## Meetings

- daily - several times a week we present our achievements so far
- epik - once a week we think of an epic for the next week which is a small development of the project

# Technologies used

- Front-End

  - HTML
  - CSS
    - SCSS
  - Java Script
    - React.js
      - styled-components
      - react-router-dom
      - js-cookie
      - node-sass
  - Node.js
    - npm
    - yarn

- Back-End

  - python3 (old version)
    - django
  - java (new version)

- Testing
  - docker

# Functionalities

## Briefly about the frontend part

The web application was designed in the SPA (Single Page Application) methodology using the React.js framework. Libraries for React such as styled-components, react-router-dom, js-cookie were used during development. When adding libraries, yarn was used, thanks to which it streamlined the installation process for individual developers.

### Web Page Map

The site map showing the individual transitions between the subpages is below. On its basis, the transition paths for react-router-dom were programmed.

<p align="center">
<img src="/files/webPageMap.png" alt="Web Page Map" width="700" height="500">
</p>

### Authorization

First page which user see is authorization page. Devices with a product code and first admin account are delivered to the final recipient. The product code is assigned to a given company. Admin can log in to the system and use it. New user in a company must register and create a new account by entering the product key. Every new account have the lowest permissions which could be change by administrator except first new account. First registered account in company have administrator permissions.

In this project four levels of authorization was created. masterUser as admin - this level has all of permissions and can delete users accounts, add or edit printers/filaments. Next level is changerUser - in this level of permission user can add or edit printers/filaments. The last permission level is commonUser - every new account have this permission type. User can only browse printers and filaments pages and search them. This three permissions levels are for end users. Only owners have permission to manage each user, company and all settings. This is fourth permissions level.

<p align="center">
   <img src="/files/authorization-mobile.png" alt="Authorization mobile page" width="300" height="600">
   <img src="/files/signin-mobile.png" alt="Signin form" width="300" height="600">
   <img src="/files/authorization-desktop.png" alt="Login form" width="1213" height="600">
 </p>

### Home page

After logging in, each user sees 3 buttons for subpages, only the administrator or changer user sees 4 whereas owners sees 6. The first two subpages are used to view, edit and add printers and materials. The settings subpage allows to change username, password or e-mail. Fourth page is available to administrator and changer user. They can add, edit or remove measurement devices. The last page visible for users available only to the administrator allows to change user permissions or remove them. Additionally, owners can manage users in given companies, as well as the companies themselves. The last, sixth subpage allows for this.

<p align="center">
  <img src="/files/home.png" alt="Home page" width="300" height="600">
</p>

### Printers

The printers subpage displays all available devices added by the admin. Any user can view items, but only users with the appropriate permissions can change them. The edit and delete buttons for a given device appear for administrator and editors only. The third button is used to assign the measuring device to a given printer, and the last button is used to calibrate it.

<p align="center">
  <img src="/files/printers.png" alt="Printers page" width="240" height="400">
</p>

### Filaments

The filaments subpage works similarly to the printers subpage, with the difference that filtering consists in selecting individual options from the list. Only the administrator and the editor have access to editing elements, adding new spools or materials. In addition, only the administrator chooses what colors are used in his company by selecting the "Material" button, he can also add a new brand.

<p align="center">
  <img src="/files/filaments.png" alt="Printers page" width="240" height="400">
</p>

### Settings

The settings page is available to every user. In this panel, everyone can change their username, password or e-mail.

<p align="center">
  <img src="/files/settings.png" alt="Printers page" width="240" height="400">
</p>

### Users

The "Users" subpage is available only to the administrator. There he can display all users assigned to a given company as well as grant them permissions. It can also remove the granted permissions as well as the users themselves.

<p align="center">
  <img src="/files/users.png" alt="Printers page" width="240" height="400">
</p>

# Awards

- The first distinction by a representative of Woodward during the faculty session of scientific clubs - Cracow University of Technology, May 2023

- Distinction during the "Student CYBERnetics Symposium" event - Military University of Technology, May 2023

 <p align="center">
  <img src="/files/wyroznienie_PG.jpeg" alt="wyroznienie PG" width="410" height="288">
 <img src="/files/wyroznienie_DF.jpg" alt="wyroznienie DF" width="410" height="288">
 </p>

# Future of this project

The project is still being developed. There are plans to introduce a system informing about the status of devices, an e-commerce system or changes to the UI itself. Minor changes are made at least once a week.
