[Assemble]:                http://assemblecss.com
[Assemble Core]:           https://github.com/lukelarsen/assemble-core

# Assemble Tables
Assemble Tables is a component of the [Assemble] CSS Framework. It will give you a solid base for tables in your project. It has some default styles that can easily be overridden so you can add your own look.

## Requirements
Assemble Tables requires [Assemble Core].

## Installation
npm install assemble-tables --save-dev

## Usage
### Gulp
```js
var gulp = require('gulp');
var postcss = require('gulp-postcss');
var assembleCore = require('assemble-core');
var assembleTables = require('assemble-tables');

gulp.task('css', function () {
    var processors = [
        assembleCore({
            zLayerValues: {
                'modal': 9,
                'tip': 10
            }
        }),
        assembleTables
    ];
    return gulp.src('./src/*.css')
        .pipe(postcss(processors))
        .pipe(gulp.dest('./dest'));
});
```

## Options
Options are set with variables. These variables are already set with their default values so they will just work out of the box. If you wish to change them just define the variable you want to change before you load the _assemble-tables.css file. You may wish you see [Assemble Core] for more examples and directions for setting up a Assemble project.

### Design Variables

##### $table-padding
- Default: 0.5em;
- Type: Number
```css
$table-padding: 10px;
```

##### $table-stripe-background-color
- Default: #EEE;
- Type: Color
```css
$table-stripe-background-color: #000;
```

##### $table-row-hover-color
- Default: #DDD;
- Type: Color
```css
$table-row-hover-color: #333;
```

##### $table-border-color
- Default: #999;
- Type: Color
```css
$table-border-color: #999;
```

##### $table-border-size
- Default: 1px;
- Type: Color
```css
$table-border-size: 3px;
```

### Modifier Variables

##### $table--bordered
- Default: false;
- Type: Boolean
```css
$table--bordered: true;
```

##### $table--outer-bordered
- Default: false;
- Type: Boolean
```css
$table--outer-bordered: true;
```

##### $table--striped
- Default: false;
- Type: Boolean
```css
$table--striped: true;
```

##### $table--numerical
- Default: false;
- Type: Boolean
```css
$table--numerical: true;
```

##### $table--responsive
- Default: false;
- Type: Boolean
```css
$table--responsive: true;
```

##### $table--row-hover
- Default: false;
- Type: Boolean
```css
$table--row-hover: true;
```

##### Table Cell Widths
You can set all the widths you need for your modals in a .table-cell-widths class. The first value is the name and the second is what the max width should be. See the example below.

###### Example
```css
.table-cell-widths{
    15: 15px;
    half: 50%;
}
```
Will output:
```css
.t-15 {
    width: 15px
}

.t-half {
    width: 50%
}
```
