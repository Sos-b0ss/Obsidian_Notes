3rd party dependencies will most likely make up almost to 80% of the code that gets pushed to production.
\
So because of this libraries that we rely on will rely on other libraries so transitive dependancies from that sometimes lead to a large chain of dependancies, and some of which may have security vulnerabilites.
\
You can use a scanning tool on your source code to identify vulnerable dependancies. You should always scan for vulnerabilies in your development pipeline and your deployment pipeline, Maybe even on your main branch on your nightly build to verify anything thats already been put into production could have newly created vulnerabilites in it. As well any time there are new pull requests or code contributions it is very important to scan that code as well.
\
On [[Github]] you can use Dependabot to automate your updates via pull requsts, and what this does is itll actually create a [[PR]] with the updated event thatll run all your [[CI]] tests and then you can merge it yourself.
\
For other options that are Full-featured Dependency Scanners check out:
- [[Info_Sec_Studies/Sec+/Security+_Definitions/Snyk]]
- [[JFrog_Xray]]
\
