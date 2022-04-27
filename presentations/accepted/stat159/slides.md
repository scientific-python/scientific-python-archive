<style type="text/css">
.black {
  color: black;
}
</style>

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>


<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<div style="text-align: left;">
K. Jarrod Millman<br/>
University of California, Berkeley
</div>

...

<div style="font-size: 300%; font-weight: 600;"> Scientific Python is </div>

<br/>

an **ecosystem** of Python packages for scientific research and data analysis

a **community** of developers, maintainers, and users of tools in the ecosystem

a **new project** that aims to better coordinate the ecosystem and grow the community


---

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>
</br>
</br>

<div style="font-size: 150%; font-weight: 400;">A short history</div>

Notes:

- personal account

  - involved at an early stage
  - many community members will tell you a similar story

- largely motivated to solve a series of problems

...

## 2000: Brain Imaging Center

<img src="images/bic.png"/>

...

## 2004&ndash;2005: Neuroimaging in Python

<img src="images/nipy.svg"/>

<div style="color: darkgray;">

> We believe that neuroscience <span class="black">ideas and analysis develop
> together</span>.
> Good ideas come from understanding; <span class="black">understanding comes
> from clarity</span>, and <span class="black">clarity must come from</span> well-designed teaching
> materials and <span class="black">well-designed software</span>.
> The <span class="black">software must be</span> designed
> as <span class="black">a natural extension of the underlying ideas</span>.
>
http://nipy.org/nipy/mission.html

</div>

...

## 2007: 1<small><sup>st</sup></small> CiSE Special Issue

<img src="images/cise2007-cover.png" width="49%" />
<img src="images/cise2007-toc.png" width="39%" />

...

## 2007: 1<small><sup>st</sup></small> CiSE Special Issue

<img src="images/cise2007-cover.png" width="39%" style="padding-bottom: 7rem;" />
<img src="images/cise2007-toc.png" width="29%" style="padding-bottom: 9rem;" />
<img src="images/cise2007-toc2.png" width="29%" style="padding-bottom: 10rem;" />

...

## 2008&ndash;2011: Growth of the SciPy Conference

<img src="images/scipy2008.jpg" width="80%" />

Note:

- < 100 participants
- > 800 participants
- Rock Auditorium has seating capacity of 100
...

## 2011: 2<small><sup>nd</sup></small> CiSE Special Issue

<img src="images/cise2011-cover.png" width="49%" />
<img src="images/cise2011-toc.png" width="49%" style="padding-bottom: 4rem;" />

...

## 2012: NumFOCUS

<img src="images/numfocus.png" width="80%"  />


---

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>
</br>
</br>

<div style="font-size: 150%; font-weight: 400;">Growth and adoption</div>

Notes:

<!-- Section: success of SP -->

...

<img src="images/the-overflow-blog.png" width="60%"/>

<!-- https://stackoverflow.blog/2017/09/06/incredible-growth-python/ -->

...

<img src="images/so-major-growth.png" width="80%"/>

...

<img src="images/so-minor-growth.png" width="75%"/>

...

<img src="images/dataiku-report.png"/>

*Pathfinder Report: Routes to Enterprise Open Source Data Science Adoption*
</br>
Data Iku, August 2018

<!-- https://pages.dataiku.com/451-open-source-report -->

...

<img src="images/numpy-summary.png"/>

...

<img src="images/github-satellite-keynote-2019.png"/>

Notes:

Really big corps are now using us to sell their product.

GitHub: Nate's talk with our faces in background

Emphasizing that importing these libraries is essentially broadening
your developer team, "giving them commit access to your project".

...

<img src="images/scipy-nature.png" width="60%"/>
<img src="images/numpy-nature.png" width="60%"/>

...

<img src="images/katie-bouman-portrait-of-a-black-hole.png"/>

2020 CZI Essential Open Source Software for Science Meeting

Notes:

US govt probably spent a billion dollars on it...

... but it's all based on free software.

...

## Teaching Python

At Berkeley, at least:

- Computer Science
- Data Science
- Information School
- Neuroimaging
- Statistics

... to name a few.

<br/>

*Teaching Computational Reproducibility for Neuroimaging*,<br/>
K. Jarrod Millman, Matthew Brett, Ross Barnowski, and J.-B. Poline<br/>
https://www.frontiersin.org/articles/10.3389/fnins.2018.00727/pdf

Notes:

In the beginning, we could not even find rooms on campus to teach
this.  Still, had several workshops, bootcamps, etc.

Now, it is ubiquitous.

This is no longer unusual, not only at UCB.

(Teaching, in itself, does not mean the tools are good for science,
but there's a practical element to it, namely...)

Students are equipped with Python by the time they arrive in research.

...

Use of Scientific Python is pervasive

It is being used in novel and leading science

It is continually improving, growing, responding to needs

Notes:

Despite this, poorly funded, mainly driven by volunteers outside of
their main jobs.

Very few people are rewarded for working on this (sometimes quite the contrary).

Re: responding to needs, NumPy is stable, yet refactoring entire data type system.

...

The Scientific Python ecosystem of libraries
is **critical research infrastructure**.

Notes:

- Research is becoming more data-dependent.
- Research therefore cannot happen without software.
- Research software relies on *reliable* computational libraries.

In some ways, software is becoming like what math is in research.
Lots of training for math, but very little for scientific software development.

Software is the instrument with which we see data.
It is the way we express our thoughts and reason about the world.

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>
</br>
</br>

<div style="font-size: 150%; font-weight: 400;">Lessons and challenges</div>

Notes:

...

## Why adoption and growth so unusual

<br/>

- Who developed the software?
- When, and with what?
- What did it replace?

Notes:

- Small handful of students, junior researchers, other volunteers
- Predominantly in their spare time, over weekends and evenings
- Often little to no financial support
- Against wishes / recommendations of many colleagues (not Ben!)

Competing against platforms built by companies with:

- Millions of dollars in funding
- Hundreds of dedicated programmers
- Pushes by big marketing teams, contracts with many corporations and universities

...

## Why it isn't surprising

<br/>

📜 Principles &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
🚜 Practices &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
🤸🏿 People

...

## Principles

<br/>

- Scientific software must be **community developed**, and **community owned**
- This is the best way to align incentives for doing good quality, transparent, reproducible science

Notes:

- We believe that researchers know their needs best
- Their ideas must be surfaced and integrated into the computational
  platform as efficiently as possible
- In this endeavor, making money for shareholders is at best a
  distraction
  - But often, it incentivises entirely the wrong things: hardware
    locks, license servers, closed file formats
  - Incentive to lock users into  proprietary systems
    - This prohibits sharing, reproducibility, and transparency

- Transparency: you *should* always be able to investigate the
  *entire* scientific stack.
- To know answers are accurate, you have to be able to look under the
  hood.
- You also need to be able to modify tools to do *new things*, to do
  *whatever* needs to be done.
- The change required is bigger than just open software; you need
  reproducible research as well (i.e. data/methods publishing). But
  it's a start.

...

## Principles (II)

<br/>

The **importance of language and library choices** cannot be underestimated.

- General-purpose
- Readable code
- Prioritize human (not computer) time

Notes:

- Re-emphasises the notion of a user-developer
- Library interfaces and language clarity / expressivity matter: it's
  how we express our thoughts.

...

## Practices

<br/>

**Technical**

- Revision control
- Testing / continuous integration
- Code review
- Documentation
- Iteration

**Social**

- Governance (*see also:* people)

Notes:

No matter how sound philosophy, we still need working code!

<!-- Code review both during development cycle, but also during use where
users can easily introspect for problems. -->

<!-- Documentation has to stay in sync with code (docstrings). -->

...

<img src="images/gh-workflow.webp"/>

...

## People

> Healthy communities are built when everyone's voice is heard, when
> their perspective is valued, and when their work is recognized.

https://scientific-python.org/about

<br/>

Work done in collaboration is better and more fun.

- **Community** is meaningful.
- **Culture** is important for good work.
- **Leadership** sets direction.
- **Governance** sets expectations and reduces misunderstandings.


Notes:

- Community

  - Many of my best friends I made through this ecosystem.

  - These have been the most fulfilling and educational collaborations
    of my life.

  - Being part of a movement where everyone is aligned is incredibly
    exciting.

  - For me, personally, it's been transformative to my career. Lots of
    people have helped me get where I am today.

- Culture

  - In a volunteer effort you cannot afford *not* to treat people
    well

  - Unsurprisingly, when people feel welcome, listened to, engaged, they produce
    better work

- Leadership

  - It helps greatly when the founders of projects set the right tone;
    one of the things that drew me into SP from the beginning

    - Various projects had you earn your badge
    - SP phone call from Berkeley: trust placed in newcomers,
      welcomed with open arms, treated with respect (listen to opinions)

...

## Challenges

<br/>
<img src="images/gh-workflow.webp" width="50%"/>


- Developer time (review time)
- A lot of time-consuming training (GSoC, etc.)
- Funding
- Implications of receiving funding (see: NumPy circa 2018)
- Coordination / cross-project decision making
- Unified user experience

Notes:

- Developer time
  - Very few full time like me
  - Contributor time varies (also: parents, breadwinners, etc.)

- We are doing a lot of training
  - Academia and industry both often use us to train people
  - That should be taught in universities / as professional courses

- Funding
  - No grant line items
  - Few company contributions
  - Mostly foundation-supported
    - Some grants, but need more and *longer term*

- Coordination
  - Used to be small (SciPy conf), now big
  - Nothing like project managers who can think about whole ecosystem,
    get user feedback, set up roadmaps, etc.
  - Coordination is haphazard

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>
</br>
</br>

<div style="font-size: 150%; font-weight: 400;">What's happening now</div>

Notes:

...

> The **Scientific Python project** aims to better coordinate the
> ecosystem and grow the community.

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

<br/>
<br/>
<br/>

1. Support & develop shared infrastructure
2. Foster the next generation of contributors
3. Create coordinating forum and mechanisms
4. Develop community-vetted strategic plan


...

## Support & develop shared infrastructure

</br>
</br>

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

...

## Shared infrastructure

<br/>

- https://scientific-python.org/calendars/
- https://theme.scientific-python.org/
- https://discuss.scientific-python.org/
- https://devstats.scientific-python.org/
- https://blog.scientific-python.org/

Notes:

  - Tools used across ecosystem such as numpydoc
  - Community calendars
  - Standard web themes for core projects
  - Common discussion forums
  - Developer statistics dashboard
  - Benchmarking & testing
  - Web analytics

BTW, a little easter egg on the NumPy frontpage to try!

...

## Foster the next generation of contributors

</br>
</br>

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

...


## People

<img src="images/community-managers.png" width="60%"/>

\+ &nbsp; `  {accessiblity, spec, theme, blog, ...} teams`


...

<img src="images/welcome-video.png" width="70%"/>

- https://twitter.com/scientific_py
- https://tinyurl.com/scientific-python-youtube


Notes:

  - Make it easy for new contributors to join the project
  - Social media
    - Onboarding
    - Dev interviews
    - SP library examples
  - Learn: material for users, contributors, maintainers
  - Blog: informal
  - Discourse discussion forum

...

## Create coordinating forum and mechanisms

</br>
</br>

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

...

<img src="images/specs-list.png"/>

https://scientific-python.org/specs

Notes:

- Coordinate projects
  - SPECs (like PEPs, high level, endorsed by "core")
    - SPECs also allow for younger projects to propose ideas
  - Venues for discussion
    - Discourse forum
    - Virtual technical meetings
  - Watch ecosystem, identify pain points, and coordinate response
    - Like developer meetings (currently virtual)
  - Eventually again have an annual developer meeting

...

## SPEC Steering Committee

<img src="images/steering-committee.png"/>

...

## SPEC Core Projects

<img src="images/core-projects.png"/>

...

## Develop community-vetted strategic plan

</br>
</br>

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

...

## Ecosystem-wide vision

<br/>

### 2000&ndash;2010

Driven by individual efforts and needs.

### 2010&ndash;2020

Individual projects adopt governance structures,
development processes, and roadmaps.

### 2020&ndash;2030

Need to think more strategically about the
ecosytem as a whole.

...

## Get projects funded

<br/>

Large-scale plans require long-term, sustained effort.

Funding is needed for increased participation.

Community is just starting to get funding.

Notes:

- Get projects funded

  - Decadal dev plan (evidence of need)
  - Workshops on grant writing
  - Funding is crucial for increased participation (via,
    e.g. full-time paid roles)

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>
</br>
</br>

<div style="font-size: 150%; font-weight: 400;">What you can do</div>

Notes:

...

## Support

- Contribute or support students who want to
- Reward and recognize efforts outside of paper writing
- Fund open, not closed software (and convince funders to do the
  same!)
- Apply lessons from SP to your work
  1. Test research code
  2. Executable papers (AKA automate everything)
  3. Collaborate widely, credit all those involved
  4. Insist on open code & data (reviewing and publishing)


*Developing open source scientific practice*<br/>
K. Jarrod Millman & Fernando Pérez<br/>
https://www.jarrodmillman.com/oss-chapter.html

...

<img src="images/abernathey-scientific-paper-outdated.png" width="100%"/>

...

<img src="images/why-contribute.png" width="100%"/>

Notes:

- Advance science
- Make an impact
- Grow as a developer
- Shape the tools you use

You are very welcome to join!

...

### Learn more

#### Website: https://scientific-python.org

<br/>

Has links to:

- Blog: https://blog.scientific-python.org
- Twitter: https://twitter.com/scientific_py
- YouTube: https://tinyurl.com/scientific-python-youtube
- Discourse: https://discuss.scientific-python.org
