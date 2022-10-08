After coding the front end, and runing the server, nothing worked as expected.
So I kept debugging until I found that the backend server reads the path to my post request which is '/register', and compares it to this path "^\/register".
So even though I provide the right credentiels I can't have the succes message.
So i changed this method if (re.match("^\/register", self.path) by this method (re.match("/register", self.path) in the run_server.py code.
AND IT WORKED.

I also added the nodemodules in the git ignore that were created when we used the npm to install the sass package.
So running an 'npm install' after cloning my project would do the trick.