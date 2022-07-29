# Mapping Arrays to Elements & SPAs

<strong>Day-6: 21st July 2022</strong>

<em> The learnings were mostly about learning to use the Arrays.map() and applying the same knowledge to get started in the monster rolodex project. </em>

<li> <strong>Map() :</strong> It maps over the elements and creates a new array.
  Whenever you use array.map() always use a key as it becomes easier for react to optimize and render it in a better way.
  Key is always added to the highest level of the element. Suppose your h1 is enclosed in a div.
  Key value helps react to optimise at the time of rendering or re-rendering. Devtools won't see key values.
 <li> Let's suppose we have a monsters array which has different monsters in it like:
   
 ```jsx
   
   class App extends Component {
   constructor(){
   super();
   this.state = {
   monsters:[
       {
          name:"Dhruv",
          id:"1234"
       },
       {
          name:"Patta",
          id:"4567"
       },
       {
          name:"Chaubey" ,
          id:"8910"
       }   
      ]   
     };
   }
   
     render(){
        return(
          <div classname="App">
             {
                this.state.monsters.map((monster) => 
                {
                  <h1 key={monster.id}>{monster.name}</h1>;
                }       
              );            
             }  
          </div>   
        );   
      }
   }
   
   
 ```
  
 <li><strong> SPAs and Non-SPAs:</strong> Let's take an example of a non-single page application.Suppose it's making request to a particular url to the server.
   The server will return the response and in that response it will have the .html,.css and .js files.<br />   
   Now the same page makes request to another url again the request will go to the server and it will return the response in that response we will have the HTML,CSS 
   and JS files which will be again used to render the site. Now, this is a lot of work as you can see in the below diagram. <br />
   <img src="https://user-images.githubusercontent.com/68496657/181816774-185049d7-4392-4748-a21a-04ece899b8db.png" alt="Non-SPA" />
"
   
   Now consider the example of <strong>SPA(single page applications)</strong> in that if the user wants to access a particular site so, for the very first time it will make a request 
   to the server. The server will return the response with the three files(HTML,CSS and JS) but now with the JS code it's also returning the react code as well to build 
   the  website. <br/>   
   But now say if the user wants to access a different page within the same website since, the react code is already there we don't need to make a request to the server.
   The HTML and CSS will be generated from the react side itself. I have attached an image just to explain the same.<br />
   <img src="https://user-images.githubusercontent.com/68496657/181817088-661b5cf7-9eec-45bf-b491-677c4748c299.png" alt="SPA" />
   
 
