Beware the Big WTF
---

Since the day I became a developer, I've always feared the _Big What The Fuck_. 

The _BWTF_ is not only related to the code you write, it is the lack of knowledge that threaten to crush your entire project. It can be as simple as a server misconfiguration that cause a gaping security flaw.

When the _BWTF_ strikes there is nowhere to go, there is no place to hide. The _BWTF_ is like the worst earthquake in the world: no building endures. A big part of your application, job and/or reputation goes to waste. And nobody wants this to happen.

> How can you protect yourself from the _Big What The Fuck_?

Well, the first step is to accept that this risk exists. The next step is to conceive a strategy to mitigate that risk. After more than 10 years striving to avoid the _BWTF_ I am now quite sure there is no way to remove that risk from your life. It is a part of your life.

> The best strategy to mitigate the risk of a _Big What The Fuck_ is **Testing**.

I am not constraining the discussion to the source code. You should consider testing to be a strategy for a better life, whith or without code. A strategy that you conceive to fight the _BWTF_ which is always lurking behind every corner, anytime.

Say you plan to go holiday to the Red Sea, let's try to work out a test to stress that decision:

- will I relax enough?
- will I cope with 6 days without my Mac?
- will it be safe?
- will I gain 4 punds by eating all the time?

You do the same activity when coding a procedure that takes 2 integers and return the sum:

- is `sum(1, 1)` equal to `2`?
- does `sum('a', 2)` throw an exception?
- is `sum('a', 2)` exception a `wrongInputType` exception?

> The more tests that you are able to produce against a decision / procedure, the more 
> chanses you have to find early issues, with less the risk of a _Big What The Fuck_ 
> in the future.

When it comes to a code scenario the most likely _BWTF_ is to forget to consider a minor requirement from the customer. Then you deliver a product that will fail in the future when that minor requirement will manifest. Your phone will ring like crazy, your inbox will choke and you'll move abroad to escape your shame.

> The _BWTF_ is due to the unpredictability of when the problem will araise. 

The later in time it shows up, the less you'll recall what the minor requirement was and where the problem lies within the code base. And how the hell it works! By the time an issue like that manifests itself, you may have moved to another technology.

In real life a _Big What The Fuck_ can be even worse. Almost four years ago I bought a brand new house and I took a loan for it. Less than two years later I moved to Sweden to join a challenging job opportunity. To this date I still haven't sold that house, but I'm still paying the mourgauge. Of course this is not a life thretening issue, but I can assure you it is annoying to throw away money like that. What if I had prepared myself with a more accurate test when I decided to buy the house? 

- are my career opportunities well developed close to the house?
- does my career ask me to be flexible about my location?
- will it be possible to sell the house without loosing big money on it?

Well, I must confess that I didn't create any of those tests at the time of the buying.

As you can see by yourself there is no known ways to completely remove the risk of a _Big What The Fuck_. The right way to behave is to mitigate that risk by running every decision / procedure against a _good amount of tests_. What the word _good_ means in this context is up to you, but in general the more the tests the less the risk. 

Another important point is that you can build you tests through time, it is always the right moment to add a new test. This is more easy within a coding scenario. You may have missed a minor requirement but as soon you recognise it you can add a specific test to secure that requirement.

My test suite for real life scenarios is _practical common sense_ but when it comes to a code scenario I can give some more specific advices which are specific to _Javascript_.

[KarmaJS](http://karma-runner.github.io/0.12/index.html) is a [NodeJS](nodejs.org) command line tool which runs your unit tests. Among it's features I should mention that you can run tests on multiple target browsers. You can test mobile devices connected to the same network. I use KarmaJS in combination with [GruntJS](http://gruntjs.com/) or [GulpJS](http://gulpjs.com/) to integrate tests into my building processes.

[MochaJS](http://mochajs.org/) is a Javascript test framework which helps in creating your specs files. It provides utility methods for a nice code organization of your unit tests.

[ChaiJS](http://chaijs.com/) is an _assertion library_ that works great with Mocha. It allows you to write `expect(foo).to.be.a.string` so your assertions comes close to a natural language.

[SinonJS](http://sinonjs.org/) is a _mocking library_ which provides a set of tools to investigate your code. Does this method fire twice? Did it receive a string argument? You can go further and completely mimic an _XHR request_.

> I maintain a simple _[NPM module](npmjs.org)_ which combines the above tools to provide 
> you with a ready to use test suite for Javascript: 
> [grunt-mocha-chai-sinon](https://www.npmjs.com/package/grunt-mocha-chai-sinon).
>
> For a more sophisticated tool that brings a building process for _single page applications_
> give a try to [PoliteJS/Workspace](https://github.com/PoliteJS/workspace).


[WebDriver](http://www.webdriver.io/) is a NodeJS bridge to [Selenium](http://www.seleniumhq.org/) functional testing suite. You can build your _FAT_ in Javascript driving a browsing session with full access to Selenium's API.

[DalekJS](http://dalekjs.com/) is a standalone alternative to _WebDriver_. Even if it is on an early stage it looks very promising.

### So remember your Takeaway:

1. the _Big What The Fuck_ is always lurking and there is no way to avoid it
2. **testing is the best strategy** you have to mitigate the risk of a _BWTF_
3. you can apply testing to your professional and private life




