#GraphQL
GraphQL was developed by facebook and publicly announce in 2015.

- Schema Definition Language (SDL) for back-end API and client side should be on same page.
- Real time data update with subscriptions. A connection is establish between the client and sever so that if there is any change in data it will pushes directly to client without any delay.

Example

```
type Person {
    name: String!
    age: Int!
    posts: [Posts!]!

}

type Post {
    title: String!
    author: Person!
}
```

## Writing Data with Mutations

There are mainly three type of mutations and they always start with **mutation** keyword.

- Creating new data
- Updating existing data
- Deleting existing data

Example

```
mutation {
    createPerson(name: "test", age: 33){
        name
        age
    }
}

**Output**
 {
     "createPerson":{
         "name": "test",
         "age": 36,
     }
 }
```
