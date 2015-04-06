---
layout:     post
title:      Getting Started with Hubot in Windows
date:       2015-02-23 00:00:00
summary:    Running Hubot in Windows.
categories: tech
---

Hubot is an open source, event driven Chatbot that can be hacked as serious productivity, monitoring and automation tool as well as your fun, quirky fellow peer. It is written in Node.js and can be extended using basic coffeescript or javascript. 

### Install NodeJS

Download NodeJS – preferably 32-bit version to have better node-gyp compatibility on Windows

![screen01](https://cloud.githubusercontent.com/assets/1732018/5625331/c0c7917a-95b3-11e4-923c-6663965ef07b.png) 
![screen02](https://cloud.githubusercontent.com/assets/1732018/5625338/d804880c-95b3-11e4-9513-bc29b15c6707.png)
![screen03](https://cloud.githubusercontent.com/assets/1732018/5625339/d9d2d35a-95b3-11e4-8603-89d02d45d6f3.png)

Check node installation using `where node` command
 
Install following NPM Modules: `npm install -g yo generator-hubot coffee-script`
 
![screen04](https://cloud.githubusercontent.com/assets/1732018/5625341/e1d62d86-95b3-11e4-959a-ce6924457da8.png)

Check yo and coffee script installation using `yo` and `coffee` command
 
### Install Hubot

Run following command:

    mkdir hubot
    cd hubot
    yo hubot

Use suggested default values or edit accordingly 


![screen05](https://cloud.githubusercontent.com/assets/1732018/5625342/f05688e2-95b3-11e4-8b05-0216a7091abc.png)
![screen06](https://cloud.githubusercontent.com/assets/1732018/5625343/f217798e-95b3-11e4-90d0-903ee7c77b52.png)
![screen07](https://cloud.githubusercontent.com/assets/1732018/5625344/f4bef5ea-95b3-11e4-953a-6e2cda9ec935.png)

Edit `example.coffee` scripts for testing - uncomment some of the sample codes
![screen08](https://cloud.githubusercontent.com/assets/1732018/5625348/03b20d08-95b4-11e4-802b-e9a5e45b46a6.png)

Run hubot via command prompt `bin\hubot`
 
![screen09](https://cloud.githubusercontent.com/assets/1732018/5625350/0b78da12-95b4-11e4-9229-745682816880.png)

### Troubleshooting 

If you encounter ERROR Error: EINVAL. Read – delete `.hubot-history` file
http://codeimpossible.com/2015/01/01/EINVAL-read-when-running-Hubot-locally/
 
![screen10](https://cloud.githubusercontent.com/assets/1732018/5625356/19eb4a8a-95b4-11e4-87b8-9321b2f615e8.png)
![screen11](https://cloud.githubusercontent.com/assets/1732018/5625359/2c450ec8-95b4-11e4-95b3-d7e450b3d867.png)

Remove `"hubot-heroku-keepalive"` and `"hubot-redis-brain"` on `external-scripts.json` to remove Heroku Warning message and disable Redis if you don't have it installed
 
![screen12](https://cloud.githubusercontent.com/assets/1732018/5625354/14b25d4c-95b4-11e4-8b64-e6d98a146946.png)
![screen13](https://cloud.githubusercontent.com/assets/1732018/5625358/20f69104-95b4-11e4-80e9-5a4a01562fcc.png)

Enjoy!


