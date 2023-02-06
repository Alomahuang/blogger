---
title: "Deploy Your React Application on Surge."
date: 2022-12-09 T00:00:00-00:00
categories:
  - Web
tags:
  - React
  - Surge
toc: true
toc_sticky: true
---

Surge is a static web hosting platform that allows you to quickly and easily deploy your React application. In this article, we will discuss how to deploy your React application on Surge, including the steps you need to take to build your React project, create a 200.html file for client-side routing, and finally deploy your application with the surge command.
{: .notice--info}

## Why we need 200.html file for client-side routing 

The 200.html file is required for client-side routing to work properly on Surge because it is used as a fallback by Surge when a user navigates to a URL that does not match an existing file in the build directory. By creating a 200.html file and configuring your client-side routing to use it as the base URL, you can ensure that your React application will work correctly on Surge.

## How 200.html works?

When a user navigates to a URL on a static website hosted on Surge, Surge will first look for a file with the same name as the URL in the build directory. For example, if the user navigates to example.com/about, Surge will look for a file named about in the build directory.

If Surge finds a file with the same name as the URL in the build directory, it will serve that file to the user. However, if Surge does not find a file with the same name as the URL, it will look for a 200.html file in the build directory and serve that file instead.

This means that if you are using client-side routing in your React application, you will need to create a 200.html file in the build directory, and configure your client-side routing to use the 200.html file as the base URL. This will ensure that when a user navigates to a URL that does not match an existing file in the build directory, Surge will serve the 200.html file and your client-side routing will be able to handle the URL and render the appropriate content.

## Build Your React Project

Before you can deploy your React application on Surge, you need to build your project using the npm run build command. This command will run the build script in your package.json file, which will compile your React code and generate a static version of your application in the build directory.

To build your React project, open a terminal or command prompt window and navigate to your project directory. Then, run the following command:

```
npm run build
```
This will run the build script in your package.json file and generate a static version of your React application in the build directory.

## Create a 200.html File for Client-Side Routing

If you are using client-side routing in your React application, you will need to create a 200.html file in the build directory. This file is required for client-side routing to work properly on Surge.

To create a 200.html file for client-side routing, follow the instructions on the Surge website: https://surge.sh/help/adding-a-200-page-for-client-side-routing

## Deploy Your Application with the surge Command

Once your React project has been built and you have created a 200.html file for client-side routing, you are ready to deploy your application on Surge. To do this, you will need to run the surge command in your terminal or command prompt window.

First, make sure that you are in the build directory, where the static version of your React application is located. Then, run the following surge command:

```
surge
```
This will start the Surge deployment process, and you will be prompted to enter your email address and password (if you have not already logged in). Follow the instructions on the Surge website to complete the deployment process: https://surge.sh/help/getting-started-with-surge

Once the deployment process is complete, your React application will be live on the internet, and you can access it using the URL provided by Surge.

In summary, deploying your React application on Surge is a simple and straightforward process. To do this, you will need to build your React project with the npm run build command, create a 200.html file for client-side routing, and then run the surge command to deploy your application. Follow the instructions on the Surge website to complete the deployment process and make your application live on the internet.












