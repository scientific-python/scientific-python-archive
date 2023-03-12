<style type="text/css">
.reveal .slides > section > h1, h2, h3 { text-align: center; }
.reveal .slides > section > section { text-align: left; }
ul { padding-left: 0rem; }
ol { padding-left: 1rem; }
.reveal blockquote {
  box-shadow: none;
  border-left: 10px solid #DDE;
  padding-left: 1rem;
  margin-left: 0;
}
.center-quote blockquote {
  margin-left: auto;
}

</style>

<div style="font-size: 300%">scikit-image</div>
<div style="font-size: 150%">From 0.20 to 2.0</div>

<br/>
<br/>
<br/>
<br/>
<div style="text-align: left;">
Stéfan van der Walt<br/>
University of California, Berkeley
</div>

<!--

We are especially interested in major challenges you
face when performing image analysis, any training efforts you do to
transfer the skills of image analysis, and the computational tools
(software, data structures, packages, workflows) you develop or rely
on in your research.

Talk is 20 minutes.

-->

...

### What is `scikit-image`?

<div class="center-quote">

> scikit-image is a collection of algorithms for image processing. It is available free of charge and free of restriction. We pride ourselves on high-quality, peer-reviewed code, written by an active community of volunteers.

</div>

...

### Community ethos

<div class="center-quote">

> We welcome each and every contributor to scikit-image. Our aim is enthusiastic and productive collaboration, to build an excellent software library, and to have a ton of fun doing it. We encourage one another to be gentle in criticism of others’ work, humble in acknowledging our own mistakes, and generous in our praise.

</div>

...

## 0.20 — released!

71 authors, 42 reviewers, 275 pull requests merged!

- Anisotropic images in `skimage.measure`
- Performance improvements, e.g. footprint decomposition in `skimage.morphology`
  <img src="images/footprint_decomposition.png" width="40%"/>
- More N-dimensional support
- More consistent API, including `channel_axis` for indicating multi-channel images
- New build system: Meson

---

## skimage 2.0

Motivation:

- Organic API growth over a decade
  - Harmonization of concepts such as random seed
- Early design decisions
  - Data type range inferral
  - `transform` module coordinate convention
- Operations on non-NumPy array containers

[SKIP3](https://scikit-image.org/docs/stable/skips/3-transition-to-v1.html), [SKIP4](https://scikit-image.org/docs/stable/skips/4-transition-to-v2.html)

...

## A pragmatic pathway

[A Pragmatic Pathway Towards skimage2](https://discuss.scientific-python.org/t/a-pragmatic-pathway-towards-skimage2/530/24)

Principles for a transition (my opinion):

1. Do not estrange your existing user base.
2. Ensure transitioning of majority of users.
3. Do not place an undue burden on maintainers.
4. Initially, allow using old and the new APIs in conjunction.

A potential route:

1. Release `skimage2` (still distributed as pip install `scikit-image`).
2. This package contains both `skimage` and `skimage2` libraries.
3. Over time, deprecate the functions in `skimage` with instructions.
4. Eventually remove `skimage`, with instructions.

---

## Challenges

...

### Software development in academia (I)

- Lacking credit & evaluation (still papers)
- Few suitable academic positions

Despite:

- Impact
- Better science
  - User-developers
  - Science more transparent, reproducible, verifiable
  - Open work often more collaborative

...

#### Software development in academia (II)

You can help:

- Contribute or support students who want to contribute
- Reward and recognize efforts outside of paper writing
- Fund open, not closed software (and convince the NSF/NIH/... to do the
  same!)
- Apply lessons from open source computationa research software to your work:
  1. Test research code
  2. Executable papers (AKA automate everything)
  3. Collaborate widely, credit all those involved
  4. Insist on open code & data (reviewing and publishing)

*Developing open source scientific practice*, K. Jarrod Millman & Fernando Pérez<br/>
https://www.jarrodmillman.com/oss-chapter.html

...

### Sustained support

**CZI EOSS (Cycle 5)**

- [skimage 2.0 API transition, types, and maintenance grant](https://chanzuckerberg.com/eoss/proposals/from-library-to-protocol-scikit-image-as-an-api-reference/)
  - Outreachy Internships
    - Projects:
      1. Enhance image warping in scikit-image with thin-plate spines
      2. Expand scikit-image gallery with biomedical examples (narrative documentation)
    - Currently in contribution period
    - Interns announced May 4th; internship from May 29th to August 25th

**Scientific Python**

Release management & maintenance

**Tidelift**

<hr/>

Which other mechanisms are available?

---

## <span style="font-family: lato; text-transform: none; font-size: 125%;">Scientific Python</span><img src="images/scientific-python-logo.svg" width="5%" style="align: bottom;"/>

<div style="display: flex;">



> The **Scientific Python project** aims to better coordinate the
> ecosystem and grow the community.

</div>

Immediate goals:

1. Coordinate (e.g., SPECs, discussion forums)
2. Support & develop shared infrastructure (`yaml2ics`, `devpy`, ...)
3. Get projects funded
4. Foster the next generation of contributors

...

## PyOpenSci

Slide here.

---

## 👋

**https://scikit-image.org**

Visit the **gallery**, **user forum**, or **developer forum**.

https://forum.image.sc/tag/scikit-image ⬅ biology community, all tools


- **Email:** stefanv@berkeley.edu
- **Mastodon:** [@stefanv@emacs.ch](https://emacs.ch/@stefanv)
- **Twitter:** [@stefanvdwalt](https://twitter.com/stefanvdwalt)
