# Minimalist ToC

A minimalist table of contents in Javascript.

## Presentation

This script `minimalist-toc.js` allow you to print a table of contents in your page. To use it, just initialize it by declaring:

- an id corresponding to the content of the page,
- an id corresponding to the location of the table of contents,
- eventually some options.

By default, the table of contents:

- display a title (`Table of contents`) inside `h2` tag,
- use an ordered list (`ol`),
- search all heading levels except `h1` (so `h2`, `h3`, `h4`, `h5`, `h6`).

This settings can be overwritten by using the options.

If your titles do not have an id, the script generates one, otherwise it uses the existing id.

Finally, as the name suggests, it is a minimalist table of contents. Only the script generating the ToC is provided. There is no defined style. So you can define your own styles without having to overwrite existing ones.

## Example

```javascript
const Minimalist_TOC = new TableOfContent();

Minimalist_TOC.init("entry-content", "entry-toc", {
  headings: ["h2", "h3"],
  title: "My custom title",
  titleTag: "p",
  listType: "ul",
});
```

Here I redefine all the options, but you can change just one or even zero if you want.

## Acknowledgments

The `slugify` function was not written by me. So, thanks to the various contributors of [this gist](https://gist.github.com/codeguy/6684588). I only made some changes to suit my needs.

## License

This project is open source and available under the [MIT License](https://github.com/ArmandPhilippot/minimalist-toc/blob/master/LICENSE).
