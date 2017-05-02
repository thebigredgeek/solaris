Motivation

One of the most immediate challenges faced by any dev team switching to GraphQL is project boilerplate. With any non-trivial project, there exists a certain need for strong code organization lest the project becomes difficult to reason about. Since most full-stack / backend developers are used to building out RESTful APIs, decisions regarding project structure are trivially stressful and don't detract developers from continuing to build RESTful APIs.

With GraphQL, most developers are entering the ecosystem for the first time. There are new terms, new patterns, and new paradigms to learn that can, by themselves, be overwhelming to the point of causing many developers to simply give up and go back to REST. Add to this the need to figure out how to structure the backend project properly, add things like realtime, and decide how to connect GraphQL to the data layer, and you are quite literally placing a stone, rather than a straw, on the metaphorical camel's back.

The goal of GraphQL tools / GraphQL server is to provide an easier way to get started building GraphQL backends as opposed to the vanilla graphql-js lib. However, I believe that at least 80% of use cases could be satisfied by something slightly more opinionated and that requires a LOT less configuration and imperative boilerplate. I do NOT think that GraphQL Server or GraphQL tools should be replaced. There is a big need for a mid-level implementation that draws fewer opinions and is more flexible. However, I think there is a huge NEED for an additional server-side library that provides higher-level abstraction atop GraphQL Server.

Proposed Solution

Enter Solaris. I think a GraphQL framework with an incredibly simple API like this would push most NodeJS developers who are still on the fence about GraphQL into giving it a try with at least a few hobby projects. It significantly reduces the barrier to entry. The developer only has to think about how they want to respond to queries and mutations, and whether or not the data returned from the handlers should be published to any defined subscriptions. There is no need to figure out what NodeJS HTTP server implementation to use, how to wire up tests, how to build, or how to lay out the file structure. At the same time, very few compromises are made about flexibility and the model can theoretically scale very well into distributed large scale systems (microservices).

Implementation / Next steps

Before moving on, we need to nail down a spec for the exact API that we would like to build. What is already defined in the gist above is totally buildable and should scale well, but I think it's important to get the community involved in reviewing the API and no-doubt making changes to it that would make it even more approachable and hopefully with even less of a flexibility tradeoff. Therefore, I propose the following steps:

Thoroughly define the thesis and scope of the project
Create a robust API design doc along with code examples and use cases
Implement a prototype and build a few small projects in it to test the concept
Iterate and release an alpha version
