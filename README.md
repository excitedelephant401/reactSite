# Development

### Link to Deployed Website
If you used the stencil code, this is `https://<your GitHub username>.github.io/<name of your repository>`

### Goal and Value of the Application
The goal of this application is to display the catalog of a toy store. Specifically, the goal is to display this catalog in a digestible manner so users can navigate it and choose and buy items. The value this application has is that it allows users to easily search through a toy store's big catalog to find an item they need or want to purchase.

### Usability Principles Considered
The primary usability principles considered in this application come from the organization of it. I put the filters and sort at the top of the screen. This was to allow for easy navigation so users could have access to the different filtering options. This is an important functionality because users want to be able to easily narrow down the catalog to meet their interests. Additionally, the sort allows users to organize the catalog by price which is important for users in deciding what items to buy. Finally, the cart is also placed prominently on the website. This is because this is a major aspect of the goal as it allows users to consolidate what they want to buy it later. Furthermore, all of the information associated with a product were added to a section specifically designated for the product.

### Organization of Components
The three major components of the app are the App.js file, Item.js, and Aggregator.js. The App.js contains all of the state variables and information for the whole page. Within App.js, the data of the catalog is mapped to each be represented as an Item.js component. Finally, the Aggregator.js component stores the information associated with the cart on the website.

### How Data is Passed Down Through Components
Data is passed down through the props of the nested components. For the Item.js component, an entry from the data variable is passed to it. The data variable is a list from the catalog json file. Also, the functions for adding and removing an item from the cart. The Aggregator.js component takes in the cart and cost variables. The cart variable is a map between an item and its quantity in the cart that represents the cart's specific state. The cost variable is a number that represents the total price of the current cart.

### How the User Triggers State Changes
The state can change in one of two ways:

  1) If a user clicks a sort or filter: This will update the data variable which stores the list of catalog items. When a user clicks a filter choice, the data will only include items with that specific filter. When a user clicks a sort option, it rearranges the order of the items in the data variable. Based on the order and items in the data variable, it is then passed through to be displayed through the Item.js component.
  
  2) When a user adds or removes an item to the cart: By clicking a button on the item, it triggers the add cart or remove cart function. This will update the cart variable by changing the quantity (adding one or subtracting one for add and remove respectively) in the map between items and quantity. Additionally, it will update the cost variable by adding or subtracting the price. One exception for this is if an item doesn't have a quantity to begin with and it is removed, the state shouldn't update.
