# futch
`fetch`, but only for RESTful APIs serving JSON.

## API
```
const url = 'https://jsonplaceholder.typicode.com/todos';

// GET
futch.get(url).then(json => console.log(json));

// POST, because there is no id
futch.save(url, {body: {title: 'Foo', body: 'Bar'}}).then(json => console.log(json));

// PUT, because there is an id 
futch.save(url, {body: {userId: 1, title: 'Foo', body: 'Baz'}, idAttribute: 'userId'}).then(json => console.log(json));

// DELETE
futch.delete(url).then(json => console.log(json));
```
