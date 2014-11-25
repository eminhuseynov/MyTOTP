MyTOTP HTML5 TOTP App for PhoneGap/Cordova
======




<h1> This project is a simple HTML5 app template , feel free to customize as you wish</h1>
So, you implemented two-factor authentication on you system using mobile application, but you do not want to use someone else’s mobile application? You can easily create and publish your own.
In this article, I will show how to create a full-featured mobile application , fully compatible  withTOTP RFC standard. Most systems usually recommend Google Authenticator, which is open source, but you need to have some sort of mobile app development skills to implement your own. With Phonegap, no such skills are needed. 

<h2>Components to be used:</h2>
<ul>
<li>	MyTOTP HTML5 application (a simple open source  app – created for this article) </li>
<li>	An adobe account (to be used with build.phonegap service)</li>
<li>	A phonegap plugin – Barcodescanner (no installation/download required, will be dynamically added by build.phonegap). We need this plugin in order to read TOTP provisioning QR codes</li>
<li>	Developer accounts on Apple Appstore and Google Play if you want to publish your app</li>
</ul>

<h3>Step 1. Install PhoneGap on your system and create an empty app</h3>
a)	Download and install NodeJS http://nodejs.org/

b)	Open Command prompt and run ``` npm install -g phonegap ```

c)	Create a folder in your system and CD to it (“cd C:\MyApp\”)

d)	Run ```phonegap create my-app``` . Your project's path will become C:\MyApp\my-app . Remember to navigate to this folder in your command prompt session when running build commands.

<h3>Step 2. Copy HTML5 application to phonegap project</h3>
Download <a href=https://github.com/eminhuseynov/MyTOTP/archive/master.zip>zip file</a> from GitHub. Copy contents  to the www folder of your project (overwrite all files)

<h3>Step 3. Modify the config file</h3>
Open config.xml of you project and add the following line:

```<gap:plugin name="com.phonegap.plugins.barcodescanner" version="2.0.0" />```

this will enable the Barcodescanner plugin in your application. 
Copy config.xml to www folder

<h3>Step 4. Build the application </h3>
a)	Login to phonegap using ```phonegap remote login``` (register on phonegap.com – free account should be enough)

b)	From the project directory (not www) run ```phonegap remote build android```

c)	Login to build.phonegap.com and download your APK

You will need to configure signing certificates to create release packages (otherwise it will be debug APKs)


Have a look at the demo <a href=http://youtu.be/yfP5770iDZ0>here</a>
