This was an experiement to get a more detailed understanding of what webpack is accomplishing for developers and why babel is required to translate and load different types of files before webpack compiles and minifies the resulting bundle.



Shout out to this dev.to article for a detailed walkthrough of the setup and some lessons learned.
https://dev.to/deadwing7x/setup-a-react-app-with-webpack-and-babel-4o3k
by Anubhav Sarkar

Major notes and takeaways:
    Installed the path package as a devDependency since we need to work with paths in our app. We wouldn't want to inject the index.js file inside the HTML file. Go ahead and install the html-webpack-plugin to help us do that automatically.
    * npm install path html-webpack-plugin --save-dev

    * why Babel? 
    * * if we were to add React code inside our JS file, Webpack will give us an error. It doesn’t know how to compile React inside the bundle.js file.
    * * webpack error for not having **appropriate loaders for react**