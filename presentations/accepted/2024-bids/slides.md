<style type="text/css">
.black {
  color: black;
}
.inline-left {
  display: inline-block;
  text-align: left;
}
.reveal ul {
  margin: 0;
}
</style>


<div style="font-size: 150%; font-weight: 600;">Scientific Python:<br/> Community, Tools, and Open Science</div>

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="200em"/>


<br/>
<br/>
<br/>
<br/>
<div style="text-align: left;">
Stéfan van der Walt<br/>
BIDS Seminar, 7 May 2024
</div>

Notes:

- Introduce yourself
- Before I joined BIDS I was a lecturer in Applied Mathematics in SA
- Joined BIDS in 2015
- It's been almost a decade, and what is fantastic about my job is that I
  get to work on different research problems every year
- I also get to follow my passion: developing open source scientific software
  - there are not very many positions in the world that allow that

---

## The scientific Python ecosystem

### Origins

Most research computing is done with commercial software.

Notes:

- In early 2000s, status quo is that most science is done with closed, commercial software.

  - MATLAB, Mathematica, and Maple

  - People use what their colleagues use for interoperability.

  - There are early examples of freely distributed software from early
    on
    - Some researchers used Fortran
    - And there were packages: SPICE, Fortran libraries like Netlib LAPACK, MINPACK, EISPACK,
      Berkeley Software Distribution, and later R, GNU Octave, etc.
    - But when I arrived on the scene, commercial software was common and firmly established

...

### Origins

Scientists notice Python.

Notes:

- Mid-90s: scientists started noticing Python.

  - Numeric written by Jim Fulton and generalized by Jim Hugunin.

- Astronomy becomes interested, writes Numarray to handle large images.

- Hardware control:
  - Hard to get new firmware, or long wait times for companies to fix bugs.
  - Can write control interfaces in low-level language.
  - But control is much easier in high-level langauge.
  - Now that you are controlling hardware from Python, can you process it there as well?
    Can you upload results to a database, or generate reports directly?
    - Power of a general-purpose language becomes obvious.

...

### Origins

Practical motivations arise.

Notes:

- Practical motivations for finding a new, unrestricted computational platform.
  - License servers are a pain.
  - Students learn a language, but often cannot afford software once they leave university.
  - Specialized languages mean users have to learn multiple languages.
  - Cannot share research with collaborators without software license, or who use different software packages.

...

### Origins

<div class="inline-left">

Philosophical motivations align.

- Transparency for validation
- Insight
- Control
</div>

Notes:

- From a philosophical viewpoint, there were problems with the status quo.

  - Science requires transparency: you must be able to *check* that your, and others', results are correct.
  - Scientists need to understand their tools to use them properly.
  - Ideally, scientists are able to *modify* tools to best fit their purpose.

...

### Modifying your tools (a short detour)

<div class="center">
<img src="images/reprap.jpg"/>
</div>

Notes:

- Got 3D printer as a gift
- A paradigm shift; no longer go to Ace and jury rig a part
- If you want to make a custom part or tool, you need to understand the problem very well
- But once you do, you can make the tool that *exactly* matches what you need
- For home improvement that doesn't matter so much; for science it is very important.

...

### Origins

<div class="inline-left">
The philosophical considerations require software that is:

- Free (money, and right to modify).
- Developed openly.
- Is owned (controlled) by the research community.
</div>

This way, we build a *commons*.

...

### Origins

An early ecosystem coalesces.

Notes:

- NumPy evolves from Numeric & NumArray.
- SciPy, IPython (precursor of Jupyter), and Matplotlib are developed.
  - Algorithms + interface + visualization.
- Albeit brittle and incomplete computational platform: an ecosystem.

<!-- Section: SP project -->

...

### Origins

A community forms.

Notes:

- Developing these packages were *fun* and *exploratory*;
  we were imagining what these tools and the ecosystem could be.
- A small community of researcher-developers formed, including many students.
  They were very enthusiastic about their new toys!
- Many meet at the annual SciPy conference, and spoke about the
  direction development should take.
- At this point in time, it's very much an aspirational project.

...

### Fast forward 10 years...

---

### The Data Science Revolution

Computational tools become a core research dependency.

Notes:

- Around 2015 or so, Data Science became A Big Deal.
- I still don't have a precise definition of data science, but the
  phenomenon arose out of some mixture of high data availability, an
  increase in computational ability, and machine learning making it
  possible to gain insights from large datasets.
- What is clear is that most fields have or are moving deeper into
  computational science.
- From the beginning, Data Science bought into the idea of open source tool-chains.
  - Perhaps this is due to decades of advocacy for open and reproducible science,
  - perhaps it was due to the ML community having bought into Python,
  - or perhaps it is simply pragmatic, given that R and Python were well known, mature, and free.
- The new-found need for computational tools greatly increased the number of users of our tools.

...

### Fast forward another 5 years...

---

### The Scientific Python Project

#### Founding

Notes:

- Our tools are now widely adopted.
- The SciPy conference has grown from eighty participants to a thousand participants.
- Developers no longer meet around a table to discuss the future.
- Maintainers are overloaded, supporting many more users than before, with little additional help.
- In response to these challenges, we create The Scientific Python project.

...

### Scientific Python is...

<br/>

a **project** to better coordinate the **ecosystem** and support the community of contributors and **maintainers**.

<div class="center">
    <img src="images/ecosystem.svg" width="40%"/>
</div>

...

#### https://scientific-python.org/


<img src="images/home.png" width="80%"/>


---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>

<img src="images/home-specs.png"/>

Notes:

- Add some notes on the SPECs and what they are

...

#### https://scientific-python.org/specs/

</br>


Scientific Python Ecosystem Coordination documents provide operational guidelines. 

</br>

<img src="images/spec-list.png"/>

...

## SPEC Core Projects

<img src="images/spec-core.png"/>

...

## SPEC Steering Committee

<img src="images/spec-committee.png" width="50%"/>

...

## SPEC 0 — Minimum Supported Versions

<img src="images/spec0.png" width="70%"/>

...

## SPEC 1 — Lazy Loading of Submodules and Functions

<img src="images/spec1.png"/>
...

## SPEC 4 — Using and Creating Nightly Wheels

<img src="images/spec4.png"/>

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>


<img src="images/home-summits.png"/>

...

## Second Scientific Python Developer Summit

Planning meeting, yesterday:<br/>
<img src="images/checkin.webp" width="60%">

- Seattle, June 3–5:<br/>https://scientific-python.org/summits/developer/2024/
- Report from last year:<br/>https://blog.scientific-python.org/scientific-python/dev-summit-1/

Notes:

- In-person work meetings

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>

<img src="images/home-development.png"/>

...

#### https://learn.scientific-python.org/development/

<img src="images/development.png"/>

...

#### https://learn.scientific-python.org/development/guides/repo-review/

<img src="images/repo-review.png"/>

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>

<img src="images/home-lectures.png"/>

...

#### https://lectures.scientific-python.org/


<img src="images/lectures.png" width="90%" />

...

#### https://lectures.scientific-python.org/

<img src="images/lectures-toc.png"/>

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>

<img src="images/home-sparse.png"/>

...




## Sparse Arrays for Scientiﬁc Python

</br>

- improve sparse structures in SciPy so they support array semantics
- deprecate SciPy’s sparse matrices and `numpy.matrix`
- assist with sparse array adoption in downstream ecosystem packages

</br>
</br>
</br>
</br>

### More information

- https://scientific-python.org/grants/sparse_arrays/
- https://scientific-python.org/summits/sparse/
- https://scientific-python.org/calendars/
- https://blog.scientific-python.org/scientific-python/dev-summit-1-sparse/

...

#### https://scipy.github.io/devdocs/reference/sparse.html 

<img src="images/scipy-sparse.png"/>

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>

<img src="images/home-community.png"/>
...


#### https://discuss.scientific-python.org/

<img src="images/discuss.png"/>

...

#### https://discord.com/invite/vur45CbwMz


</br>
</br>

<img src="images/discord.png"/>

...

#### https://blog.scientific-python.org/

<img src="images/blog.png" width="70%" />

---

## Tools

<img src="images/tools.png">

...



</br>

<style>
.container{
    display: flex;
}
.col{
    flex: 1;
}
</style>

<div class="container">

<div class="col">

### Development

- [lazy_loader](https://github.com/scientific-python/lazy_loader/)
- [spin](https://github.com/scientific-python/spin)
- [pytest-doctestplus](https://github.com/scientific-python/pytest-doctestplus)
- [repo-review](https://github.com/scientific-python/repo-review)
- [changelist](https://github.com/scientific-python/changelist/)

</br>
</br>

### Web

- [scientific-python-hugo-theme](https://github.com/scientific-python/scientific-python-hugo-theme)

</div>

<div class="col">

### Organization

- [yaml2ics](https://github.com/scientific-python/yaml2ics)
- [discuss.scientific-python.org](https://discuss.scientific-python.org/)
- [vault-template](https://github.com/scientific-python/vault-template)

<br/>
<br/>

## Insight

- [devstats](https://github.com/scientific-python/devstats)
- [https://views.scientific-python.org/](https://github.com/scientific-python/devstats)

</div>

<div class="col">

### GitHub

- [upload-nightly-action](https://github.com/scientific-python/upload-nightly-action)
- [attach-next-milestone-action](https://github.com/scientific-python/attach-next-milestone-action)
- [sync-teams-action](https://github.com/scientific-python/sync-teams-action)
- [reverse-dependency-testing](https://github.com/scientific-python/reverse-dependency-testing)
- [action-check-changelogfile](https://github.com/scientific-python/action-check-changelogfile)
- [action-towncrier-changelog](https://github.com/scientific-python/action-towncrier-changelog)

</div>

</div>

...

#### https://scientific-python.org/calendars/

<img src="images/calendar.png" width="80%"/>

...

#### https://devstats.scientific-python.org/

<img src="images/devstats.png" width="80%"/>

---

## On the horizon

Fernando Pérez, academic director, vision:

https://bids.berkeley.edu/about/directors-vision-2024

A renewed emphasis of the importance of open software and research:

> Our scientists partner with an extended, distributed **community** of
> other researchers and developers to **build** an **ecosystem** that benefits
> **all**. This is how we will build much more in coming years: work
> grounded in the **expertise** of our scholars and immediately **applied** to
> our research and educational needs, but in **open collaboration** with
> partners near and far, to build **access** to **research** and **education**
> that is **impactful**, **accessible**, and **fair**.

...

## On the horizon

<div class="inline-left">

[Open Source Project Office](https://bids.berkeley.edu/news/uc-berkeley-joins-effort-advance-open-source-initiatives-across-uc-system)

Areas we intend to work on:

- statistics in Python
- domain stacks (astronomy, earth & space science)
- supply-chain security<br/>
  [Panel on May 9th](https://events.berkeley.edu/BIDS/event/246188-understanding-the-xz-security-breach-and-open-source-).
- coordinated releases
- summer schools
- vetted, shared governance models

... and more.

</div>

Notes:

- OSPO: an attachment-point for open source conversations on campus

---

### Q&A

https://scientific-python.org

<br/>

Follow me on Mastodon:<br/>
<br/>
<a href="https://emacs.ch/@stefanv">@stefanv@mentat.za.net</a>

---

# Extra slides

...

## Challenges in OS Scientific Software

- Grow the contributor pool
- Sustain the contributor pool
- Governance

...

## Support

<div class="inline-left">

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

</div>

...

### Benefits for Contributors

- Advance science
- Make an impact
- Grow as a developer
- Shape the tools you use

You are very welcome to join!

...

#### https://scientific-python.org/grants/

<img src="images/grants.png"/>

...

### (Sideline) What about AI?

Are "traditional" scientific computational tools (algorithmic implementations) still viable.

Notes:

- Won't go too deeply into this now, but it's an interesting question to consider:

  - Given the resurgence in AI research, and the many incredible applications we've seen, is there still room for libraries that implement "classic" algorithms?

- My quick answer to that is: yes.

  - Libraries are as much about establishing APIs, i.e., human interfaces, as they are about code, and the skill of producing those and shipping them remains relevant.

  - Sometimes, you know what you need to do with your numbers. E.g., you may simply want to compute an FFT. Then, you want NumPy or SciPy around to do that for you. Often, you need to pre-process your data, or post-process AI output. AI and classical tools work well enough together.

  - Not all problems are well suited to AI and we are still in the very beginning of understanding the reliability of AI predictions, and knowing its failure modes. This is an evolving space that we're watching with interest.

...

### Some notable BIDS projects

<div class="container">

<div class="col">
<img src="images/viridis.png"/><br/>
<img src="images/mothra_small.jpg"/>
</div>

<div class="col">
<img src="images/fritz.png"/>
</div>

</div>


---
