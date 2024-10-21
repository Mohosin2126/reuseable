## Fetching All and Setting Data using `useEffect` in React

In this example, we demonstrate how to fetch data from an API and set it in the component state using the `useEffect` hook in React.

```js
const [users, setUsers] = useState([]);

useEffect(() => {
    fetch("https://url")
        .then(res => res.json())
        .then(data => setUsers(data))
        .catch(error => console.error('Error fetching data:', error));
}, []);


```
## Fetching  Data using By Email
```js
const url = `http://localhost:5000/bookings?email=${user?.email}`;
```

## Fetching the data by ID using `useEffect` and `useParams` No 1

### On Button Click

```js

<Link to={`/Path Name/${_id}`}>

```
### In Route Page

```js

{
    path: "/Path Name/:id",
    element: <Elements Name>,
    loader: () => fetch("URL"),
}
 
```

### In the Page to Show Particular Element by ID

```js
const allStories = useLoaderData();
const { id } = useParams();
useEffect(() => {
    const findStories = allStories?.find((story) => story._id == id);
    setDetails(findStories || {});
}, [allStories, id]);

```
## Fetching the data by ID using `useEffect` and `useParams` No 2

### On Button Click

```js

<Link to={`/Path Name/${_id}`}>

```
### In Route Page

```js

{
  
    path: '/Path Name/:id',
     element: <Elements Name>,
    loader: ({params}) => fetch(`http://localhost:5000/${params.id}`)
}
```
### In the Page to Show Particular Element by ID

```js
const {name, category, recipe, price, _id} = useLoaderData();

```
## Fetching the data by ID using `useEffect` and `useParams` No 3

### On Button Click

```js

<Link to={`/Path Name/${_id}`}>

```
### In Route Page

```js

{
  
    path: '/Path Name/:id',
     element: <Elements Name>,
}
```
### In the Page to Show Particular Element by ID

```js
const {id} = useParams();

```






