This "new-user" directory is for Wheelcore admins or those who want to transition from Quick Deployment into Rich Deployment.

Download node.js (https://nodejs.org/en/download) and open the command line interface tool of your operating system in this directory. If you do not know what the command line interface (CLI) is of your operating system simply do a quick internet search for "(Your OS) Command Line" or "(Your OS) Terminal" and see what results you get. Every single operating system, whether it be Windows, iOS, MacOS, Linux, Android, etc., has the capability of running a CLI either through built-in tools or an emulator. Once you have opened the command line and navigated to this directory (look up what the "cd" command does in a command line interface to understand this better), go on ahead and run the following two commands, one at a time, to make sure everything is installed correctly:

node -v

npm -v

These commands will return the installed version of Node.js and npm. Now run the following command to generate a package.json file with basic settings:

npm init -y

To start a local server and serve an index.html file, you need to install a package that handles the HTTP server, such as http-server. We will install it with the following command:

npm install --save-dev http-server 

Now, in the package.json file, edit the scripts section:

{
   "name": "my-project",
   "version": "1.0.0",
   "scripts": {
      "start": "http-server -p 8080"
   },
   "devDependencies": {
      "http-server": "^14.1.1"
   }
}

This will allow you to start a local server by running npm start.

Your "index.html" file is sitting under the "files" folder in your Username directory. So we don't need to go through the process of making an html file. You already have one. Now we will run the following command after you save your package.json file:

npm start

The local server will start on port 8080. To access the web application, open a browser and type:

http://localhost:8080/

If you want to change the port, you can change it in the start script in the package.json file, for example:

"start": "http-server -p 3000"

to run the server on port 3000.



