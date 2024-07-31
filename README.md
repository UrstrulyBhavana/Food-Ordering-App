# Food-Ordering-App Config Driven UI

 API endpoint for Swiggy 
https://www.swiggy.com/dapi/restaurants/list/v5/?lat=12.9351929&lng=77.62448069999999&page_type=DESKTOP_WEB_LISTING
[ This URL contains a large dataset in JSON format, which includes detailed information about restaurants in the specific location.
This data includes restaurant names , locations , ratings , delivery times , cuisine types , and other details ]

import React from "react";
import ReactDOM from "react-dom/client";

React and ReactDOM libraries are being imported. React is used to create components, and ReactDOM is used to render these components in the browser.

Header Component :-  The Header component is a functional component that returns a JSX structure for the header of the page. It contains a logo image and a navigation menu.

RestaurantCard Component :- The RestaurantCard component is another functional component which takes restaurant data as a prop and displays it. It Extracts relevant details (image ID, name,
cuisines , delivery time , cost for TWO) from resData and returns a JSX structure displaying this information. The image URL is constructed by concatenating the base URL with "ClodinaryImageID".

resList :- resList is an array of objects where each object contains information about a restaurant, such as its name, image, cuisines, delivery time, and cost for two. This data is used to populate multiple RestaurantCard components.
code initializes a React root and renders a Header component followed by a list of RestaurantCard components. The resList array is mapped to generate a RestaurantCard for each restaurant, passing the respective data as props.

AppLayout Component :-  The App component is the root component that serves as the main container for other components. It renders the Header and a list of RestaurantCard components.
ReactDOM.createRoot:- This function is used to render our root component (App) into the DOM. It attaches React's virtual DOM to the actual DOM.
Mounting: ReactDOM.createRoot(document.getElementById('root')).render(<App />) mounts the App component into the element with id="root", which is where our React app will appear on the page.
The App component serves as the main component that organizes and displays the Header and a list of RestaurantCard components. The RestaurantCard component is used to render details for each restaurant dynamically based on the data provided.
