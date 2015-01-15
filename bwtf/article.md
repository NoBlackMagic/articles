Beware the Big WTF
---

Since I've started to be a developer I've always feared the _Big What The Fuck_. The _BWTF_ is not only related to the code you write, it is indeed a lack in your knowledge that crushes the solution on which you are working on. It can be as simple as a server misconfiguration that leads to a big security issue.

When the _BWTF_ strikes there is nowhere to go, no secure place to hide. The _BWTF_ is like the greatest heartquake in the world: no building endures. A big part of your application, job and/or reputation is compromised. And nobody want this to happen.

So how can you protect yourself from the _Big What The Fuck_?

Well, the first step is of course to accept that this risk exists. The next step is to conceive a strategy to mitigate that risk. After more than 10 years striving to avoid this problem I am now quite sure there is no way to remove the _BWTF_ risk from your life.

The best strategy to mitigate the _Big What The Fuck_ risk is testing. And I do not constrain the discussion to the source code. You should consider testing to be a strategy for a better life, whith or without code. A strategy that you conceive to fight the _BWTF_ that is always lurking behind every corner, anytime.

If I plan to go holiday to the Red Sea I try to work out a test to stress that decision:

- will I relax enough?
- will I resist 6 days without my Mac?
- will it be safe?
- will I gain 4 punds by eating all the time?

I do the same activity when I write a procedure that takes 2 integers and return the sum:

- is `sum(1, 1)` equal to `2`?
- does `sum('a', 2)` throw an exception?
- is `sum('a', 2)` exception a `wrongInputType` exception?

The more the tests that you are able to produce against a decision / procedure, the more the chanches you have to find early issues, the less the risk of a _Big What The Fuck_ in the future.

When it comes to a code scenario the most likely _BWTF_ is to forget to consider a minor requirement from the customer. Then you deliver solution that will fail in the future when that minor requirement will manifest. The _BWTF_ is due to the unpredictable timing for the problem to raise. The later in time it shows up the less you'd recall what the requirement was and where the problem is coded. And how in hell it works! By the time an issue like that manifests you may have moved to another technology.

In the real life a _BWTF_ can be even worst. Almost four years ago I bought a brand new house and I took a loan for it. Less than two years later I moved to Sweden to join a great job opportunity. To date I am still to sell that house but I still pay the loan for it. Of course this is not a life thratening thing but I can assure it is really annoying to trash money that way. What if I did prepare myself with a more accurate test when I decided to buy the house? 

- is my career well developed close my house to be?
- is my career likely to move me abroad?
- will it be possible to quickly sell the house without loosing big money?

Well, I must confess that I didn't create any of those tests at the time of the buying.

As you can see by yourself there is no known ways to completely remove the risk of a _Big What The Fuck_. The right way to behave is to mitigate that risk by run every decision / procedure against a _good amount of tests_. What the word _good_ means in this context is up to you, but in general the more the tests the less the risk. 

Another important point is that you can build you tests through time, it is always the right moment to add a new test. This is more true for a coding scenario. You may have missed a minor requirement but as soon you recognise it you can add a specific test for secure that requirement.

My test suite for real life scenarios is _practical common sense_ but when it comes to a code scenario I can give some more specific advices which are specific for _Javascript_:

[KarmaJS](http://karma-runner.github.io/0.12/index.html) is a [NodeJS](nodejs.org) command line tool which runs your unit tests. Among it's features I should mention that you can run tests on multiple target browsers and even mobile devices connected to the same wi-fi. I use it in combination with [GruntJS](http://gruntjs.com/) or [GulpJS](http://gulpjs.com/) to integrate tests within code building processes.

[MochaJS](http://mochajs.org/) is a Javascript test framework which helps in creating your specs files. It provides utility methods for a nice code organization of your unit test.

[ChaiJS](http://chaijs.com/) is an _assertion library_ that works amazingly with Mocha. It allows you to write `expect(foo).to.be.a.string` so you code assertions are really close to a natural language.

[SinonJS](http://sinonjs.org/) is a _mocking library_ which provides a set of tools to investigate your code. Has this method been called twice? Did it receive a string argument? You can go as far as to completely mimick an _XHR request_.

[WebDriver](http://www.webdriver.io/) is a NodeJS bridge to [Selenium](http://www.seleniumhq.org/) functional testing suite. You can build your _FAT_ in Javascript driving a browsing session with full access to Selenium's API.





