Sources:

\
What is a [[URI]] and why does it matter:

# What's a URI and why does it matter?

[Henry S. Thompson](http://www.ltg.ed.ac.uk/~ht/)

[School of Informatics](http://www.inf.ed.ac.uk/), University of Edinburgh

[Markup Systems](http://www.markup.co.uk/)

26 August 2010

## 1. Introduction

URI stands for Uniform Resource Identifier, and it's the official name for those things you see all the time on the Web that begin '`http:`' or '`mailto:`', for example `http://www.w3.org/`, which is the URI for the home page of the World Wide Web consortium. (These things were called URLs, for Uniform Resource Locators, in the early days of the Web, and the change from URL to URI is either hugely significant or completely irrelevant, depending on who's talking—I won't have anything to say about this issue here. If you've never heard of URIs (or IRIs, the even more recent fully internationalized version), but are familiar with URLs, just think 'URL' whenever you see 'URI' below.)

Historically, URIs were mostly seen as simply the way you accessed web pages. These pages were hand-authored, relatively stable and simply shipped out on demand. More and more often that is not the case: in at least three different ways:

-   Web pages for reading have been complemented by pictures for viewing, videos for watching and music for listening;
-   The Web is now more than a conduit for information, it's a means to a variety of ends: we use it to _do_ things: purchase goods and services, contribute to forums, play games;
-   The things we access on the Web are often not hand-authored or stable, but are automatically synthesized from 'deeper' data sources on demand. Furthermore, that synthesis is increasingly influenced by aspects of the way we initiate the access.

It's against this background that I think it's worth exploring with some care what URIs were meant to be, and how they are being used in practice. In particular, I want to look at what illumination might be contributed from our understanding of how other kinds of identifiers work.

## 2. The official version

Insofar as there are definitive documents about all this, they all agree that URIs are, as the third initial says, **identifiers**, that is, names. They identify **resources**, and often (although not always) allow you to access **representations** of those resources. (Words in **bold** are used as technical terms—their ordinary language meaning is in many cases likely to be more confusing than helpful.)

'Resource' names a role in a story, not an intrinsically distinguishable subset of things, just as 'referent' does in ordinary language. Things are resources because someone created a URI to identify them, not because they have some particular properties in and of themselves.

'Representation' names a pair: a character sequence and a **media type**. The media type specifies how the character string should be interpreted. For example JPG or HTML or MP3 would be likely media types for representations of an image of an apple, a news report about an orchard or a recording of a Beatles song, respectively.

The relationship of these three concepts (URI, resource, representation) per the official version is illustrated in this diagram:

![Illustration of URI-Resource-Representationstory for the Oaxaca weather report, taken from WebArch](https://www.cogsci.ed.ac.uk/~ht/WhatAreURIs/urr.png)

Figure 1. The URI-resource-representation story, from [Jacobs and Walsh, eds. 2005, _The Architecture of the World Wide Web_](http://www.w3.org/TR/webarch/)

This can't be the whole story, since nothing in Figure 1 above looks anything like a weather report. What Web users experience in practice involves a further relationship, between a representation and what we might call a **presentation**:

![Illustration of Representation-Presentation
story for the Oaxaca weather report](https://www.cogsci.ed.ac.uk/~ht/WhatAreURIs/present.png)

Figure 2. The representation-presentation story

There is important potential for variation in two aspects of the pictures above:

-   Different representations may be available for the same resource, in at least four ways:
    1.  Different technologies, manifested as different media types, for example GIF or JPG or PNG for an image, PDF or HTML or XHTML or TXT for structured text;
    2.  Different intended presentation platforms, for example desktop screen versus portable device;
    3.  In the case of text, different natural languages, for example the weather report in English or Spanish;
    4.  Different versions, either as a document evolves, or, more interestingly, because a resource is time-varying by nature, for example _today's_ weather report.
-   Different presentations may be determined by the same representation, ranging from simple changes in size, scale or fonts to changes in modality (digital display, print, even audio or braille) or even non-physical presentation for non-human consumption, for example, by the web crawlers used by search engines.

Figures 1 and 2 above illustrate the static relationship between the various constituents of the URI story. There is also a dynamic story, which is where the Web comes in:

![Click in browser->HTTP GET request->server->HTTP 200
response->Browser rendering](https://www.cogsci.ed.ac.uk/~ht/WhatAreURIs/requestResponse.png)

Figure 3. The HTTP request-response story

The underlying mechanism for accessing representations via the Web, the HyperText Transfer Protocol, or HTTP, provides for control over the first three kinds of variation. That is, by specifying parameters in the request from client to server to access a URI, the _consumer_ can determine which representation the server responds with. In Figure 3 above, for example, we see the initial request includes an `Accept` header which specifies the XHTML media type, and that is indeed what the server sends back in the response.

The fourth kind of variation, variation of representation over time, is quite different, and leads on to some new and very interesting issues. In the cases of the Oaxaca weather report or the home page of your favourite online newspaper, it does seem right to say there is only _one_ resource, despite the fact that the representations you can retrieve of such resources will vary a great deal from day to day.

There's an illuminating parallel here with the class of words in ordinary language which linguists call **indexical**, words such as _this_, _here_ and _tomorrow_, as well as _you_ and _I_. An indexical such as _now_ has a single **meaning** but multiple **interpretations**. The meaning is something like "the time at which the utterance containing the word is made", and is the same for every use of the word. But the interpretation is, well, whatever time it happens to be when the word is used, and this of course changes all the time. More generally, the meaning of an indexical can be understood as a function from contexts (that is, contexts of utterance) to interpretations.

The situation with time-varying resources is just the same—indeed the gloss we gave to the examples above (_yesterday's_ weather report, etc.) underlines this. Once the parallel is pointed out, it can be seen to apply to other, admittedly more specialised, URIs, such as `http://localhost/...` or `file:///home/ht/....`, which identify resources whose representations depend not (or not only) on _when_ they are accessed, but also _where_.

To sum up: Although historically URIs were understood as a kind of Web-enabled file name, with a simple "URI points to web page" model, the move to separate conceptually the (stable) resource identified by a URI from its (potentially varied) representations was necessary to make sense of actual practice. The resource abstraction has gone on to provide powerful new functionality, a subject we will return to below.

## 3. The actual state of play

The phrase "Web 2.0" means many different things, but _one_ thing it is often used to refer to is a significant change in the way representations determine presentations. What a user sees on the screen today as a result of accessing a resource identified by a URI often depends as much if not more on running Javascript programs embedded in the retrieved (X)HTML representation, and on the results of _other_, behind-the-scenes, resource accesses, as it does on the (X)HTML itself. The coinage **AJAX** refers to this approach. For example, the presentation of a map which a user sees when using Google Maps is entirely constructed from images retrieved behind the scenes by the Javascript which makes up virtually all of the original representation as retrieved from the Google Maps URI.

As the proportion of a presentation that depends directly and declaratively on the initially retrieved representation diminishes, and the proportion based on local computation and representations retrieved behind the scenes increases, there is a kind of historical regression going on, which goes back to treating URIs instrumentally, as ways of moving data. What you can send and retrieve is all that matters, and the resource-representation distinction no longer seems to be doing useful work.

There are two things underlying this blurring of the resource-representation distinction in Web 2.0 usage:

-   The kinds of flexibility provided by the kind of variation discussed above, in particular variation with respect to media type or natural language, are just not relevant to most behind-the-scenes web access;
-   The distinction between the URI as such, and the rest of the request to the server, particularly with respect to explicit parameter specifications, is much less evident from the standpoint of the Javascript programmer. Both URI and parameters are things which have to be specified as part of a web request, and this encourages the viewpoint that _taken together_ they identify what is wanted.

If behind-the-scenes URI usage tends to encourage a near-equation of resource and representation, other aspects of sophisticated Web 2.0 usage tend in the opposite direction. If the presentation experienced by a user varies independently of any user-controllable aspect of URI access, or evolves in response to user actions, the sense in which the URI visible at the top of the browser can be said to still 'identify' a representation which corresponds to that presentation has become attenuated almost to the point of vanishing.

If what you see depends on a cookie, you can't post a pointer to it in an email message, because the recipient won't have the right cookie. That's not necessarily a bad thing (you probably wouldn't want to be able to send an email message which lets someone into your bank account), but does act to diminish the connection between URI, resource and representation. If what you see depends on the IP address your request comes from or on a radio button value that doesn't show up as a URI parameter, then not only can you not point to it in email, but you can't (reliably) bookmark it, and Google doesn't index it, because its crawlers will never see it: crawlers don't tick boxes or share your IP address.

The original value proposition of the Web was produced by the network effect: for anything you were interested in, someone else somewhere was too, and they had produced a website about it, and search engines could find it for you.

But the Web as information appliance has evolved: not only is large amounts of web-delivered information not available via search engines, for the kind of reasons discussed above, even the famous pagerank algorithm which launched Google's success doesn't work particularly well anymore, as the proportion of hand-authored pages has declined, and information access is increasingly controlled by a self-reinforcing feedback loop between Google and the big players in the information aggregation game, such as Wikipedia, Tripadvisor and MedicineNet: page ranking in Google today depends to a substantial extent on statistics over search terms and clickthroughs.

From the user perspective, a related phenomenon which threatens to further erode the centrality of the URI-resource connection is the use of the search entry field in browsers instead of the address field. Already in December of 2008, for example, 8 of the top 15 search terms reported by one service over the last five months were in fact the core parts of domain names (non-`www.`, non-`.com`), and some actual domain names, such as `myspace.com`, `yahoo.com` and `hotmail.com`, were in the top fifty. Arguably the time when URIs were the primary currency of the Web is past, and they will disappear from view and consciousness for the vast majority of Web users in much the same way as the angle brackets and equal signs of raw HTML have done.

## 4. The emerging future

As long ago as the mid-1990s, information scientists had taken the URI-resource-representation split to its logical conclusion: it was OK to create URIs for resources for which no representation existed yet (for example a planned but not-yet-drafted catalogue entry), or even for resources for which no (retrievable) representation could in principle _ever_ exist (a particular physical book, or even its author). By the end of the 1990s, the generalisation of the resource concept was complete, and we find, in the defining document for URIs (since superseded, but without significant change in this regard):

> A resource can be anything that has identity. Familiar examples include an electronic document, an image, a service (e.g., "today's weather report for Los Angeles"), and a collection of other resources. Not all resources are network "retrievable"; e.g., human beings, corporations, and bound books in a library can also be considered resources.

> [Berners-Lee, Fielding and Masinter 1998 _RFC 2396, Uniform Resource Identifiers (URI): Generic Syntax_](http://tools.ietf.org/html/rfc2396)

Since then the principle that a URI can be used to identify _anything_, that is, that there are few if any limits on what can "be a resource", has assumed more and more importance, particularly within one community, namely the participants in the so-called Semantic Web programme. This move is not just a theoretical possibility: there are more and more URIs appearing "in the wild" which do _not_ identify images, reports, home pages or recordings, but rather people, places and even abstract relations.

But this in turn has lead to a problem. Time was, when you tried to access a URI, you either succeeded or failed. Success, as illustrated in Figure 3 above, and specifically signalled by the first line of the response message, `HTTP/1.1 200 OK`, meant a representation was coming next, and all was well. Failure meant the infamous "404 Not Found" (whose official rendition is `HTTP/1.1 404 Not Found`) and no representation. Furthermore, success meant that the presentation determined by the representation you retrieved could be counted on to pretty well reproduce the resource identified by the URI itself. You could look at the image, or read the report, or listen to the recording, etc.

But what if we have a URI which identifies, let's say, not the Oaxaca weather report, but Oaxaca itself, that city in the Sierra Madre del Sur southeast of Mexico City? What should happen if we try to access that URI? If the access succeeds, the representation we get certainly won't reproduce Oaxaca very well: we won't be able to walk around in it, or smell the radishes if it happens to be the 23rd of December.

This is the point at which the word 'representation' is a problem. Surely we can retrieve _some_ kind of representation of Oaxaca: a map, or a description, or a collection of aerial photographs. These are representations in the ordinary sense of the word, but _not_ in the technical sense it is used when discussing Web architecture. Unfortunately, beyond pointing to the kind of easy examples we've used all along (a JPG is a good representation of an image, a HTML document can represent a report very well, an MP3 file can represent a recording pretty faithfully), it's hard to give a crisp definition of what 'representation' means in the technical sense, in order to justify the assertion that, for example, an image of Oaxaca does not 'represent' Oaxaca. The definition implied above, namely that a representation of a resource should determine a presentation that reproduces the resource for the perceiver, begs the question of what is meant by 'reproduce'. [The Architecture of the World Wide Web](http://www.w3.org/TR/webarch/), which is a systematic attempt to analyse the key properties on which the success of the Web depends, coined the term **information resource** for those resources for which a representation is possible. It defines the term in this way:

> The distinguishing characteristic of [information] resources is that all of their essential characteristics can be conveyed in a message.

This may seem like an academic question, one which indeed has important connections to both philosophy, particularly the philosophy of aesthetics, and to information science and the notorious question concerning "the nature of _the work of art_". But it has real practical consequences. There is real debate underway at the moment as to exactly what it _means_ for a web server to return a `200 OK` response code, and about exactly what kind of response is appropriate to a request for a URI which identifies a non-information resource. This question arises because, particularly in the context of Semantic Web applications, although no representation of the resource itself may be available, a representation of an information resource which _describes_ that resource may be available. So, to go back to our example, there may be a representation available for a report on a visit to Oaxaca, or for a collection of images of Oaxaca, or even a set of formally-encoded propositions about Oaxaca. Such descriptions are often called **metadata**.

![Two related resources: Oaxaca itself and Oaxaca metadata](https://www.cogsci.ed.ac.uk/~ht/WhatAreURIs/range14.png)

Figure 4. The URI-resource-metadata story

## 5. Conclusions

URIs are at the heart of the Web: we use them both intentionally and without realising it every time we take advantage of the myriad possibilities the Web offers us. Their use is evolving in a number of directions, not all obviously compatible with one another, or with their original conception and the basic technical framework which supported them when the Web was young. Understanding all this is a necessary and worthwhile challenge, both from the perspective of scientific enquiry (just what _are_ these things?) and from the perspective of stewardship (how do we ensure that the Web will continue to work well for everyone?). Insights into these questions may come from surprisingly distant quarters, as well as from observation of everyday use and practice.

The intention of this brief introduction has been to introduce the terminology and issues surrounding URIs and their role on the Web, and as such cannot have done justice to the complexities involved in many areas. The next section points the way for those who want to dig in and explore the details.

## 6. Further reading

The [Technical Architecture Group](http://www.w3.org/2001/tag/) (TAG) of the [World Wide Web Consortium](http://www.w3.org/) (W3C) was established

> to document and build consensus around principles of Web architecture and to interpret and clarify these principles when necessary, to resolve issues involving general Web architecture brought to the TAG, and to help coordinate cross-technology architecture developments inside and outside W3C.

> (from the [TAG charter](http://www.w3.org/2004/10/27-tag-charter.html))

The TAG's largest piece of work to date is [Jacobs and Walsh, eds. 2005, _The Architecture of the World Wide Web_](http://www.w3.org/TR/webarch/), sometimes referred to as 'WebArch' or just AWWW. It contains definitions, principles, constraints and best practice, set out in a relatively informal way, with motivating examples. Further TAG work has been published as separate 'findings', which are listed, along with other information about the TAG's work, on [the TAG homepage](http://www.w3.org/2001/tag/).

The [Internet Engineering Task Force](http://www.ietf.org/) (IETF) is responsible for the formal specifications at the heart of the Web. Recent IETF publications of particular relevance to the issues discussed here are:

-   [Berners-Lee, Fielding and Masinter 2005 _RFC 3986, Uniform Resource Identifier (URI): Generic Syntax_](http://tools.ietf.org/html/rfc3986)
-   [Duerst and Suignard 2005 _RFC 3987, Internationalized Resource Identifiers (IRIs)_](http://tools.ietf.org/html/rfc3987)
-   [Fielding et al. 1999 _RFC 2616, Hypertext Transfer Protocol -- HTTP/1.1_](http://tools.ietf.org/html/rfc2616)