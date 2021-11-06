* the "loading=lazy" attribute. You can use the `loading=lazy` attribute to defer the loading of the image until the user scrolls to them.
* Use the `<datalist>` element to create native HTML autocomplete.
        ```html
        <div class="wrapper">
            <h1>
                HTML search
            </h1>

            <input list="items">
            <datalist id="items">
                <option value="CreeCodeCamp">
                <option value="CreeCodeCamp">
                <option value="CreeCodeCamp">
                <option value="CreeCodeCamp">
                <option value="CreeCodeCamp">
                <option value="CreeCodeCamp">
            </datalist>
        </div>

        ```

* Email, call and SMS.

* Ordered lists `start` attribute.

Use the `start` attribute to change the starting point for your ordered lists.

```HTML
<ol start="11">
    <li>HTML</li>
    <li>CSS</li>
    <li>JS</li>
    <li>PYTHON</li>
</ol>


```

* Use `<input type="reset">` to create clear button for your forms.

```HTML
<form>
    .
    .
    .
    <div>
        <input type="reset" value="Reset">
        <input type="submit" value="Submit">
    </div>
</form>

```

* The `meter` element

You can use the `<meter>` element to display quantities. No JavaScript/CSS is needed.

```HTML
<label for="value1">low</lable>
<meter id="value1" min="0" max="100" low="30" high="75" optimun="80" value="25"></meter>

<label for="value2">low</lable>
<meter id="value2" min="0" max="100" low="30" high="75" optimun="80" value="50"></meter>

<label for="value3">low</lable>
<meter id="value3" min="0" max="100" low="30" high="75" optimun="80" value="80"></meter>

```

* `window.opener`

Pages opened with `target="_blank"` allow the new page to access the original’s `window.opener`. This can have security and performance implications. Include `rel="noopener"` or `rel="noreferrer"` to prevent this.

*  Base Element

If you want to open all links in the document in a new tab, you can use <base> element:

```HTML
<head>
    <base target="_blank">
</head>
.
.
.
<!-- Esto abre en otra paguina -->
<a href="wwww.google.com"> Google </a>

```

* Favicon cache busting

To refresh your website’s favicon you can force browsers to download a new version by adding ?v=2 to the filename.

This is especially helpful in production to make sure the users get the new version.

(https://favicon.io/)


* Native HTML sliders

You can use `<input type="range">` to create sliders.

*HTML Accordion
You can use the `details` element to create a native HTML accordion


* Use the `type="search"` for your search inputs and you get the "clear" button for free.

* `download` attribute

You can use the `download` attribute in your links to download the file instead of navigating to it.

* Performance tip

Use the `.webp` image format to make images smaller and boost the performance of your website.

* Use the `poster` attribute to specify an image to be shown while the video is downloading, or until the user hits the play button.

* Use the `spellcheck` attribute to define whether the element may be checked for spelling errors.
* Use the `<optgroup>` element to create a grouping of options within a `<select>` element.




