# Mandai_Slideshow

## Description

This repo is to keep track of the slideshow display server hosted on a raspberry pi.
The raspberry pi will be in kiosk mode, and make use of node.js and bootstrap.
Most of the setup is adapted from https://www.iotshaman.com/blog/content/configuring-raspberry-pi-to-run-a-nodejs-server.

### Dependencies

Run the following commands to install nodejs, npm and node-semver.

```
$ sudo apt-get install nodejs npm node-semver -y 
$ sudo npm install n -g
$ sudo n stable
$ sudo npm install npm@latest -g
```
Install git to clone a sample application

```
$ sudo apt-get install git -y
```

## Downloading Sample Application

```
$ git clone https://github.com/kbrown333/api_starter.git
$ cd api_starter
$ npm install
```

### Running the App

```
$ npm start
```
