## Namaste Food


## What is a Microservice?
  
   A microservice is a software architectural style that structures an application as a collection of loosely coupled, independently deployable services. Each service is designed to perform a specific business function and can be developed, deployed, and maintained separately from other services.

   Microservices are often used in large, complex applications to improve scalability, maintainability, and flexibility. By breaking down the application into smaller, more manageable services, developers can more easily add new features, fix bugs, and scale the application as needed.

   Microservices communicate with each other through well-defined APIs, often using lightweight protocols such as HTTP or messaging systems like RabbitMQ or Kafka. This allows each service to be developed and deployed independently, without having to worry about the implementation details of other services.
  


## What is Monolith architecture?

  
   Monolithic architecture is a traditional software development approach where all the components of an application are combined into a single program, typically a single codebase, and deployed as a single unit. In this architecture, the entire application is built, tested, deployed, and scaled as a single entity.
   
 In a monolithic architecture:
    Tightly Coupled Components:
            All the components of the application are tightly coupled, meaning that changes to one component can have a ripple effect on other components, making it difficult to make changes or add new features.

    Single Deployment Unit: 
           The entire application is deployed as a single unit, which can make it difficult to scale or update the application without affecting the entire system.

    Single Technology Stack: 
          Since all the components of the application are tightly coupled, they often use the same technology stack, which can limit the flexibility and scalability of the application.

    Scalability Challenges:
          Scaling a monolithic application can be challenging, as the entire application must be scaled together, which can lead to wasted resources.

    Development and Deployment Challenges: 
          Since the entire application is built, tested, and deployed as a single unit, it can be difficult to make changes or add new features without affecting the entire system.



## Why do we need a useEffect Hook?

   
    The useEffect hook in React is used to perform side effects in functional components. Side effects are actions that occur outside the scope of the component, such as fetching data from an API, subscribing to events, or updating the DOM.

     Here are some reasons why we need the useEffect hook:

        Fetching Data:
            When you fetch data from an API, you typically want to do this only once when the component mounts. The useEffect hook allows you to do this by using an empty dependency array ([]) as the second argument, which tells React to only run the effect once when the component mounts.

        Subscribing to Events:
            If you need to subscribe to events, such as keyboard events or scroll events, you can use the useEffect hook to do this. You can then return a cleanup function from the effect, which will be called when the component unmounts to unsubscribe from the event.

        Updating the DOM:
            If you need to update the DOM, such as adding or removing classes or manipulating the DOM directly, you can use the useEffect hook to do this. You can then return a cleanup function from the effect, which will be called when the component unmounts to clean up any changes made to the DOM.

        Managing State:
            If you need to update the state based on some condition, you can use the useEffect hook to do this. You can then return a cleanup function from the effect, which will be called when the component unmounts to clean up any changes made to the state.



## What is Optional Chaining?
   
    
  Optional chaining is a feature introduced in JavaScript ES2020 (also known as ECMAScript 2020) that allows you to access properties of an object or elements of an array without having to explicitly check if each property or element exists. It is represented by the question mark (?) and the dot (.) operators combined as ?..

      const arr = [1, 2, 3];
      console.log(arr?.[0]); // 1
      console.log(arr?.[3]); // undefined
   
  Optional chaining is particularly useful when working with APIs that may return deeply nested objects or arrays, as it allows you to access properties and elements without having to check each level of the object or array.



## What is Shimmer UI?
    Shimmer UI is a design pattern used in user interfaces to indicate that content is loading or that an action is in progress. It involves displaying a subtle, animated shimmer effect over the area where the content will appear. This effect typically consists of a series of light and dark lines that move horizontally or vertically, giving the impression of movement and activity.

    The shimmer effect is often used in situations where loading times may be longer than usual, such as when fetching data from a server or when performing a complex operation. By displaying the shimmer effect, users are given visual feedback that something is happening, which can help reduce frustration and improve the overall user experience.

    Shimmer UI is commonly used in mobile applications, especially those with a feed or list-based interface, as it helps to maintain the visual hierarchy of the page while content is loading. It can also be used in web applications, although it is less common due to the faster loading times of most web pages.

   in short:
    Shimmer UI is a simple yet effective way to indicate that content is loading or that an action is in progress, and it can help to improve the user experience in applications with longer loading times.




## What is the difference between JS expression and JS statement
   
    Expression:
        Resolves to a value and can be used as part of a statement.
   Statement: 
       Performs an action and does not inherently resolve to a value.



## What is Conditional Rendering, explain with a code example

  Rendering the Component based on the condition is called conditional Rendering...
      if(ListOfRestaurantslength===0)
          {
             return <Shimmer/>
          }

## What is CORS?

   CORS stands for Cross-Origin Resource Sharing. It's a security feature implemented by web browsers to restrict cross-origin HTTP requests initiated from scripts running on a webpage.

    In simpler terms, CORS is a security mechanism that allows a web server to specify who can access its resources (such as files, APIs, etc.) from other domains. This is important because, without CORS, a malicious website could use a script to make requests to a different website that the user is logged into, potentially accessing sensitive information.

   CORS works by adding HTTP headers to the responses from the server, which indicate whether a request from a different origin (domain, protocol, or port) should be allowed. These headers include:

    Access-Control-Allow-Origin:
        This header specifies which origins are allowed to access the resource. For example, if the header is set to "*", any origin can access the resource. If it's set to a specific origin, only that origin can access the resource.

    Access-Control-Allow-Methods:
        This header specifies which HTTP methods (such as GET, POST, PUT, DELETE, etc.) are allowed when accessing the resource.

    Access-Control-Allow-Headers: 
        This header specifies which headers are allowed when making a request to the resource.

    Access-Control-Allow-Credentials: This header specifies whether the resource supports credentials (such as cookies or HTTP authentication) when making a request.

    Access-Control-Max-Age: 
      This header specifies how long the results of a preflight request (a request that checks whether a request is safe to send) can be cached.

      CORS is an important security feature that helps protect against cross-origin attacks, but it can also be a source of frustration for developers who are trying to access resources from different domains.



## What is async and await?

   async and await are two keywords in JavaScript that are used to work with asynchronous code. They were introduced in ECMAScript 2017 (ES8) and are part of the Promise API.

   async: 
        The async keyword is used to define a function that returns a promise. When you mark a function as async, it means that the function will always return a promise, even if it doesn't explicitly do so. Inside an async function, you can use the await keyword to pause the execution of the function until a promise is resolved or rejected.

  await: 
        The await keyword can only be used inside an async function. It is used to pause the execution of the function until a promise is resolved or rejected. When you use await with a promise, the function will pause until the promise is resolved, and the value of the promise will be returned. If the promise is rejected, the function will throw an error.

              async function fetchData() {
                const response = await fetch('https://api.example.com/data');
                const data = await response.json();
                return data;
         }
          fetchData().then(data => {
            console.log(data);
          }).catch(error => {
            console.error(error);
          });

       In this example, the fetchData function is marked as async, which means it returns a promise. Inside the function, we use the await keyword to pause the execution of the function until the fetch request is resolved. Once the request is resolved, we use await again to pause the execution of the function until the response is converted to JSON. Finally, we return the data, which is then logged to the console when the promise is resolved.
   
       It's important to note that async and await are syntactic sugar for working with promises. Under the hood, an async function still returns a promise, and await is just a way to pause the execution of the function until a promise is resolved or rejected.



