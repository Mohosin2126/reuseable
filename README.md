## Fetching and Setting Data using `useEffect` in React

In this example, we demonstrate how to fetch data from an API and set it in the component state using the `useEffect` hook in React.

```js
const [users, setUsers] = useState([]);

useEffect(() => {
    fetch("https://url")
        .then(res => res.json())
        .then(data => setUsers(data))
        .catch(error => console.error('Error fetching data:', error));
}, []);



