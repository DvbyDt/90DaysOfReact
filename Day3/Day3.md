# React-Scripts

<strong> Day3: 18th July 2022 <br /><br /> </strong>
<em> On this day I learnt about the folder structre that npx create-react-app created. What lies in package.json file in your react app. </em>

<li> The package.json file contains all the information about the packages and the versions that your project is using.
<li> We will be first looking at the scripts in the package.json file: <br /><br/>
   <img src="https://user-images.githubusercontent.com/68496657/181208005-f86945a1-d692-4a02-adfb-148360e18c40.png" alt="Read-Scripts" /> <br/>
 <li> Read scripts were developed to better build our application and to test it.
  <li> If you write "npm start" in your command line, the start in npm start takes all your code and pushes it throught localhost to render. Once you have written npm start the output in localhost for the very first time will look like this: <br/>
  <img src="https://user-images.githubusercontent.com/68496657/181209347-af4cad71-04ed-4f0e-bed1-d272c03ca069.png" alt="First Time Render" /> 
  <li> If you write in the command line: npm run build it will make a production build for your application and this will create a folder in your directory called as build. <br />
  <img src="https://user-images.githubusercontent.com/68496657/181210856-9e62214f-405c-4378-9b79-e1a716806f49.png" alt="Build in Directory" />
  <li>Now coming to starting point of our React app it's: Index.js.
    <li> In index.js if you see there the first two import statements importing from react and react DOM. <br />
      <img src="https://user-images.githubusercontent.com/68496657/181302769-51de2136-efb8-4ddf-8249-44ad7149e77e.png" alt="Index.js" /> <br/>
  <li> 'react' specifies that it's an underlying engine and Dom is used for website development.<br/>
   
<strong>Day 4: 19th July 2022</strong>
   <li> On building your react app for the first time you get the build folders we discussed above. <br />
   <img src="https://user-images.githubusercontent.com/68496657/181210856-9e62214f-405c-4378-9b79-e1a716806f49.png" alt="Build in Directory" />
   <li> So, just to briefly explain the build folder: 
      <ol>
         <li> <strong>manifest.json: </strong> It makes the react app progressive web application compliant. It contains the icons(favicon and both the logo files). This is used to access this application offline as a deskstop application.
          <li> The npm run build command just optimises the files in the build folder.
           <li> It optimises the usign: WebPack and Babel.
           <li> WebPack: It just divides the files in the static directory into smaller and most optimised chunks.
           <li> Babel: It is used for optimizing the Javascript code. It has a reduced format. Optimial and fastest version for browser to consume.
         <li> <strong>robots.txt: </strong> It is used for SEO optimisation. This is used to rank your website on Search engines.
          <li> <strong> Note: Don't eject: engineers at fb are working full time to make create react app as cool and as optimized as possible so, it's normally advised that you don't do eject in react.</strong>
       


