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


<div style="font-size: 150%; font-weight: 600;">Scientific Python:<br/> In support of the developer community</div>

<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="200em"/>


<br/>
<br/>
<br/>
<br/>
<div style="text-align: left;">
Stéfan van der Walt<br/>
EuroSciPy 2024, 28 August 2024
</div>

Notes:

Introduce yourself, history with the scientific Python ecosystem, etc.

---

### What, and why?

<br/>

a **project** to better coordinate the **ecosystem** and support the community of contributors and **maintainers**.

<div class="center">
    <img src="images/ecosystem.svg" width="40%"/>
</div>

Notes:

Explain how conversations used to happen around the table at SciPy and EuroSciPy.
How developers all used to know one another.

...

### Timeline

- July 2018 — New landing site for Scientific Python ([issue #1](https://github.com/scientific-python/scientific-python.org/issues/1))
- December 2018 — Asked by the Moore Foundation for a short proposal
- January 2019 — first draft
- June 2020 — funding approved
- December 2020 — Jarrod Millman and I officially start The Scientific Python Project

Notes:

- A lot of work's been done since then! We'll outline some of it here.

...

#### https://scientific-python.org/

<img src="images/home.png" width="80%"/>

---

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

<img src="images/spec0.png"/>

...

## SPEC 1 — Lazy Loading of Submodules and Functions

<img src="images/spec1.png"/>
...

## SPEC 4 — Using and Creating Nightly Wheels

<img src="images/spec4.png"/>

...

## SPEC 6 — Keys to the Castle

...

## SPEC 7 — Seeding pseudo-random number generation

...

## SPEC 8 — Securing the Release Process

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>


<img src="images/home-summits.png"/>

...

## Second Scientific Python Developer Summit

<img src="images/seattle-2024.jpg" width="60%">

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

<img src="images/repo-review.png" width="75%"/>

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
- deprecate SciPy’s sparse matrices and, eventually, `numpy.matrix`
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

## CZI grant

<img src="images/czi-grant-announce.png" style="border: 1px solid;" width="70%"/>

- In collaboration with Quansight
- Accessibility
  - https://pydata-sphinx-theme.readthedocs.io/en/stable/
- Translation
  - https://blog.scientific-python.org/scientific-python/translations/
  - https://scientific-python-translations.github.io/
- Scientific Python Hugo theme
- DevStats
- interactive docs
  (building on work by Pyodide & JupyterLite teams)
- Release management / tooling

---

<!-- Section: SP project -->

<div style="font-size: 300%; font-weight: 600;"> Scientific Python</div>
<img alt="Scientific Python logo" src="images/scientific-python-logo.svg" width="100em"/>

</br>
</br>

<img src="images/home-community.png"/>
...


#### https://discuss.scientific-python.org/

<img src="images/discuss.png" width="60%"/>

...

#### https://bit.ly/talk-sp

<img src="images/discord-qr.png" width="15%"/>
<br/>

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

### How can you get involved?

...

### Q&A

https://scientific-python.org

<br/>

Follow me on Mastodon:<br/>
<br/>
<a href="https://emacs.ch/@stefanv">@stefanv@mentat.za.net</a>
