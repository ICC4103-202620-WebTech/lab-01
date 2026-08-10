# Lab 1 — Your Personal Page

**Monday, August 10** · Covers Class 1 (HTML, CSS and the DOM) · Learning Outcome 1

## Objective

Build and publish a personal page written in hand-written HTML and CSS. The page must state **what
its parts are**, not only how they look, and it must be usable on a phone and on a laptop without a
CSS framework.

This is the page you will keep working on: in Lab 2 you will add behaviour to it with the DOM.

## Before you start

You need these three things working on the machine you bring to the lab. None of them is part of the
lab, and none of them is worth spending the session on:

- A **GitHub account**.
- **git** installed and able to push to GitHub.
- A text editor and a browser with DevTools.

## The deliverable

You are delivering **two things that point at each other**: a repository with the source of your
page, and that same page published and reachable on the open web.

**1. The repository.** Create a **new, empty, public** repository in **your own** GitHub account,
named `webtech-lab-01`. Do not fork this one, and do not reuse a repository from another course.

**2. The files.** At the root of the repository:

| File | What it is |
|---|---|
| `index.html` | Your page. The name matters — GitHub Pages serves it as the site's home page. |
| At least one `.css` file | Your stylesheet. The name is up to you. |
| `README.md` | See below. |

Any images you use are also committed to the repository. Do not link to an image sitting on someone
else's server.

**3. The published site.** Enable **GitHub Pages** on the repository, serving from the root of your
default branch. The resulting URL looks like `https://<your-user>.github.io/webtech-lab-01/`. Open
it in a private window before you submit: if it does not load there, it is not published.

**4. The two links.** Both are required, in both directions:

- Your `README.md` contains your full name and the **URL of the published site**.
- Your page contains a link to **the repository** it was built from.

**5. Canvas.** Submit **one** of the two URLs — the repository or the published site, whichever you
prefer. Because each one links to the other, either is a valid way in. Submitting a URL that does
not lead to the other half is an incomplete delivery.

This lab is **individual**. One submission per student.

---

## Requirements

### 1. The document

Your page is a single HTML file served as the site's home page, plus at least one **external**
stylesheet. Styles written inside `<style>` tags or in `style` attributes do not count.

The document must include, at minimum:

- A doctype declaration.
- A language declaration on the root element.
- A character encoding declaration.
- A **viewport** declaration. Without it the browser on a phone renders your page as a shrunken
  desktop page, and every layout requirement below fails on the device that matters most.
- A `title` that names you. It is what appears in the browser tab and in search results.

### 2. Content

The page is about you. It must contain at least:

- Your full name, your degree and your year of admission.
- A short introduction — two or three sentences, written by you.
- A list or table of your skills: languages, tools, anything you actually use.
- At least **two** items that stand on their own — a project, a course, a job, something you have
  built or done. Each one has its own heading and its own description.
- At least one image with a caption.
- At least one link to a site outside your page, one link to your GitHub profile, and the link to
  this page's own repository required by the deliverable.
- A contact form. See requirement 6.

### 3. Semantic markup

The markup is marked against the vocabulary from Class 1. Your page must use, correctly:

- `header`, `nav`, `main`, `footer` — `main` appears exactly once.
- `section` and `article`, each used for what it means: a thematic grouping with a heading, and a
  self-contained piece respectively.
- `figure` with `figcaption` for the captioned image.
- At least one `aside`, `time`, `address` or `blockquote`, used where it genuinely carries meaning.

Headings form an outline: exactly one `h1`, and no level skipped on the way down. Heading levels are
structure, not font sizes — if a heading is the wrong size, that is a CSS problem.

`div` and `span` are allowed where no element carries the meaning you need. A page built mostly out
of them does not meet this requirement.

### 4. Layout

Your CSS must contain at least one **Grid** container and at least one **Flexbox** container, and
each must be the right tool for the shape it arranges. Using Grid for a row of navigation links, or
Flexbox to build a two-dimensional page skeleton, meets the letter of this requirement and not its
intent.

`float` is not a layout tool. Do not use it to place blocks side by side.

### 5. Responsive behaviour

The page must be usable at a viewport width of **375px** and at **1280px**:

- No horizontal scrolling at either width.
- No text overflowing its container, and no image wider than the screen.
- At least one region of the page **reflows** — a group that shows several columns on a wide screen
  collapses to a single column on a narrow one.

You will be marked on the result, not on the technique. Grid can produce that reflow without a single
breakpoint; media queries are also acceptable where they are genuinely needed.

### 6. Accessibility

Accessibility is structural, and it is graded:

- Every image has an `alt` attribute whose value describes the image, or is empty if the image is
  purely decorative.
- Every form control has a `label` associated with it. Placeholder text is not a label.
- Body text meets a contrast ratio of at least **4.5:1** against its background. Check it in the
  DevTools contrast inspector, not by eye.
- The whole page can be traversed with the Tab key, in an order that makes sense, and the focused
  element is **visibly** distinguishable. If your CSS removes the default focus outline, it must
  replace it with something at least as visible.

Your contact form asks for a name, an email address and a message, and has a submit button. Choose
the `type` of each control so that a phone shows the right keyboard. The form does not do anything
when submitted — there is no server yet. That is Class 8.

### 7. What you may not use

- **No CSS framework.** No Bootstrap, no Tailwind, no stylesheet loaded from a CDN. Bootstrap arrives
  in Lab 4, once the primitives are in place.
- **No JavaScript.** The page is HTML and CSS only. Behaviour is Lab 2.
- **No page builder or site generator.** The HTML and the CSS are files you wrote.

You may use CSS features we did not cover in class; nothing in this lab requires them.

---

## Documentation

You are expected to work from the official documentation rather than from tutorials:

- MDN — [HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- MDN — [CSS layout](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout)
- WCAG 2.2 — [Quick Reference](https://www.w3.org/WAI/WCAG22/quickref/)
- GitHub — [Publishing with GitHub Pages](https://docs.github.com/en/pages)

## Grading

| Item | Weight |
|---|---:|
| The document: doctype, language, encoding, viewport, external stylesheet, title | 10 |
| Content: everything listed in requirement 2 is present | 10 |
| Semantic markup and heading outline | 25 |
| Layout: Grid and Flexbox, each used for the right shape | 20 |
| Responsive behaviour at 375px and 1280px | 15 |
| Accessibility: alt text, labels, contrast, keyboard and focus | 15 |
| Delivery: published on GitHub Pages, and the repository and the page link to each other | 5 |

Using a CSS framework, JavaScript or a page builder voids the layout and semantics sections.

## Deadline

**Tuesday, August 11, 20:00**, on Canvas.
