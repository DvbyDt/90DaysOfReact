# Class Components 

<strong>Day5:20th July 2022</strong>

<em>The learnings on this day were about the Class components. Along with starting building a monster rolodex project. </em>

<li> Class components are extended from the component in the react library.
<li> So, these are basically classes containing a render() which returns a JSX code inside it and in that JSX code we specify what we want to be rendered.
<li> A better developer in React is one who knows when rendering and re-rendering occurs in the React. In React 18 Strict Mode for better debugging they've started 
    doing a double invocation for certain things in a components lifecycle! If you see renders twice, this will be why!!
<li> State of a component is an object that denotes it's value which can change during the lifetime of the component. Here is an example App component with name state: <br />
  
  ```jsx 
  class App extends Component{
    constructor(){
      super();
      this.state = {
        name:'Dhruv Vashist'
        };
      } 
    render(){
    return(
     <div>
       <h1>{this.state.name}</h1>
    </div>  
    ); 
    }
  }
```

  
<li> You might think considering the above example that changing values in react can be done easily(if you consider the above example) by:
  
```jsx
   <button onClick = {() => {
     this.state.name = "Manish";
     }
    }
    >
  ```

  thinking that this will change the name state to Manish instead of Dhruv.
   <li> React will re-render a component only when we have a completely different state. It will shallow merge to the current state and give me a new state. 
     Unless you are passing the state to be changed it won't change the value. To actually change the value you have to make use of the setState() :

 
```jsx
     <button onClick = {() => {
        this.setstate(() => {
           name: "Manish"
         }
        );
       }                
      }
     >
  ```
     
     
   <li>	ShallowMerge: It won't care if there are different values it will just merge if it matches the key.So, for shallow merge keep in mind that you have to 
     use the exact same values that are being used in the state or at the time of declaring.     
   <li> setState and Secondary Callback: Consider the below example.
     
   ```jsx
        
     	<button onclick={() => 
	        this.setState ({
              name : 'Manish' ;
          });
          console.log(this.state); // Answer is still the previous value i.e. Dhruv 
          // This will have previous value because react may or may not update this value as it works in batches and 
           //sees which will be the optimal point to update the this.setState value.
        } 
      >
     
   ```
     
  <li> To counter or solve the above issue just make use of the callback functions.
   
  ```jsx
    
    <button onclick = {() => {
          this.setState(
         () => {
            return {
               name: "Manish"
            };
          },
         () => {
            console.log(this.state);//Now it will show the latest value(Manish) and not the older one.
          }
        );
      }}   
      //Here we are passing a function and a secondary callback to the this.setState();
      //It's in the form this.setState(() => {}, () => {});
    
  ```


      
