# visionary-anderton

Chrome extension, part of the [Visionary project](https://github.com/visionary-be/visionary).   


## License : GNU General Public License v3.0
[Read the license](./COPYING).


## file organisation

`/src` folder = "source" folder  
`/build` folder = "build" folder. You shouldn't need to go inside: when gulp is running, it compiles all files from the `src` folder into the `build` folder.  
`/distr` folder = "distribution" folder. When a release is ready, it is zipped into this folder, ready for submission or testing in the browser.  

## setup your dev environment

To Install Gulp, in your Terminal type:

1. `npm install --global gulp-cli`
2. `npm install gulp gulp-minify-css gulp-uglify gulp-clean gulp-cleanhtml jshint gulp-jshint gulp-strip-debug gulp-zip gulp-sass gulp-prompt gulp-replace gulp-bump browser-sync --save-dev`
3. `npm update` to install remaining packages.

## starting your work...

`gulp` : This tasks cleans up the build folder then compiles js/css files, then serves the `build/`folder via URL: [http://localhost:2017](http://localhost:2017). It watches any changes you make on your js and scss folders, and live reload (via browserSync) your browser to reflect thoses changes. It is perfect for quick development.  In the background, it compiles any changes to the `./build` folder.

## publishing the extension on the Play Store

`gulp release` : this task creates the zip file in the `dist/`folder, that you can submit to the Play Store.


