# Anypoint Store Social Bot

+ [License Agreement](#licenseagreement)
+ [Use Case](#usecase)
	* [Setup](#setup)
+ [Considerations](#considerations)
+ [Run it!](#runit)
	* [Running on premise](#runonopremise)
	* [Running on Studio](#runonstudio)
	* [Running on Mule ESB stand alone](#runonmuleesbstandalone)
	* [Running on CloudHub](#runoncloudhub)
	* [Deploying your Anypoint Template on CloudHub](#deployingyouranypointtemplateoncloudhub)
	* [Properties to be configured (With examples)](#propertiestobeconfigured)

# License Agreement <a name="licenseagreement"/>
Note that using this template is subject to the conditions of this [License Agreement](AnypointTemplateLicense.pdf).
Please review the terms of the license before downloading and using this template. In short, you are allowed to use the template for free with Mule ESB Enterprise Edition, CloudHub, or as a trial in Anypoint Studio.

# Use Case <a name="usecase"/>
Anypoint Store Social Bot is an experience that demonstrates how customers can interact with social bots powered by services like Facebook. This template should serve as an implementation best practice and how Omnichannel APIs can be reused with Facebook Messenger. The Bot provides the functionality by querying existent last order from Retail Omnichannel Experience API for authenticated user (customer) from Anypoint Store.

## Setup <a name="setup"/>
What is important to set for communication of messenger user (customer) with social bot:
1. Create Facebook App
2. Create Facebook Page
3. Configure Template with access_token and keystore
4. Deploy Template to CloudHub
5. Configure Facebook App
6. Open your created Facebook Page, click on Send Message and Test Button
7. Start chat with social bot

Detailed information on [Facebook Messenger App Setup](https://developers.facebook.com/docs/messenger-platform/getting-started/app-setup).

# Considerations <a name="considerations"/>

To make this Anypoint Template run, there are certain preconditions that must be considered. **Failing to do so could lead to unexpected behavior of the template.**

# Run it! <a name="runit"/>
Simple steps to get Anypoint Store Social Bot running.
See below.

## Running on premise <a name="runonopremise"/>
In this section we detail the way you should run your Anypoint Template on your computer.


### Where to Download Mule Studio and Mule ESB
First thing to know if you are a newcomer to Mule is where to get the tools.

+ You can download Mule Studio from this [Location](http://www.mulesoft.com/platform/mule-studio)
+ You can download Mule ESB from this [Location](http://www.mulesoft.com/platform/soa/mule-esb-open-source-esb)

### Importing an Anypoint Template into Studio
Mule Studio offers several ways to import a project into the workspace, for instance:

+ Anypoint Studio Project from File System
+ Packaged mule application (.jar)

You can find a detailed description on how to do so in this [Documentation Page](https://docs.mulesoft.com/studio/7.4/import-export-packages).

### Running on Studio <a name="runonstudio"/>
Once you have imported you Anypoint Template into Anypoint Studio you need to follow these steps to run it:

+ Generate keystore (You can find a detailed description on how to do so in this [Documentation Page](https://docs.mulesoft.com/mule-user-guide/v/4.1/tls-configuration#generating-keystores-and-truststores))
+ Locate the properties file `mule-<env>.properties`, in src/main/resources
+ Complete all the properties required as per the examples in the section [Properties to be configured](#propertiestobeconfigured)
+ Once that is done, right click on you Anypoint Template project folder
+ Hover you mouse over `"Run as"`
+ Click on  `"Mule Application"`

### Running on Mule ESB stand alone <a name="runonmuleesbstandalone"/>
Complete all properties in one of the property files, for example in [mule.prod.properties](../master/src/main/resources/mule.prod.properties) and run your app with the corresponding environment variable to use it. To follow the example, this will be `mule.env=prod`.

## Running on CloudHub <a name="runoncloudhub"/>
While creating your application on CloudHub (or you can do it later as a next step), go to Runtime Manager > Manage Application > Properties to set the environment variables listed in "Properties to Configure" as well as the mule.env.

To create your application in CloudHub, go to Deployment > Advanced to set all environment variables detailed in "Properties to Configure" as well as in mule.env.

### Deploying your Anypoint Template on CloudHub <a name="deployingyouranypointtemplateoncloudhub"/>
In Studio, right click your project name in Package Explorer and select Anypoint Platform > Deploy on CloudHub. More details [here.](https://docs.mulesoft.com/runtime-manager/deploying-to-cloudhub)

## Properties to be configured (With examples) <a name="propertiestobeconfigured"/>
In order to use this Mule Anypoint Template you need to configure properties (Credentials, configurations, etc.) either in properties file or in CloudHub as Environment Variables.
Detailed list with examples:
### Application properties

+ https.port `8081`

### Access Token from your Facebook App
+ access_token `your-facebook-page-token`

### API properties
+ omni-experience-api.host `api.example.com`
+ omni-experience-api.port `443`
+ omni-experience-api.basePath `/api`
+ omni-experience-api.protocol `HTTP`

### Keystore properties
+ keystore.location `keystore.jks`
+ keystore.password `pass1`
+ key.password `pass2`
+ key.alias `1`

### Anypoint Store
+ anypoint.store.url `http://anypoint-store.com`
+ user.login.url `http://anypoint-store.com/login`
