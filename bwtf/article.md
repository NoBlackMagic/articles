Beware the Big WTF
---

Since I've started to run the developer profession I've always feared the _Big What The Fuck_. The _BWTF_ is not a simple issue related to the code you write, it is indeed a lack in your knowledge that causes a big problem in the solution you are working on. It can be as simple as a server misconfiguration that leads to a big security issue.

When the _BWTF_ strikes there is nowhere to go, no secure place to hide. The _BWTF_ is like the greatest heartquake in the world: no buildings last. It is likely that a big part of your application, job and/or reputation is compromised. And nobody want this to happen.

So how can I protect myself from the _Big What The Fuck_?

Well, the first step is of course to accept the risk, the next step is to conceive a strategy to mitigate that risk. After more than 10 years workinf on the argument I am now quite sure there is no way to remove the _BWTF_ from your life.

The best strategy to mitigate the _Big What The Fuck_ risk is testing. And I do not limit the discussion to my source code. I consider testing to be a strategy for a better life in general. To avoid the _BWTF_ that is always lurking behind every corner, anytime.

If I plan to go holiday to the Red Sea I try to work out a test to stress that decision:

- Will I relax enough?
- Will I resist 6 days without my Mac?
- Is it safe?
- Will I gain 4 pund by eating all the time?

The same activity I do when I write a procedure that takes 2 arguments and return the sum:

- is `sum(1, 1)` equal to `2`?
- does `sum('a', 2)` throw an exception?
- is `sum('a', 2)` exception a `wrong input type` exception?

The more the tests that I am able to pack against a decision / procedure, the more the chanches I have to find issues, the less the risk of a _Big What The Fuck_.

When it comes to a code scenario the more likely to be a _BWTF_ is to forget to consider a minor requirement from the customer. Then you deliver an almost functional solution that will brake somewhen in the future when that minor requirement will raise. The _BWTF_ is due to the unpredictable timing for the problem to raise. The later in time the less you'd remember what the requirement is, where the problem is coded. How the hell it work! You may have moved to another technology by the time an issue like that manifests.

In life a _BWTF_ can be even worst. Almost four years ago I bought a brand new home and I took a loan for it. Less than two years later I moved to another country to join a great company. By the time of the writing I am still to sell that house. And I am paying the loan for an empty house. Of course this is not a life thratening thing but I assure it is really annoying to trash money like this. What if I prepared myself with a more accurate test when I've decided to buy the house? 

- Is my career well developed close my house to be?
- Is my career likely to require me to move abroad?

Well, I have to confess that I've missed to create those tests by the time of the buying.

As you can see by yourself there is no known ways to completely remove the risk of a _Big What The Fuck_. The right way to behave is to mitigate that risk by run every decision / procedure against a good amount of tests. What the word "good" means in this context is up to you, but in general the more the tests the less the risk. 

Another important point is that you can build you tests in time, it is always the right moment to add a new test. This is more true for a coding scenario. You may have missed a minor requirement at the beginning but as soon you recognise it you can add a specific test for that requirement.

My test suite for real life scenarios is _practical common sense_ but when it comes to code scenario I can give some more specific advices which are specific for _Javascript_:

- KarmaJS
- MochaJS
- SinonJS
- ChaiJS



