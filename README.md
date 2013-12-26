# Gulp compass

Compile Sass to CSS using Compass

## Requirements

`gulp-compass` requires the compass ruby gem in order to compile compass. This can easily be installed via Terminal.

```
$ gem update --system
$ gem install compass
```

Please refer the [user guide](http://compass-style.org/install/)

## Installation

```
$ npm install gulp-compass --save-dev
```

## Usage

load your compass ``config.rb`` file.

```javascript
var compass = require('gulp-compass');

gulp.task('compass', function() {
  gulp.src('./src/*.scss')
    .pipe(compass(
        config_file: './config.rb'
    ));
});
```

set your compass settings.

```javascript
var compass = require('gulp-compass');

gulp.task('compass', function() {
  gulp.src('./src/*.scss')
    .pipe(compass(
        css: 'app/assets/css',
        sass: 'app/assets/sass',
        image: 'app/assets/images'
    ));
});
```

## Configuration

### Configuration Options

#### style

**default:** nested

**description:** The output style for the compiled css.
One of: nested, expanded, compact, or compressed.

#### comments

**default:** true

**description:** Show line comments or not.

#### relative

**default:** true

**description:** Are assets relative.

#### css

**default:** css

**description:** The folder inside the project to output css into.

#### sass

**default:** sass

**description:** The folder inside the project to find sass in.

#### project

**default:** your project base

**description:** The location where all your assets are store.