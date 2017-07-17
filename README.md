# SAP Cloud Platform Training - Backend Code

## Prerequisites
1. Eclipse Neon or Oxygen installed - [Click here](https://www.eclipse.org/downloads/?)
2. Maven installed (optional) - [Click here](https://maven.apache.org/download.cgi)
3. Git installed - [Click here](https://git-scm.com/downloads)
4. Java Web Tomcat 8 installed and Server Runtime configured - [Click here](https://tools.hana.ondemand.com/)
  * Remember to install the additional Software from Help -> Install new Software... -> SAP Cloud Platform Tools
5. Have a SAP Cloud Platform Trial Account - [Click here](https://cloudplatform.sap.com/index.html)

## Steps - 1. Running application locally
1. Clone this Repository in your machine
2. Open Eclipse and import this project (Import -> Existing Project into Workspace)
3. Right click on your imported project and select Maven -> Update Project (Or run it from the command line if installed)
4. Right click on your imported project and select Run As -> Run on Server
5. Select the SAP -> Java Web Tomcat 8, click Finish. This should setup and start your server
5. Access the application at [http://localhost:8080/scptraining-be/](http://localhost:8080/scptraining-be/). Don't mind the 404.
6. If you access this path [http://localhost:8080/scptraining-be/api/task](http://localhost:8080/scptraining-be/api/task) you should see an empty array, like: []
 
## Steps - 2. Deploy to the cloud
1. On your Eclipse, right click on your project and select Export -> War File, save it to your Desktop (Or get it from the Maven Build)
2. Access [your SCP cockpit](https://account.hanatrial.ondemand.com/cockpit)
3. Navigate to Applications -> Java Applications
4. Click on the Deploy Application button and select the following:
- War File Location: Select the file you exported on Step 1
- Application name: scptrainingbe
- Runtime Name: Java Web Tomcat 8
- Leave other fields with their default values
5. Click on the Deploy button and wait for the upload
6. Once Deployment is done, Start the application
7. Once the application is Started, click on its name on the Java Applications view
8. On the application view, click on its link in order to launch a new browser tab. Again, don't mind the 404, yet ;)
9. Append `/api/task` in the end of the URL. You should see an empty array, like: []

If you reached this point without any error, you are good, your API Server is up and running!

## Steps - 3. UI Deployment
1. Go to: [https://github.com/frankrafael/scptraining-ui](https://github.com/frankrafael/scptraining-ui) and continue from there.