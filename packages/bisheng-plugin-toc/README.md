# bisheng-plugin-toc

[![](https://img.shields.io/travis/benjycui/bisheng-plugin-toc.svg?style=flat-square)](https://travis-ci.org/benjycui/bisheng-plugin-toc)
[![npm package](https://img.shields.io/npm/v/bisheng-plugin-toc.svg?style=flat-square)](https://www.npmjs.org/package/bisheng-plugin-toc)
[![NPM downloads](http://img.shields.io/npm/dm/bisheng-plugin-toc.svg?style=flat-square)](https://npmjs.org/package/bisheng-plugin-toc)
[![Dependency Status](https://david-dm.org/benjycui/bisheng-plugin-toc.svg?style=flat-square)](https://david-dm.org/benjycui/bisheng-plugin-toc)

Generate a Table of Contents (TOC) for Markdown files in [`bisheng`](https://github.com/benjycui/bisheng).

## Usage

Install:

```bash
npm i --save bisheng-plugin-toc
```

Add 'bisheng-plugin-toc to `bisehng.config.js`'s plugins.

```js
module.exports = {
  plugins: ['bisheng-plugin-toc?maxDepth=2'],
};
```

In template:

```jsx
<ul>
  {
    pageData.toc.map((heading, index) => {
      const text = JsonML.getChildren(heading)[0];
      return <li key={index}><a href={`#${text}`}>{text}</a></li>
    })
  }
</ul>
```

## License

MIT