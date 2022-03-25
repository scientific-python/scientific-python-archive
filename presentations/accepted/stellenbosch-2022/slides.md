<style type="text/css">
.black {
  color: black;
}
</style>

# Scientific Python

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

## Past, present, and future

<br/>
<div style="text-align: left;">
Stéfan van der Walt<br/>
University of California, Berkeley
</div>

...

## 2016: LIGO observes gravitational waves

<img src="images/LIGO_Hanford_aerial_05.jpg" width="49%" style="padding-bottom: 3rem;"/>
<img src="images/LIGO_measurement_of_gravitational_waves.svg" width="49%"/>

Notes:

2016
Laser Interferometer Gravitational-Wave Observatory

...

## 2019: EHT images a black hole

<img src="images/bh_diagram.jpg" width="44%"/>
<img src="images/EHT-image.jpg" width="54%"/>

...

## 2021: Ingenuity takes off on Mars


<img src="images/ingenuity.gif"/>

Notes:

2021
first powered controlled extraterrestrial flight

What do they have in common? Each has pipelines that utilize the Scientific Python ecosystem.
In this talk, I'd like to discuss why this is so special, how we got here, and what lies on the road ahead.

---

## What I do

[Show icons of all the open source projects]

Notes:

Your story of how you got involved in Scientific Python.

...

<img src="images/colormaps.webp"/>
<br/>
<img src="images/mothra_logo-text.png" width="10%" style="padding-bottom: 3rem; padding-right: 2rem;"/>
<img src="images/mothra-result.jpeg" width="80%"/>

...

<img src="images/cesium-blue-light.png"/>

<div style="color: darkgray;">

> Cesium is an end-to-end machine learning platform for time-series, from calculation of features to model-building to predictions. Cesium has <span style="color: black;">**two main components**</span> - a <span style="color: black;">**Python library**</span>, and a <span style="color: black;">**web application platform**</span> that allows interactive exploration of machine learning pipelines. Take control over the workflow in a Python terminal or Jupyter notebook with the Cesium library, or upload your time-series files, select your machine learning model, and watch Cesium do feature extraction and evaluation right in your browser with the web application.

</div>

Notes:

Importantly: non-regularly sampled time-series

...

<img src="images/naul-recurrent.png"/>

Naul, B., Bloom, J.S., Pérez, F. et al. A recurrent neural network for classification of unevenly sampled variable stars. Nat Astron 2, 151–155 (2018). https://doi.org/10.1038/s41550-017-0321-z

...

## SkyPortal

<img src="images/skyportal_responsive.png"/>

...

## Fritz

<img src="images/fritz.jpg"/>

...

## Fritz

<img src="images/fritz-animated.gif"/>

...

## What I do

A little bit of everything...

- Passionate about tool building
- But to build good tools you need to use them

Notes:

The applied mathematician's dream.

Scientific need -> use tools to solve problems -> see flaws in tools
-> improve -> repeat

---

<!-- Section: success of SP -->

## Scientific & engineering advances

<img src="images/LIGO_measurement_of_gravitational_waves.svg" width="30%" />
<img src="images/ingenuity.gif" width="50%"/>
<img src="images/EHT-image.jpg" width="40%"/>

Notes:

- Three major recent advances
- What do they have in common -> pipelines use SP
- This is just a small selection

...

<img src="images/numpy-nature.png" width="60%"/>
<img src="images/scipy-nature.png" width="60%"/>

...

NumPy downloads slide

...

StackOverflow trend picture

...

GitHub: Nate's talk with our faces in background

...

Katie Bouman's slide with our projects shown

...

## Teaching Python

At Berkeley, at least:

- Computer Science
- Data Science
- Information School
- Neuroimaging

... to name a few.

Notes:

This is no longer unusual, not only at UCB.

(Teaching, in itself, does not mean the tools are good for science,
but there's a practical element to it, namely...)

Students are equipped with Python by the time they arrive in research.

...

Use of Scientific Python is pervasive

It is being used in novel and leading science

It is continually improving, growing, responding to needs

Notes:

NumPy, e.g., stable, what could you want to change about it.
But we are refactoring the whole data type system.

...

The Scientific Python ecosystem of libraries
is **critical research infrastructure**.

[bridge image]

---

## Adoption

### Why is widespread adoption of SP ecosystem unusual?

Consider:

- Who developed the software
- When, and with what?

Notes:

- Small handful of students, junior researchers, other volunteres
- Predominantly in their spare time, over weekends and evenings
- Often little to no financial support

Competing against platforms built by companies with:

- Millions of dollars in funding
- Hundreds of dedicated programmers
- Pushes by big marketing teams, contracts with many corporations and universities

...

## Why is SP so successful?

1. Principles
2. Practices
3. People

...

## Principles

- Scientific software must be community developed, and community owned
- This is the best way to align incentives for doing good quality, transparent, reproducible science

Notes:

- We believe that researchers know their needs best
- Their ideas must be surfaces and integrated into the computational
  platform as efficiently as possible
- In this endeavor, making money for shareholders is at best a
  distraction
  - But often, it incentivises entirely the wrong things: hardware
    locks, license servers, closed file formats
  - Incentive to lock users into  proprietary systems
    - This prohibits sharing, reproducibility, and transparency

...

## Principles (II)

http://nipy.org/nipy/mission.html

<div style="color: darkgray;">

> We believe that neuroscience <span class="black">ideas and analysis develop
> together</span>.
> Good ideas come from understanding; <span class="black">understanding comes
> from clarity</span>, and <span class="black">clarity must come from</span> well-designed teaching
> materials and <span class="black">well-designed software</span>.
> The <span class="black">software must be</span> designed
> as <span class="black">a natural extension of the underlying ideas</span>.
>
> <span class="black">— Matthew Brett, ~2007, for NiPy</span>

</div>

Notes:

- Re-emphasises the notion of a user-developer
- Library interfaces and language clarity / expressivity matter: it's
  how we express our thoughts

...

## Practices

None of this matters if we cannot rely on the answers.

- Revision control
- Testing / continuous integration
- Code review
- Documentation
- Iteration

Notes:

Code review both during development cycle, but also during use where
users can easily introspect for problems.

Documentation has to stay in sync with code (docstrings).

...

<img src="images/gh-workflow.webp"/>

...

## People

> Healthy communities are built when everyone's voice is heard, when their perspective is valued, and when their work is recognized.

Work done in collaboration is better and more fun—depending on the people.

- Community
- Culture
- Leadership

Notes:

- Community

  - Many of my best friends I made through this ecosystem.

  - These have been the most fulfilling and educational collaborations
    of my life.

  - Being part of a movement where everyone is aligned is incredibly exciting.

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

---

## Challenges

- Developer time (review time)
- Funding
- Coordination

<br/>
<img src="images/gh-workflow.webp" width="50%"/>

Notes:

- Developer time
  - Very few full time like me
  - Contributor time varies (also: parents, breadwinners, etc.)

- Funding
  - No grant line items
  - Few company contributions
  - Mostly foundation-supported
    - Some grants, but need more

- Coordination
  - Used to be small (SciPy conf), now big
  - Nothing like project managers who can think about whole ecosystem,
    get user feedback, set up roadmaps, etc.
  - Coordination is haphazard

...

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

> The **Scientific Python project** aims to better coordinate the
> ecosystem and grow the community.

1. Coordinate projects
2. Get projects funded
3. Support & develop shared infrastructure
4. Improve onboarding & communication

...

### Coordinate projects

[screenshot discussion forum / SPEC document or approval flow]

Notes:

- Coordinate projects
  - SPECs (like PEPs, high level, endorsed by "core")
    - SPECs also allow for younger projects to propose ideas
  - Venues for discussion
    - Discourse forum
    - Virtual technical meetings
  - Watch ecosyste, identify pain points, and coordinate response

## Get projects funded

Notes:

- Get projects funded

  - Decadal dev plan (evidence of need)
  - Workshops on grant writing
  - With funding: full-time roles -> wider involvement

## Support & develop shared infrastructure

[scientific python screenshot]

Notes:

  - Tools used across ecosystem such as numpydoc
  - Standard web themes for core projects

...

## Improve onboarding & communication

[screenshot of blog, youtube]

Notes:

  - Developer meetings on pain points
  - Social media
    - Onboarding
    - Dev interviews
    - SP library examples
  - Learn: material for users, contributors, maintainers
  - Blog: informal
  - Discourse discussion forum

## The people behind these efforts

[screenshot of teams]

---

## What can you do?

