# On finally learning to program at the age of 40

This year I finally learned to program at the age of 40, after failure after failure despite having taken to computers like a duck to water and being seemingly destined to enter IT as far back as elementary school. Maybe it'll be of some use to you to show that it's never too late, or that sometimes you just need to find the right language to make it happen.

Programming for me started back in the 1980s with our first computer. It was an odd beast called an ADAM Computer, and looked like this:

![](Coleco_Adam_(adjusted_version).jpg#thumbnail)

<sub>*Image by [Andrew Lih](https://en.wikipedia.org/wiki/Coleco_Adam#/media/File:Coleco_Adam_(adjusted_version).jpg) under [CC BY-SA 2.0](https://creativecommons.org/licenses/by-sa/2.0/).*</sub>

It was a sort of hybrid of personal computer, COLECOVISION gaming system, and a typewriter. The computer itself is as you can see in the image, with two tape drives in place of a disk drive or cartridge, an actual TV instead of a monitor, and an interesting printer that had a switch on it that let you turn it into a full-blown typewriter. A lot of other ADAM computer users had actual disk drives but we didn't, and the tapes took forever to load. They would make this sound for about a minute or two: rrr rrr rrr REEE, rrr rrr rrr REEE, rrr rrr rrr REE, rrr rrr rrr (repeat). rrr is the slow moving forward sound while REEE was a quick rewind, so it must have been reading forward while then needing to move back to the next block that was located behind it. (Feel free to tell me more [on Twitter](https://twitter.com/mithridates) or [on Reddit](https://old.reddit.com/user/Dhghomon/) if you know more about how these drives worked - I'm still curious.)

I remember my dad doing a lot of tape recording in the basement when we first got it, but wasn't sure why it resulted in getting so many games out of it. (My favourite was called [Gateway to Apshai](https://en.wikipedia.org/wiki/Gateway_to_Apshai), a sort of Roguelike game. I asked him about it a few months ago, and it turned out that he used [Forth](https://en.wikipedia.org/wiki/Forth_(programming_language)) to make it happen. Here's what he wrote:

>I used Forth a bit when we had the Coleco Adam computer which had a Zilog Z80 CPU. Not sure if you remember but I ordered a tape from the U.S. (for the tape drive) that came with several hacker programs and a manual called The Hackers Guide to the Adam which allowed us to download ColecoVision cartridge games to blank tapes so we got a ton of games. I didn't write any programs myself but the programs on the tape came with the source code so you could follow the logic. In some cases I needed to tweak the parameters and re-save in order to optimize whatever needed to be hacked. It was interesting and fun to do.

The key point is that he showed me something called BASIC that at the time I assumed was the only programming language in the world. I took to it and followed along with [books like this one called the Mystery of Silver Mountain](https://archive.org/details/the-mystery-of-silver-mountain/mode/2up) and [Hunt the Wumpus](https://en.wikipedia.org/wiki/Hunt_the_Wumpus), and pretty soon had picked up how to program. I began making my own small RPGs based on [Steve Jackson's Sorcery! books](https://en.wikipedia.org/wiki/Steve_Jackson%27s_Sorcery!). 

They ended up like a larger version of this code below copied from Wikipedia with a lot of `RAND` for the dice rolls and `GOTO` calls. I remember having to add finer and finer line numbers as time went on (adding a line 65 in between 60 and 70, then a line 67, finally renumbering the whole thing when I ran out of room) and somehow managing to play a musical score at the beginning of the game along with a single line drawing.

```basic
10 INPUT "What is your name: "; U$
20 PRINT "Hello "; U$
30 INPUT "How many stars do you want: "; N
40 S$ = ""
50 FOR I = 1 TO N
60 S$ = S$ + "*"
70 NEXT I
80 PRINT S$
90 INPUT "Do you want more stars? "; A$
100 IF LEN(A$) = 0 THEN GOTO 90
110 A$ = LEFT$(A$, 1)
120 IF A$ = "Y" OR A$ = "y" THEN GOTO 30
130 PRINT "Goodbye "; U$
140 END
```

All this I had done all on my own in an era well before being able to search for sample code online, and by all accounts it looked like I was destined to work in IT. Meanwhile, at school we were being taught to use something called [Logo](https://en.wikipedia.org/wiki/Logo_(programming_language)). This was way less fun, and involved pretty much just making a turtle draw shapes on the screen. You would give it functions like `FD 90, RT 90` and then make it do that four times with `REPEAT 4` and it would draw a square. Drawing a circle took forever because you would have to do `REPEAT 360` to make it happen, and you'd have to watch the turtle do 360 operations just to make a circle. So sometimes you'd cheat a bit and do `REPEAT 180` and make the turtle move right 2 degrees at a time so the computer would end up drawing pretty much the same thing but only have to make 180 calculations instead of 360.

And then for extra fanciness you can make shapes like the one below where you tell it to do a circle, *then* tell it to turn right a bit and then start the next circle. Wow.

!["Programming" in the 80s](Logo.png#thumbnail)

<sub>*Image by [@susam](https://github.com/susam) under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).*</sub>

Now the funny thing about this Logo experience is that I had almost completely forgotten it until I saw [this video by Bryan Cantrill](https://youtu.be/LjFM8vw3pbU?t=246) who is about my age and also had an early childhood experience with it. For him it was the same: he remembered feeling complete apathy about the whole thing and trying to make this turtle draw. Fortunately for him, he ended up encountering C and getting really drawn into programming. I didn't, but it was my own doing. Here's how it went with me:

So in computer class in the 1980s we would all sit inside a windowless room in Ranchlands Community School in Calgary at our computers and make the turtles do stuff. Being super easy to use, it actually didn't even feel like a programming language to me and a few others who found it easy. The teachers noticed this and told us that there was a Logo competition coming up soon and that we should take part. Memory of the competition is a bit vague but I think it was citywide, or maybe a provincial competition, so that meant the odd experience of seeing kids from other schools in the same room as you. It's always weird as a child to encounter kids from other schools as you try to sum them up and make sense of who are the cool kids, who aren't, and what their school vibe is like. So a few of us from our school went, we got into teams, and were supposed to put something together that impressed the judges. It went on for two or three days where we would do some work there at the competition, do some more at home, and finally have a product for the last day that gets judged and hopefully wins a prize.

This was where the apathy began to *really* sink in. My teammate was a lot more into the competition than I was, and my lack of interest was starting to show. Eventually we put something together that I think got in 4th or 5th place, which he was unsatisfied with. I felt relief though as by the time the competition ended I knew that this world of programming was something I wanted absolutely *nothing* to do with, and I didn't want to win and be sent to some other competition as a star Logo programmer. Back then just being good at computers = nerd, and my life's goal at the time was to get the girl I had a crush on throughout elementary to like me back. So even up to then I had been keeping a distance from computers when out in public so that I could maintain the image of "Yeah, I'm good at computers but I'm not a *computer guy* or anything".

So after the two or three days of watching the Logo-proficient and what they had put together, we got a t-shirt and a bottle (I think) for participating, and that was the last I ever did anything with it. Meanwhile BASIC continued for a while until we switched the ADAM computer out for a [386](https://en.wikipedia.org/wiki/Intel_80386) one day in the early 90s and I forgot all about it. The problem was that there was no internet to quickly search for code samples, and I wasn't about to actually go and spend money on a book about programming that for all I knew would take me back into that world of competitions and (I was sure of it) probably rejection from the girl.

By the way, here's the line from the Bryan Cantrill video above that brought it all back. His first experience with Logo:

>I was reflecting on all the languages and I guess the first language I ever used was Logo, which in hindsight was kind of child abuse. Logo is awful. And if you read the Wikipedia page for Logo now, you'd be like "Well, this is fine. It's like a Lisp dialect that influenced-" It's like no, no, that's all wrong. Logo was a turtle that didn't know how to do anything, and by turtle I mean like a triangle on a CRT that couldn't do anything. And the magic of it was like you would tell it to "box" and it would tell you "I don't know how to box". And I remember, like, I was in third grade in the kind of mandatory computing class as was kind of, of my vintage. And I remember feeling - for someone who wasn't necessarily prone to this - but feeling overwhelmed with apathy that this thing didn't know how to box. Didn't know how to like, make a box. Like, I don't care that you don't know how to make a box. I don't think it cared that it didn't know how to make a box...and then you would tell it, you'd be like "no, you make a box by going, you know, forward 5, rotate 90, forward 5, rotate 90, forward 5, rotate, 90..." and then you would like tell it that that's how you "box"...these kind of four steps. And then you could like type "box" and it would make a box. And I still didn't care, and I don't think it cared. Like, my first exposure to computing was like just like one of total "I do not give a shit at all about this thing."

Update: just received input from my mom about what she remembers of the room where we learned Logo:

>Yup. A small, cramped windowless room. 10 students at a time? Uninspired beginning to learn about computers I think.

Ironically, it was the room that I liked most about Logo class: the dark windowless room was filled with *computers*, which felt futuristic as hell at the time. You would walk [into the side door of the school](https://www.google.com/maps/@51.1184352,-114.1787332,3a,34.3y,281.04h,93.62t/data=!3m6!1e1!3m4!1sVLFZfvR9gzLrvbdzFYkexQ!2e0!7i13312!8i6656), take a quick right and then find yourself in another world composed of a single dark room with whirring computers on three sides. That's why it was more the pity that they were used for Logo and Logo only. Now back to the subject:

So the period from the 90s to the 2000s involved no programming whatsoever. Two things did happen during this period, however, that proved to be crucial: I became a huge fan of Star Trek: The Next Generation, and of Ultima 7. As Data was my favourite character, I would often ponder how Dr. Soong might have put him together, and how long it would take for us to reach that stage. As for Ultima 7, just [read this post](http://www.chrisguincreations.com/the-drawing-board/16dqd44vpx1eae5tqw17p81itqblwi). The post sums up how I felt about it here:

>Ultima VII was perhaps the first game I ever played where it seemed clear that the world did not exist merely to serve me as a game player.  The store owners did NOT keep their stores open 24 hours a day for my benefit.  If they were at dinner or asleep, I was out of luck. If I invaded someone's house, they yelled at me.  If I broke all their jars and looted the (mostly useless) stuff inside of them, the jars did not respawn when I left the house and came back in - they were broken for the rest of the game.  It felt real in a strange way.  Goofy as it may sound, it's like there was a world I was visiting. 

![Ultima 7](Ultima_7.jpg#thumbnail)

I had and still do have the same feel when I play Ultima 7: the world is so packed with detail that I'll play it even now just to go talk to people, visit bars and watch the people read the numerous books, and just walk around the world and see what happens.

So this period was crucial to making me interested in programming again. Programming wasn't about turtles and depressing competitions anymore, but could be about science fiction, movies, fantasy games, music, and everything else I considered to be cool and worthwhile in life. I knew by then that there was a language called C++ that was used to make games, and maybe it could let me make an android like Data and games like Ultima 7 one day, but I had no connection to programming anymore and the internet still wasn't a thing. That gave me a certain (okay, a lot of) veneration for C++ but I had nowhere to go from there, and my main interests were elsewhere.

Eventually I moved from Canada to Japan, then Korea, [where I learned that language too](http://www.pagef30.com/2013/02/how-i-learned-korean.html) and continue to live. 

One day I met a Korean-Canadian guy from Toronto who was working in Korea as a programmer, which piqued my curiosity. As an ethnic Korean he was able to work freelance without needing a strict employer to allow him to keep his visa, and would just sit at Starbucks all day and program in two languages that he said were called PHP and Python. I knew the name PHP, but thought it was just the name of a bulletin board thanks to an [expat bulletin board](https://forums.eslcafe.com/korea/viewforum.php?f=1) that was popular at the time and built in PHP 3 (and still is!!!!). He told me that I should give them a try since I pick up new skills quickly and it would only help my career. He said that he recommended Python out of the two, and that I should start out with that.

The first experience with Python was more or less utter confusion with only a few small successes. I remember reading threads about Python 2 vs. 3 and how 2 was so much better and that 3 was being forced down everyone's throat. Whatever that means. I noticed some familiar things like `print` but the familiar `$` was nowhere to be seen, and there weren't any line numbers or `GOTO`. I managed to put some things together without a main function, but didn't really know how a program went from start to finish without line numbers and other such helpful things. 

Even worse, by then the internet was useful enough that it was easy to find discussion after discussion of the benefits of one language vs. another. I noticed that there was another language called Ruby that seemed more like my style, so I gave it a try for a bit. Then I saw that there was another one called Lua that felt like maybe it was made for me. I couldn't figure out how to install or use it, but I was kind of convinced for who knows what reason (syntax I think, or had read somewhere that it was easy) that Lua was what I wanted. I had some vague idea that this was the easiest programming language one could learn and if I just learned that well I could just sort of pick up all the others later on.

A few months later I met the same friend at a Starbucks and he asked me how Python was going. I told him about how I felt like Lua was the language for me, without giving any real reason why, and clearly hadn't grasped how to code yet. He eventually commented that "Eh, maybe it's just not in your genes." I insisted that it was, somehow. How could it not be? I learned BASIC by myself when I was in elementary, I knew I had the genes. I just had to get really into Lua and learn it well...or should I learn Javascript? People are saying you should learn that first...no, Python. Although I do like Ruby better...shouldn't I just learn that and I'll pretty much know Python by the end anyway? And on and on it went until I lost interest again. I did eventually learn [how to take user input in Python and use it to return results](http://www.pagef30.com/2010/04/creating-necessary-and-useful-content.html), but if I remember correctly I don't think I used a single external function to do it.

I ended up living in Canada again for a few years, and programming was nowhere on the radar. I was at a company called TransCanada Pipelines where becoming a good project controller (or similar position) was key for the employees in our group. The only programming-related event during this period (2011 to 2015) was one time when we were implementing SAP and we heard that there were all these C++ guys in the other building. They were contractors that were there to customize SAP for pipeline and other energy projects, and were getting paid gobs and gobs of cash doing it. This was during the era in Calgary when there was so many projects that you more or less couldn't get people out of bed for less than $100. Summer students napped at their desks and still didn't get let go because even the little bit of help they provided was better than nothing...but eventually that era ended too.

Oil prices crashed in 2015, so did the Calgary economy, and our entire team was let go. With a nice layoff package I decided that this was the time to really learn to code. During this time in Canada (2011 to 2018) all I wanted to do was return to Korea, and I considered either finishing university or learning to code, and decided that the latter was the way to go. Maybe I could get really good at it and get a position in Korea that allowed for a proper visa this time. It actually turned out that finishing university was the right choice (and that's how I did end up back here), but in the meantime in 2015 I opted for this instead of university, and finally got a feel for what Python was. I picked up how to write functions, how to make objects, etc. but the `self` keyword was still confusing and so was using objects. A bit more effort would have sufficed to get over that, but just then the old wanderlust struck again:

- "Python's horrible for making games - this won't let you make anything like Ultima 7." 
- "Why not try out C++? No, that's too hard. How about C#? Let's try that."
- "Wow, this is pretty complicated. Still, looks like C# is the way to go! Wait, what's this? F#? This language is really cool. Why aren't all languages like this?"
- "F# is awesome! Why aren't more people using it though? Maybe I should finish properly learning Python..."
- "So Python it is, nice and easy! Unless it's Javascript. Then I can do anything in just a browser. Maybe start with some browser-based games? Time to give that a try..."

Then the layoff package money started to dry up and it was time to find work again. Upon getting another job, I went downtown one day to celebrate with the former coworkers. Across the room at the coffee shop somebody called out my name - it was an old friend that I hadn't seen since the mid-90s. He was working in finance and asked me what I was doing downtown in Calgary, and I told him that I had gotten a new job that started the next week. "Oh, I bet it's programming! You were always so good at that." he said. I replied, "Oh, not programming...I haven't really done any of that for a long time. It's in project controls."

The job in project controls was fine, of course. But I remember this conversation well because once again it got me thinking about why I had never learned to code when by any measure I seemed destined for it when I was young. I was too busy with other things though to give programming another try.

I finished university, returned to Korea in 2018, and in August the next year gave my notice as a copywriter at the company I was working at the time. With a month left until my last day, I started to think about picking up another skill - maybe *really* learning Python this time. I could put in a few hours a day, get pretty good by my last day, and then spend a month or so binging on it before it was time to find work again. So I did that for a few days...and the wanderlust struck again. "Fine, you can look at other languages a little,"  I said, "but you have to keep Python as your focus. Just an hour or so a day and Python for the rest."

That was when I gave Rust a try for the first time. I had read a bit about it and heard that apparently it was really precise and tough to learn, but that people who loved it swore by it. More importantly, it was very performant. It looked like a nice tough language to take a quick look at before quickly fleeing back to the safety of Python.

I started with Rust on [learn x in y minutes](https://learnxinyminutes.com/docs/rust/) and the [Rust playground](https://play.rust-lang.org/). Curly braces to capture variables to print was the same as Python, but a lot of it looked like the C# that I had tried out a bit before. As I started to learn it I checked to see what you could do with this language, and the answer was invariably *pretty much anything*. So I could make something like Ultima 7, or anything I wanted. But what was even more interesting was how the detail and the low-levelness of the language did nothing to turn me off: I found myself drawn in even more. It's probably the time spent growing up in the 80s that has something to do with it as I felt a lot of nostalgia as I got more and more into the language. Everything I wrote was turned straight into a binary and I could see the computer's internals again. Tons of Rust discussions were about how to optimize code, and I found this fascinating. But at the same time this language was high-level and safe enough that I didn't need to worry about shooting my foot off, so to speak. It felt like a language that, if I devoted myself fully to it, could make almost anything possible (at least as far as a single language can do this) - and that's why the wanderlust completely disappeared.

Who knew that this sort of code would do the trick!

![100](Rust_love.png#thumbnail)

[Programming Rust](https://www.oreilly.com/library/view/programming-rust/9781491927274/) was too much for me on first reading (too many references to C++ and C for one), so I read [the Rust Book](https://doc.rust-lang.org/book/) and then came back to it, and ended up enjoying it the most. What helped the most though was binging on videos of live coding streams. The first one was the 70 or so videos by [Brooks Builds](https://www.youtube.com/watch?v=SRDqvQqWAuE&list=PLrmY5pVcnuE_dyWibakRuGJcuiwAkhGZB), a Javascript developer who recorded himself going through the Rust Book every step of the way. There's something about watching someone struggle through a language that you are learning too that makes you mentally participate in a way that other types of streams can't do. I had the same experience with the [Lernen to Talk Show](https://www.youtube.com/playlist?list=PLF3lNEjv7avTzYQwXU4DssdwRvG35O7Ei) in German by a guy who recorded himself every week in Germany as he learned the language and got better every video. Watching the person struggle when you know the answer is probably the part that brings you in the most. ["It's mit einer deutschen Familie, not mit einem deutsche Familie!"](https://youtu.be/8BnZAXFAiHg?t=231) or "Just use into_iter() and it'll compile!" are the moments where you feel like you're really learning alongside someone else (and in fact you are) and this can't be replicated by someone who has already learned the language and is already typing or chatting merrily away without a single error.

After that I started watching [Brian Myers](https://www.youtube.com/user/bcmyers05) who also learned Rust basically by binging. [Jon Gjengset](https://www.youtube.com/channel/UC_iD0xppBwwsrM9DegC5cQQ) I was saving for last (this was before he started Crust of Rust to teach simpler things) and in the meantime also watched all of [Hello Rust](https://www.youtube.com/channel/UCZ_EWaQZCZuGGfnuqUoHujw), [Ryan Levick](https://www.youtube.com/channel/UCpeX4D-ArTrsqvhLapAHprQ), [Doug Milford](https://www.youtube.com/watch?v=Az3jBd4xdF4&list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5), [Tensor Programming](https://www.youtube.com/watch?v=EYqceb2AnkU&list=PLJbE2Yu2zumDF6BX6_RdPisRVHgzV02NW), [this Rust crash course](https://www.youtube.com/watch?v=zF34dRivLOw), [the Rust videos by dcode, etc.](https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL) (not all in that order) One other stream I enjoy is [rhymu8354](https://www.youtube.com/c/rhymu8354/videos) who is a 25+ year C++ guy who has made his own Ultima 5-ish game and started Rust recently.

So after about six months of that I found that I had properly learned to program for the first time in my life. There was no secret to it: it really was just the single focus and the binging that did it. Having only a Surface Go, I made sure to steer clear of anything with too many external crates but I made some things like a [hanja converter](https://www.youtube.com/watch?v=jc1UvlBnKRw) (hanja = Chinese characters as used in Korea) that worked just great, and eventually I put together a textbook called [learn Rust with easy English](https://github.com/Dhghomon/easy_rust/blob/master/README.md) in order to make the language easy to learn for English L2 speakers without a translation of the Rust Book in their own language, or just people who want a plain introduction to the language. I just finished that book last week. I have yet to put together anything earthshakingly impressive in Rust but at least when someone else does I can read along and follow what they did! It's incredibly satisfying to take something so unfamiliar and make it familiar after a lot of hard work.

The moral of the story I guess is just the classic "find something you like and keep doing it". This wasn't new to me (I *really* wanted to find something I liked), it just took me that long to find the language that fit. And the other nice thing is that it has made other languages so readable and approachable, even C and C++ (well, only kind of for C++), which I read for the first time a month or two ago. It's also *really* weird (also fun) to look at something like Python again that just works without any of the specifics that you use in Rust. It feels like everything is generics but no traits, while you need to give the right input to avoid problems down the line. Meanwhile, Rust's compiler works more along these lines: "No, that's wrong. No, those are two different types. Try dereferencing. You didn't declare that mutable yet. You gave that value to another variable so you don't own it anymore. That reference might not live long enough, try again. You didn't tell me what to do with all the possible variants of the enum." until it finally works - but once it compiles, you have something that is more or less already debugged. 

For anybody else, I hope this will show that 1) wanderlust and lack of focus isn't necessarily forever, and 2) depending on your personality type, maybe the easiest language isn't necessarily the one that you will take most strongly too. It brings to mind the discussions on places like [/r/languagelearning on Reddit](http://old.reddit.com/r/languagelearning) inevitably started by someone who "really wants to learn (famously Language X) but should I just keep up with the easier Spanish/French/etc. even though I hate it and really just want to learn Language X?" The answer there is always of course not - just learn the language you want to learn. I imagine that this advice is easier to give for something like natural languages that are not so tightly tied to a career path as programming languages are, but since programming languages have a lot of carryover as well, maybe the same advice could work here too.

But then again, I'm not sure. I'm already gainfully employed doing other things unrelated to Rust, and the only career I can see with it at the moment considering my background and where I live is helping companies over here implement it. It's certainly not the type of language that you learn in order to be a junior programmer in a big team, much less at the age of 40. But if you're the type of person for whom the skill of programming itself has proven elusive time and time again, maybe finding the right one, regardless of which one it is and how useful it is, could do the trick.
