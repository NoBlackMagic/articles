Save Your Becon
---

### Free backup strategies to avoid headache

Backups are strange animals. In a perfect world you don’t need backups. You put efforts in building a solid backup strategy, you buy external drives, cloud storage, amazing software which you wish you never have to use in life.

So what? Why am I wasting all those efforts? Why do I live with a tera drive always plugged in my computer? Is a terabyte enough by the way?

And when something really bad happen, when you see the bloody blue screen on a Windows machine, when your kid feeds your powerless Mac with hot milk, what do you do? Do you remember how the restore procedure works? I never did for sure.

But today is your lucky day because I am about to tell you that useful and dead simple backup strategies exist. And they are just few clicks away.

The trick is to find the problem which is more likely to show up then solve it in the simplest and most efficient way before to consider a more complex scenario.

Now try to be honest when you answer the following questions. How many times did a villain rob your computer? How many times did you get infected with a destructive virus? How many times did you screwed your code base because you kept coding in the night when you'd better sleep tight?

For me is the last scenario that caused myself the worst headaches ever. A lot of times it happens to me to enter this mystical mental space in which "I see the light", so I feel the urge to start to write my solution scrambling existing code here and there. Oh some times I get things done, but it is a matter of luck. 8 times out of 10 it doesn't work at all!

The (urgent) need to come back to a stable code base is a daily scenario in a developer life. Indeed it could happen more than once a day if it was "one of those days".

So there is Git. Well, yes but no. Of course Git is one of the most powerful tools at your disposal but it is not the easiest one. You should invest the time of learning Git as version control and collaboration tool, but for now let's keep it simple. Dead simple.

The most efficient way to being able to restore a stable code base is to create a copy of the project before you start a development session. On a Mac is a matter of right clicking the project's folder and choose "duplicate". Dead simple.

What is simple often works well so let analyze what you have to do in case you need to revert your code. You trash the current project's folder and rename the copy to match the original one. Dead simple and impressively quick.

Now you can improve your backup strategy by adding versioning support. You are going to keep a copy for each stable version of your code base. Right click on you project's folder and choose "compress archive. This option is available with slight different names on different OS but you have it. 

Every time you create a new archive the OS will automatically append a version number to it. You don't have to bother and you can access date time informations on the archive's details panel. If you want to go further I suggest to rename the archive prefixing it with de current time in a "YYMMDDHH" format. Now the version number is given by the version time and all your archives are alphabetically sorted on your file manager view.

Of course there is a price to pay for this simplicity. It's space. You are going to need a lot of space if you version your project often. Luckily external drives are cheap nowadays and even cloud storage is not that expensive.

You can create your versions into your Dropbox folder so they are cloud stored right away and when you reach home you move the old ones to your gigantic external drive for a permanent storage.

So what about automation? Well so far we considered only manual backup and versioning strategies that you can trigger very quickly, but of course you want to schedule your backup strategy.

The easiest possible solution is Mac' Time Machine which by default will backup all your computer every hour. You can even trigger a manual backup by choosing "backup now" on the tray icon. Some advantages are a computer wide backup, the restore user interface and the native support in every Mac. The main drawback is that you need to live with your gigantic external drive always plugged in. And if you are not a Mac fan then there is no drawback, there is a problem. TimeMachine is available only on Mac, but I am sure there are likewise solutions for both Wibdows and Linux, if you know one please post it as a comment and I will integrate.

Another great backup tool is Carbon Copy Cloner, again is a Mac tool. CCC creates a bootable clone of your machine and you can schedule it the way you like it. I use CCC as disaster recovery strategy. I clone my machine at least once a week so if I loose my machine, they stole it or my dog play with it I can buy a new one and clone it back. In few hours I can be back on track. This is also a good strategy when I simply change my machine for a new one. It's almost 8 years I do like this and I never had a problem with it.

For the whom who wants to play a little bit with some scripting my suggestion is to buy a cheap hosting service which provides an FTP access. With this tool and some bash code you may be able to automate the archive & versioning of your projects adding also a remote upload feature.

In fact to do a backup on an external hard drive is far to be sufficient to preserve all of our data. External drives are getting cheaper and cheaper and that means that they are also more prone to failure. Wil you be happy to pay hundreds of dollars to extract your photo archive from a ruined disk? I bet you will pay but you will be really pissed off!

The trick, again, is no more complicated that reducing the risk by spreading your backups on more than one drive. 

I keep my Carbon Copy Cloner disk at home and the TimeMachine one at the office. All my data is redoundant in two drives that are geographically far one from the other. My data can survive me coding drunk, a robbery, a fire and even an heartquake! With this strategy in place I do sleep tight.

To conclude this article the takeaway is: think simple as making a copy of your project before to try something new. Make a clone of your machine before to try some unknown software or script. Backup I more than one place, use Dropbox, Google Drive and any other remote storage service you can put your hands on.

Sleep tight on night and live a happier life!


