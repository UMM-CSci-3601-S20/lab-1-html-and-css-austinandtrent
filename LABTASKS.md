# Lab Tasks <!-- omit in toc -->

Be sure to follow the setup instructions in the [README.md](README.md) to set up
GitHub pages (including changing the line in the `Running your project` section of
the [README.md](README.md) to link to your team's GitHub pages page).

- [Summary](#summary)
- [Extending the HTML](#extending-the-html)
- [Add CSS for the new HTML](#add-css-for-the-new-html)
- [Create a new CSS file](#create-a-new-css-file)
- [Technical Requirements for the CSS](#technical-requirements-for-the-css)
- [How do you know you are "done"? How will you be graded?](#how-do-you-know-you-are-%22done%22-how-will-you-be-graded)

## Summary

Your tasks for this lab are:

- To add a small bit of HTML using classes and IDs to allow you to format
  different components in different ways.
- To develop an additional, new look for a web page using different CSS without altering
  the HTML.

All of the formatting (including the positioning of elements in the page) must
  be done using CSS. **Do not alter the HTML** with two exceptions:

- You have to extend the HTML in the first part. You should do that before you do
  any of the CSS work.
- If you want to load Google Fonts you'll want to add those tags to your HTML so
  they'll be available in your CSS. (There are ways to do this entirely in CSS
  but the "standard" approach typically involves modifying the HTML.)

Be intentional and sparing with your use of absolute sizes for things like font and
location. Your style sheet should make the web page look nice for both a phone and
a computer screen, and your choices should not interfere with accessibility in
obvious ways.

## Extending the HTML

The current HTML has three major sections:

- CSci Program Student Learning Outcomes (PSLOs)
- CSci major requirements
- CSci faculty

You should add a new section to the HTML (without changing any of the existing HTML)
that provides a list of some of the tools we'll be using in this class:

- [`git`](https://git-scm.com/)
- [GitHub](https://github.com/)
- [GitKraken](https://www.gitkraken.com/git-client)
- [Visual Studio Code](https://code.visualstudio.com/)
- [JUnit](https://junit.org/)
- [Karma](https://karma-runner.github.io/latest/index.html)
- [Protractor](https://www.protractortest.org/#/)
- [GitHub Actions](https://github.com/features/actions)

Some requirements:

- Add some sort of header for this section that indicates what information is
  being presented.
- Each item should be be a link to the same URL as provided in the links in the
  list above.
- The following items should be in class "cloud": GitHub.com and GitHub Actions.
  Every other item should be in the class "local".
- All items should be in a class indicating that tool's area of functionality:
  - `version-control` for `git`, GitHub.com, and GitKraken`
  - `ide` for Visual Studio Code
  - `testing` for JUnit, Karma, Protractor, and GitHub Actions

You can provide multiple, space-separated classes for an item, e.g.,

```html
  <li class="local version-control" id="git">
    <a href="https://git-scm.com/"><code>git</code></a>
  </li>
  <li class="local ide" id="vscode">
    <a href="https://code.visualstudio.com/">Visual Studio Code</a>
  </li>
```

## Add CSS for the new HTML

Add CSS that incorporates this new HTML into the look and feel of the original
version of the web page. A few specific requirements:

- The tool list information should be displayed as a block like the other three sections.
- The header should be obviously different from the content.
- The `local` and `cloud` items in the list should be formatted differently.
- The `version-control`, `ide`, and `testing` items should be formatted differently
  from each other.

These last two are somewhat tricky since you're trying to provide information along
two independent axes through just text formatting. You might do some thinking and
reading about how you can [style text](https://www.w3schools.com/css/css_text.asp)
in CSS and [work with fonts](https://www.w3schools.com/css/css_font.asp).

## Create a new CSS file

We've created a stub `style2.css` CSS file that you should flesh out to provide a
different, but complete and coherent styling of the HTML page.

## Technical Requirements for the CSS

Please read carefully the list of technical requirements below and follow it precisely.

- Your page must be viewable using the three different **external CSS files** included
  in your repository (one will be an example and you will alter the other two).
- Your **CSS must validate** using a [CSS validator](https://jigsaw.w3.org/css-validator/),
  except perhaps warnings about features not supported in all browsers.
  - Pro tip: Some newer CSS features are not widely supported. If a CSS feature you use
    is not supported in some browsers, please clearly indicate which browsers support it
    and which ones don't.
  - We've provided links to both the HTML validator and the CSS validator in the
    `Validation` section of the page. Both validate "out of the box", and you should
    make sure they continue to validate as you go through the lab.
  - Your CSS must make the page **look reasonable and be relatively easy to navigate.**
    We will take points off for features that lead to a problematic user experience. Take
    care that your design avoids common pitfalls.
    - Avoid links that are hard to see.
    - Avoid unpleasant color combinations.
    - Avoid fonts that are hard to read.
      > Pro tip: Fonts specified in CSS can be different in different browsers! Just
      > because `font-family: "Comic Sans"` looks sweet in Internet Explorer 5 (which you
      > better not be using) does not mean it will in Chrome or Firefox.
      >
      > You can use nifty fonts from places like
      > [Google Fonts](https://fonts.google.com); this will require
      > an (acceptable) change to the HTML file to load in the necessary
      > font files. Tools like [FontJoy](http://fontjoy.com) can be useful for
      > helping find font combinations that look good together.
    - Your page must look reasonable in all standard browsers (recent Chrome, Firefox,
      Safari, IE, Edge) and adapt the layout so that elements remain accessible and visible when the window is resized.
      > Pro tip: Making web pages that can resize across many different screen sizes
      > and devices is referred to as _responsive web design_. This is very important
      > since [more web views are happening
      > on phones now than on computers](https://www.theguardian.com/technology/2016/nov/02/mobile-web-browsing-desktop-smartphones-tablets).
      >
      > By using fancy styling and other tools to adjust how a web page looks,
      > developers can make a single page that will look good
      > on multiple screen sizes rather than constructing multiple
      > designs for each type of device. To see how your page would look on some phones
      > or tablets:
      >
      > Open your page in Chrome > right-click the page > click "inspect element" > click
      > the little phone symbol in the top-left corner. This will show roughly what your
      > site would look like on the chosen device. In Firefox, click on the Developer
      > button and choose Responsive Design mode. Or just resize your browser
      > window so that it's really narrow and see how it behaves.
  - Your CSS can leverage the fact that the page has the following
    **elements of interest**; see [the links in the README](./README.md) for support
    in understanding how to use CSS to alter the look of the page. You should
    particularly care about these features that were included to make the CSS more fun:
    - A **navigation bar.** Actually, this is just a list that is presented as a
      navigation bar in `style1.css' It must behave reasonably when you resize the window.
      In your style files, it may be horizontal or vertical, but should differ
      in some meaningful way between your two CSS files.
    - Four images of the faculty members **each of which has a div with a unique id**
    - Course requirements with a variety of parts that have class attribute values
    - Four faculty members in a list with their names and office locations in div classes
    - Multiple divs that have unique ids **but have the same class attribute value**
    - Multiple lists, both ordered and unordered **so that you may handle lists
      in different ways** and show some cool css features

## How do you know you are "done"? How will you be graded?

- Be sure to view the rubric for the assignment to see how the technical requirements
  from the list above will impact your grade
- Your CSS file must include **5 CSS rules with comments** that describe
  the impact of the rule and how it differs from our original style sheet.
  - a rule is a selector followed by settings for this selector
  - you may include more rules to make the page look really cool, but please comment
    on the 5 that you wish to have graded
- In addition to the minimum of 5 CSS rules with comments,
  your CSS you must use _and point out in comments somewhere_ in your edited style
  files each of the following: **grouping, nesting, a class, and an id**.
    > Pro tip: If you play with grouping and nesting after you've already written a bit of CSS, it'll be easier to understand why it's so cool. A good explanation of grouping and nesting can be found [here](http://lmgtfy.com/?q=grouping+and+nesting+css&l=1). Also, you can see some general info on CSS selectors [here](http://www.w3schools.com/cssref/css_selectors.asp).
