# Scientific Python: Past, Future, Present

- In 2015, gravitational waves were detected by LIGO for the first time.
- In 2019, the Event Horizon Telescope Collaboration produced the first ever image of a black hole through interferometry ((Very Long Baseline Interferometry, VLBI).
- In 2021, Ingenuity, the Mars helicopter, made the first powered controlled extraterrestrial flight by an aircraft.

What do they have in common? Each has pipelines that utilize the Scientific Python ecosystem.

Why is that special?

Let's step back and consider what the Scientific Python ecosystem is:

- Software developed by a small handful of students and junior researchers
- Often with little to no financial support
- Done in the open, through feedback from the community of users

Contrast this with the commercial systems that historically drove much of science:

- Millions of dollars in funding
- Developed by hundreds, or even thousands, of dedicated programmers
- Developed behind closed doors

Immediately, several questions arise:

- Why is it important to pursue the community path? Why not simply rely on the commercial offerings.
- Are scientists equipped to develop their own software platforms?
- How can volunteers even contemplate competing with large scale commercial efforts.

Are these efforts CRAZY or doomed to failure even before they started?

[show image headers of Nature papers]

I think we have an answer to that ready: no, they are not doomed, we have at least one proof of existence: the Scientific Python ecosystem.

## Why is it important to pursue the community path?

Let's start by considering the incentives of the community, versus a company building software for that community.

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
  Again, it is in the vendor's interest to give accurate results, otherwise software won't sell.
  But, you cannot verify your entire software stack: at least part of it is a "black box".
  And science absolutely needs transparency: you cannot trust results, state them with full confidence, unless you know how they are produced.

  Here, you can argue that, in practice, commercial scientific software is often very reliable.
  And that may be true, from your experience with a certain software package.
  But as a postdoc in neuroscience, I have seen first hand closed analysis software behaving badly, and no way for the operator to inspect what went wrong.
  *Any* software can behave badly, so it is imperative that you have the option to investigate what is wrong and to fix it.

  > https://en.wikipedia.org/wiki/Therac-25
  > A computer-controlled radiation therapy machine produced by Atomic Energy of Canada Limited (AECL) in 1982.
  > It was involved in at least six accidents between 1985 and 1987, in which patients were given massive overdoses of radiation.
  > Because of concurrent programming errors (also known as race conditions), it sometimes gave its patients radiation doses that were hundreds of times greater than normal, resulting in death or serious injury.
  > Two software faults were to blame.
  > One, when the operator incorrectly selected X-ray mode before quickly changing to electron mode, which allowed the electron beam to be set for X-ray mode without the X-ray target being in place.
  > A second fault allowed the electron beam to activate during field-light mode, during which no beam scanner was active or target was in place.
  > Previous models had hardware interlocks to prevent such faults, but the Therac-25 had removed them, depending instead on software checks for safety.

  Again, as all good programmers will tell you: programmers make
  mistakes, and *any* software can behave badly.
  It is imperative that you have the option to investigate what is wrong and to fix it.

This point also leads us to our next question:

## Are scientists equipped to develop their own software platforms?

- Scientists need to have a deep understanding of their computational codes.
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
  > Wider use of code leads to better generality and fewer bugs.

For scientists who are *not* equipped to work on their own software have two options:
(a) let them blindly use other people's building blocks, or
(b) train them so that they, too, can contribute to and understand the software ecosystem.

## Can volunteers compete with large scale commercial efforts?

In short: yes.

One does not need to build an entire ecosystem, all at once, in order to start using open platforms for science.

1. Certain code paths are more commonly used than others; need to make sure that the commonly used components are well implemented,
   and that users can extend those paths as needed.
   That, e.g., is why it is so important that a package like NumPy, the fundamental array data structure for scientific Python, is well implemented.

Reference: bridge topological optimization
https://github.com/williamhunter/ToPy/wiki/Examples-of-ToPy-results

Like with a bridge, you build the trusses that provide support.

2. Open platforms are good at ingesting and exporting data; as long as you can wrangle data from your existing
   software, parts of your pipeline can be replaced piecemeal.

## What are advantages of community development over commercial methods?

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
  - Volunteer time varies
    - Not that easy for everyone to contribute (parents, breadwinners, etc.)
  - Not many full-time devs
  - Bottleneck mostly at "Review" step above

- Sustainable: funding is hard to come by
  - Ironically, it is easy to pay for commercial software from a government research grant,
    but quite hard to support open source software development
  - In other words, we can easily use tax payer money to fund the development of closed software,
    but we cannot use that money to build shared critical research infrastructure
  - And this *is* critical reinfrastructure: we would not want to pay for a bridge that only certain people can use, so why do that for software?

- Informally coordinated
  - Commercial projects typically have multiple people whose job it is only to think about roadmaps, features, talk to users, coordinate between different developer teams, etc.
  - Projects in the ecosystem are loosely coordinated, but each is run by itself.
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
