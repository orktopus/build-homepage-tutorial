# Share your website with the world, with the help of Azure!

### This tutorial will walk you through how you can share your website with the rest of the world. In this tutorial, we will start with checking out a very simple project. We will first run this project in our own machine to see how it works, and make some changes as we like. Then we will deploy the website as an Azure App. Deploying an Azure app will allow us to share our website with others! We will also see how we can continue to make changes to our website even after it is deployed in Azure

## **Pre-requisites**:
To complete this tutorial successfully and deploy your website you will need the following:

1. Git: Git is used widely by software developers (and others) for __version control__. You can install it from here: https://git-scm.com/downloads
2. Visual Studio Code (VS Code): It is a light-weight code editor from Microsoft. Think of it as Microsoft Word... but for code
3. Azure Subscription: In order to deploy our website to Azure and share it to the world, we will need an Azure subscription
4. Node.js: Technical lingo: __Javascript runtime library__. In other words: It is a tool/platform/environment that we will use to run our code. You can install it from here: https://nodejs.org/en/download/
5. Npm: Short for node package manager. This will automatically be installed when you install node.js from above. NPM helps us retrieve common code that has already been created by someone else, and use it for our development. It is super useful!


## **Things we will also need/explore**:
In order to complete the tutorial, we will also touch upon a few other technologies. Here's a list of things that we will touch upon. Don't worry, you don't need to install all of them right away, we will install them along the way

1. Github: Github is where our initial code will be. We will clone (copy) our code and make changes to it
2. Azure App Service Extension: This will be a tool we will add-on to VS Code that will then help us deploy our website in azure
3. Express: Another tool that will helps deploy our website in node.js
4. Powershell: Tool to **run** our website locally


## Part 1: Deploying our website locally
In this first part we will start with some existing code, make some changes and deploy it locally to see it running and working. 

**Step 1: Get the source code from Github**
Start with opening a new powershell window (from windows start menu). We will now create a new folder and copy some starting code to that folder
To clone the source code to a convenient location on your machine, do the following steps:

    $ mkdir C:\git
    $ cd C:\git
    $ git clone https://github.com/orktopus/build-homepage-tutorial.git

**Step 2: Run the website locally**
    
    $ cd build-homepage-tutorial
    $ npm install -g express-generator
    $ npm install
    $ npm start

At this point, your website is running on your local machine. You can check it out by opening a browser window and typing in:

     http://localhost:3000

You can now see a very simple version of the website. Alas, it doesn't have any useful information. Next you will modify this website to make it your own.

**Step 3: Modify your website in vscode**
Open a new powershell window, and run the following commands to open our code folder in vscode.

    $ cd C:\git\build-homepage-tutorial
    $ code .

From the explorer tab, open views > index.pug Now you can see the generic text on your website....  
Go ahead and make some changes. Now refresh your web browser and you should see your changes!


## Part 2: Deploying our website to Azure

**Step 4: Install Azure App Extension** :

1. From "View" Menu, select "Extensions"
2. Search and install "Azure App Service" extension

**Step 5: Sign In to your Azure account**:
Once the extension is installed, log into your Azure account - in the Activity Bar, click on the Azure logo to show the AZURE APP SERVICE explorer. Click Sign in to Azure... and follow the instructions. 

**Step 6: Deploy the website to azure**:

1. In the AZURE APP SERVICE explorer, click the blue up arrow icon to deploy your app to Azure.
2. Choose "Create New Web App"
3. Type a unique name for your app (without spaces), such as <your-name>-homepage
4. Choose a location in a region near you or near other services you may need to access.
5. Choose your Node.js version, LTS is recommended.
6. Choose the directory you have currently open (build-homepage-tutorial)
7. Click Yes when prompted to update your configuration to run npm install on the target server. Your app is then deployed.
8. Click yes to "Always deploy the workspace....", so that next time you change your website, the changes are automatically deployed to Azure
9. Once the deployment completes, click Browse Website in the prompt to view your freshly deployed website.

Congratulations! Your website is now deployed! Share it with a friend or a fellow coder to your right or left. And check out their website too!
