
# Simple Azure deployment test

This repo is very simple and only contains an index.html. This is all that is needed to deploy the most simplest Azure Web App. 

The remainder of this readme provides instructions on how to deploy this very simple web page to Azure. 

## Create an empty Azure Web App 

This assume you are using the new Azure portal.

- Logged into the Azure portal and go to the main page.
- Click *New*.
- Click *See all*.
- Choose *Web App*.
- Click *Create*.
- Enter a name for you app, eg mytestapp
- Select a subscription and resource group.
- Select an *App Service plan/location*
	- Click *Create New*.
	- Enter a name for the *App Service plan*, eg mytestapp.
	- Select a location.
	- Select a *Pricing Tier*.
		- Click 'View all'
		- I recommend the 'Free' option just if you are experimenting.
	- Click *OK* to create the *App Service plan*.
- Click *Create* to create the *Web App*.
- Wait for the Web App to be deployed.

## Hook the Azure Web App up to a GitHub repo for deployment

- Go into the *Settings* for the Web app you just created.  
- Click *Deployment Source*.
	- Click *Choose Source*.
		- Click *GitHub*.
	- Click *Authorization* and connect to your Github account.
	- By default your personal account will be selected. You can change this to a different organization if required.
	- Now chose the Github project that you want to deploy. For example if you are deploying this repo choose *simple-azure-deployment-test*.
	- Select the branch to deploy or leave it as default (*master*).
	- Click *OK*.  
- Wait for deployment to complete.

You should now have simple web page that you can access at <web-app-name>.azurewebsites.net. 

For example if you called the app *mytestapp* then you can browse to the web page at [http://mytestapp.azurewebsites.net](http://mytestapp.azurewebsites.net).

## Updating your deployment

To update your deployment, simple push changes to the GitHub repo. Those changes will be automatically deployed to your Azure Web App.