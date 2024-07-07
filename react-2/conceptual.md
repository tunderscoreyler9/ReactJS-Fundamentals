### Conceptual Exercise

Answer the following questions below:

- What is the purpose of the React Router?
React Router helps manage navigation within single-page applications (SPAs). It allows you to update the URL and display the corresponding component without requiring a full page reload. This creates a seamless user experience

- What is a single page application?
SPAs are web applications that load a single HTML page initially and dynamically render subsequent content based on user interaction. This avoids the need for full page reloads, resulting in a faster and more fluid user experience

- What are some differences between client side and server side routing?
  - Client-Side Routing: Routing happens entirely within the browser using JavaScript (e.g., React Router). This improves performance as the client doesn't need to request a new page from the server for each URL change.
  - Server-Side Routing: Routing is handled by the server (e.g., Node.js with Express). The server delivers the appropriate HTML page based on the requested URL. This approach offers better SEO (Search Engine Optimization) as search engines can easily crawl the initial HTML page

- What are two ways of handling redirects with React Router? When would you use each?
React Router offers two ways to handle redirects:

  - Using Redirect Component: This explicit approach directs users to a different URL using the Redirect component. It's suitable for situations where you want a clear separation of logic for handling redirects.
  - Using exact Path Matching: Omitting exact in path matching allows for partial matches, potentially leading to unintended redirects. Use this cautiously or with additional logic to ensure the desired behavior

- What are two different ways to handle page-not-found user experiences using React Router?
React Router offers two approaches to handle situations where a user requests a non-existent route (404 error):

  - Using a Catch-All Route: Define a route with a path pattern that matches any URL (e.g., *). This route component will render whenever a user navigates to a path that doesn't have a specific route defined. You can use this component to display a custom "Page Not Found" message or redirect the user to a default page.
  - Using Error Boundaries: Error boundaries are a mechanism introduced in React 16. React will catch errors that occur within a component tree wrapped by an error boundary component. You can then define a fallback UI within the error boundary that displays a user-friendly message in case of errors, potentially including a "Page Not Found" message for unmatched routes.


- How do you grab URL parameters from within a component using React Router?
The useParams hook provided by React Router allows you to access dynamic segments of the URL within a component. These segments are defined as named parameters within route paths using a colon (:paramName).
```
import { useParams } from "react-router-dom";

function MyComponent() {
  const { paramName } = useParams();  // Replace 'paramName' with your actual parameter name

  // Access the parameter value
  return (
    <div>
      You requested the parameter: {paramName}
    </div>
  );
}
```


- What is context in React? When would you use it?
Context is a feature in React that enables you to share data across components in a React application without explicitly passing props down through every level of the component hierarchy. This is particularly useful for global state or data that needs to be accessed by deeply nested components within your application

- Describe some differences between class-based components and function
  components in React.
React offers two fundamental ways to define components: Class-based components and Functional components. Here's a breakdown of their key differences:

Class-Based Components:

Defined using the class keyword and extend the React.Component class.
Utilize lifecycle methods (e.g., componentDidMount, componentWillUnmount) to manage component behavior during different stages of its lifecycle.
Can manage internal state using this.state.

- What are some of the problems that hooks were designed to solve?
Prior to hooks, managing component behavior and state within React functional components was challenging. Hooks were introduced to address these limitations by providing a way to:

  - Share State Logic: Hooks like useState allow you to manage state within functional components without relying on class properties.
  - Extract Component Logic: Hooks like useEffect enable you to perform side effects (e.g., data fetching, subscriptions) within functional components, similar to class-based lifecycle methods.
  - Improve Code Reusability: Hooks promote code reuse by allowing you to create custom hooks that encapsulate common logic and can be shared across components.
  - Simplify Functional Components: Hooks provide a more concise and functional approach to managing component behavior, making functional components a more viable alternative to class-based components in many scenarios