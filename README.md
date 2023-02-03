# react-router-v6
This repository is created based on the 20th module of the course "React - The Complete Guide 2022" by Maximilian Schwarzmüller. The apps here are the same apps in projects: routing-react (https://github.com/IS-Projects/routing-react) and great-quotes-routing-react (https://github.com/IS-Projects/great-quotes-routing-react), but in this repository they use react-router version 6 instead of 5.

The changes in the projects reflect the following items that apply to version 6:

- Switch component is replaced by Routes component.
- Component is added as the value for the prop "element" inside Route.
- No need to use exact since React Router 6 already recognizes the best option for the link, which also means the order of the routes is no longer important.
- NavLink does not have activeClassName property, instead className accepts a function that can check if the element is active or not.
- Redirect component is replaced by Navigate component with the prop "replace" in it. If used without replace, the page is simply pushed.
- For nested routes, we need to wrap Route with Routes always. Also, the main path needs to include the "/*" to be able to reach to the nested element. And the nested element path now needs to be written as a relative path to the parent path.
- An alternative for nested routes is to put it in the main routes file, and then use the Outlet component to specifiy where we want the nested component to be in.
- useHistory hook is replaced by useNavigate hook. 
	- To push a website, we simply pass the path as an argument. Ex: navigate('/welcome')
	- To replace the website, we add the object {replace: true} as another argument. 	Ex: navigate('/welcome', {replace:true}) 
	- To go back or forward to pages we simply pass numbers as arguments. Ex: navigate(-2)
- As of Feb 19, 2022, Prompt component is not supported in this version.
