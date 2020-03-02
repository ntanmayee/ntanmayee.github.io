---
title: "Serve Static Files with Minimum Effort"
layout: post
date: 2020-03-02 11:36
headerImage: false
tag:
- phd-hacks
- server
- nodejs
- https
blog: true
author: tanmayee
description:
---
Suppose you have a group of files that you want to share with a group of people.<!--more--> In my case, I had some experimental results and analysis that I wanted to share. I couldn’t put up these files on a public platform because of security reasons, so I needed some method of access control. I suppose the naïve way would be to send everyone an email, but I wanted to keep updating some files as I continues the analysis, so emails would have been too mesy to deal with.

I thought a simple HTTP server should serve the purpose, but I didn’t want to spend too much time writing the code for authentication and SSL.

Then, I found [http-server](https://github.com/http-party/http-server), which is command line http server. Perfect!

Steps -
1. Install node.js, npm and npx
```
sudo apt install nodejs nodejs-dev node-gyp libssl1.0-dev npm
```
2. Install http-server
```
sudo npm install --global http-server
```
3. Generate SSL files as mentioned in the README
```
openssl req -newkey rsa:2048 -new -nodes -x509 -days 3650 -keyout key.pem -out cert.pem
```
4. Navigate to the folder with the static files you want to serve
```
npx http-server --username user --password pass -S -C cert.pem -K key.pem --no-dotfiles --log-ip
```

That’s it!
