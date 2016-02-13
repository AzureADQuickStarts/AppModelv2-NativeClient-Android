#App model v2.0 preview: Native Client for Android (Android API Level 18+)

This sample shows how to build an Android application that calls a web API that requires a Work Account for authentication. This sample uses the Active Directory authentication library for Android to do the interactive OAuth 2.0 authorization code flow with public client.


## Quick Start

Getting started with the sample is easy. It is configured to run out of the box with minimal setup. 

### Step 1:Register an app

First, create an app in the [App Registration Portal](https://apps.dev.microsoft.com)

Make sure to:

- Add the **Mobile Application* platform for your app.
- Enter the correct **Redirect URI**. The default for this sample is `urn:ietf:wg:oauth:2.0:oob`.
- Leave the **Allow Implicit Flow** checkbox enabled. 

Copy down the **Application ID** that is assigned to your app, you'll need it shortly. 


### Step 2: Download the Android Native Client Sample code and add it to your Eclipse Workspace

#### Download the Android Native Client sample code

* `$ git clone https://github.com/AzureADQuickStarts/AppModelv2-NativeClient-Android.git`


#### Load the sample using Maven

 
### Step 3: Configure the Constants.java file with your Azure AD application settings

This will be where you use the information you gathered in Step 1 and Step 2.

#### Open the Constants.java file in "ToDoActivity"

* In Eclipse, navigate to the /src folder
* Find the com.microsoft.aad.test.todoapi folder
* Open the Constants.java file

Update the constants with your Azure Active Directory information. Explination of the mapping is below.

Explination of the parameters:
  
  * CLIENT_ID is required and represents your tenant. A Client ID is a way we know what permissions you are requesting for your application and validate your application in your tenant is authorized to be used by the user. 
  
  * REDIRECT_URI is where the token is redirected to.
  
  * SERVICE_URL is your web API you wish to access*
  
  
### Step 4: Run the application!

Now that you've configured the app to point to the right Azure Active Directory endpoints, you can run the app! This is easy because the sample application already knows the semantics of the Rest API from our Samples so the application is ready to read and write tasks!

#### Debug the application and run the emulator

* In Eclipse, right mouse click on the ToDoActivity sample
* Select "Debug As.." and pick Android Application.

At this point, you should see your emulator launch and load the ToDoActivity in to your emulator. You can also deploy directory to any device running Android API Level 18 or higher.


##### NOTE

The current defaults are set up to work with our [Azure Active Directory Sample REST API Service for Node.js v2](https://github.com/AzureADQuickStarts/AppModelv2-WebAPI-nodejss). You will need to specify the clientID of your Web API, however. If you are running your own API, you will need to update the endpoints as required.




