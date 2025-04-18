[Resume](../resume_page.md) [Projects](../projects.md), [Blog](../blog.md)

# Programming Langauges I've Tried
I figured that as I'm not going to write an exhaustive list of programming languages I've worked with on my resume (Mainly because a lot of them I'm not actively fluent in, or I haven't used in a number of years so I'm out of practice with) it would be a good idea for me to have a post where I can list out every language I've gotten to hello world or later with. I won't be including any joke languages or childrens languages as I don't consider those worth noting given nobody has seriously built anything of note with them outside of jokes. That being said I will include low code systems as they attempt to be things that people can build real things with.

I have created a repo which I've called language notes on my github. THe idea of the repo for me is to have a generic repo which I can dump code chunks into for disparate lanugages. For example, doing hello world in F# is not going to be worth having its own repo, but being able to remember how exactly that toolchain works with a simple notes file and how to do simple things like, for loops, if statements, function calls, etc is useful to have on hand. I can then return to each language and write similar programming exercises in each of them.

# Language Notes Repository
So I've been interested in expanding my programming languages repotoir, and I've decided on a plan to systemize my progress. Essentially I've found that if I'm just working on my projects without some sort of defined goal I end up losing interest or going in circles. With something as nebulous as expanding my language repotoir it's going to be even worse as one can either dig in super deep or just skim the surface. To that end I've started a language notes repository which I'm going to dump hello worlds and more for each language I try. The goal is not to master any one language but just to have seen the tool chains and gotten things setup at least once. My idea is to first add hello worlds, then add maybe prime finders, then maybe windowed applications, then maybe conclude the languages on a simple game like pong.

This has had the secondary benefit of making my most used languages chart look weird with a bunch of languages that I've used slightly populating my list just because I personally find the idea of it amusing. I may expand my goal of familiarity to say that I want to make each of the languages take at least 0.1% of my public github code simply to ensure that I'm fleshing out my own understanding. 

# Exercise Plan
For each language I intend to write a handful of items each item I'll squash into a singular commit, and I'll try and keep a consistent scheme with regards to my commit messages. 

- Hello World. Adding the folder for the specific lanugage and a basic hello world application to show how to write to the console. 
- Prime Number Finder. Find the first 100 Primes, expanding out notes as appropriate to cover things like calling functions, creating variables, and other language quirks. 
- File Operations. Grab a list of every file either on the drive or below it in the directory tree. Provide some basic stats on that collection of files (Count, Size, and maybe others)
- Windows. Possibly adding a user interface to one of the other exercises if appropriate. 
- Simple Game (Pong, Brick Breaker, PIG) whatever I happen to feel like at the time of creation.

So far I've just created a bunch of hello worlds, and one prime number finder for COBOL of all lanugages. So we'll see how well I actually stick to this broad strokes plans. 


## C, C++
The core of most embedded systems. At some point I need to take a look at GCC as it must be the easiest language to port to a new platform. I want to get back into these languages as the low level nature of them means that you have to think more about what you're doing. That being said, you still end up relying on higher level libraries if you're going to create anything serious in these. It's for this reason that I never really got to the point of writing GUI programs in here, that being said I really would like to give it a go. 

## C# and .NET
Microsoft's darling I want to do a lot more in this language as it seems like a nice balance between the lower and higher levels. A lot of the .NET libraries could use a serious upgrade in terms of their documentation. I've built a website using this combination; however, the sheer number of ways of doing everything with the same framework, and the incomplete documentaiton sources really makes it a pain to jump in and out of this language. Ideally I'd love to get into a month or two long project where I don't get interrupted with other work so that I could really learn to love the .NET environment.

## F# and .Net
Not as talked about as it honestly deserves to be, but it's a reminder that the sharp is partially for the dot net integration. This language is a functional programming langauge with a syntax that I found quite usable. I don't have many ocassions to use functional programming; however, it's been a nice one to experiment with. 

## Q# Programming
The Q Sharp programming language is a quantum computing programming language. They can be run in simulations or even deployed to azure. It seems like a fun way to try and implement random things in a way that they would at least in theory run on a quantum computer. At least It can allow me to stop viewing quantum computers as some sort of strange magical thing.

## Visual Basic (.NET)
Another Unjustly hated language, Visual basic was one of the first lanaguages I learned. It's hated for the lack of efficiency, which is honestly rich considering that python has become as popular as it is. The thing that's nice with visual basic from my perspective is the easy creation of user interfaces, combined with the plethora of libraries to handle all the fundamentals making lots of complicated operations significantly simplified. 

Currently the Visual Basic ide of choice is Visual Studio, which is somewhat frustrating when VS Code exists. Microsofts insistence on maintaining the secondary IDE for free versus paying users is not exactly my favorite decision; however, it is understandable. The overall setup of the language is super convenient for creating simple desktop utilities and items of interest which can run on Windows systems with cleanly managed install and uninstall being handled by the platform.

## Python, MicroPython, and CircuitPython
Python is an easy going language that I'd recommend for anyone who has enough clock cycles to spare. It makes things easy and quick to program. Whatever you want to do there's a python library for it. If you need efficiency then start running for the hills as outside of items where you can rely on a foreign language interface for fast code you're kind of stuck with painfully slow operation. The embedded system versions are an interesting case of people insisting on developing in a language they're familiar with, and honestly the speed and ease of development are underrated for a lot of applications. Processing even in embedded environments is now so far into the crazy pants region that if you're not optimizing for power consumption or cost or something else difficult, Micro Python is a good option. 

If you're going to ask me the difference between Micro and Circuit python. Don't. Beyond the fact that Circuit python appears as a USB drive with the code exposed directly there for easier editing in-situ, I'm honestly quite unsure as to adafruits motivation behind their variant of the languge. That being said if you're working with their platforms you can be assured of good libraries working in Circuit Python which may be enough to sway you to their platform. 

## Matlab and Simulink
A properietary language by Mathworks it used to wear a solid crown of gold for its mathmatical operations; however, the growth of python libraries has slowly eroded its fan base. Even in academia where it's still quite popular there's a bit of a growing feeling that why would you develop in matlab when you could devleop in python taking advantage of all that openness. The libraries for most fields of engineering are really where it still shines; however, even that is slowly being surplanted by specialized python libraries. 

With singualar libaries ranging from $500 - $5,000, I think that the only hope for Matlab to remain relevant long term is to open up their language as a whole while charging for their libaries. The most basic Matlab license is $980, add a simulink license onto there and you're looking at $1,480 more. This is insane when I can pop onto python and do most operations just as quickly, if not quicker thanks to the internets familiarity with Python making resources more easily available. 

## Rust
I've never done a major project in rust; however, I've tutored it. And honestly having to learn it in that fashion just ahead of a student. It was the right call. It's a really nice language for efficient operation, and while its memory safety features makes it painful to code in at times, it also makes it a delightful challenge to get done whatever is needed. Their package manager system is great for running and compiling code with one of the many crates that provide higher level functionaltiy so that you don't need to. 

## Go 
Not a bad language. Taught myself a bit of it over a couple of evenings. Mainly just to the hello world level; however, I can see why the language is popular with so many developers. I considered recreating and improving upon some VB.net code I wrote in high-school; however, I ended up running into issues with out of date libraries and decided to hold off on the project, or swap to something simpler if I chose to rewrite the code. 

## Ruby
I maintained some Ruby code at one point. Not a bad language by any means, and one I'd be interested in working in again. This site itself is technically running via ruby I'm fairly certain as github pages uses Jekyll in my setup which is a Ruby libary for simple static websites. 

Jekyll is a a useful system for any sort of quickly thrown together site that doesn't require a lot of fancy features to work. It's HTML, CSS, Liquid, and Markdown. Nothing else. You don't want to be trying to update these sites dynamically, the closest I'd say is reasonable to do here is to use scripts combined with a CI system to create new commits and redeploy the site at periodic intervals. There is some form of password protection available, but it's not built in by default and appears to be as basic as singular passwords for pages, no hope of adding logins or the like.

## Java
Unjustly hated, this was my primary language through high school primarily surplanted due to a lack of time. It's fairly rigid structure can be a real boon to anyone learning. I saw recently that in the latest verison they've relaxed some of the rules, and this upsets me greatly. Not every language needs to be python. Python is all the Python that the world needs. Java is definitely a language for those who are very much fans of using lots of classes in their code, with a heavily object oriented basis it can make developing larger applications simple if the class structures are appropriate genericified. 

Probably the reason that most people are learning Java at an early age now is to be able to effectively create minecraft mods. Something that me and my high-school friend group quite enjoyed doing.

## Javascript (and friends)
An unfairly liked language. With all of its quirks it's a miracle to me that it became as popular as it has; however, it now dominates the internet. Alongside its children, libraries that make it honestly look like a completely different language. React the little atom iconed library by facebook is responsible for so many user interfaces its kinda silly.

Under Javascript you get Type Script which essentially adds typing to the language. It's my recommendation to find one and stick with it as you'll be jumping between systems forever if you don't settle down here and decide which setup you'll get familiar with. If you're unlucky enough to hop between languages like a pinball in a very enthusiastic game, then hang onto an AI programming assistant and hope that you can make the constant transition. 

## Erlang
I just started learning this language the other night and it was what inspired me to create and document this list. It's an interesting functional programming language. I'm particularly intrigued by the prospect of it deployed on embedded systems where the process system and the shift towards threads may allow much more to be done with much less effort on embedded systems. Effectively adding a form of built in RTOS without the need to handle all that overhead directly. I did find one project which apparently runs it on the RP2040, so I'll be intrigued to give that a go. 

Learning a bit more Erlang I'm struggling to figure out an ideal project to really sink my teeth into the language. Part of the issue does happen to be the user interface which is not Erlang's strong suit, generally recommending that people instead start with Erlang for their logic, then build the user interface seperately communicating through sockets or the like. Not a bad solution to the problem by any means, but also not necessarily my favorite. 

## Bubble.io
Go to bubble.io to make low code/ no code applications. And if you're creating a simple database application which can somehow afford to pay upto $349 per month, it may be a dream platform. What I can say is that all of these low - no code platforms are genuinely great applications within their narrow field where their set of tools is actually relevant. As soon as you start having to plug in some custom code in places, you're heading straight for the realm of more money than it's worth. It's very similar with automation platforms which purport to be no-low code, you may get lucky and they have just the tool you need in which case you're basically set with a powerful system that was able to be built in an hour; however, if you're in the real world something will be different and you'll end up not being able to fully utilize their automation, or need to highly customize something to make it work.

Honestly I wish some of these platforms would start selling standalone/ self-hosted platforms as that would likely be something I'd purhcase. 


