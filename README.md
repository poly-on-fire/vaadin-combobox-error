# vaadin-combobox-error
creation of the smallest (polymer starter-kit) project that I could to demo error for vaadin team

## How to test it without deploying it

* go to https://df-lab.firebaseapp.com/
* turn on chrome developer or whatever dev tool
* notice no error
* go to View Two in the menu
* notice that view does not come up, console fills with errors

## How to test it and prove that it works fine not deployed to firebase

* git clone project
* run the refresh_npm.sh command to get it all loaded up
* cd public
* run bash command 'polymer serve'
* navigate to app log in with google (optional)
* click on View Two and notice that no error messages, drop down works

## Hoe to run it localhost and diagnose error

* git clone project
* run the refresh_npm.sh command to get it all loaded up
* run bash command 'firebase serve'
* navigate to localhost:5000 or whatever it is
* see above ^ notice that it errors same as https://df-lab.firebaseapp.com/
