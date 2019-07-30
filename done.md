# Done

First off, a caveat. I am most certainly not qualified to judge any of
the writings I judge, so please see everything I am writing as notes to
myself to remind me of key ideas in the paper or book at hand and what
I thought of them. They are as biased and right and wrong about things
as I personally am. So if you do not trust me as a person, do not trust
my write-ups.

## Computer Science

### Papers
* [Growing a Proof Assistant](https://williamjbowman.com/resources/cur.pdf) by **William Bowman** (2016)

I am hesitant to write anything about this paper at all, as it is a draft
and subject to change. I will, however, write down a few things that came
to my mind when I first read the paper. Maybe I will reread it when it is
done.

The paper presents a racket lang implementing a proof assistant. The key
idea is to make proof assistants easier to extend and work with apart
from writing proof. Maybe I am missing something obvious, but for me
most of the features presented before chapter 5 are not actually features
of the lang at hand but of Racket itself. After a long-winded motivation,
we finally arrive at the notion of tactics in Cur - the language at hand -,
which are interesting and definitely worth the read. My major problem with
the language is that it sacrifices a convenient syntax to write proofs - the
sweetexps are not really helping much - to make it easier to integrate into
Racket. The proof system looks a little clumsy to me, but we gain extensibility
for it. If that scratches an itch, it might be useful, but I really think
the syntax does not help to make the proofs themselves readable.

* [Parsing With Derivatives - A Functional Pearl](http://matt.might.net/papers/might2011derivatives.pdf) by **Matthew Might et al.** (2011)

Beautiful little pearl on how to make Brzozowski derivatives usable
for real-world parsing through performance tweaks (memoization, fixpoints,
laziness). Uses Racket code (which helped me a lot with understanding
some of the underlying equations).

* [Simply Easy! An Implemenetation of a Dependently Typed Lambda Calculus](http://strictlypositive.org/Easy.pdf) by **Andres Löh et al.** (2007)

Interesting implementation of a dependently typed lambda calculus.
The paper is worth reading for the description of current Haskell
programs alone: "a ghastly hodgepodge of generalized algebraic data
types, multi-parameter type classes with functional dependencies,
impredicative higher-ranked types, and even data kinds." Some of
the figures completely puzzled me (e.g. figure 10 on the type
rules in the language that is being laid out), but I am used to
that in type system papers. The rules are usually explained in
the text anyway, so I just skim the figures.

The main contribution of this paper for me is not that it shows
dependent types are possible to implement (anyone who has heard
of Agda, Coq, or Idris will know that by now), but that it can
even be straightforward. The implementation given in the paper
is mind-boggingly simple, and I think that is pretty amazing.

* [Situations, Actions, and Causal Laws](http://www.dtic.mil/dtic/tr/fulltext/u2/785031.pdf) by **John McCarthy** (1963)

Another one of these classic papers that I had missed. I don’t
think I completely understand the paper, although, as per usual
McCarthy does not fail to instill a lot of thoughts in my slow
mind. His idea of the Advice Taker is an interesting forgotten
concept (probably due to the AI winter, though I am not around
long enough to really judge that).

His relational approach to the computational view of reality
reminds me a lot of Prolog, obviously, although I am unsure
how much Prolog was really influenced by the Advice Taker (I
should probably read more about that as well).

* [Reflections on Trusting Trust](http://www3.cs.stonybrook.edu/%7Ecse509/p761-thompson.pdf) by **Ken Thompson** (1984)

While I do not fully agree with the moral view of the world
presented in this talk, I think the idea of a malicious compiler
is cute. It has not occurred to me yet but is obvious when
you think about it - a trademark of interesting ideas.

* [Out of the Tar Pit](http://shaffner.us/cs/papers/tarpit.pdf) by **Ben Moseley and Peter Marks** (2006)

The essential paper on FRP. Apart from giving an excellent
introduction into what FRP is and should be, the authors
also spend a great deal of time on explaining how different
programming paradigms deal with state and complexity and
their individual shortcomings (that were supposedly overcome
through FRP).

Great paper, very long, but - at least in my opinion - out
of necessity, not borne from babbling.

* [Type Systems as Macros](http://www.ccs.neu.edu/home/stchang/pubs/ckg-popl2017.pdf) by **Stephen Chang et al.** (2017)

A bit hard to read and involved, but very deep insights.
I might try to recreate in zepto.

The syntax of all of the languages and systems presented
were ugly. That’s not that big of a problem, though, if
one puts a bit more abstraction around them they could
actually be pleasant to work with.

* [Rapid Case Dispatch in Scheme](http://scheme2006.cs.uchicago.edu/07-clinger.pdf) by **William Clinger** (2006)

An inside view into how Larceny does optimizations of `case`.
Interesting if a bit complex and hard to read if one is unfamiliar
with reading intermediate form Larceny programs. The examples
are rather simple, though. I think the mixing of strategies
to achieve maximum performance sounds like a hard optimization
to get right but worth its while.

* [Do Be Do Be Do](https://arxiv.org/pdf/1611.09259v1.pdf) by **Sam Lindley et al.** (2016)

Frank is certainly an interesting language. I am not quite
sure I understand all of its semantics and implications, though.
Especially the explanation of Core Frank left me not quite satisfied,
but that might just be me and my personal problems with the notation
again. Might have to give that one another read if I want to go deeper
into effects languages.

* [Sketchpad - A Man-Machine Graphical Communication System](https://www.cs.purdue.edu/homes/hosking/197/canon/sutherland.pdf) by **Ivan Sutherland** (1964)

This is one of the most humbling papers I have ever read. The complexity
of the system described—Sketchpad—is mind-boggling, considering the tooling
of the time. I marvel at it in the same way we marvel at things of complexity
that have been built by generations that had to do without the conveniences
and abstractions that we now have. I did not take away a lot in the hard
technical sense, and yet it influenced my thinking greatly already.

* [Hygienic Macro Expansion](http://web.cs.ucdavis.edu/%7Edevanbu/teaching/260/kohlbecker.pdf) by **Eugene Kohlbecker et al.** (1986)

The fundamental paper on hygienic macro expansion. Reads fairly nicely.
I was familiar with the concept before reading the paper, but it really
feels like my basic grasp on the concept is much stronger now. Very
helpful for the system (System Z) I am currently working on, as I will
have to implement it in a language that is not Scheme or even a Lisp there
and that is a fairly badly documented process I find.

* [A prettier printer](http://homepages.inf.ed.ac.uk/wadler/papers/prettier/prettier.pdf) by **Philip Wadler** (1997)

Philip Wadler is my spirit animal. In this paper he essentially conjures
up a wonderfully simple and composable algebra of printing and uses it
to implement a simple, efficient, and readable pretty printer. It makes
me want to implement one of my own. Then again, why would I if I cannot
even begin to capture the beauty of this paper? Very readable and very
pretty indeed.

* [Flattening Combinators: Surviving Without Parentheses](http://www.westpoint.edu/eecs/SiteAssets/SitePages/Faculty%20Publication%20Documents/Okasaki/jfp03flat.pdf) by **Chris Okasaki** (2003)

A theoretical pearl by Chris Okasaki (of "Functional Datastructures" fame).
It shows how to rewrite arbitrary combinators to stack expressions, similar
to what you would to in reverse polish notation. It’s a simple yet very beautiful
showcase of how to rewrite postifx notation to combinators and vice versa
and invents an interesting approach to Gödel numbering on the way, in less
than eight pages. The latter of the two implications is a bit harder to digest,
and less applicable to what I am doing, but relatively obvious, which astounded
me considering I am not a very battle-hardened theoretical computer scientist.
Maybe my reading just starts to bear fruits or maybe it is Okasaki’s pristine
writing.

* [Why New Programming Languages for Simulation?](http://people.csail.mit.edu/fred/why.pdf) by **Gilbert Louis Bernstein and Fredrik Kjolstad** (2016)

Coming from the language designers of Ebb and Simit, respectively, this nice
little summary on why to create new languages is very centered around simulation,
but can be easily generalized. It tries to tackle the age-old question of "Why
should we create even more programming languages?" with a simple answer: better
abstraction, better tools need time to be developed. And we can do better than
we currently are. Which is a nice sentiment that I deeply share, as a hobby/semi-serious
language designer.

* [Lambda: The Ultimate Declarative](http://repository.readscheme.org/ftp/papers/ai-lab-pubs/AIM-379.pdf) by **Guy Steele** (1976)

This paper is filled to the brim with interesting ideas. The symmetry of lambdas
and actors was especially surprising. Rewriting function calls to jumps is not
that new an optimization, apparently, which is also interesting to know; the bit
about implementing tail-recursion as `GOTO` going back to the PDP-1 puts shame to
every language that still does not implement proper tail recursion. And I should
try to play around with the CPS-converter given in Appendix A, that one was really
interesting.

* [Debunking the ‘Expensive Procedure Call’ Myth, or, Procedure Call Implementations Considered Harmful, or, Lambda: The Ultimate GOTO](http://repository.readscheme.org/ftp/papers/ai-lab-pubs/AIM-443.pdf) by **Guy Steele** (1977)

An interesting insight into programming in the 70s. Coming from today it is
pretty much impossible that one learns that using `GOTO` is good for your
programs, neither as an optimization (most modern compilers are better than
average Joe Programmer at understanding how to optimize the program anyway)
nor as a stylistic choice (most blindly obey Djikstra’s quip about `GOTO`
being harmful without having read the actual article, in my experience).
Now, I personally still find that sometimes `GOTO` might be acceptable
(in error handling/cleanup cases, very sparingly, for instance), but
the issue that Steele and adressed in this paper is pretty much accounted
for by now. Maybe I am mistaken, and am in the wrong business, though.

* [Adding an LLVM Backend to Bigloo Scheme](https://gupea.ub.gu.se/bitstream/2077/34201/1/gupea_2077_34201_1.pdf) by **Mikael Brockman** (2013)

An interesting masters thesis on compiling Scheme—more specifically,
Bigloo Scheme—into LLVM. It is surprisingly short and spends very little
time actually talking about the specifics of the implementation, but
the authors approach seems interesting. I played around with a LLVM
backend for zepto that works on the textual IR level, but I did not find
a good way to make it modular and abandoned it after implementing a useless
subset of Scheme; this is to say this undertaking resonated with me.
I should take a look at the final product at some point.

* [SECD: Design Issues](http://prism.ucalgary.ca/bitstream/1880/46590/2/1989-369-31.pdf) by ? (?)

I cannot remember how I found this paper and a quick search for it
doesn’t reveal much information, either. Its title seems to be "SECD:
Design Issues" and it seems to be a report on the work of a research
group at the University of Calgary (led by Graham and Birtwistle,
maybe?), probably in the late 80s or early 90s (89 at least, according
to the citations). It describes an effort to create a chip for the
SECD ~virtual~ machine. It is really interesting and I learned tons
reading it, especially because I have little idea of hardware design
and manufacturing.

* [Exceptional Continuations in JavaScript](http://www.schemeworkshop.org/2007/procPaper4.pdf) by **Florian Loitsch** (2007)

An interesting little paper on how to implement continuations in a
language that doesn’t have them. It’s a bit clumsy if you compare
it to first-class continuations, but this is more or less a given,
at least in my opinion. It also helps my understanding of how to
implement continuations, even if I have already implemented them
myself. If I ever need to do so again, I might look at it beforehand,
as the techniques described in the paper are interesting.

* [Scheme: An Interpreter for Extended Lambda Calculus](http://repository.readscheme.org/ftp/papers/ai-lab-pubs/AIM-349.pdf) by **Gerald Sussman and Guy Steele** (1975)

This paper blew my mind. I had no idea that the initial implementation
of Scheme had such a wonderful actor system. Sure it is a bit more
crude than what we are used to these days, but it is still much more
advanced than I would have expected. The same for the pattern-matching
implementation, which is wonderfully elegant and simple. I could reimplement
a simple pattern-matcher in zepto for a blog post maybe. In general the
code presented in the blog post is incredibly advanced, at least much more
than anything I would’ve thought is to be found in a paper from the mid-70s.

On another note, them basically implementing `Promise.race` and then calling
it useless is wonderfully ironic.

* [i, Poet: Automatic Chinese Poetry Composition through a Generative Summarization Framework under Constrained Optimization](http://homepages.inf.ed.ac.uk/mlap/Papers/IJCAI13-324-1.pdf) by **Rui Yan et al.** (2013)

I have had a lingering interest in AI for a long time, but decided never to
act on it, partly because it is not my domain of expertise and partly because
everyone seems to want to jump on that bandwagon with bad ideas lately. I still
read about it and think I have a pretty okay grasp on the concepts, I just never
had a project that required me to write a truly learning system. With that in mind,
this is still a very interesting paper, because it describes in great detail an
approach to AI writing poetry in a sensible way. It’s a bit annoying that they did
not provide an example poem that was generated—I was really interested in seeing
one of those—, but I liked the idea of having multiple neural nets, one for writing
the draft and one for refining it. That felt similar to how I approach writing:
brainstorm and build, then make sense of the mess you’ve just created. I have always
been a poor editor, so maybe the second neural net would be of greater help for me,
but I assume it will be some time until I can tap into the potential of AI that
helps me convey what I want to write.

* [An Incremental Approach to Compiler Construction](https://github.com/namin/inc/blob/master/docs/paper.pdf) by **Abdulaziz Ghuloum** (2006)

I am not sure I agree with the methodology—and the implementation—provided in
this paper. It mgith be that the reader has implemented a compiler after they’ve
worked through the paper, but the compiler is really bad, the architecture does
not lend itself well to extension, and paedagogically the reader has not gained
as much as they would have with a better engineered, "do things the right way"
compiler. The compiler presented in there is a big messy hack and noone should
have to base their compiler on that.

* [The Security Impact of HTTPS Interception](https://jhalderm.com/pub/papers/interception-ndss17.pdf) by **Zakir Durumeric et al.** (2017)

This paper broke my heart. It is incredible that at this day and age people still
think HTTPS interception can increase security instead of severely decreasing it.
I don’t think I have to say more on that matter. Almost 11% percent intercepted
traffic is damn scary.

* [Generational Garbage Collection and the Radioactive Decay Model](http://www.cesura17.net/~will/Professional/Research/Papers/radioactive.pdf) by **William Clinger** (1997)

The main take-away from this paper is that I am probably too thick to implement
a good garbage collector. Generational garbage collectors are relatively hard
to build properly—I’ve tried and failed before. Larceny is a truly interesting
Scheme implementation. I should try it out sometime, because I thoroughly enjoyed
reading papers about it—its documentation on its compiler passes are pretty
pristine.

* [BigchainDB: A Scalable Blockchain Database](https://www.bigchaindb.com/whitepaper/bigchaindb-whitepaper.pdf) by **Tren McConaghy** et al.

More blockchain bullshit. Yay. This incredibly badly written paper presents a
fundamentally flawed idea—basically a shitty framework to RethinkDB—a database
that’s failed as well, and for good reasons. I know I sound like an ass here,
but I’ve lost patience with people who have no idea about how to build a database
building databases, because I am the one who cleans up after the mess when a
startup ends up choosing that tech and the DB ends up blowing up (mostly because
of configuration flaws, of course, but if your default configurations are
broken, your system likely is broken as well). Bottom line: I did not enjoy
reading this paper.

* [Generalized Parser Combinators](http://www.cs.uwm.edu/%7Edspiewak/papers/generalized-parser-combinators.pdf) by **Daniel Spiewak** (2010)

I actually tried to implement GLL parser combinators for zepto before and failed
at the trampolining, so this paper clarified a lot of things that I did not understand.
I wanted to try and implement a GLL again in the future and after reading this paper,
I feel equipped to tackle the problem. As an aside: Scala code still looks weird to me.
Kind of like I felt reading Haskell before I knew it.

* [Lambda: The Ultimate Imperative](http://repository.readscheme.org/ftp/papers/ai-lab-pubs/AIM-353.pdf) by **Gerald Sussman and Guy Steele** (1976)

I’ve read this paper before, and it is still wonderful. Scheme speaks to me in a
very peculiar way. But, instead of waxing poetic, I will just quote the end of
the paper, because there is a very deep insight for language designers to be
found here: "No amount of language design can *force* a programmer to write clear
programs. If the programmer’s conception of the problem is badly organized, then
[their] program will also be badly organized. The extent to which a programming
language can help a programmer to organize [their] problem is precisely the extent
to which it provides features appropriate to [their] problem domain. The emphasis
should not be on eliminating "bad" language constructs, but on discovering or
inventing helpful ones."

* [The impact of syntax colouring on program comprehension](http://www.ppig.org/sites/default/files/2015-PPIG-26th-Sarkar.pdf) by **Advait Sarkar** (2015)

With a sample size of ten I feel like it would be a bit dubious for me to derive
general conclusion from this paper—especially considering three datasets had to be
excluded from part of the conclusions, reducing the sample size to seven. Nonetheless,
it is interesting research into how effective syntax highlighting really is, because
most of the arguments for or against syntax highlighting seem to be strawman arguments
or highly subjective (I won’t link to blog posts that come to mind, because I’m not that
much of an ass). In toto, this paper is a valuable addition to the conversation about the
cost and gains of syntax highlighting.

* [Fast Deterministic Selection](https://arxiv.org/pdf/1606.00484.pdf) by **Andrei Alexandrescu**

I always liked Alexandrescu’s talks. Sadly, I’ve not yet managed to
try out D, the programming language he is mostly working on except for
his work on C++. This paper presents a fun new algorithm for selection
in a field of research that has not seen great advances since Hoare’s
seminal paper (except for Median of Medians, which builds on it). I
am looking forward to try it out in D and see how it performs. I might
also want to implement it in another language if it performs well.

* [The view from the left](http://strictlypositive.org/view-Dec6.ps.gz) by **Conor McBride & James McKinna** (2004)

I can’t say I understood a lot of it, but I still feel like a learned
a lot, just struggling through it and looking up all kinds of things.
I respect Connor McBride a lot—I was not familiar with James McKinnas
work, but I am will be keeping an eye out from now on—and so that was
rewarding in itself already.

* [I am not a number: I am a free variable](http://strictlypositive.org/notanum.ps.gz) by **Conor McBride & James McKinna** (2004)

Another Epigram paper, but shorter and more approachable, because it
describes the implementation of a specfic feature (syntax manipulation).
It’s probably also closer to my field of expertise and thus easier for
me to understand. I enjoyed this paper as well. That being said, their
insistence of putting an accent on role is a little irritating, because
I don’t understand it—one of the reasons I don’t like The New Yorker
articles sometimes. Also, I like how they talk about their users when
they say: “Our foes cannot choose wicked names in order to make mischief.”

* [Futexes Are Tricky](https://www.akkadia.org/drepper/futex.pdf) by **Ulrich Drepper** (2011)

Indeed they are. This paper is a very useful resource if one needs to
use futexes. It’s not that great for light reading—at least not section
2, which goes into great detail to explain every input for the syscall.
It’s useful, just not made for reading as prose. The whole paper is written
in a tutorial-style, and realitvely instructive. I enjoyed learning about
futexes, in any case.

* [Distributed Algorithm for Optimal Power Flow on a Radial Network](http://smart.caltech.edu/papers/distributedalg.pdf) by **Qiuyu Peng and Steven Low** (2014)

Coming from a field I’ve not had much exposure to, this paper is filled
with lingo I don’t understand. It didn’t prevent me from finding it
intriguing, though, and I think I actually learned something.

* [Optimal Decentralized Primary Frequency Control in Power Networks](http://smart.caltech.edu/papers/optimaldecent.pdf) by **Changhong Zhao and Steven Low** (2014)

This paper is from the same source as the one above, and so I had the
same trouble. Sadly this one also suffers from bad writing; I assume
the authors are not native English speakers. This was detrimental to
my reading experience, unfair as it is. I am unfamiliar with the
territory and the writing increased the cognitive load—not a great
combo.

* [Ornamental Algebras, Algebraic Ornaments](https://personal.cis.strath.ac.uk/conor.mcbride/pub/OAAO/LitOrn.pdf) by **Conor McBride** (2011)

Yet another paper by the infallible Conor McBride. This meditation on
data types and their relationship is based on a simple idea that blew
my mind completely: data types are but a kind of refinement types of
each other, joined by forgetful functions in the one direction and
information-adding functions in the other. Pretty darn clever.

* [Model, View, Controller](http://heim.ifi.uio.no/~trygver/1979/mvc-2/1979-12-MVC.pdf) by **Trygve M. H. Reenskaug** (1979)

Another one of those papers that was incredibly insightful and solved
a problem we still face today, very cleanly. It’s incredibly short,
more of a personal note than a paper, but it cleanly sets boundaries
between components.

* [What Not to Do When Writing an Interpreter for Specialisation](https://www.cs.rice.edu/~taha/teaching/02F/511/papers/jonesWhatNot96.ps) by **Neil D. Jones** (1996)

Pretty dry but highly informative. This makes me want to write a toy
project that implements program specialization. I should probably reread
the paper when not jetlagged anymore.

* [OpenConflict: Preventing Real Time Map Hacks in Online Games](https://www.shiftleft.org/papers/openconflict/openconflict.pdf) by **Elie Bursztein et al.** (2011)

An impressive amount of engineering by the authors went into cracking
online games and then fixing them. Super fun to read and interesting, even
though my knowledge of elliptic curve cryptography is way too basic to
understand the protocol described in the later parts of the paper well.
It is written well enough to incentivize me to keep reading, though, so
all is well.

* [Symmetric Cryptography in Javascript](http://bitwiseshiftleft.github.io/sjcl/acsac.pdf) by **Emily Stark et al.** (2009)

Interesting read, even if it’s a little outdated. I would love to see an
up-to-date version, especially because the benchmakrs where so browser-focused.
A lot has changed since 2009 in browser performance.

* [Why and how to use arbitrary precision](http://perso.ens-lyon.fr/philippe.theveny/cise.pdf) by **Kave R. Ghazi et al.** (2010)

This paper ties in to my lates project, a [reimplementation](https://github.com/hellerve/bc)
of bc. The constant folding part is especially interesting. I didn’t
know about GCC’s usage of mpfr in optimizations either and that section,
albeit short, was especially intriguing for that reason.

* [Designing extensible, domain-specific languages for mathematical diagrams](https://www.cs.cmu.edu/~kqy/resources/diagrams_obt.pdf) by **Katherine Ye et al.** (2017)

Super exciting idea! As a novice to most of the fields I read papers
from—I mean, how many domains can you have domain knowledge in, really?—,
having illustrations definitely helps a ton! Making this simpler, more accessible,
or just having better tooling should help tremenduously in incentivizing people
to build diagrams, which in turn incentivizes me to dive deeper into the field.

* [Visualizing LSTM decisions](https://arxiv.org/pdf/1705.08153v1.pdf) by **Jos van der Westhuizen & Joan Lasenby** (2017)

As always when it comes to papers outside of my limited domain of expertise
I cannot say I understood this paper thoroughly. This time, however, I feel
a little better, because someone with actual knowledge around the topic
presented on it at our ML paper reading group, which is nice.

After concurring that the paper was borderline unreadable, she explained
LSTMs, a very helpful addition. I feel equipped to talk about them more now.
The choice of illustrative examples in this papers was abominable.

* [Painterly Rendering for Animation](https://disney-animation.s3.amazonaws.com/uploads/production/publication_asset/47/asset/p477-meier_1996.pdf) by **Barbara J. Meier** (1996)

A beautiful paper, both in its writing—which is simple, not convoluted,
and does a great job at explaining everything—and its idea, which is
super simple: mixing particle rendering and painterly rendering of still
images. The particle rendering is necessary for continuity between frames,
and the idea seems obvious in hindsight, which is evidence for how powerful
it is.

* [Coherent Noise for Non-Photorealistic Rendering](http://graphics.pixar.com/library/NPRNoise/paper.pdf) by **Michael Kass & Davide Pesare** (2011)

Yet another nifty solution for the shower door effect, this time using coherent
noise. It seems to perform quite well and should be reasonably cheap, so I’m all
for it, though I cannot estimate whether it actually helps with anything.

* [Playing Atari with Deep Reinforcement Learning](https://arxiv.org/abs/1312.5602) by **Volodymyr Mnih** (2013)

Yet another paper from my paper reading group. It, too, was a bit painful to
read through, even though the topic seemed interesting at first. Of course, I
learned a lot about Reinforcement Learning in our session, but I don’t think
the paper would’ve told me much—especially because the data in Reinforcement
Learning is often so different from the data in other flavors of ML. The
linear algebra didn’t help, of course, although it wasn’t _too_ bad.

* [Generating Pseudo-random Floating-Point Value](http://allendowney.com/research/rand/downey07randfloat.pdf) by **Allen B. Downey** (2007)

Extremely interesting algorithm, but I never really generated random floating
point values, so I cannot really say whether the algorithm is any good. It’s
deeply satisfying to read anyway if you’re into numerics.

* [Phyllotaxis](http://algorithmicbotany.org/papers/abop/abop-ch4.pdf) (Chapter 4 of “The Algorithmic Beauty of Plants”) by **Przemyslaw Prusinkiewicz && Aristid Lindenmayer** (1990)

This paper (or rather chapter) spawned a creative coding session, a few algorithmic
experiments, reflections on phyllotactic mechanism in the 2D layout of galaxies,
and an art print for my girlfriend, so I cannot complain.

* [Stylizing Animations by Example](http://graphics.pixar.com/library/ByExampleStylization/paper.pdf) by **Pierre Bénard et al.** (2013)

Wow, this was dense. I can’t say I understood all of the math—but then I don’t
think that’s expected. What I can say is that this is more of a reference
paper than one you would read for fun, but maybe that’s just me. I’m not
sure of the general usefulness of having read it, other than for the issue
at hand (taking pictures and interpolating the frames between them by
models).

* [Gyrophone: Recognizing Speech From Gyroscope Signals](https://crypto.stanford.edu/gyrophone/files/gyromic.pdf) by **Yan Michalevsky et al.** (2014)

Pretty scary stuff I didn’t know about, although I don’t know how I could
have possibly missed it. At first I thought of it as a rather constructed attack,
but as soon they showed that the gyroscope can be upgraded to work at 8kHz
I was pretty scared.

* [The Brigade Renderer: A Path Tracer for Real-Time Games](https://www.hindawi.com/journals/ijcgt/2013/578269/) by **Jacco Bikker & Jeroen van Schijndel** (2012)

Interesting concept, I would like to see it in action. The visual format
of the paper irritated me somewhat, especially the poor quality of the
illustrations.

* [Improving Noise](http://mrl.nyu.edu/~perlin/paper445.pdf) by **Ken Perlin** (2002)

One of Ken Perlin’s seminal papers on noise that led to simplex. I’m forever
grateful to Perlin, mostly for the beauty and elegance of smooth noise functions
in general, and simplex in particular.

* [Efficient computational noise in GLSL](http://webstaff.itn.liu.se/~stegu/jgt2012/article.pdf) by **Ian McEwan et al.** (2011)

Another take on noise; I might steal this implementation for my own GLSL
code.

* [Simplex noise demystified](http://staffwww.itn.liu.se/~stegu/simplexnoise/simplexnoise.pdf) by **Stefan Gustavson** (2005)

The third noise paper today. It just details simplex noise again, and again
in Java, but with a few improvements for speed—and it includes an implementation
for higher dimensions (namely 3D and 4D).

* [An efficient line drawing algorithm](http://staffwww.itn.liu.se/~stegu/circle/circlealgorithm.pdf) by **Stefan Gustavson** (2003)

An algorithm that’s beautiful in its simplicity. I read this not for practical
reasons, and so the clarity of the algorithm appealed to me greatly. I’m going
to write a blog post on this.

* [A Cellular Texture Basis Function](http://www.rhythmiccanvas.com/research/papers/worley.pdf) by **Steven Worley** (1996)

Another seminal paper, this time by Worley. I am fascinated by Voronoi cells
and Worley’s contribution makes them even more interesting to me. The paper is
somewhat hard to read, though, not very hands-on and mathematical. I enjoyed it
because I already knew the concept it explains, but if I hadn’t I doubt I would
have understood.

* [Stackelberg Games for Adversarial Prediction Problems](https://pdfs.semanticscholar.org/2e82/acecef77e72e14eb805b7ee9c145ab00e726.pdf) by **Michael Brückner & Tobias Scheffer** (2011)

My first dabblings into Adversarial AI. While the paper wasn’t too enjoyable to
read, the ideas are quite fun to work with. I’m interested in seeing an actual
application in, say, a spam filter.

Again, going through the paper with my reading group was what actually made me
understand it. Otherwise I wouldn’t have grokked it, I think.

* [Making digital filters sound "analog"](http://quod.lib.umich.edu/cgi/p/pod/dod-idx/making-digital-filters-sound-analog.pdf?c=icmc;idno=bbp2372.1992.009) by **Dave Rossum** (1992)

Short, but interesting paper on analog modeling. I’m told this is another classic,
although I feel like I’m missing the point a little. Maybe I’m not involved enough
to see the appeal.

* [Practical Exhaustive Optimization Phase Order Exploration and Evaluation](http://www.cs.fsu.edu/~whalley/papers/taco09.pdf) by **Prasad A. Kulkarni et al.** (2008)

Very well-written and clear paper on pahse ordering. I was surprised that the
authors didn’t try to keep a list of ordering "prefixes" (i.e. a dictionary
from `sequence of phases` to `current output`) in memory to speed up the
application-maybe the space used by this datum is motr than I imagine?
I’m also unfamiliar with the framework they used, so it might well be an
infeasible idea in their environment.

Then again, some of the numbers blew my mind: “For this study, we stop the
exhaustive search on any function if the time required exceeded an approximate
limit of 2 weeks. Please note that exhaustive phase order evaluation for most
of the functions requires a few min utes or a few hours, with only the largest
enumerated functions requiring a few days.” How is that even possible? It’s
the magic of exponentiality, I guess, but oh my.

There’s more that threw me off about the paper, though. The “results” section
in particular had my alarm bells go off when the authors didn’t detail why they
excluded certain functions from the benchmark and the results. Maybe I’m too
used to thinking in terms of psychology where this kind of methodological error
has poisoned a lot of papers.

* [Opportunities and Challenges for Data Center Demand Response](http://smart.caltech.edu/papers/dcdrsurvey.pdf) by **Adam Wierman et al.** (2014)

This was a fairly interesting and approachable read for a complete newbie like
me. I have no idea how the grid and power distribution acutally works, but the
authors managed to make me feel as if I had a good overview over the state of
the grid and the role data centers play within it now. Highly recommendable,
and I was especially intrigued to hear about the elaborate systems that are
in play between consumers and producers of energy within the grid.

* [Succinct Indexable Dictionaries with Applications to Encoding k-ary Trees, Prefix Sums and Multisets](https://arxiv.org/pdf/0705.0552.pdf) by **Raman et al.** (2007)

An interesting paper for an interesting algorithmic problem that I currently
don’t have. It is fairly theoretical in its description, spending a lot of time
proving various of its properties. Nonetheless, I enjoyed the paper’s problems
and proposed solutions. I might need some more time to think about it and its
implications.

* [How to Write a 21st Century Proof](https://lamport.azurewebsites.net/pubs/proof.pdf) by **Leslie Lamport** (2012)

I’ve been obsessing over TLA+ for the last few days, and reading Lamport’s
papers about it has been a highly entertaining addition to my currculum. I’m
not sure I will ever find the time to tinker with it enough to suggest it to my
clients, but I’ll sure as hell try.

* [Euclid Writes an Algorithm: A Fairytale](https://lamport.azurewebsites.net/pubs/euclid.pdf) by **Leslie Lamport** (2011)

A cute little story that has an underhanded agenda (I don’t particularly like
that, but in this case I was aware what it would be and read the paper for it
anyway). The illustrations are not my cup of tea, and the humor is not mine
necessarily, either, but the contents are educational.

* [On Conditional Branches in Optimal Search Trees](https://arxiv.org/pdf/cs/0604016.pdf) by **Michael B. Baer** (2006)

Pretty intersting paper on the performance of branching. The implementation
of branching using search trees always seemed like overkill to me, but clearly
there must be something there. I’m not a performance expert, after all, and the
explanations provided in this paper are fairly impressive.

* [The Implementation of Case Statements in Pascal](http://eprints.utas.edu.au/126/1/CaseStmts.pdf) by **Arthur Sale** (1981)

This paper is mostly interesting for historical purposes: the considerations
applied to compiler optimizations were completely different, largely driven by
resource constraints that we generally can forget about—this doesn’t mean that
we don’t have problems with the efficiency of compilers anymore, of course.

* [A Superoptimizer Analysis of Multiway Branch Code Generation](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.602.1875&rep=rep1&type=pdf) by **Roger Anthony Sayle** (2008)

This paper tries to be an update for the above Pascal Case paper. One major
update, apart from 27 years of research difference, is that the author actually
tries to go through the data to find out which approaches to optimization would
actually make a difference. This is something that Sale—the author of the 1981
paper—requested, and so, over a quarter of a century later, he got what he
asked for.

* [FSA-based Packet Filters](http://staff.polito.it/riccardo.sisto/cisco/report.pdf) by **Pierluigi Rolando et al.** (?)

Highly detailed paper on packet filtering that highlights a few of the more
interesting optimizations that are possible in filters. I enjoyed the in-depth
descriptions of the algorithms used to reduce memory and CPU usage.

* [The Structure and Performance of Efficient Interpreters](https://www.jilp.org/vol5/v5paper12.pdf) by **M. Anton Ertl & David Gregg** (2003)

This paper didn’t age particularly well in real numbers, but the general
assessments are still more or less true. Of course some of the statements—Java
being 119 times slower than C, for instance—are incredibly outdated, but the
optimizations (threaded code vs. switch statements, for instance) are still
fresh. The title, however is a little misleading, because it’s mostly about
branching, not general efficiency.

* [The Anatomy of a Search Engine](http://infolab.stanford.edu/~backrub/google.html) by **Sergey Brin & Lawrence Page** (1998)

It baffles me that this paper is less than 20 years old. So much has changed
with the advent of the tool described in this paper. It’s a fun read, but
somewhat frightening. I like how open the early architecture of Google was,
because it is an interesting piece of technology.

* [Iago Attacks: Why the System Call API is a Bad Untrusted RPC Interface](https://cseweb.ucsd.edu/~hovav/dist/iago.pdf) by **Stephen Checkoway & Hovav Shacham** (2013)

I can’t say I understand the threat model of this paper fully, but what I can
say is that the technical details are interesting, and the descriptions are
worth reading. I quite enjoy learning about the nitty-gritty internals of
memory allocators, even if their explicit goal is to break applications.

* [Rigorous Benchmarking in Reasonable Time](https://kar.kent.ac.uk/33611/7/paper.pdf) by **Tomas Kalibera & Richard Jones**

This paper seemed very familiar—I think I’ve read it before, but forgot to put
it on here. It’s fairly nice in its demands for rigour in benchmarking, and pretty
useful for me at the moment. Let’s see how I do in implementing ideas from this
paper—I’ve not been known for my scientific rigour in the past.

* [Fast Functional Lists, Hash-Lists, Deques and Variable Length Arrays](https://infoscience.epfl.ch/record/52465/files/IC_TECH_REPORT_200244.pdf) by **Phil Bagwell** (2002)

An interesting idea; I admire Phil Bagwell’s work on data structures, and this
paper doesn’t let me down. Though it is at times very hard to read, the
contents are highly stimulating. One of the more promising data structures
that I’ve recently discovered.

* [Lively Linear Lisp — 'Look Ma, No Garbage!'](http://home.pipeline.com/~hbaker1/LinearLisp.html) by **Henry G. Baker** (1991)

This is a little pearl, dense, powerful and beautiful. There is some deep
insight in this paper, although some of the statements rely on a purely
functional—in the sense of not performing IO—environment, such as “Nested
functional composition has the obvious mechanical interpretation, since the
intermediate results are utilized by exactly one consumer. The mechanical
metaphor also shows that parallel execution of subexpressions is possible
and correct (so long as the primitive CONS itself—the creator of argument
lists—evaluates its arguments in parallel), since there is no mechanism whereby
the subexpressions can communicate.”, which in my mind is only sensible in a
“box is getting hot” environment.

* [A Little Implementation Language](http://www.ultimate.com/phil/lil/lil.html) by **P.J. Plauger** (1976)

The language described is cute and the idea beautiful. While I agree with the
author that a language like this might not be needed in this day and age—and,
admittedly, not in the last 40 years—I think it would be rewarding and possibly
worth it to investigate whether it is suited as an intermediate representation
for a compiler, similar to the god-awful LLVM IR, but more readable.

* [The use of subroutines in programmes](http://www.laputan.org/pub/papers/wheeler.pdf) by **David J. Wheeler** (1952)

It is sometimes baffling to me now that practices that are now very much the
norm have not always been the norm. Of course I rationally know this to be the
case, but it is still surprising when a paper like this one catches me
off-guard.

* [Some Were Meant for C—The Endurance of an Unmanageable Language](https://www.cl.cam.ac.uk/~srk31/research/papers/kell17some-preprint.pdf) by **Stephen Kell** (2017)

I come from an entirely different school than the author of this paper, and
naturally I disagree with him. It is, however, a deeply insightful paper with
a lot of interesting ideas about how and why C is still unparalleled in certain
areas. A highly educational read with a selection of fun little programs to
look at.

* [The rsync algorithm](https://www.andrew.cmu.edu/course/15-749/READINGS/required/cas/tridgell96.pdf) by **Andrew Tridgell & Paul Mackerras** (1996)

rsync is a remarkable piece of software, and the algorithm that powers it is
testament to that. I love this description of the algorithm, high-level and
short as it might be. It is quite enjoyable to read, and I think I understood
the algorithm itself quite well.

* [The Paradigms of Programming](https://dl.acm.org/citation.cfm?id=359140) by **Robert Floyd** (1979)

Turing award speeches are always a good place to look for interesting ideas,
and this one is no exception. The picture Floyd paints of our profession is
still depressingly accurate—to the point that you wonder how we still haven’t
learned from it. But then again, such is the case with many of the papers on
this list.

* [Some thoughts on security after ten years of qmail 1.0](https://cr.yp.to/qmail/qmailsec-20071101.pdf) by **Daniel Bernstein** (2007)

While his writing is a little obnoxious, the insight imparted on us in this
paper is extremely valuable. The ideas are all simple, which is what makes them
so great. I will definitely steal some of the design ideas for the next project
that I have to design and build from scratch; some are even applicable without
a major redesign/rebuild.

* [When Textbook RSA is Used to Protect the Privacy of Hundreds of Millions of Users](https://arxiv.org/pdf/1802.03367.pdf) by **Jeffrey Knockel et al.** (2018)

This is one of the scariest things I’ve read in this list. While many of the
flaws are depressingly basic, they’re also not ounlandish, in a perverse way.
One more reason to be sad at the state of programming as a craft and science.

* [Optimizing Pattern Matching](http://pauillac.inria.fr/~maranget/papers/opat/) by **Fabrice Le Fessant & Luc Maranget** (2001)

One thing that struck me while reading thee papers was how *simple* most of the
discussed optimizations were. While I’ve very publicly dabbled in compiler
development from time to time, many optimization techniques I’ve looked at
still seem scary and complex. Not the ones described in this paper. I don’t know
whether that’s a testament to the author’s abilities to describe them—to me,
anyway—or rather due to their objective simplicity.

* [Notation as a Tool of Thought](http://www.jsoftware.com/papers/tot.htm) by **Kenneth E. Iverson** (1979)

This paper is all over the place. I didn’t particularly enjoy reading it, even
though I admire Iverson greatly. The point he was trying to make was, at least
in my eyes, poorly illuminated, especially due to him repeatedly jumping into
long-winded examples—in fact, a significant part of this paper is spent on
explaining solutions to various problems that I didn’t care about going in: what
I wanted to hear was how mathematical notation is flawed, and how Iverson
intends to fix it.

[A little Scheme in Pharo](https://files.pharo.org/books-pdfs/booklet-AMiniSchemeInPharo/2018-03-17-MiniScheme.pdf) by **Stéphane Ducasse & Guillermo Polito** (2018)

This paper is fun to reimplement. It’s more of a tutorial than a paper, really.
What’s especially fun about this is that, intentionally or not, some of the code
required to make this work is missing (namely applying primitives). As a total
Pharo newbie, it was fun to figure out how to do this. It took me two
approaches, but I was pleased with the final result. And it sure helped make my
workflow more efficient.

[Making Digital Filters Sound Analog](https://quod.lib.umich.edu/i/icmc/bbp2372.1992.009/--making-digital-filters-sound-analog?view=toc) by **Dave Rossum** (1992)

This paper is a little old, and feels naive and simplistic when you compare it
to the complex edifices that now come out of analogue modelling efforts. Of
course it’s worth reminding yourself what humble beginnings anologue-modelled
DSP had, only two decades ago, and this paper is good at that!

* [Cyclic Symmetric Multi-Scale Turing Patterns](http://www.jonathanmccabe.com/Cyclic_Symmetric_Multi-Scale_Turing_Patterns.pdf) by **Jonathan McCabe** (2010)

A super fun read that inspired me to play around with Turing patterns some more.
The paper is a little sparse on specifics on how to add the multiscalability
that produces the fractal qualities seen in the last part, and I wasn’t able to
reproduce them yet. I will continue to work on it!

* [Software Engineering at Google](https://arxiv.org/abs/1702.01715) by **Fergus Henderson** (2017)

As a paper it’s quite terrible. It doesn’t read especially interesting, and the
information in it is of course biased. Some of the practices discussed in the
paper are huge read flags that make me highly uncomfortable, but seem not to
faze the author. O tempora, o mores.

* [Randomly-Scoped Lambda Calculus](http://www.club.cc.cmu.edu/~rharwood/tmp/random.pdf) by **Ben Blum** (2013)

A very enjoyable writeup of a ridiculous idea. I’m excited by ridiculous ideas,
and I’m excited by this paper.

* [The Final Pretty Printer](http://davidchristiansen.dk/drafts/final-pretty-printer-draft.pdf) by **David Christiansen, David Darais & Weixi Ma** (2017)

A very interesting twist on Wadler’s paper on pretty printing from the 20th
century; I enjoy extensibility, and providing it in a monadic way is, while
foreign to me, extremely intriguing. As always with these kinds of papers it
went a little bit over my head, but this is why I enjoyed it so much. I’ll have
to reread it once I implement seriously useful tools for working with Carp.

* [GLL Parsing with Flexible Combinators](https://pure.royalholloway.ac.uk/portal/files/31169565/paper.pdf) by **L. Thomas van Binsbergen et al.** (2018)

While the topic is certainly fairly interesting, this paper lost me about
halfway through and I only got back into it about 5 pages later, in the section
about Evaluation. Surely the implementation is interesting, but I find the
description unnecessarily obtuse and convoluted; that might just be me, though.

* [Programming Paradigms for Dummies: What Every Programmer Should Know](https://www.info.ucl.ac.be/~pvr/VanRoyChapter.pdf) by **Peter Van Roy** (2009)

While an interesting overview of different programming paradigms, this already
feels a little dated. It also feels a little biased towards Oz/Mozart, of which
I’m not a huge fan—so bias met bias. Nonetheless, it’s very comprehensive and
thoughtful an approach to classifying paradigms.

* [Crash-Only Software](https://www.usenix.org/legacy/events/hotos03/tech/full_papers/candea/candea.pdf) by **George Candea & Armando Fox** (2003)

This paper is msotly historically interesting, because it describes a paradigm
that, through Erlang and related technologies, has entered the mainstream by
now. The paper talks about these concepts in the context of Java, which is
interesting enough in its own right, but I’d have hoped for at least a mention
of Erlang; I guess it wasn’t part of the general consciousness of Computer
Science back then.

* [A Programming Language for Mechanical Translation](http://www.mt-archive.info/MT-1958-Yngve.pdf) by **Victor Yngve** (1958)

This is one of those papers where the age is perceptible from the first
sentence. I quote in full: “It has been said that the automatic digital
computer can do anything with symbols that we can tell it in detail how to do.”
The paper presents a valiant if a little dated approach to parsing natural
language, but is almost entirely impenetrable due to the writing style that is
exceedingly descriptive.

* [Climbing Up the Semantic Tower — at Runtime](http://fare.tunes.org/files/climbing/climbing.pdf) by **François-René Rideau** (2018)

This paper is deceptively short and mind-bogglingly dense. I enjoyed reading it,
even though I don’t understand half of it. The [Youtube video](https://www.youtube.com/watch?v=heU8NyX5Hus)
linked to in the paper helped clear thins up tremendously, but still it is quite
hard to follow for me. Exciting times!

* *An Industrial Case: Pitfalls and Benefits of Applying Formal Methods to the
Development of a Network-Centric RTOS* by **Eric Verhulst et al.** (2008)

I never heard of the operating system OpenComRTS before. It seems like a well
thought out project with some interesting features, and I’d like to take a
closer look at it when I find the time. For now I’m just enamoured with the idea
of verifying a kernel with TLA+.

* [The Implementation of Lua 5.0](https://www.lua.org/doc/jucs05.pdf) by **Roberto Ierusalimschy et al.** (2005)

This paper gives a concise technical overview of some of the more interesting
VM techniques employed in the Lua interpreter. Lua is probably my favorite VM to
look at, and the authors do a pretty great job at explaining why that is.

* [From Interpretation to Compilation](ftp://ftp.cs.ru.nl/pub/Clean/papers/2008/janj08-CEFP07-InterpretationToCompilation.pdf) by **Jan Jansen et al.** (2008)

This paper is quite useful as a reference for people wanting to build compilers
for functional languages; it shows a few implementation techniques that might
be interesting to explore for people wanting to speed up the code their compiler
generates (and who doesn’t want that). That being said, I’d enjoy revisiting
the benchmarks in this paper over 10 years later and seeing how the compiler
discussed in it fairs against newer versions of GHC.

* [YOLOv3: An Incremental Improvement](https://pjreddie.com/media/files/papers/YOLOv3.pdf) by **Joseph Redmond & Ali Farhadi** (2018?)

This is probably the most entertaining paper I read all year, and I don’t even
know anything about machine learning, let alone image classification. It’s quite
fun, though, and I really enjoy the unprofessional tone.

* [An Introduction to Dependent Types and Agda](http://www2.tcs.ifi.lmu.de/~abel/lehre/SS09/Fun/DepTypes.pdf) by **Andreas Abel** (2009)

This one just boggled my mind. It’s the first time I really felt like I
understood the power of dependent types as proof systems, and it gave me a great
intuition into how to start learning Agda. I realized that the concepts actually
aren’t complicated at all, but it took me a while to really understannd that.

* [“Major key alert!” - Anomalous keys in Tor relay](https://nymity.ch/anomalous-tor-keys/pdf/anomalous-tor-keys.pdf) by **George Kadianakis et al.** (2017)

This was a fascinating read. The topic is captivating—security topics always
have a certain pull to them—and the language is clear enough so that a layman
like me who does not bring a deep knowledge of the technologies used in the
Tor network understands the approaches used by the researchers and
feels—probably illusorily—like they are able to interpret the findings as well.

* [Simple, Fast, and Practical Non-Blocking and Blocking Concurrent Queue Algorithms](http://www.cs.rochester.edu/~scott/papers/1996_PODC_queues.pdf) by **Maged Michael and Michael Scott** (1996)

This paper has it all: source code, pseudo code, a comprehensive-seeming study
of the prior arts, and a goo set of benchmarks. It made me want to try to
reimplement the algorithm, if only to play around with some C or Carp.

* [A Mulching Proposal—Analysing and Improving an Algorithmic System for Turning the Elderly into High-Nutrient Slurry](https://ironholds.org/resources/papers/mulching.pdf) by **Os Keyes et al.** (2019)

One of those rare papers that’s both very fun and quite insightful. It’s
undoubtedly silly, but the message is very clear, and very real: any one way of
judging algorithms—especially checklist-style analyses—will fall short of
underlying social and/or ethical implications. You can’t rely on blue prints for
making decisions that have implications beyond the technical.

* [Experiences Threat Modeling at Microsoft](https://adam.shostack.org/modsec08/Shostack-ModSec08-Experiences-Threat-Modeling-At-Microsoft.pdf) by **Adam Shostack** (2008)

Very legible, an easy and enjoyable read! Threat modeling is a fun activity, and
this paper is a classic!

* [Linda In Context](http://worrydream.com/refs/Carriero%20-%20Linda%20in%20Context.pdf) by **Nicholas Carriero & David Gelernter** (1989)

Although at some points unfair to its competition, this paper showcases a
compelling programming model seemingly lost to time—at least in the mainstream.
That’s fairly sad, as the case the authors make for Linda is fairly solid. I
don’t know as much about its context as I probably should; oh well, yet another
thing to look at!

* [Mirrors: Design Principles for Meta-level Facilities of Object-Oriented Programming Languages](http://bracha.org/mirrors.pdf) by **Gilad Bracha and David Ungar** (2004)

A quite informative and comprehensive overview of mirrors, though a little
dated. I quite enjoy the descriptions of the tradeoffs involved when designing
reflection systems, however, and I’ve admired the authors’ work for a while now.

* [Object Oriented Shader Composition Using CLOS](https://github.com/Shinmera/talks/blob/master/els2018-glsl-oop/paper.pdf) by **Nicolas Hafner** (2018)

Short and crisp. The paper presents an interesting idea, but I’d have liked more
examples, especially if and how incoming and outgoing variables are merged. From
the listings I assume that this merge can’t always happen completely
automatically—Figure 1 and Figure 3 name the incoming vector `position`, while
Figure 2 names it `vertex_data`—, but I’m not sure whether that’s just taken
care of by implementing the superclass in CLOS.

* [Dedalus: Datalog in Time and Space](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2009/EECS-2009-173.pdf) by **Peter Alvaro et al.** (2009)

I got this paper by a talk from Peter
Alvaro—[see also](https://github.com/hellerve/programming-talks)—, because he
talked a little bit about Dedalus and I got very intrigued. I was familiar with
the basic idea behind it—Datalog plus negation and time—, and that was lucky,
for otherwise I wouldn’t have taken away much. The paper is very technical in a
domain I don’t know much about, and much of the jargon doesn’t immediately click
for me. I was able to get the gist of it with the background by the talk,
however, and enjoyed the paper a lot.

* [The Inferno Operating System](http://www.vitanuova.com/inferno/papers/bltj.pdf) by **Sean Dorward et al.**

The lineage of Inferno is clear: Plan9 was a great influence, and the language
Limbo is clearly an ancestor of Go. Rob Pike sometimes earns a little ridicule
for how persistent he was pushing the ideas underlying Plan9, Inferno, and Go,
but once he found the niche that Go is filling today, it all started to fall
into place. Nonetheless, the GUI applications developed in Limbo are
interesting, and their structure is undoubtedly appealing.

* [Some Elements of Mathematica Design](https://www.stephenwolfram.com/publications/academic/elements-mathematica-design.pdf) by **Stephen Wolfram** (1992)

The insight in this paper is not earth-shattering—and a little self-congratulatory,
unsurprisingly—, but it’s useful. API design is a discipline that’s near and dear to my
heart, and Stephen Wolfram certainly has some insight into that.

* [Descriptive Complexity: A Logician’s Approach to Computation](https://www.ams.org/notices/199510/immerman.pdf) by **Neil Immerman** (1995)

An extremely dense paper, it was recommended to me as one of the most
interesting papers in complexity research. It was a little hard to follow for
me, but it was enjoyable nonetheless. I’m not usually concerned with complexity
classes, but of course I feel a certain attraction to the field (maybe only
motivated by the desire to relive my study days, where these kinds of questions
were at least of grade-related importance).

* [Soutei, a Logic-Based Trust-Management System](http://okmij.org/ftp/Prolog/Soutei.pdf) by **Andrew Pimlott & Oleg Kiselyov** (2006)

I have a certain fondness for Datalog, and the system described in this paper
perfectly encapsulates all of the things that I love about it. Descriptive
policies tend to be almost inexpressable in many popular programming languages,
and Datalog is extremely good at it. The bits of Haskell code shown are pretty
elegant as well.

### Books

* [You Can’t Spell Trust without Rust](https://cdn.rawgit.com/Gankro/thesis/d2f0b64fe93c23923f3a43a7038427083edad4c5/thesis.pdf) by **Alexis Beingessner** (2015)

As one Reddit user helpfully put it: “You can’t spell slaughter without laughter
either”. Technically this is not a book but a master’s thesis, but I’ll count
it as a book for reasons of vanity. It is relatively readable, but not very
exciting either. Rust excites me less and less the more I do with it, and this
thesis didn’t help. I’ll read a bit more about it, but for now I’ll have to
conclude that Rust is not for me, neither theoretically nor practically.

* *If Hemingway Wrote JavaScript* by **Angus Croll** (2014)

One of the most delightful tech books I’ve ever read. It is whimsical, and
while only tangentially pedagogical, an incredibly gratifying read. I expect
to revisit it again and again—its disjointed nature makes this very easy and
immediately valuable.

* *How Not to Program in C++* by **Steve Oualline** (2003)

This book didn’t age very well. Much of its content feels outdated, and some of
the brain teasers feel petty, just fluff to fill up the book. I enjoyed a few
of the riddles a lot, but in general I was annoyed at them pretty quickly.

* [10 PRINT CHR$(205.5+RND(1)); : GOTO 10](http://nickm.com/trope_tank/10_PRINT_121114.pdf) by **Nick Montfort et al.** (2013)

It’s pretty grandiose.

* [97 things every programmer should know](https://www.gitbook.com/book/97-things-every-x-should-know/97-things-every-programmer-should-know/details) by **Kevlin Henney (editor)** (2010)

While most of the adivce in this book is fairly solid, the writing varies
wildly. Some of the experts could’ve used a lot more editor attention, but who
am I to judge? The contents are fairly light, and I think most of the advice is
not as profound or rarely brought to the attention of us lowly developers as
the authors think. Maybe I’m just still grumpy about Uncle Bob’s incoherent
ramblings, who knows.

* [The Craft of Text Editing](http://www.finseth.com/craft/) by **Craig A. Finseth** (1999)

I had to read this one, what with me implementing [my own terminal
editor](https://github.com/hellerve/e) and all. There is a lot of interesting
information in this one. Some of it is purely historical, as some standards have
popped up and changed the assumptions (for instance UTF-8, ANSI escape
sequences, and such). Some of it is still interesting.

Reading this gave me feature envy for `e`, but I think it’s best if I don’t
change it, even if some algorithmic improvement woud arguably be low effort and
high impact. Take for instance gap buffers: they are fairly well understood and,
considering all the resources that you get on them, more or less trivial to
implement. But `e` is an editor mostly for programming and writing “regular”
prose, where the lines aren’t all that long. Add this fact to the consideration
that, while gap buffers are easy to implement, they would complect the design of
the editor, and I’d veto them until they prove necessary to my users—of which
there aren’t many, as I assume—or to me. So, while it was an interesting read, I
will refrain from implementing my new-found knowledge prematurely.

* [Experimenting with Programming Languages](http://www.vpri.org/pdf/tr2008003_experimenting.pdf) by **Alessandro Warth** (2008)

The original description of OMeta. OMeta has quickly become one of my favorite
approaches to parsers—it is weird, original, and fun to work with. The ideas of
worlds described in chapter 4 are less well known, but just as eye-opening. As
always, reading this gave me an itch to try and build dozens of things—it’s hard
to read Warth’s work without wanting to try it all out.

* [PLANNER: A Language for Manipulating Models and Proving Theorems in a Robot](https://dspace.mit.edu/bitstream/handle/1721.1/6171/AIM-168.pdf?sequence=2) by **Carl Hewitt** (1970)

I regard PLANNER as one of the most interesting chapters in the history of
programming languages. It’s the grandfather of theorem provers and logic
programming languages like Prolog alike, and it’s fun to read about its
implementation. This document is not really a front-to-back kind of read and
more of a reference work, but it is quite enlightening!

* [Tutorial on Good Lisp Programming Style](https://www.cs.umd.edu/~nau/cmsc421/norvig-lisp-style.pdf) by *Peter Norvig & Kent Pitman* (1993)

A very insightful little pamphlet that aged pretty well. I was able to take
some of the prescribed rules directly into [SBCLi](//github.com/hellerve/sbcli).
The writing is concise and to the point, but never curt or unmotivated. It was
tremendous fun!

## Recreational

### Papers
* [A Study of Prisoners and Guards in a Simulated Prison](http://www.zimbardo.com/downloads/1973%20A%20Study%20of%20Prisoners%20and%20Guards,%20Naval%20Research%20Reviews.pdf) by **Philip Zimbardo et al.** (1973)

One of the most famous papers of psychology. I had to read one
of Zimbardo’s books when studying psychology at University, but
never got around to actually reading this infamous paper. It is
both well-written and topically interesting, but extremely disturbing.
I doubt any ethics committee would let an experiment like that
happen these days.

*EDIT:* It is also harshly criticized these days. If you want to read
dissenting voices, I suggest you check out [this
article](https://medium.com/s/trustissues/the-lifespan-of-a-lie-d869212b1f62).

* [On Being Sane In Insane Places](https://isites.harvard.edu/fs/docs/icb.topic625827.files/On_Being_Sane_In_Insane_Places-1.pdf) by **David Rosenhan** (1973)

Another very interesting pyschological paper that I discovered
much too late. It is a paper in the same vein as the Zimbardo
paper above. Very clearly written, at times seeming unscientific,
but asking important questions and providing an excellent basis
for thinking about how psychiatry should work and how it does.
Of course, the situation described in this paper is not the
situation we are in right now (we have gone a long way since
the 70s after all), but we should be wary of the fact that back
then, too, we thought we did things the right way when in fact
we didn’t.

* [High-Selectivity Electrochemical Conversion of CO2 to Ethanol using a Copper Nanoparticle/N-Doped Graphene Electrode](http://onlinelibrary.wiley.com/doi/10.1002/slct.201601169/full) by **Yang Song et al.** (2016)

Saying I understood this paper would be an overstatement. It was an
interesting read nonetheless and the research in it sounds promising.
To a clean future!

* [Can Additional Homeopathic Treatment Save Costs? A Retrospective Cost-Analysis Based on 44500 Insured Persons](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0134657) by **Julia Ostermann et al.** (2015)

This study is a very important step towards a real cost evaluation
of homeopathy. While I would be careful not to generalize, because
the study had a lot of moving pats that are unaccounted for, the
sample size is pretty huge and the conclusions are pretty decisive
in that I can say that, no, homeopathic treatment is not generally
cheaper than traditional western medicine.

* [Caesarean sections and for-profit status of hospitals: systematic review and meta-analysis](http://bmjopen.bmj.com/content/bmjopen/7/2/e013670.full.pdf) by **Olir Hoxha et al.** (2017)

Somewhat unsettling research, but unsurprising—I am a cynic, after
all. It’s also not necessarily bad a priori that more C sections are
performed, I guess, but it hints at an underlying profit-driven environment
in profit-driven hospitals (duh). This holds true regardless of patient
history, apparently, which, if generalizable (which I hope is not the case)
would be highly appalling.

* [Schrodinger’s Cat and World History: The Many Worlds Interpretation of Alternative Facts](https://arxiv.org/pdf/1703.10470.pdf) by **Tom Banks** (2017)

A highly entertaining read.

* [Tezos:  A Self-Amending Crypto-Ledger Position Paper](https://www.tezos.com/pdf/position_paper.pdf) by **L.M. Goodman** (2014)

I’m still pondering whether I should take part in the crowd sale.
But this sounds really cool.

* [On the Typography Of Flight-Deck Documentation](https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/19930010781.pdf) by **Asaf Degani** (1992)

One of the most insightful looks into typography that I’ve found.
I don’t anticipate I will be responsible for any flight-related
typography any time soon, but the advice given in this paper is
rock-solid.

* [Legible, are you sure? An experimentation-based typographical design in Safety-critical context](http://lii-enac.fr/articles/vinot-chi-2012.pdf) by **Jean-Luc Vinot & Sylvie Athènes** (2012)

Related to the item above, but a bit more analytical and focusing
on digital graphical interfaces instead of print. It’s also not
as easy to infer simple rules from the paper, but it’s still
presenting deep insights.

*False Suffocation Alarms, Spontaneous Panics, and Related Conditions—An Integrative Hypothesis* by **Donald F. Klein** (1992)

An interesting take on panic attacks, suffocation, and brain
signalling.

* [Tezos — A Self-Amending Crypto-Ledger White paper](https://www.tezos.com/pdf/white_paper.pdf) by **L.M. Goodman** (2014)

Still not convinced.

* [Deconstructing the evidence-based discourse in health sciences: truth, power and fascism](http://www.ucl.ac.uk/Pharmacology/dc-bits/holmes-deconstruction-ebhc-06.pdf) by **Dave Holmes et al.**

I thoroughly enjoyed this read, reading it as a joke.

* [Is the Chocolate-Eating, Coffee-Drinking, Dog-Walking Red Wine Drinker a Prototype?](https://www.princeton.edu/~joha/publications/Haushofer_et_al_Food_Preferences.pdf) by **Haushofer et al.** (2014)

It had to be tested.

* [Motivation and Nonsense in Chinese Secret Languages](https://brannerchinese.com/publications/Branner_final_pre-publication_draft_of_Secret_Languages_paper_dated_201004_corrections20111004.pdf) by **David P. Brenner** (2010)

One of the most interesting, readable papers I’ve ever read. The ease with which
the topics are discussed and broken down, even for laymen like me, is positively
startling, in a good way.

* [Attitudinal emotions and head movements in Danish first acquaintance conversations](http://www.ep.liu.se/ecp/093/013/ecp12093013.pdf) by **Bjørn Wessel-Tolvig & Patrizia Paggio** (2012)

I’m a layman, but this paper seems like it lacks a lot of data. The topic is
fairly intriguing and should be studied more, but, as the authors themselves
admit in the conclusion, there is just too little data for any claim to be made,
which is a bummer.

* [Is Justified True Belief Knowledge?](http://www-bcf.usc.edu/~kleinsch/Gettier.pdf) by **Edmund L. Gettier** (1963)

This is one of those rare papers where someone broke new ground by writing a few
pages (three, in this case) that just happened to blow everyone away. In this
case the paper is even more compelling, because it is understandable even to
someone who is not well-versed in the context of the paper. Very enjoyable,
enlightening read, and a style to which I aspire (like most, I imagine).

* *The Proper Treatment of “Your Ass” in English* by **John Beavers & Andrew Koontz-Garboden** (2003)

Very entertaining read. It’s not really my area of expertise—not at all,
really—, and still it’s quite fun to read. Of course the pun density is quite
high, but that just comes with the territory.

* [Fandomized Algorithms and Fandom Number Generation](https://github.com/lkuper/fandomized-algorithms) by **Lindsey Kuper & Alex Rudnick** (2013)

Short, but sweet, but I don’t think I’ll try the tech out any time soon.

* [A Mathematician’s Lament](https://www.maa.org/external_archive/devlin/LockhartsLament.pdf) by **Paul Lockhart** (2002)

I must’ve read it for the second time, but I can’t remember reading it for the
first time (except for a recollection of some of the things that have been said,
without knowing where they come from). It’s a good, enjoyable, cathartic read.

### Books

* *Abhandlung über den Ursprung der Sprache* by **Johann Gottfried Herder** (1772)

This book was intriguing in multiple respects: way ahead of its time
and yet so much of it is reflecting the sentiments of its time, sometimes
in a painful manner, such as when Herder talks about Black people—or anyone
Non-white, for that matter. The first part is a bit hard to decypher, but
the second part is making up for it. If you want to take anything away
from this book, the last four pages actually summarize his main point
quite nicely (starting at the paragraph labeled `3.`).

* *Erzählte Zeit—50 deutsche Kurzgeschichten der Gegenwart* by **Manfred Durzak (Editor)** (1989)

A great collection of German short stories detailling life in Germany
during various periods of the 20th century. I don’t think I can write
up a coherent comment about the book; there is just too much ground to
cover. I skipped two short stories that didn’t appeal to me writing-wise,
but other than that I was very happy with the layout, sequencing, and the
stories themselves. I don’t think there is a translation to any other
language of this particular book, but I’m sure most of the individual
stories are translated.

* *The Lover* by **Marguerite Duras** (1984)

Beautifully written story; it was the first book I read of Duras’ and I definitely
missed out. I need to read the Hiroshima Mon Amour screenplay next, and I
think I would like to see the movie, although I’m typically not a fan of
movie adaptations if I really liked the book. We’ll see.

* *Die Berliner Antigone—Erzählungen und Gedichte* by **Rolf Hochhuth** (1986)

Although I’m not a big fan of his style—he is a touch too preachy, like many
great German poets after the war, although for good reason—he delivers solid
stories that are interesting as historical commentary. Both of the prose and
the poems in this book are too clearly pointed for me, although I assume it is
hard to write about the war and the holocaust without being preachy. One of the
few who don’t fall into that trap is Paul Celan, himself a holocaust survivor
and incredible writer, and I don’t think a comparison is fair.

* *Selected Poems* by **E. E. Cummings (edited by Richard S. Kennedy)** (2007)

I like E.E. Cummings’ early and a few of his late poems. I have no taste for
his cubist poems, and his poems dealing with love and sexuality are severely
overrated in my eyes. The section introductions written by the editor try to
give an overview over the author’s views and environment that influenced his
writing, but most of them end up being toadyish.

* *Die Sekunden danach* by **Matthias Politycki** (2009)

I reread it after years of not reading any of his works. It’s still one of the
most enjoyable poetry books on my shelf. His style is clear, but subtle, and
effortlessly lighthearted. My favorite poems are about his random encounters,
often with women, beautiful moments, captured in a clear and unspectacular
manner. I like his matter-of-fact tone a lot.

* *On Value* by **Triple Canopy & Ralph Lemon** (2015)

I purchased this book at the PS1 warmup party at MoMA. I don’t know what I
expected, but this sure wasn’t it. I enjoyed the read, however. The book
is a series of essays and conversations by and of modern artists, particularly
dancers. Their throughts on their art and craft and its presentation felt both
intimate and illuminating, curated and natural.

* *Scotland and Its Whiskies: The Great Whiskies and Their Landscapes* by
  **Michael Jackson** (2001)

A beautifully written book with equally beautiful photography. Michael Jackson
is one of the best writers this most special of drinks has ever seen, and it
was the writer it deserved. This book is a playful tale of a journey through
Scotland and its pretty distilleries. Highly recommended read.

* *The Witch’s Vacuum Cleaner* by **Terry Pratchett** (2017)

Terry Pratchett at his youngest. The stories are incredibly charming and cute,
and it is well suited for reading to anyone, though I’d recommend someone who’s
close to you. Strangers can act funny if you shout even the best stories at
them.

* [CLOSURE](https://github.com/steveklabnik/CLOSURE) by **\_why, the lucky stiff** (2013)

I was quite obsessed with \_why for some time, ca. 2012. Over the years I’ve
thought of him every now and then, but I didn’t know about this last relic he
gave to his followers—I don’t think he’d like that term very much, but I think
it’s appropriate. Anyway, I devoured it. It’s pretty great.

* *He sacado mi esperanza a lucir* by **Hans-Eckardt Wenzel** (2014)

A beautiful book of poems by one of my favorite German musicians. I picked it
up when I saw him live—books are great memorabilia. The poems are great in
their own right, but it’s even better if you want to learn Spanish from German
or the other way around, because it’s also quite wordy poetry.

* *Nachtstücke* by **E.T.A. Hoffmann (Artemis und Winkler edition)** (2012)

I knew all of the stories in this book already, but haven’t read them in years
and this edition is a little different from what I remembered. It’s a classic
of German romantic literature, and rightfully so. Others have said better than
I ever could what this book is.

* *Herz, stirb oder singe* by **Juan Ramón Jiménez (Diogenes edition)** (1977)

A gorgeous book of poems that I’ve read a bunch of times over the years. It has
been very influential on my poetry and, less obviously, my Spanish. This
edition is uncharacteristically sparse on detail on the author, which intrigued
teenage me even more. Now, of course, Jiménez is one of my favorite poets.

* *Unter dem Stern des Bösen* by **Gabriel García Márquez** (1966)

A confusing little book that I love. It’s another one of the books I just had
to reread this year, especially because I’m reading another one of his in
Spanish right now, very slowly and despairing about whether I will ever not be
terrible at the language. This one I read in German, and it was like visiting
an old friend with a different address, familiar, yet different.

* *Parzival* by **Wolfram von Eschenbach (Schöningh Edition)** (1965)

This is one of the most pleasurable editions of Parzival that I’ve read. It is
a small selection of the core stories within the book, which makes it a little
more palatable to the modern reader. It is less meandering and more focused,
although it is still a fairly foreign read.

* *Brigitta* by **Adalbert Stifter** (Reclam edition from 2003)

One of the more boring books that I’ve read in my life. The story is not
necessarily bad, but the writing reads incredibly self-indulgent to me. It is
fairly short and has pretty parts, but on a whole I didn’t enjoy reading it.

* *Gute Reise, Genosse* by **Kirill Gradov** (1984)

Insightful book into the life in the Sovjet Union. I first read it when I was
around 12 years old, and it had great influence on the way I pictured living in
the Sovjet Union. It is still a nice read, and feels like a glimpse into a
foreign world.

* *Prosaminiaturen—Opus III* by **Wolfgang Haak** (2008)

Paul Celan and he have influenced my writing—in German— like no other
writers have. This is one of my favorite books, and I read it every other
year, at least partially. Highly recommmended read.

* *Writings to an Unfinished Accompaniment* by **W. S. Mervin** (1976)

Mervin is one of my favorite American poets. I didn’t know him before I found a
double edition of this and another of his books in a used book store in Berlin.
I devoured them. He is definitely part of the canon, but somehow I didn’t hear
about him until very late.

* *The Moving Target* by **W. S. Mervin** (1976)

I prefer the book above, but it is interesting to see how Mervin’s writing
changed and developed over the years. Had I read this one first, however, I
probably wouldn’t have been enamoured with his writing as much.

* *Eiche und Angora* by **Martin Walser** (1962)

A painful and funny, sad and satiristic play. I didn’t know about it before
finding it in a used book store, and read it within a few days. It is touching
while still maintaining its comedy. This might be my new favorite play, and my
favorite book to deal with Germany’s disgraceful past.

* *Erzählungen* by **Christa Wolf** (1983)

I’m a big fan of Wolf’s writing. She is often introduced as one of East
Germany’s most important writers, and rightfully so. Her short stories are
surprisingly critical of the regime (surprising that they were published, that
is to say), and incredibly candid.

* *Brief an Lord Liszt* by **Martin Walser** (1982)

This book is deeply personal and honest, a recollection of a feud without
fingerpointing, but with all of the drama. Masterfully crafted and cutting.

* *Der Revisor* by **Nikolai Gogol** (1836)

It is quite fascinating how this pushed all of my buttons. I was deeply annoyed
with almost every character in the story (which is exactly what the author
wanted, I suppose). I’d love to see it on stage sometime.

* *Lenz* by **Georg Büchner** (1839)

Terribly fascinating in both story and backstory. The reclam edition I read came
bundled with a few resources and a very comprehensive explanation of the history
and context of this fragment. It is very disjointed, but beautifully written and
highly gripping.

* *Der zerbrochene Krug* by **Heinrich von Kleist** (1807)

A weird, but satisfying book. As with Lenz, the backstory—particularly the bits
about Goethe—are fascinating as well. I understand it doesn’t jive well with
audiences, but that’s a mark of many great plays anyway.

* *Antigone* by **Sophocles** (Translation by Wilhelm Kuchenmüller, 1955)

This short play, in a beautiful translation by a capable philologist, sucks even
the reader in with its mesmerizing rhythm (iambic pentameter throughout). It’s
a compelling story set after the fallout of the Seven Against Thebes that
imagines the fate of Antigone and Ismene after Eteokles and Polynices died. It
is powerful in its appeal to humanity and as an example of what happens when
power and rage combine to blind their master.

* *Die Germanen* by **Rudolf Simek** (2006)

This book is a good, non-ideological look at the histories of the Germanic
peoples, how they connect, how they differ, and how they interrelate with other
cultures of the time (mostly the Huns and the Romans). I very much enjoyed
reading this, because it helped understand that the Germanic peoples were not
just barbarians, but also not the peoples the Germans or Slavic people owe their
heritage to. It’s more complex than that, and this book does not shy away from
the complexity, isntead embracing it and trying to make sense of it.

* *Ein fliehendes Pferd* by **Martin Walser** (1978)

This is the third book by Martin Walser that I read this year. This year, he’s
slowly morphing into my favorite author. His calm, collected writing, centered
around realistic characters, is both entertaining and insightful. This book in
particular has a beautiful calmness about it.

* *Pankraz der Schmoller* by **Gottfried Keller** (1856)

This might be my least favorite book of this year. Even though it is short, it
was hard for me to get through. I quite enjoyed the afterword, as it gave me
some context about the book and the period it was written in, but the book
itself wasn’t my cup of tea at all.

* *The Truth* by **Terry Pratchett** (2000)

This was one of the first discworld novels I ever read, and I still enjoy it.
Nuff said.

* *The Black Swan: The Impact of the Highly Improbable* by **Nassim Nicholas Taleb** (2007)

Very informal and pretty insightful, but obscured by an unnecessarily relaxed
style that makes some of the reasoning feel pretty sloppy.

* *Deutschstunde* by **Siegfried Lenz** (1968)

A beautiful book on multiple levels. The title alone hints at the duplicity of
the story: it is both the tale of having to write an essay, and an exploration
of German nature itself. It’s decidedly descriptive, all deductions are made by
the reader—though as always you are compelled to follow the main character’s
reasoning—, and you are free to leave this book with your own conclusions.

* *Ansichten eines Clowns* by **Heinrich Böll** (1963)

I read this book for the fourth or fifth time in 2018, and I was still gripped
by it. It’s a great book to devour. I enjoy the story, and the radical honesty
with which all of the characters—including the main character—are portrayed.

* *Die Gruppe 47* by **Helmut Böttiger** (2012)

A well-written history of the most important group of German writers post-WWII.
It’s informing and entertaining, and it’s incredibly well-researched, citing
from books, letters, private correspondences of famous authors and publishers.
I’m already telling everyone to read it.

* *Der Goldkäfer* by **Edgar Allan Poe** (1843)

A beautiful story. I read it for the third or fourth time this year (2018), and
it is always a quick and enjoyable read. My edition also boosts a set of
gorgeous illustrations from the early 20th century, which accompany the story
very nicely.

* [Out of the Aeons](http://www.hplovecraft.com/writings/texts/fiction/oa.aspx) by **H.P. Lovecraft & Hazel Heald** (1935)

A fantastic little short story. Lovecraft is one of my favorite writers, not so
much because of the stories he told, but because of his flowery prose and
magnificent command of the English language. I learned a new word from this
story: “proboscidian”.

* *Gateway* by **Frederik Pohl** (1977)

Easily one of my favorite books this year. The premise is extremely intriguing
and sets a great scene for big questions about humanity and space. The narrator
is not the nicest person, but he makes for a very intriguing character to
explore. Thanks to @lamarqua for getting me into this by giving me—and
Meredith—the book in the first place.

* *If on a winter's night a traveler* by **Italo Calvino** (1979)

A masturbatory postmodernist tale that serves mostly itself. It’s not
impenetrable and has its moments, but in the end it’s nothing more than an
exercise in mutual patting of backs between the author and the knowledgeable,
well-read reader who understands that literary tradition is blasé and properly
teling a story bourgeouis.

* *The Prince* by **Niccolò Machiavelli** (1513/1532)

Maciavelli was a product of his time, and his meditations are primarily
interesting from a historical perspective. His works shaped the thoughts of many
emperors, and his knowledge of the lives and deeds of historical figures was
almost unparalleled. My edition in particular featured accompanying commentary
by Max Oberbreyer from 1879 that felt more dated than the original work, but
were nonetheless illuminating and very useful for a bit of context on the people
Machiavelli uses as examples.

* *A History of the World in 6 Glasses* by **Tom Standage** (2006)

A neat little book with a good history (as far as I can tell) of some of the
world’s most influential drinks. The chapter on only drink I knew some of the
history of prior to reading the book—Rum—was a bit of a red flag, though,
because the author has a nasty habit of pretending his favorite theory about
a historical factoid that’s still a topic of discussion—the etymology of the
drink’s name, for instance—is gospel and the only one worth mentioning. It is
nonetheless informative and fun to read.

* *Das Vorbild* by **Siegfried Lenz** (1978)

Another incredibly poignant book by Siegfried Lenz. He was an incredibly
descriptor (and caricaturist) of the German spirit of the time, and all of his
characters feel like archetypes. I had a lot of fun reading this, even though
not a single one of the characters was likable—and I think they weren’t meant
to be.

* *Picknick am Wegesrand* by **Arkadi & Boris Strugatzki** (1972)

A fun, gripping read. I have my gripes with the last part and especially the
ending (I won’t spoil it here, though). My edition also featured an afterword by
Stanislaw Lem which was insufferable, pretentious, and mistakes opinion for the
scientific method; it ruined an otherwise perfectly good read for me.

* [Zen and the Art of Motorcycle Maintenance](https://en.wikipedia.org/wiki/Zen_and_the_Art_of_Motorcycle_Maintenance) by **Robert M. Pirsig** (1974)

This might’ve been the best, most insightful I’vé ever read. I’m just floored.

* [Notes on the Synthesis of Form](https://en.wikipedia.org/wiki/Notes_on_the_Synthesis_of_Form) by **Christopher Alexander** (1964)

The core idea, breaking down tradeoffs, linking them, and working your way up
again, is worth talking about. Unfortunately, the book gets a little repetitive
after a while and the appendices (a case study and mathematical formulation) are
not so fun to read. I’ll have to revisit those.

* *Gedichte* by **Rose Ausländer** (2017)

I really enjoy Rose Ausländer’s early poems. Her later poems (from the seventies
and eighties, to be precise) feel very different, and are a little too direct
and not linguistically interesting enough for me. Nonetheless the edition that I
have has a good collection of different samples from different periods in her
life, and it’s great fun to read them side by side.

* *The Revolution Betrayed* by **Leon Trotsky** (1936)

Both politically and historically interesting, this book is a good vivisection
of the state of the Soviet union of the 1930s by a disillusioned revolutionary.
It keeps surprpising me how many of the basic arguments against communism and
socialism have been dealt with such a long time ago, and while people keep
bringing them up, unchallengedly, when we have books like this one that clearly
explain what the Soviet union was and wasn’t, and where it all went down the
drain.

* *Perfecting Sound Forever: An Aural History of Recorded Music* by **Greg Milner** (2010)

A fun read, but has its shortcomings. It’s extremely centered around recording
history in the US, features a bunch of weird quacky types (such as Mr. Diamond),
and it features almost exclusively men as protagonists of the history of
recording—which might reflect the industry makeup, but was very obviously weird
to me. Nonetheless, I learned a bunch of things about the history of recording
and some of the more important historical records.

* *What’s Yours is Mine: Against The Sharing Economy* by **Tom Slee** (2017)

A beautiful examination of the race to the bottom that is the Sharing Economy
since it got the big money. There’s lots of interesting insight to be had in
the book, but it’s most useful as a reference work, quantifying the feeling of
political and social activists, economists, and politicians around the world,
and giving us a numerical frame for a policy debate that’s long overdue.

* *Jürgen* by **Heinz Strunk** (2017)

What a painful, gorgeous book. It hurts a lot to read, and puts its fingers on
the pain points of German culture; and that’s a great thing! I read the book in
little more than a day, and it was a day well spent!

* *Eine Frau schaut auf Männer, die auf Frauen schauen: Essays über Kunst, Geschlecht und Geist* by **Siri Hustvedt** (2019)

I didn’t know any of Siri Hustvedt’s work going into this book, I just thought
the title sounded interesting in the bookstore. The book is extremely
stimulating, because it is very eclectic, touching on topics I’m familiar with
and some I know nothing about. I didn’t agree with the message of all of the
essays, or even enjoy all of them, but it’s a good book nonetheless; and it made
me decide to finally read some Kierkegaard!

* *De coniuratione Catilinae* by **Salust** (41 B.C.)

It’s scary how little the rhethoric of populist deception has changed in the
last 2000 years. Some of the monologues by Catilina could be transplanted 1-to-1
to the current times, and would make as much sense as they did back then.

* *Monsieur Ibrahim et les Fleurs du Coran* by **Éric-Emmanuel Schmitt** (2001)

Understandable even for me, this book is beautiful in its simplicity. I enjoyed both the
writing and the story. I wanted to read more Éric-Emmanuel Schmitt for a long time, and I
believe now might finally be the right time.

* *Diese Einsamkeit ohne Überfluß* by **Sigrid Damm** (2000)

What a beautiful tale, about so many things. She tells us about her work, about her life,
and about the time that is 1995. Sadly my edition (by Suhrkamp) is riddled with spelling
mistakes that reek of OCR, but I tried not to think about that.

* *Leibhaftig* by **Christa Wolf** (2002)

A moving tale of an illness and about life in East Germany—especially when trying to both
have a career and make a difference. I felt with the author, and I felt an urge to help
her, and in the end it left me feeling both happy and helpless, knowing that health and
illness are things that come and go, and that they’re part of life.

* *Die letzte Wette* by **Jason Starr** (2002)

An emotional but accurate betrayal of human interactions, relationships, and lives gone
wrong. It felt very genuine and the characters made sense to me—though some were a little
over the top, but such is fiction—, and most elicited at least a little bit of
understanding, no matter how misguided or fallible they were. The mark of a good book.

* *Das Bonusgeheimnis* by **Martin Suter** (2014)

Funny as always. The stories are entertaining, and, though satirical, not too far away
from reality. The punchlines never fail to deliver, and the book generally aged well.

* *In der Nacht leuchten die Wörter* by **Ernesto Cardenal (1979)

I’m not a big fan of epic, long poems. This book was worth reading anyway, for its
political and historical dimension alone. The author’s descriptions and depictions of life
in Central America in the midst of multiple USA-led “regime changes” is visceral. ¡Viva la
revoluçion cubana!

## Management

### Papers

* [Open Source Archetypes: A Framework For Purposeful Open Source](https://blog.mozilla.org/wp-content/uploads/2018/05/MZOTS_OS_Archetypes_report_ext_scr.pdf) by **Mozilla Foundation & Open Tech Strategies** (2018)

This book provides a good overview of open source archetypes (duh) that can help
in the decision when and how to go about creating a community and licensing your
software as open source. Obviously a great amount of work was invested in
creating this.

### Books

* *Zero To One: Notes on Startups, or How to Build the Future* by **Peter Thiel & Blake Masters** (2014)

I’m not in the crazy startup space that Thiel and Masters describe, and I’m
quite happy about that. There is some insight in that book, and a bunch of
bullshit and survival bias. It’s written quite entertainingly, and sifting
through it for the gems is never boring, so I quite enjoyed the read.

* *[The Great CEO Within](https://docs.google.com/document/d/1ZJZbv4J6FZ8Dnb0JuMhJxTnwl-dwqx5xl0s65DE3wO8/preview#)* by **Matt Mochary** (2018)

This book is astonishingly good. While I work for a consultancy and not a
startup and face a very different set of opportunities and challenges than
startup management does, large parts of this book were insightful, useful, and
interesting to read. What a way to start my management section.

* *The Hard Thing about Hard Things* by **Ben Horowitz** (2014)

This book is part autobiography, part management advice. I enjoyed reading it;
it’s lighthearted, doesn’t feel overly long, and doesn’t dwell on anything for
too long. Nonetheless, I’m not sure how useful it truly is; it’s fairly personal
and biased, but at least it doesn’t give off a false sense of objectivity.
