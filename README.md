# vaadin-combobox-error
creation of the smallest (polymer starter-kit) project that I could to demo error for vaadin team

## Diagnosis for problem when running in firebase hosting

* View Two blew up in previous version, inexplicably, and only in firebase hosting
* Fixed now, by renaming(in bower_components) vaadin-combo-box/vaadin-combo-box.html to vaadin-combo-box/vaadin-combo-bux.html or really to anything other than vaadin-combo-box/vaadin-combo-box.html
* in db-combo-box.html import must match same
* works like a charm

This makes absolutely no sense, but since it's an easy fix and it also works in my own codebase, I'm proving this for vaadin's own usage and letting it go.

# To replicate

* git clone project per usual
* run  `refresh_npm.sh` bash command per usual
* you will have to rename vaadin-combo-box/vaadin-combo-box.html to something else and then make sure matches with import in db-combo-box.html

# How to simulate firebase hosting

* in root of project
* you have already run the `refresh_npm.sh` bash command
* run the `firebase serve` bash command
* should be visible in localhost:5000