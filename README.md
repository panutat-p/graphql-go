# graphql-go

Documentation\
https://graphql.org/learn

GraphQL for Go\
https://github.com/graphql-go/graphql

Go generate based graphql server library\
https://github.com/99designs/gqlgen

## Opinions

https://www.reddit.com/r/programming/comments/ujtvt4/graphql_is_a_trap

> A real life example, we have a data heavy application (think a big ass excel spreadsheet) that needs to work on a computer as well as a phone.
> Users tend to use their computers to do deep analysis on the data, but they use their phones more as a reference to just a few data points.
> On a computer, we have tons of extra screen space, a strong internet connection, and users want to see as much as possible,
> so we load everything in a single call and show it all to the user. On mobile, we have much less screenspace, users usually only care about a few data points, and we want to optimize for speed and payload size.
> 
> GraphQL allows us to do this with a single end point vs multiple end points or a single endpoint with a bunch of query parameters (which is basically just graphQL).
> Maintaining two separate endpoints wouldn't be the end of the world, but if we decided we wanted to all the data on mobile,
> but spread over 5 pages without loading unneeded data, the problem gets worst for REST.
> The GraphQL endpoint can do that without needing any changes, but we'd need to build additional REST endpoints.
>
> That leads me into the other big advantage for us, it allows our client teams to change their use cases without needing API changes.
> If we learn mobile users are starting to focus on a different subset of the data or we need to move a data point from page 5 to page 2,
> the client can just change what they request instead of needing the API to be changed.
>
> They're different tools and you should use the one that fits your needs best. GraphQL allows you to trade some simplicity for flexibility.
> If your API and your client are tightly coupled, you probably don't need the flexibility GraphQL can provide.
> If you want to provide a more generic way for clients to access data or are trying to support conflicting use cases, then GraphQL could be an option to do that.

https://www.reddit.com/r/webdev/comments/1509p4m/im_not_impressed_by_graphql_and_i_still_prefer

> Graphql has specific pros and cons while rest has other pros and cons. I don’t see them as direct replacements
> The simple fact you added something on the backend and will be adding something on the frontend yourself, tells me that’s not a good use case for graphql.
> Graphql is amazing when you have backend and frontend teams. The FE doesn’t need to talk to the BE guys or do special documentation with graphql.
> If it’s the same person doing both, for me it makes zero sense to use graphql.
> Either way your specific criticism is a bit weird.
> If you add a new property and you want to actually use it, you need to have code on your UI showing or manipulating it.
> Also including it on the query doesn’t seem like much more work…
> If you have a query with thousands of lines you have bigger architectural problems than graphql.
