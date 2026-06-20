---
marp: true
theme: gaia
paginate: true
backgroundColor: #ffffff
color: #444444
math: katex
style: |
  section {
    font-family: "Helvetica Neue", Arial, sans-serif;
    padding: 48px 58px;
    background: #ffffff;
    color: #444;
  }
  
  section::after {
  font-size:0.9em;
  top: 100px;
  right: 40px;
  bottom: auto;
  left: auto;
  }
  
  section.title::after {
  display: none;
  }

  section.title {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    color: #555;
    border-bottom: 18px solid #7ba6b8;
  }

  section.title h1 {
    color: #555;
    font-size: 1.4em;
    line-height: 1.22;
    margin-bottom: 0.35em;
  }

  section.title h2 {
    color: #777;
    font-size: 1.05em;
    border: none;
    margin-top: 0;
  }
  
 

  section:not(.title) h1 {
    font-size: 0.78em;
    font-weight: 400;
    margin: 0 0 0.15em 0;
  }

  section:not(.title) h2 {
    font-size: 1.35em;
    font-weight: 500;
    margin: 0 0 1.05em 0;
    padding-bottom: 0.28em;
    border-bottom: 5px solid currentColor;
  }

  section.intro h1, section.intro h2, section.intro strong { color: #7ba6b8; }
  section.background h1, section.background h2, section.background strong { color: #2e55a1; }
  section.method h1, section.method h2, section.method strong { color: #3d7f4f; }
  section.results h1, section.results h2, section.results strong { color: #a51e5a; }
  section.conclusion h1, section.conclusion h2, section.conclusion strong { color: #e57224; }
  

  .center {
    text-align: center;
  }

  .large {
    font-size: 1.35em;
    line-height: 1.45;
  }

  .huge {
    font-size: 1.65em;
    line-height: 1.35;
  }

  .small {
    font-size: 0.76em;
  }

  .tiny {
    font-size: 0.62em;
  }

  .two {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 36px;
    align-items: start;
  }

  .three {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 26px;
    align-items: start;
  }

  .box {
    border: 2px solid #d6d6d6;
    border-radius: 14px;
    padding: 20px 26px;
    background: #fafafa;
  }

  .bluebox {
    border-left: 8px solid #7ba6b8;
    padding: 16px 22px;
    background: #f4f8fa;
  }

  .greenbox {
    border-left: 8px solid #3d7f4f;
    padding: 16px 22px;
    background: #f4faf6;
  }

  .pinkbox {
    border-left: 8px solid #a51e5a;
    padding: 16px 22px;
    background: #fbf4f8;
  }

  table {
    font-size: 0.78em;
    width: 100%;
  }

  th {
    background: #f2f2f2;
  }

  td, th {
    padding: 0.32em 0.55em;
  }
  
  pre {
  font-size: 0.68em;
  line-height: 1.18;
  margin: 0.25em 0 0.55em 0;
  }
  
  .fig {
  width: fit-content;
  max-width: 100%;
  margin: 0 auto;
  text-align: center;
  }

  .fig img {
    display: block;
    max-width: 100%;
  }

  figcaption {
    color: #777;
    font-size: 0.62em;
    margin-top: 0.3em;
  }

---

<!-- _class: title -->

# Marp 

## Slide Template

Date

Name
Affiliation

<!--
Speaker note:
Write speaker notes here.
They are not shown to the audience, but can be used in Presenter View or during HTML export.
-->

---
<!-- _class: intro -->

# 1. Introduction
## Text Style

- **Bold**
- ~~strikethrough~~
- _italic_
- > quote
- `inline code`
- ```Haskell
  import qualified Data.List as L
  import Data.Map
  ```
- $\KaTeX$



---
<!-- _class: background -->
# 2. Background
## Text Size

<div class = "three">
<div class ="huge">
huge
</div>
<div class = "large">
large
</div>
normal
<div class = "small">
small
</div>
<div class = "tiny">
tiny
</div>
</div>
<br>
<hr>
Heading
<div class = "two">

### \### a
#### \#### a
##### \##### a
###### \###### a
</div>


---
<!-- _class: method -->
# 3. Method
## Boxes and Columns

Two Column
<div class = "two">
  <div class = "box">
    box
  </div>
  
  <div class = "box">
    box
  </div>
</div>

<br>
Three Column
<div class = "three">
<div class = "bluebox">
blue box
</div>
<div class = "greenbox">
green box
</div>

<div class = "pinkbox">
pink box
</div>
</div>

---

<!-- _class: results -->
# 4. Results
## Table and Image
| Left align | Center align | Right align | 
| :--------- | :----------: | ----------: | 
| left       | center       | right       |


<div class ="two">

<div class = "small">
  
  - image
    - use *figure* (centerlize)
    <figure class ="fig">
      <img src="sample_dep.png" height="80">
      <figcaption> Figure 1. caption </figcaption>
    </figure>
    
    - import directly    
      ![h:80](sample_dep.png)
      <figcaption>Figure 2. caption</figcaption>

</div>


<div>

- drawio.svg

![w:9em](sample_diagram.drawio.svg)
<figcaption> Figure 3. When <code>sample_diagram.drawio.svg</code> is edited with the VSCode draw.io extension, the changes are applied automatically. </figcaption>
</div>

---
<!-- _class: conclusion -->
# 5. Conclusion
## Marp CLI

<small>
Install:

```bash
npm install -g @marp-team/marp-cli
```

Preview / export:

```bash
marp slide_template.md --preview
marp slide_template.md -o slide_template.pdf
marp slide_template.md -o slide_template.html
marp slide_template.md -o slide_template.pptx
```

Export with local images:

```bash
marp slide_template.md --allow-local-files -o slide_template.pdf
```

Watch mode:

```bash
marp slide_template.md --watch
```
</small>