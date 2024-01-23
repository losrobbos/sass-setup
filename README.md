# SASS setup

Install SASS:
`npm i -D sass`

Setup a folder "src" in your project

Place all your .scss files in that folder.

Place a script in package.json:

```
  "scripts": {
    "css": "sass --no-source-map src:dist"
  },

```

This script will translate the SASS files in the "src" folder to CSS files and places the generated the CSS files in the folder "dist".

Run the script: `npm run css`

Now we should see the generated CSS files in a new folder "dist".

Now you can use those generated CSS files in your HTML files.

Enjoyy sassy stuff!

## Source Maps 

By default SASS generates so called "source maps".
Those are files with the extension ".css.map". 
Those files allow to debug your SCSS in the browser, by linking 
the SCSS lines to the generated CSS lines. 
Meaning: When you are viewing the styles in the Dev Tools of the browser,
you will see from which line in the SCSS file that style comes from.

With the "--no-source-map" option we disable the generation of the 
source maps. If you want to keep them: Simply remove that that option
and use this script:

`"css": "sass src:dist"`


