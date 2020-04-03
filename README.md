## Note

- Replace Your Paytm Merchant ID and secret Key inside index.js
- To connect to emulator in localhost. Replace localhost to 10.0.2.2.
- Copy hosted URL to flutter code. Something like this "http://localhost:5000/{Firebase-Project-Name}/us-central1/customFunctions"
- Checksum folder is copied from paytm github repo.

# Requirements

1. Install Node js from [here][nodejs]
2. Install firebase-tools package in npm
   npm install -g firebase-tools
3. Login to Firebase-CLI
   npx firebase login
4. Create a Firebase project to use functions.
5. Create firebase project in CLI
   npx firebase init
   choose host functions only
   choose your project

[nodejs]: https://nodejs.org/en/

# Installation

1. Install npm packages from functions.
   cd functions
   npm i
2. To run server locally.
   cd ..
   npx firebase serve --only functions

# Installation Steps from PAYTM Docs

1.  The _checksum.js_ file contains _genchecksum()_ and _verifychecksum()_ functions. The merchant module should call these methods with the appropriate set of parameters as mentioned in the API document given [here][link1]
2.  Keep all the files in the folder from where you will be calling the _genchecksum()_ and _verifychecksum()_ methods.
3.  The _checksum/server.js_ file contains set required parameters and code to generate checksum to run the default transaction flow.

[link1]: https://developer.paytm.com/docs

# For Offline(Wallet Api) Checksum Utility below are the methods:

1. genchecksumbystring : For generating the checksum
2. verifychecksumbystring : For verifing the checksum
