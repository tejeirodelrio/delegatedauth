# About delegatedauth
A simple Node.js web application configured for [Heroku](www.heroku.com) that implements the **delegated authentication** SOAP web service from Salesforce.

#What is Delegated Authentication?
Single Sign On with Salesforce as the service provider requires an infrastructure with an identity provider that either implements standard interface using SAML (called Federated Authentication) or exposes the identity service using a SOAP based API - which is called Delegated Authentication. See this article to understand the concepts and how to implement your own identity provider.
This sample covers the Delegated Authentication and implements a sample SOAP web service using Node.js technology.
It can be easily deployed Heroku. Read the instructions below how to install and run the sample.

The Salesfrorce documentation describes delegated authentication in more detail.
Check this doc: https://help.salesforce.com/HTViewHelpDoc?id=sso_delauthentication_configuring.htm&language=en_US

#Installation

To run this example with your own Salesforce org, you need to contact Salesforce to enable delegated authentication single sign-on.

Assumes you have configured your local environment with the [Heroku Toolbelt](https://toolbelt.heroku.com/)

Open a terminal window and start typing... (output of each command ommitted)

    git clone https://github.com/tegeling/delegatedauth.git
    cd delegatedauth
    heroku login
    heroku create
    git push heroku master
    
##Run Heroku

    cd delegatedauth
    heroku scale web=1
    heroku logs --tail
    
#OR

Here is a friendly Heroku button.. It will create into Heroku for you, but the redirect_uri OAuth parameter is still configured as a servlet init param, so will need some intervetion before this works

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

#How to use
