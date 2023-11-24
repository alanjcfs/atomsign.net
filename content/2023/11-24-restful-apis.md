# RESTful

I was reading [Phoenix/Routing](https://hexdocs.pm/phoenix/routing.html) documentation when I came across this
statement:

> This is the standard matrix of HTTP verbs, paths, and controller actions. For a while, this was known as RESTful
> routes, but most consider this a misnomer nowadays.

This led me to the [orange site](https://news.ycombinator.com/item?id=32141027) wherein I now have sufficient experience
to understand what REST means and why JSON APIs aren't considered REST. Whether this knowledge is practical remains to
be seen; I do think it makes me a better software engineer, even though I have no horse in this race.

In summary, [an HTML response](https://htmx.org/essays/how-did-rest-come-to-mean-the-opposite-of-rest/#an-html-response)
is considered RESTful because links and forms contain within it all the possible actions that can be taken by a user.
[A JSON response](https://htmx.org/essays/how-did-rest-come-to-mean-the-opposite-of-rest/#a-json-response), however,
usually contains only data, and it means that a front-end developer working with a JSON API must know beforehand which
endpoints to use to take actions.

As an application grows in complexity, and its endpoints consumed by other applications, we may become dissatisfied by
how we need to look up API documentation to know what is possible to do, because a JSON response usually contains no
information regarding "hypermedia controls" or other metadata. An HTML document of a banking page showing your current
balance may may contain links to withdraw, deposit, transfer money, but a JSON document likely only shows your current
balance. How do you know which URL to use to withdraw, deposit, or transfer money without looking at the
documentation?

It helped me understand why [json-api](https://jsonapi.org/) was created. Although I understood the goal of the
specification was to standardize JSON responses, I hadn't realized the history behind it. XML, which looks like HTML,
already contained hypermedia information, but JSON took off quickly because it was simple and not verbose.
