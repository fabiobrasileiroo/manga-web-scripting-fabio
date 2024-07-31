# Manga Web Scripting

A package to scrape images of manga chapters from [mangaonline.biz](https://mangaonline.biz).

## Installation

To install the package, run:

```bash
npm install manga-web-scripting
```

### Usage with ES Modules
Example configuration using "type": "module":
```js
{
  "name": "my-project",
  "version": "1.0.0",
  "main": "server.js",
  "type": "module",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node server.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "description": "",
  "dependencies": {
    "manga-web-scripting": "^1.0.0"
  }
}

```

### How to Use?
``` js
import scrapeImages from 'manga-web-scripting';

(async () => {
  try {
    const anime = 'naruto';
    const chapter = 1;
    const images = await scrapeImages(anime, chapter);
    console.log('Scraped images:', images);
  } catch (error) {
    console.error('Error:', error.message);
  }
})();
```