# vaadin-combobox-error
creation of the smallest (polymer starter-kit) project that I could to demo error for vaadin team

## Diagnosis for problem when running in firebase hosting

* View Two blew up in previous version, inexplicably, and only in firebase hosting
* Fixed now, by renaming(in bower_components) vaadin-combo-box/vaadin-combo-box.html to vaadin-combo-box/vaadin-combo-bux.html or really to anything other than vaadin-combo-box/vaadin-combo-box.html
* in db-combo-box.html import must match same
* works like a charm

This makes absolutely no sense, but since it's an easy fix and it also works in my own codebase, I'm proving this for vaadin's own usage and letting it go.

## To replicate

* git clone project per usual
* run  `refresh_npm.sh` bash command per usual
* you will have to rename vaadin-combo-box/vaadin-combo-box.html to something else and then make sure matches with import in db-combo-box.html

## How to simulate firebase hosting

* in root of project
* you have already run the `refresh_npm.sh` bash command
* run the `firebase serve` bash command
* should be visible in localhost:5000

## With this final resolution

The reason for the error is the setup

1. you have any 404 import (in this case it was `vaadin-valo-theme/vaadin-combo-box.html`)
2. the 404 is redirected back to `index.html` in your config file: https://github.com/poly-on-fire/vaadin-combobox-error/blob/master/firebase.json#L15 (edited)


So you have to configure the `rewrite` rule properly and not to redirect 404 to `index.html`

See also: https://github.com/Polymer/polymer-starter-kit/issues/941#issuecomment-257493920


And this config looks good: https://github.com/Polymer/docs/issues/1755#issuecomment-249678734 (edited)

Wow thanks Sergey. Wouldn't have found those if you had given me six weeks to search for them. Thanks. 