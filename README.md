# SingleHTML
Merge JS, CSS, HTML and Images into a single HTML using Python

## Scenario

Let's say you have a web application with one HTML, 2 CSS, 2 JS and 2 PNG files.  
Because this is a report you want to send to customers, 
you want to share your web page as a **single standalone HTML file**.

True, you can develop it as a single big HTML file from the beginning, but that wouldn't be so nice, right?  
It's mush better to develop it with many files and only distribute it as a single file.

## How to use

For this directory tree:

```
root-folder
├── index.html
├── build_dist.py
├── js
│   └── somescript.js
├── css
│   ├── styles1.css
│   └── styles2.css
├── images
│   └── img1.png
└── dist
```
> The HTML file must be named `index.html` and 'dist' folder must be there. everything else can change

From `root-folder` run:

```
python build_dist.py
```

And a standalone `oneindex.html` file will be created in the dist folder.

This file contains all the js and css from the files specified with `link` and `script` tags in index.html. It also contains all images specified with `img` tags.

To store the images in the HTML file, they are converted to base64 text.

## About this project

The idea was born as a [Stack Overflow answer](https://stackoverflow.com/a/61586957/10727283) in 2020, and later brought here
