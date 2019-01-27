## About

This is a gulp and SASS set-up for creating and compiling the CSS for WordCamp Bristol 2019.

It works alongside the TwentySeventeen theme and is additional CSS, to overwrite and augment the CSS that is already there. 

This is NOT intended to be a child theme, as we can't include PHP files.


## Basic Features

- Sass source files and additional .scss files are nicely sorted and compartmentalised in the SASS folder.
- Outputs a single minified CSS file in CSS / theme.min.css
- This is stored at the following git repo, https://github.com/chozma/wordcamp-bristol-2019 and the CSS file mentioned above is used by the site. This is set in the WordPress backend by going to Appearance -> Customise -> Remote CSS


## Installation
There are several ways to install this, these aren't intended to be a step by step guide but to give you a prompt of the best way to get going.

- Download the repo from https://github.com/chozma/wordcamp-bristol-2019
- Open a terminal and navigate to the directory where you just put the repo
- Make sure you have installed Node.js and Browser-Sync (optional) on your computer globally
- Run: `$ npm install` - this will install all the gulp dependencies for you


### Running
To work with and compile your Sass files on the fly start:

- `$ gulp watch`

To be honest, this is probably all you need.

If you have a copy of TwentySeventeen on a local server, you can make use of Browser-Sync:

- First change the browser-sync options to reflect your environment in the file `/gulpconfig.json` in the beginning of the file:
```javascript
{
    "browserSyncOptions" : {
        "proxy": "localhost/theme_test/", // <----- CHANGE HERE
        "notify": false
    },
    ...
};
```
- then run: `$ gulp watch-bs`


## Footnotes

This gulp set-up has been taken from the very fantastic https://understrap.com/, but all PHP and JS files have been stripped out.
