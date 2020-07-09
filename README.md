# microfrontend-example.github.io
Sample micro front end application that has angular component and plain javascript

The idea behind Micro Frontends is to think about a website or web app as a composition of features which are owned by independent teams. 
Each team has a distinct area of business or mission it cares about and specialises in. 
A team is cross functional and develops its features end-to-end, from database to user interface.

Core Ideas behind Micro Frontends
1. Be Technology Agnostic
    Each team should be able to choose and upgrade their stack without having to coordinate with other teams. Custom Elements are a great way to hide implementation details while providing a neutral interface to others.
2. Isolate Team Code
    Don’t share a runtime, even if all teams use the same framework. Build independent apps that are self contained. Don’t rely on shared state or global variables.
3. Establish Team Prefixes
    Agree on naming conventions where isolation is not possible yet. Namespace CSS, Events, Local Storage and Cookies to avoid collisions and clarify ownership.
4. Favor Native Browser Features over Custom APIs
    Use Browser Events for communication instead of building a global PubSub system. If you really have to build a cross team API, try keeping it as simple as possible.
5. Build a Resilient Site
    Your feature should be useful, even if JavaScript failed or hasn’t executed yet. Use Universal Rendering and Progressive Enhancement to improve perceived performance.

Consider below website: 
https://nnsantosh.github.io/microfrontend-example.github.io/

It has two main components: Product Search and other one is Shopping Cart

The Product Search component is built using angular elements.
Code: https://github.com/nnsantosh/product-search-element

The Shopping Cart component is plain JavaScript

Exchange of data between angular element and non angular element is happening through the use of DOM eventlistener in this case.

When user selects products and adds to Cart from the Product Search component, the product details are displayed in the Shopping Cart component.

For now the use the below two product names for searching: iphone and blackberry.

For demo purpose the service has hardcoded data for these two products only.

More details on developing angular element can be found here: https://blog.bitsrc.io/using-angular-elements-why-and-how-part-1-35f7fd4f0457



