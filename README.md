# O'Reilly Presentation Theme

This theme is intended to work alongside the presentation template in Atlas. In order for these styles to be applied correctly, new projects must begin with all the base files included in https://github.com/oreillymedia/presentation-template. When not creating a new presentation within Atlas, begin by downloading these following files and adding them to your project repository: https://github.com/oreillymedia/presentation-template/archive/master.zip.

Create each slide as a separate html file, with a parent container of: 
    <section data-type="chapter">

When using the Atlas editor, new files will automatically be created with this parent container.

The first (title) slide in your deck should have a parent container of:
    <section data-type="titlepage">

To change the background color to black, add the following CSS to your project's theme:

html.css:

    html {
      background-color: black;
    }

    section[data-type="chapter"] *, section[data-type="titlepage"] * {
      color: #fff;
    }

    section[data-type="chapter"] h1, 
    section[data-type="chapter"] strong {
      color: #cc0000;
    }

    section[data-type="titlepage"] h1 {
      text-shadow: -1px -1px 5px #666;
    }

pdf.css:

    @page {
      background-color: black;
    }

    section[data-type="chapter"] *, section[data-type="titlepage"] * {
      color: #fff;
    }

    section[data-type="chapter"] h1, 
    section[data-type="chapter"] strong {
      color: #cc0000;
    }

To horizontally center the contents of a block element (an entire slide, items in a list, etc.), add a class of hcenter to the parent element. For example the html might look like this:

    <section data-type="chapter">
    <h1>A slide with a list.</h1>
    <ul class="hcenter">
      <li>A list item.</li>
      <li>A second list item.</li>
    </ul>
    </section>

To vertically center the contents of a slide, add a class of "vcenter" to the parent element. For example, the html might look like this:

    <section data-type="chapter" class="vcenter">
    <h1>A slide with just a heading.</h1>
    </section>

In both PDF and HTML output, the slide content will be scaled to fit in a single slide. _Basic Presentation Tip_: Adding a lot of text to a single slide is not going to be very legible for your audience. Plan accordingly.

The HTML slideshow is powered by deck.js. Use left and right arrow keys to navigate between slides. When building the HTML output, make sure to go to the build settings and combine the HTML into a single file.