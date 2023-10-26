Source:
100+ Web Development Things you Should Know - 
https://www.youtube.com/watch?v=erEgovG9WBs
\
Web development is the best job in the world. You build on a platform with nearly 5 billion daily active users all connected together like the neurons of a global super intelligent brain. A system that can cure disease, eliminate poverty, advance science, and stuff like that, but mostly it's used to share memes, create parasocial relationships, amplify drama, and most importantly make tons and tons of money.
\
If you want to get into it, you're gonna need to know some stuff, like a lot of stuff. In web development 101 we'll take a look at a 101 different concepts that you'll need to know when building full stack web apps.
\
This is the internet, it's a network of billions of machines connected together, what do you write to it? Like mail? No a lot of people use it and communicate, I guess they can communicate with nbc writers and producers. Alison can you explain what [[Internet]] is? It was officially born on january 1 1983, thanks to the establishment of the [[Internet_Protocol_Suite]] ([[IP]]), which standardized the way these computers communicate. 
\
The internet protocol is used to identify different computers on the network by assigning each one of them a unique [[IP_Address]]. These computers can then send data back and forth with the [[Transmission_Control_Protocol]] ([[TCP]]). [[TCP]] breaks data into a bunch of small [[Packets]], kind of like puzzle pieces. Then it sends them through a bunch of physical components, like fiber optic cables and [[Modem]]s before they're put back together by the receiving computer. (see [[Open_Systems_Interconnection]] or [[OSI_Model]])
\
You can think of the [[Internet]] as hardware, but the internet is not the same thing as the web. The [[World_Wide_Web]], or [[WWW]], is like software that sits on top of the [[Internet]]. Where people can access web pages with the [[Hypertext_Transfer_Protocol]] ([[HTTP]]).
\
What's special about [[HTTP]] is that it gives every page of content a [[Uniform_Resource_Locator]] or [[URL]] and more broadly Uniform Resource Identifier or [[URI]]. Humans typically use a tool called a web [[Browser]] to access a [[URL]], where it can be rendered visually on their screen. The [[Browser]] is called the [[Client]], because it's consuming information but on the other end of that [[URL]], there's another computer called a [[Server]]. It received an [[Programming_Studies/Web_Development/Web_Dev_Definitions/HTTP_Request]] from the [[Client]], then sent a [[HTTP_Response]] containing the web page content. These are called [[HTTP_Messages]], but more on that later. 
\
What's interesting is that every web page has a unique [[Domain_Name]] like "fireship.io", or "example.com" a [[Domain_Name]] can be registered by anyone, via a [[Registrar]], who's accredited by the '[[Internet_Corporation_for_Assigned_Names_and_Numbers]]' "[[ICANN]]", a nonprofit responsible for overseeing namespaces on the internet.
\
When you navigate to a domain in a [[Browser]] it gets routed through the [[Domain_Name_System]] that maps these names to an actual [[IP_Address]] on a server somewhere. [[DNS]] is like the phone book of the internet. 
\
Now when you look at a webpage the actual content you see is represented by [[Hypertext_Markup_Language]]. Most browsers have [[Dev_Tools]], where you can inspect the structure of the [[HTML]] at any time.
\
To build your own web page, you'll want a [[Text_Editor]] or [[Code_Editor]] like [[VS_Code]]. An [[HTML]] document is just a collection of [[HTML_Elements]] in a text document, and an [[Element]] is an opening and closing tag with some content in the middle, like a paragraph and heading. It also has [[Element]]s that handle user input like the [[Select]]" and "[[Input]]" elements, which are used to build [[HTML_Forms]].
\
In addition [[Element]]s can have one or more [[HTML_Attributes]] to change their behavior. For example an input can have a type like, "[[Text]]", or "[[Number]]", which the [[Browser]] will render differently to collect the appropriate value. 
\
But the [[Element]] that puts the "hypertext" in '[[HTML]]', is the a [[Tag]] or [[Anchor_Tag]]. It's a link that allows one page to navigate to a different page based on its [[URL]]. These [[Element]]s are [[Nested]] together in a hierarchy to form the [[Document_Object_Model]] or [[DOM]] from the root element.
\
A web page is split into two parts the [[Head]] contains invisible content like [[Metadata]] and a [[Title]]. Then we have the [[Body]] for the main content that the end user actually sees. The reason we wrap everything in [[Tag]]s is to give [[Browser]]s and [[Bots]] hints about the [[Semantic]] meaning of the web page. This allows [[Search_Engine]]s to display results properly and also helps with [[Accessibility]] for devices like [[Screen_Readers]], that allow anybody regardless of disability to enjoy the content. 
\
One of the most common [[Element]]s you'll come across is a [[Div_Tag]] [[Div]]. Divisions are used to define a section of the webpage. On its own a [[Div]] might not seem to do anything and currently produces this plain black and white website.
\
That begs the question, "how do we make this website look cool?". 
The second language you'll need to learn as a web developer is [[Cascading_Style_Sheets]] or [[CSS]], which allows you to change the appearance of the [[HTML]] [[Element]]s. (see [[CSS_Properties]])
\
One way to accomplish that is with an [[Inline_Style]]. Using the style attribute on an [[Element]] the style itself contains a collection of properties and values that change the appearance of the [[Element]]. Like we might make the background color black and the text color red.
\
What we've created here is an [[Inline_Style]] that will only be applied to this one [[Element]], however [[CSS]] [[Cascade]]s, which means it can be applied to multiple [[Element]]s at the same time, providing better code reusability.
\
Another option is to move our code into a [[Style_Tag]], but to make the code work we'll first need to define a [[Selector]] so it knows which [[Element]]s to target. A [[Selector]] for example can target all of the paragraph elements on the page, but that's too broad. We can be more granular by defining a [[Class]] that style can then be applied to one or more [[Element]]s with the [[Class]] attribute. What's interesting though is that we now have [[Class]]es that apply different styles to the same [[Element]].
\
[[CSS]] contains a bunch of [[CSS_Specificity]] rules that determine which styles are relevant to an [[Element]], in a way that's self-evident and elegant like a benevolent elephant.
\
Most often though we don't use [[Style_Tag]]s, but instead use an [[External_Stylesheet]], which is linked to the webpage and the [[Head]] of the document. When it comes to [[CSS]] by far the most difficult thing to learn is layout and positioning.
\
The best way to think of formatting is the [[Box_Model]]. Think of every [[Element]] like a box, the outside of that box is wrapped, with [[Padding]], borders, and margin. The boxes then take up space on the page, from top to bottom. Some [[Element]]s, like [[Head]]ing, have a display of [[Block]] by default. Which means they take up all available horizontal space other [[Element]]s like [[Image]] are displayed [[Inline]], which means they can line up horizontally side by side.
\
The problem is that the default position is usually not desirable, it can be changed by customizing the position property on an [[Element]].
\
[[Relative_Positioning]] allows an [[Element]] to move a certain number of pixels from its normal position. [[Absolute_Positioning]] is similar but the 'position values' are relative to the [[Element]]s nearest ancestor. Then we have [[Fixed_Positioning]], which will keep an [[Element]] on the screen even as the user scrolls away from it, because it's fixed to the entire viewport.
\
Changing the position of an [[Element]] is one thing but one of the biggest challenges web developers face is creating [[Responsive_Layout]]s. Users can access your web page from all kinds of different screens, and it should look good on all of them. [[CSS]] provides a bunch of different tools to help make this happen one of which is [[Media_Queries]].
\
A [[Media_Query]] allows you to get information about the device that's rendering the web page and apply different styles accordingly, but more importantly it provides layout tools like, [[Flexbox]]. 
\
Applying display flex allows the [[Parent]] to control the flow of the [[Child]]ren to easily create rows and columns for more complex layouts. Display grid & [[Grid_Layout]] can be used to control multiple rows and columns at the same time.
\
Now [[CSS]] is usually not considered a [[Turing_Complete]] programming language on its own, however it does have mechanisms, like [[Calc()_Function]] to perform mathematical operations and custom properties, which are like [[Variable]]s that you can reuse in multiple places.
\
Vanilla [[CSS]] is rarely enough though, and many developers choose to extend it with tools like [[Syntactically_Awesome_Stylesheets]] or [[SASS]], that add additional programmatic features on top of it.
\
That brings us to the third language you'll need to know as a web developer, [[JavaScript]] technically you don't need [[JavaScript]] to build a website, however most developers choose to use it to make the user interface more interactive.
\
To run [[JavaScript]] code on a web page open up a [[Script_Tag]], then write some [[JavaScript]] code inside of it. The browser interprets the [[HTML]] from top to bottom and runs this code when it encounters it in the [[DOM]]. 
\
In most cases [[JavaScript]] is written in a separate file then referenced as the source, on the [[Script_Tag]]. Usually it's preferred that this code runs after the [[DOM]] content has loaded, which can be accomplished with the [[Defer_Attribute]].
\
[[Js]] is a big complicated programming language, which is more formally known as [[ECMAScript]] and is standardized in all major browsers. There are several different ways to declare a [[Variable]]. A variable that might be reassigned in the future uses the [[Let]] keyword, while a [[Variable]] that can't be reassigned uses [[Const]].
\
It's a [[Dynamically_Typed]] language, which means no [[Type_Annotations]] are necessary. That's not always ideal so many developers choose [[TypeScript]] as an alternative, to add static typing on top of [[JavaScript]].
\
Now one of the most common reasons you would use [[JavaScript]] in the first place is to handle [[Events]]. Whenever the user does something on a web page the [[Browser]] emits a [[Events]] that you can listen to with an [[Event_Listener]], like a click, mouse move, form input change, and so on. (see [[Browser_API]])
\
We can tap into these [[Events]] using [[Browser_API]]s. Like "document", which in this case provides a [[Method]] called "[[Query_Selector]]", that allows us to grab an [[Element]] with a [[CSS]] [[Selector]]. Once we have that [[Element]] set as a [[Variable]] we can then assign an [[Event_Listener]] to it.
\
An [[Event_Listener]] is a [[Function]] that will be called or re-executed anytime the button is clicked. The language has a variety of built-in [[Data_Structures]] like an [[Array]] to represent a collection of values. However the most fundamental [[Data_Structure]] is the [[Object]], also commonly called a [[Dictionary]] or [[Hashmap]].
\
Anything that's not a [[Primitive_Type]], like a [[String]] or number, inherits its base functionality from the [[Object]] [[Class]]. It relies on a technique called [[Prototypal_Inheritance]], where an [[Object]] can be cloned multiple times to create a chain of ancestors, where the [[Child]] inherits the properties and methods of its ancestors.
\
This is different from [[Class]]-based inheritance, which is kind of confusing because [[JavaScript]] also supports [[Class]]es. However these [[Class]]es are just [[Syntactic_Sugar]], for [[Prototypal_Inheritance]], but now we're getting a little too low level most developers.
\
Don't ever want to have to touch the word prototype, so what we do instead is use a [[Kanban/Cards/LetsGrow.io_Cards/Frontend_Framework]] like, [[React]], [[View]], [[Svelte]], [[Angular]] and so on all, of these [[Framework]]s do the same thing, in a slightly different way. Which is represent the [[UI]], as a tree of [[Component]]s. A [[Component]] can encapsulate [[HTML]] [[CSS]] and [[JavaScript]] into a format that looks like its own custom [[HTML]] [[Element]]. Most importantly they produce [[Declarative_Code]], that describes exactly what the [[UI]] does, and that's much easier to work with than [[Imperative_Code]], that you would normally get with just plain vanilla [[JavaScript]].
\
At this point we've taken a look at the [[Frontend]] of the [[Fullstack_Framework]], but now we need to switch gears to the back end. Starting with [[NodeJS]] which is a [[Server_Side]] runtime based on [[JavaScript]]. You can run [[Server_Side]] code for web applications in all kinds of different languages, but [[NodeJS]] is the most popular because it relies on the same language as the [[Browser]].
\
It's also based on the same [[v8_Engine]] that powers the chromium browser to run code in a single threaded non-blocking [[Event_Loop]]. This allows [[Node]] to handle many simultaneous connections quickly and efficiently. In addition it allows developers to share work remotely thanks to the [[Node_Package_Manager]], a package is also called a [[Module]] which is just a file that contains some code with an [[Export_Statement]], so it can be used in another file. The file can consume a [[Module]] with an [[Import_Statement]], but now we need to think about how to deliver the actual website, from the server to the client.
\
The classic option is [[Server_Side_Rendering]], in this approach the [[Client]] will make a [[Get_Request]] for a certain [[URL]]. Every request has an [[HTTP_Method]] and [[Get-Request]] means you want to retrieve data from a server as opposed to [[HTTP_Method]]s, like [[POST-Request]] and [[Patch-Request]], where the intent is to modify data.
\
The server receives the request and then generates all the [[HTML]] on the server and sends it back to the client as a response. The response contains a [[Status_Code]], like 200 for success, or levels 4 and 500 for errors. For example, if the web page doesn't exist the server will return a 404 [[Status_Code]], which you've likely seen before as a web user, as [[404_Not_Found]].
\
[[Server-side_Rendering]] or [[SSR]] is extremely popular, but in some cases it may not be fast enough. Another approach is the [[Single-page_Application]] or [[SPA]]. With this approach the server only renders a shell for the root [[URL]], then [[JavaScript]] handles the rendering for all other pages on the website the [[HTML]] is generated almost entirely [[Client]]-side in the [[Browser]], making the website feel more like a native [[iOS]] or android app.
\
When the app needs more data it still makes an [[HTTP]] request, but only requests a minimal amount of data as a "[[JavaScript_Object_Notation]]" or [[JSON]] which is called, a [[Data_Interchange_Format]], that can be understood by any programming language. This can result in a great user experience, however it can be very difficult for [[Bots]], like search engines, and social media link previews to understand content on the page.
\
This led to another rendering strategy called, [[Static-site_Generation]] or [[SSG]]. In this case every webpage on the site is uploaded to a server in advance, allowing bots to get the information they need. A front-end [[JavaScript]] framework usually takes over to [[Hydrate]] the [[HTML]] to make it fully interactive, and behave like a [[Single-page_Application]].
\
Performance is extremely important and you'll want to use tools like, [[Lighthouse]] to optimize metrics like: [[First_Contentful_Paint]] / [[FCP]] and [[Time_to_Interactive]] / [[TTI]].
\
Now to implement one of these patterns, most developers will use a full stack framework like, [[Next_Js]], [[Ruby_on_Rails]], [[Laravel]] and so on. These abstract away many of the more tedious things developers don't want to deal with.
\
One of which is [[Module_Bundlers]], which are tools like [[Webpack]] and [[Veed]], that take all of your [[JavaScript]], [[CSS]] and [[HTML]] and package it in a way that can actually work in a [[Browser]]. They might also provide a [[Linter]], like [[ESLint]], to warn you when your code doesn't follow the proper style guidelines.
\
Oh and cant forget you are definitely going to need a [[Database]], to build a full stack web application, because you need somewhere to store your data. Like data _about_ your users, but in order to **get** that data, you'll need to give users a way to log in via a process called [[User_Authentication]].
\
Now before you deploy your code you'll need to test it with a [[Web_Server]] there are tools like [[Nginx]] and [[Apache]]. Using these tools, you create an [[HTTP]] server, but your [[Fullstack_Framework]] will likely do this for you by serving the files on [[Localhost]], which makes your own [[IP_Address]] behave like a remote web server.
\
When it comes time to deploy you'll likely use a big [[Cloud]] provider like [[AWS]]. Most apps are [[Container]]ized, with [[Docker]] making them easy to scale up and down based on the amount of traffic that they receive.
\
There are many tools out there that function as a [[Platform-as-a-Service]] or [[PAAS]], to manage this infrastructure for you in exchange for your money, or if you don't want to get locked in with a giant tech corporation you might host your app on a decentralized blockchain, with [[Web3]]. Also check out and research, [[IAAS]], [[SAAS]], & [[BAAS]].
\
This just about sums up about one percent of what you'll need to know to call yourself a full stack web developer. If that seems overwhelming, don't worry too much almost nobody knows what the hell they're doing and we all just use google to figure things out on the fly.
\
Goodluck!