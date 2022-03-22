# Scientific Python: Past, Future, Present

- In 2016, gravitational waves were detected by LIGO, the Laser Interferometer Gravitational-Wave Observatory, for the first time.

https://en.wikipedia.org/wiki/First_observation_of_gravitational_waves
https://www.ligo.caltech.edu/page/detection-companion-papers
https://github.com/gwastro/pycbc
https://github.com/gwpy/gwpy/blob/main/setup.cfg#L41

- In 2019, the Event Horizon Telescope Collaboration produced the first ever image of a black hole through interferometry ((Very Long Baseline Interferometry, VLBI).

- In 2021, Ingenuity, the Mars helicopter, made the first powered controlled extraterrestrial flight by an aircraft.

https://github.com/readme/featured/nasa-ingenuity-helicopter
"...the Python ecosystem played a key role in everything from ground control to flight modeling to data processing."

What do they have in common? Each has pipelines that utilize the Scientific Python ecosystem.

In this talk, I'd like to discuss why this is so special, how we got here, and what lies on the road ahead.

## But first, a personal retrospective

- In the early 2000s, I was an engineering student, working on my master's thesis
- Most computational work back then was done using MATLAB
- We had a free license—at least for the folks who ran Windows machines
- I was not one of them
- The options were to (a) figure out how to install ML on Linux and get the license server working or
  (b) figure out how to do my work with entirely free software that ran easily on Linux
- Already then, I had a strong feeling/philosophy that scientific software should be open source
- And, since master's students have endless amounts of time, I chose to use Octave—a MATLAB clone
- Of course, Octave wasn't quite ready, and so that became a big part of my master's project
- I enjoyed working on that project, I certainly learned a lot
- But Octave had a problem: it was always chasing MATLAB; and while it had innovative features, such as
  its fast and elegant C++ interface, it could not truly innovate
- Meanwhile, my master's advisor decides that I needed more computational guidance.
- He introduces me to Ben.  Thus, my thesis meetings turn into mountain biking discussions.
- But then around 2004 Ben takes a sabbatical in Colorado, where he meets a young postdoc by the name of Fernando Perez.
  Fernando, btw, is the original author of IPython, which you now know as Jupyter.
- Goodness knows what that exchange looked like, but two things we know:
  - Ben returns an evangelist for the Python language, and
  - Fernando arrives in Stellenbosch in 2005 to give a workshop on scientific tools in Python.
- The rest, as they say, is history:
  - Ben and his students made a big leap, and switched all their courses and research over to Python.
  - I stopped working on Octave.
  - Instead, myself, Albert Strasheim, and other students started working on improving NumPy
    (which, at the time, was functional but in great need of support).
  - Worth emphasising is that my advisor *let* me work on all this.
  - What we found was that the Scientific Python community was incredibly friendly and open.
    Genuinely nice people, who cared a great deal about the tools they were building.
  - Developing these tools was exciting: no longer trapped in the confines of emulating an existing platform,
    this opened the doors to Python's full expressivity.
  - Python being a general purpose language meant that, now, scientific tools could be smoothly integrated
    into a much wider ecosystem of pre-existing software.

So, that's how Stellenbosch University got roped into all of this very early on.

In some ways then, this talk is about showing the potential of an open philosophy and approach.
We will get into some of the hairier details, but even if we disagree on some of the smaller details along the way,
I hope that the big picture remains compelling.

OK, so let's get back to our original question.

## Why is all this so special?

Let's consider what the Scientific Python ecosystem is:

- Software developed by a small handful of students and junior researchers
- Often with little to no financial support
- Done in the open, through feedback from the community of users

Contrast this with the commercial systems that historically drove much of science:

- Millions of dollars in funding
- Developed by hundreds, or even thousands, of dedicated programmers
- Developed behind closed doors

So, that in itself is remarkable: that you consider such an endeavor,
take part in it, and then get away with it.

And is that the case?  Or are these efforts CRAZY and doomed to failure even before they started?

[show image headers of Nature papers]

No, in fact it looks like there is not only proof of existence here, but also proof of success.
And, my take on that is that it is because of an underlying philosophy.
- A philosophy of *why* such software should be used and
- A philsophy around *how* such software should be developed.

http://nipy.org/nipy/mission.html#nipy-mission

> We believe that neuroscience ideas and analysis ideas develop
> together.
> Good ideas come from understanding; understanding comes
> from clarity, and clarity must come from well-designed teaching
> materials and well-designed software.
> The software must be designed
> as a natural extension of the underlying ideas.

Now, let's consider:

- Why is it important to pursue the community path? Why not simply rely on the commercial offerings.
- Are scientists truly equipped to develop their own software platforms?
- How can volunteers be so audacious to think they can compete with large scale commercial efforts.

## Why is it important to pursue the community path?

Consider the incentives of the community, versus a company building software for that community.

- The community needs to do excellent science.
- For that, they need computational software.
- Through experience, they know what that software should work and operate like.

A company, on the other hand:

- Needs to make money for its shareholders
- Needs to please its users enough that they will pay for the software (or, otherwise find some other way to extract payment)
- If they are successful, they have access to good programmers

At first glance, then, this is a perfect marriage:

- Academics have a need for software, the company can provide it
- Academics have grants, and they can pay the software provider
- The company has the programmers, so as long as the academics can tell them what they need, the programmers can provide

But even a superficial evaluation identifies immediate flaws in this plan—ways in which incentives are not as well aligned as they seem:

- It is in the company's interests to make money.
  Therefore, they want *as many people as possible* to use their software.
  This means that hardware locks, license servers, and closed file formats become very attractive.
  This means that it makes sense to lock users into a proprietary system from which they cannot easily escape.
  This means that it makes sense to give products to students for free, but to charge them later when they cannot easily stop using it.
  This means that, if your colleague wants to try your research code, they also need a software license.

  Imagine, for example, that your research relies on some closed Windows binary with a license key.

  - You cannot send your full analysis to a colleague to repeat, unless they have the same
    machine architecture as you do, as well as a license.
  - In five years from now, chances are that even you will not be able to run that program any more.

- Users of the software have no ownership over it.
  If you need a specialized hardware interface to read from an instrument, want to deploy to a cluster, or use a different memory allocator,
  you are out of luck unless the software supports it.
  It is in the vendor's interest to satisfy most users, so they can sell more copies, but they may not satisfy *your* requirements.

- Scientists cannot verify what is happening under the engin cover.
  In principle, science needs transparency: to trust results, to state them with full confidence, requires knowing how they were produced.
  Therefore, it is odd to carefully craft your code, but to use as a foundation a "black box".

  Here, you can argue that, in practice, commercial scientific software is often very reliable.
  After all, it is in the vendor's interest to give accurate results, otherwise software won't sell.
  So, for me this perhaps debatable as a pragmatic concern, but certainly not as a principle.

  As a postdoc in neuroscience, I saw first hand closed analysis software behaving badly, and no way for the operator to inspect what went wrong.

  > Relate experience of sitting next to another postdoc doing an analysis and seeing NaNs stream by.

  *Any* software can behave badly, so it is imperative that you have the option to investigate what is wrong and to fix it.

  > https://en.wikipedia.org/wiki/Therac-25
  > A computer-controlled radiation therapy machine produced by Atomic Energy of Canada Limited (AECL) in 1982.
  > It was involved in at least six accidents between 1985 and 1987, in which patients were given massive overdoses of radiation.
  > Because of concurrent programming errors (also known as race conditions), it sometimes gave its patients radiation doses that were hundreds of times greater than normal, resulting in death or serious injury.
  > Two software faults were to blame.
  > One, when the operator incorrectly selected X-ray mode before quickly changing to electron mode, which allowed the electron beam to be set for X-ray mode without the X-ray target being in place.
  > A second fault allowed the electron beam to activate during field-light mode, during which no beam scanner was active or target was in place.
  > Previous models had hardware interlocks to prevent such faults, but the Therac-25 had removed them, depending instead on software checks for safety.

  Trust, but verify.  Or don't trust but verify.  But always verify.

  As all good programmers will tell you: programmers make
  mistakes, and software is quite good at being bad.
  It is imperative that you have the option to investigate what is wrong and to fix it.

But who, do you ask, is going to do all of that. The scientist, of course.  Which leads us to our next question:

## Are scientists equipped to develop their own software platforms?

- As we discussed earlier, with the NiPy example, scientists need to have a deep understanding of their computational codes.
  That's how computational ideas crystallize. That's how we get answers that are more right than wrong.
- Relying on commercial software guarantees that you cannot know what the building blocks look like that you are using.
- Open source software does not fully address that concern (you can still simply build blocks), but it at least gives you the option to look.
- More importantly: when researchers become involved in the maintenance of their computational stacks, they get into the habit of skeptically checking results, of fixing software problems, and train themselves to understand the building blocks better.

So, the question may not be so much whether they are able to develop their own software (they are), but whether they can afford *not to*.

Note that scientists have done this for a long time: there are many FORTRAN libraries out there, written in times before commercial platforms became common.
Even with commercial platforms, many researchers build their codes on top of those platforms.

Building their own software, they immediate see some advantages:

- They have control over the software---can build whatever they want!
- They understand the software.
- They can verify that the software operates correctly.
- They can share the software.

Some further benefits come when they don't develop in isolation, but decide to share and develop the software as a community:

- Work can be divided, and everyone benefits from every improvement.
- This works, because unlike with cars and microwaves (and commercial software), you can produce copies of software for free.
- More eyes generate higher quality software.
  > During my PhD, I wrote the beginnings of what now is scikit-image, and image processing library.
  > I was reading and breathing image processing at the time, so it was a good time to write code.
  > Even so, once I released the software and the community started looking at it, they fixed innumerable bugs.
  > You might say: "Yes, but he's a terrible programmer." Perhaps ;)
  > But I'd say that all programmers are fallable, and that
  > wider use of code leads to better generality and fewer bugs.

For scientists who are *not* equipped to work on their own software have two options:
(a) let them blindly use other people's building blocks, or
(b) train them so that they, too, can contribute to and understand the software ecosystem.

We've said that following the community path is important because it aligns incentives;
we've said that scientists need to own their code.

## But can volunteers hope to compete with large scale commercial efforts?

<!-- Review from this slide -->

In short: yes.
The longer version: you may have to be strategic about it in an environment where you don't control the players.

Fortunately, one does not need to build an entire ecosystem, all at once, in order to start using open platforms for science.

1. Certain code paths are more commonly used than others; need to make sure that the commonly used components are well implemented,
   and that users can extend those paths as needed.
   That, e.g., is why it is so important that a package like NumPy, the fundamental array data structure for scientific Python, is well implemented.

Reference: bridge topological optimization
https://github.com/williamhunter/ToPy/wiki/Examples-of-ToPy-results

Like with a bridge, you build the trusses that provide support.

2. Open platforms are good at ingesting and exporting data; as long as you can wrangle data from your existing
   software, parts of your pipeline can be replaced piecemeal.

## What are advantages of community development?

- You can influence the direction of development so the tools better suit your needs.
- You can share your code freely and others can run it.
  By sharing your code, you are helping to build the universal free numerical library.
- There are no license fees, and the license is extremely liberal.

  Commercial packages have licenses that are tens of pages long.  Here is the one used by most of the SP ecosystem:

  > Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

  > 1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

  > 2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

  > 3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

## How does community developed software guarantee high standards

To understand this, one must understand the development workflow.

1. Contributor makes a copy of a library (we call this a branch) and starts adding their own changes to it
2. When they are ready, they submit this code for public code review
3. The first round of review is done by a machine:
  - Does the code conform to code & documentation standards?
  - Does the code pass a stringent series of tests?
  - Do all included examples execute?
4. The second round of review is done by humans
  - Based on their feedback, the author adapts their contribution, and the changes are again reviewed.
    - Reviewers check:
      - That contribution fits into project scope
      - That is has good documentation
      - That test coverage is maintained
      - That algorithms are correctly implemented
      - That algorithms have a good API (usage interface)
5. Once reviewers are happy with the contribution (often requires two to sign off), changes are included with the project.
   We say "the branch is merged".

## What are the weak points of community developed research software

- Developer resources are limited
  - Sadly, I am one of a very small handful of people in the world who is paid
    to work full-time on Open Source scientific software.
  - Most contributors are volunteers, and volunteer time varies
    - Not that easy for everyone to contribute (parents, breadwinners, etc.)
  - Bottleneck mostly at "Review" step above

- Sustainable: funding is hard to come by
  - Ironically, it is easy to pay for commercial software from a government research grant,
    but quite hard to support open source software development
  - In other words, we can easily use tax payer money to fund the development of closed software,
    but we cannot use that money to build shared critical research infrastructure
  - And this *is* critical reinfrastructure: we would not want to pay for a bridge that only certain people can use, so why do that for software?

- Informally coordinated
  - Commercial projects typically have multiple people whose job it is only to think about roadmaps, features, talk to users, coordinate between different developer teams, etc.
  - Projects in the ecosystem are loosely coordinated, but each one is run by itself.
    Projects do copy one another over time, but process is somewhat haphazard.

## What are we (scientific-python.org) trying to do to address these problems

- Better coordinate projects
  - Create venues where they can talk to one another
  - Provide mechanisms whereby we can record community practices,
    and communicate those: SPECs
    - Documents like PEPs, NEPs, SKIPs, etc.
    - High-level design and practice documents
    - Proposed by any project
    - Endorsed by so-called "core" libraries
    - Adopted by any project that agrees

- Help projects to apply for grant funding
  - Write up a community-vetted decadal development plan (evidence for need)
  - Workshops on grant writing
  - With funding, projects can provide full-time roles for more people in the ecosystem.
    We need as much help as we can get.
    <!-- expand a bit -->

- Support development of shared infrastructure
  - Tools that are common to multiple projects, such as numpydoc
  - Standard web themes for core projects (https://theme.scientific-python.org)

- Improve communication and onboarding
  - Developer meetings on specific technical pain points
  - Social media channels
    - Onboarding videos
    - Developer interviews
    - SP library examples
  - Learn: a site with learning material for users, contributors, and maintainers of the SP ecosystem
  - A blog for informal posts
  - A discussion forum, where users/developers can talk about projects that span the ecosystem

## How can you support the open scientific software endeavor

Unless the research community stands up for itself and its needs, commercial actors will keep having undue influence in software decisions.
(I can assure you those companies have sales reps who work quite hard to convince universities to buy their products.)

Yet, we don't really need more *users*—we have plenty! Of course, that doesn't hurt us, and we want everyone to use this software stack.

The alternative to commercial software is cheaper software, better suited to your research.
We should be willing to pay *something* for that:

- If you have students, allow them to work on the ecosystem in parallel to their research.
- Reward and recognize those who develop open source software
  (sadly, there's a long line of people who got punished by not getting tenure).
  We must stop counting papers as the only academic currency.
  Remember that most articles will gather dust on a shelf, whereas contributions to an active SP project will live forever and have an impact on many researcher's lives.
- Find a way to donate to the open source scientific software, and stop sending those funds to commercial players.
  Talk to your research council representatives about ways to redirect funding to
  development of open, free, computational research infrastructure.
- Take lessons from the way SP is developed, and apply it to your own research:
  - Test your code, perhaps using continuous integration;
  - Make your papers executable, so they can be re-run by yourself and others;
  - this means *automating* as much of the process as possible;
  - collaborate more widely (we tend too much towards academic siloes);
  - insist on open code, open data, and on sharing, wherever possible.

"Developing open source scientific practice", K. Jarrod Millman & Fernando Pérez
https://www.jarrodmillman.com/oss-chapter.html
https://osf.io/h9gsd/

## Where to learn more

Follow our YouTube channel for weekly updates: ...
Our website: https://scientific-python.org

Check out our blog (if active by then)?

## Credits

Ben Herbst
Stellenbosch University, afforded me the chance to work on this software as a PhD student and later lecturer
All of you who will help us to change the computational landscape
