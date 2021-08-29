# Electron-Webrunner

## Usage

`cd` into this repo.

Run: `npm start`
^ you'll have to download [nodejs](https://nodejs.org/en/) to get that working

## Info

There is a repo on my github titled `webrunner`, which is a flask webserver I built to run online experiments in the Kurtz lab (because of COVID). Now that we moved back to local in-person data collection, I'd rather not re-writer all my experiments.

This repo contains some scripts that let you run online experiments locally. It's basically just an [electron](https://www.electronjs.org) app that points to whatever particular html page you want it to.

What's the point of this? Why go through the hastle of bringing in electron and nodejs? It's pretty difficult/impossible to get full access to your local pc's filesystem with just html/js alone. Using electron lets you read/write anywhere on the local filesystem, which is very convenient for running in-person experiments.

This is set up to work with an example experiment from the `webrunner` server, but could pretty much work with anything (like [jsPsych](https://www.jspsych.org)). Just swap out the `exp.html` file and put in whatever local resources you need (i stored all mine in the folder titled `static`). 

There are lots of tools for running behavioral experiments locally, like [psychtoolbox](http://psychtoolbox.org), [psychopy](psychopy.org/), etc <-- try those if you don't like webcoding. The benefit of using html/js for stuff like this is that it (a) is designed for displaying visual interfaces, which is good for experiments; (b) is constantly evolving because everyone's working on the internet; and (c) it works on almost every computer.

**Note:** this is pretty bare-bones; hasn't really been tested on anything other than the computers I use.
