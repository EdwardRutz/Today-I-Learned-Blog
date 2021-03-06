# Webpack Dev Server

1-16-18, Edward Rutz

#### Today I learned webpack-dev-server is finicky but worth it...

#### Score:  Webpack-dev-server: 2, Junior Dev: 1.
#### Update, 1-17-18, Final Score: Webpack-dev-server: 2, Junior Dev: 3.

The Webpack-Dev-Server provides a fast way to develop apps along with live-updating changes to a webpack bundle. No more stopping the server, rebuilding and restarting with hot reloading. It is a useful in development but using it in production is not recommended.

So far using webpack-dev-server is finicky. On the bright side, my ability to configure webpack, webpack.config.js, package.json files and troubleshoot is growing stronger. 

One benefit of webpack-dev-server is the ability to live-update the bundle.js file with the changes made to the index.js file.  This is much easier than remaking the bundle.js after each change.

Each installation of the webpack-dev-server led to a different result...the webserver hanging, errors with Content Security Policy (CSP) and failing to update.  This is more likely a reflection of my lack of experience with it but it still burns time I'd rather spend coding.

For now I have spent enough time fiddling with it and will use another web server and the Watch command to update bundle.js. Or even do it manually with each change. It is more important to keep coding without interruptions.  Will give it another try later.

#### Steps to adding the watch command and for dealing with CSP issues.

##### Add a Watch command to automate building bundle.js
- In package.json add ```"watch": "webpack --w"``` to the scripts object...
- RESULT: 
```
       "scripts": {
          "build": "webpack",
          "watch": "webpack --w"
        },
```
- Next run ```npm run watch``` to monitor changes
- RESULT:
```
Webpack is watching the files…
```

##### Solving Content Security Policy Issues
- [MDN: Content Security Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy/default-src)
- [SO: CSP](https://stackoverflow.com/questions/42401952/inline-style-error-with-content-security-policy-and-javascript#42402277)

#### UPDATE
- Webpack is pretty cool when you get it working!
- Now for the fun, building React apps


#### TL;DR

- The web-dev-server is a powerful tool that may take time to learn and configure correctly.
- Spend more time coding and less time wrestling configurations to get a tool to work.
- It is super convenient once you get it working.



------------------------------------

## REFERENCES
- [Linkedin Learning: Learning Webpack 3](https://www.linkedin.com/learning/learning-webpack-3/welcome)
- [Github: Webpack-Dev-Server](https://github.com/webpack/webpack-dev-server)
- [Webpack.js.org](https://webpack.js.org/configuration/dev-server/)
- [Webpack-Dev-Sever Docs](https://github.com/webpack/docs/wiki/webpack-dev-server)
- [Webpack Book: Webpack-Dev-Server](https://survivejs.com/webpack/developing/webpack-dev-server/)
- [Webpack Wiki: webpack-dev-server](https://github.com/webpack/docs/wiki/webpack-dev-server)
- [Hot Reloading with Webpack](https://shellmonger.com/2016/02/02/automatic-builds-with-webpack/)
- [Setting up React ES6 with Webpack and live reloading](https://www.bravedigital.com/setting-react-es6-webpack-live-reloading/)








