# GitFlow for Juniors and Dinosaurs
---

I’ve started to Git when I've almost become a Dinosaur, in the beginning it was for me just another remote backup utility that some insane guy (GitHub) was giving away for free. By time and mistakes I’ve learn a couple of things, and **today Git boosts my productivity** as long I follow few basic best practices.

### Quick Takeaway from my story:

1. Git and related services are free tools that facilitate your coding experience and team collaboration
2. **Use action points checklists** (included here!), is the easiest way to git
3. Git allows you to try new paths, do it!

In this article you will find links to in-depth resources to master the art of Git.

> So keep calm and Git this article done.



## What is Git?

Git is a source control and versioning tool that works well with text files. Like source code.

The point is to keep track of the changes that you make on a particular set of files. When your change is set and well tested you can mark it as done. 

> This is called **commit**.

Git stores all your commits into a local database (called _repository_ or _repo_) so at any time you can recall a particular commit and see the state of the art at that time. 

> This is called **checkout**.

Problem solving 101 is “finding the right path”, along that way you walk some dead ends so you need to go back and try another lead. Git helps you doing that. You can create a sidetrack of your project, work on it, roll it back if it was a dead end or confirm it as “the right way”.

> This is called **branching**.

But wait! There is more than that. You can Git with other people through online services like _GitHub_ or _BitBucket_ and enjoy a straightforward collaboration experience.




## Git is a Collaboration Tool

Tools like _GitHub_ or _BitBucket_ allow you to keep your Git repository in the cloud. When you commit a new change then you publish it to the remote repository. Other guys can point to the same repository to download your change.

> This is called **push** and **pull**.

The _remote repository_ is available to the world as URL. 

> It’s called **source**.

When you create a new _branch_ (a project's sidetrack) you can _push_ it to the _remote repository_ so other guys can _pull_ it and try out your solution.

Remote collaborators can even contribute to your job by proposing their own commits, eventually they can ask you to merge they commits into your repository. 

> This is called **pull request**.






## GitFlow 101

The way you use Git affects the quality of your project management experience. There is no “right way” to do Git but there are some good candidates. _GitFlow_ is just one of the most famous ways to structure your project and developers with Git.

> GitFlow is a practical Git way to software development projects organisation.

It takes in consideration the needs for:

- produce new features
- perform testing activities
- bug fixing (dead quickly)
- release stable products

It conceived for team collaboration through services like _GitHub_ or _BitBucket_.   
(or custom servers as well).

### The basic branch structure

Any _GitFlow_ project lists at leas these two branches:

- **main branch** - contains the stable releases of your project
- **develop branch** - contains the latest available set of completed features

From the _develop branch_ you can create your _nightly build_ and provide your clients with early beta versions or preview releases.

### Add new features to your project

Let say that from release 1.0 to release 2.0 you plan to complete "X" features. 

A feature can be whatever stuff that **add business value to your project**. If your product is a website then a feature can be something like:

- _in order to increase mobile fruition I want the layout to adapt across many screen sizes_
- _in order to increase loading time performances I want to concatenate all CSS files automatically_

> Above features are exposed in a **gerkin like language**.   
> 
> The sentence must point out the business value first then give a straightforward 
> indication of the action to undertake to fulfil that requirement. 
> 
> You must be able to test whether a feature is done or not, and the _gherkin 
> language_ structure helps a lot because it forces yourself to pinpoint the real stuff.

If you use _GitHub_ or _BitBucket_ you can **create a new issue** (or task) for each of your features. You do that in the project's management page. Use the _gherkin description_ as title for your issue then add details, notes, images in the body field.

Each issue you create receives an unique ID. A number like #1. We’ll get to this in a minute. But you can also label your issues to organise them into groups: feature, bug, desired improvement, etc.

### Give a Branch to every new Feature

Features are the building blocks of your success. Once you write them down you need to work them out in order to build a new stunning release. Your team list 5 hight skilled developers and you need them to work in parallel to maximise the time to market. Now is when feature branches come into the picture.

When John picks up the feature « #3 implementing the responsive layout », he creates a new branch from development.

**HOW TO START WORKING ON A NEW FEATURE:**
- pull develop branch
- create a new branch «feature/#3_responsive-layout »
- push the new branch so your colleagues can see you are working on it
- work / commits / push

The new branch name follow the schema:

    feature/#{issueID}_{short-name}

### Pull Requests and Code Review

When John is done with the feature he must obtains his colleagues approval before to merge his code in the development branch. This process is called Code Review.

Why is that? Well, code reviews increases quality and reduces bugs.

Do you remember your time at school when you used to read your writings backwards seeking for misspellings? You did it that way because if you read your writing top down you miss your own mistakes. You knew your text so well that you couldn’t focus on the single words. Reading backward was a strategy to force your brain into a “review mode” and focusing on the words more than the contents.

It is extremely difficult to catch your own bugs because you know your code too well. But what is almost impossible to find yourself could jump before the eyes of the guy sitting next to you. He will be able to point out bugs, bad names, poor performance implementations and so on.

By receiving an giving code review you will improve your skills. You get in touch with different ways to problem solving, different approaches to code writing and organisation. You get better at your job and you help you mates to get better with you. Code Review is a win-win.

**HOW TO ADD YOUR FEATURE TO THE PROJECT:**
- push your commits to your feature branch
- create a Pull Request to merge your feature to develop
- link at least two reviewers in the PR description (*)
- discuss / modify your code / push new commits that fix PR’s comments
- wait until explicit approval
- merge your feature into develop!

(*) in both GitHub and BitBucket you can link your colleagues by adding « @nickname » into the PR description. It works in commits and issues description as well.

If you are running your project alone you still can benefit from the code review practice. The trick is to wait at least one day before to merge a completed feature. You can start to work on a completely different task, even a different project. Or just take a day off. The more you walk away from the job you’ve done the more effective your self code review will be.

### Test before you Release

Now the features you planned to include in your 2.0 release are completed and the develop branch is fully functional. This is the moment to perform a last testing session.

Whether you do manual tests or run a quality automation tool you should collect all the yellow / red alarms into a new set of issues. Label those issues « test-fix ». Use the issue’s title to briefly describe the bug (be effective here!) and then focus on filling up a good body:

1. link the feature that relates the bug: « #{issueID} brief feature desc »
2. list the steps to reproduce the bug
3. explain why this bug is important, point out the business value that is affected

Those informations will help you and your team to prioritise the bug fixing. Very often minor bugs are fixed after the release. It is a trade-off between quality / deadlines / marketing efforts.

When you start to work on a test-fix you should do it in a new branch that you create from develop. Use the following the schema:

    test-fix/#{issueID}_{short-bug-description}

**HOW TO FIX A PRE-RELEASE BUG:**
- pick up a test-fix issue
- read carefully and reproduce the bug
- pull develop branch
- create a new branch «test-fix/#22_broken-menu-iphone »
- push the new branch so your colleagues can see you are working on it
- work / commit / push
- create a Pull Request to merge your test-fix to develop
- link at least two reviewers in the PR description (*)
- discuss / modify your code / push new commits that fix PR’s comments
- wait until explicit approval
- merge your test-fix into develop!

It is very important to run the fix through the code review process. It mitigates the risk to introduce new bugs by fixing an existing one!

### Create the new Release

At this point of the story you are the proud owner of a bug free development branch. Everything is set and you are ready to announce your stunning release!






## Quick Git Glossary

Let’s focus on the terms and actions about Git that you learned so far:

### repository or repo

It is your project, you name it after the main folder.

Git stores all it’s local informations into a hidden folder named `.git`and you can publish those informations to services like GitHub or BitBucket.

### commit

It’s when you mark a couple of changes as done. 
A commit is identified by an alphanumeric ID and it’s stored into the repo’s database.

### branch

It’s a version of your project and it can co-exists with other versions.

You can easily jump from one version to another, it’s up to Git to do the magic for you. Every Git repository have a default branch named `master` which represent the standard version of your project.

In software development the master branch contains the current stable version of the codebase, when you start working on a new feature you should create a new branch named after the new feature

### merge

It’s the action to take all the new commits from one branch “A" and apply the branch “B". 

Say your website is stable and your codebase is available in the master branch. Then your client calls and you start to work on the new-slideshow feature, you do that in a new branch. You produce a couple of commits and you reach a stable version of the slideshow. 

If you were using just folders and files this is the moment in which you have to manually copy all the new stuff to your stable website. It’s a slow painfully and unproductive procedure.

But thanks to Git you can merge new-slideshow into master and in less than an eyeblink the job is done!

### origin

Is the URL that identifies a remote repository.

You can use services like GitHub or BitBucket to host your project online. This decision leads to two main consequences:

- all your files are safely stored online (as a backup)
- you can open your project to other developers and work together

The third point to consider is that the source code you move online can be public or private based to the service that you use / buy. Everything is free for open source projects anyway.

### push

Is the action to publish all your branch's local commits to the origin.

It’s when you perform the backup action and your code become available to others for collaboration. It is important to outline that only commits are published. If you have some 

### pull

Is the action to download all your branch’s remote commits to your local repository.

When you work with other people you do this action every time you start to work to receive the people’s commits. You want to work on an up to date codebase, don’t you?

### pull request - or “PR"

Is the action to merge two remote branches on an origin. 
Because of the collaborative nature of services like GitHub or BitBucket, the normal procedure to merge two remote branches is to politely ask for this to happen.

The service will compile a page in which to list all the commits and show all the code changes that are involved. The same page contains also a discussion board so your collaborators can discuss with you the request, comment your code (do code review) and eventually accept your request.

After a PR is accepted and merged everybody should pull from the target branch.







PROJECT ITERATION (before you start each task)
- read or review project's materials. Mail, visuals, notes, etc
- review the current status of your work
- review the commits history to remember what you've done before
- review the existing tasks to update and improve the descriptions and related materials (Es notes, schemes, pictures)
- focus on simplification: can you split a task into many simple ones?
- create some more tasks, at least some general stuff, reminders, etc
- carefully choose the task that bring the more business value with the less efforts. Be thoughtful on this evaluation
- add a note to that task that you are working on it, you can also use labels for that


SINGLE TASK ITERATION
- choose which task to work on
- pull develop branch
- check visual status on the browser
- create new branch feature/#{id}_{short-name}
- push the new branch (so others see what you are working on)
- check visual status on the browser
- do your job to complete the task (*)
- close your last commit for the task
- check again the visual status on the browser
- push your branch 
- check on github that all your commits are listed on the branch' page
- create a pull request to merge your commits to develop (**)
- code review your pull request (***)
- merge the pr 
- checkout develop on your mac
- check the actual visual status of develop (should be like you never did the task)
- pull updates for develop
- check again the visual status (now you should see your task)
- you are done!

(*) describe how to commit to link the issue

(**) a Pull Request (PR) is a request to merge your commits into another branch, usually develop. Somebody need to check and approve your request before to merge it. You must be keen to that guy providing a brief but complete description of the job you did. GitHub collects a lot of information automatically: related issue, involved files and commit history for the PR. Don't repeat those informations. Add only what it can make the difference during code review. Es you can mention which strategies you used, link tutorials you followed or online resources you tried to emulate. Those are useful informations. Remember that sooner you will be asked to review somebody else code! You can also try to code review your own PR by dressing the PR's hat.

(***) when you code review your efforts are set to help and learn. You help the PR's owner seeking for bugs, misspellings, unclear comments, code style errors and general improvements. You learn by reading more senior guy's code. You should always clone the PR branch locally to run the project. If it doesn't work you should check it out with the author, maybe you found a big wtf! The focus on code style.

