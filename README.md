[Assemble]:                http://assemblecss.com
[Assemble Base]:           https://github.com/lukelarsen/assemble-base
[Stupid Table]:            https://github.com/joequery/Stupid-Table-Plugin/tree/dd20279ae24f29ea07cba8c035be685b6e9dcf50

# Assemble Tables
Assemble Tables is a component of the [Assemble] CSS Framework. It will give you a solid base for tables in your project. It has some default styles that can easily be overridden so you can add your own look.

## Requirements
Assemble Tables requires [Assemble Base].

## Installation
npm install assemble-tables --save-dev

## Usage
### Gulp
```js
var gulp = require('gulp');
var postcss = require('gulp-postcss');
var assembleBase = require('assemble-base');
var assembleTables = require('assemble-tables');

gulp.task('css', function () {
    var processors = [
        assembleBase,
        assembleTables
    ];
    return gulp.src('./src/*.css')
        .pipe(postcss(processors))
        .pipe(gulp.dest('./dest'));
});
```
Then import the _assemble-tables.css file from your css file.
```css
@import '../node_modules/assemble-base/base';

/*
Override variables here before the Assemble Components are loaded.
*/

@import '../node_modules/assemble-tables/assemble-tables';
```

### HTML
```html
<table class="table">
    <colgroup>
        <col>
        <col>
        <col>
    </colgroup>
    <thead>
        <tr>
            <th>Lorem</th>
            <th>Ipsum</th>
            <th>Sit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
    </tbody>
</table>
```

## Options
Options are set with variables. These variables are already set with their default values so they will just work out of the box. If you wish to change them just define the variable you want to change before you load the _assemble-tables.css file. You may wish you see [Assemble Base] for more examples and directions for setting up a Assemble project.

### Design Variables

##### $table-padding
- Set table padding.
- Default: 0.5em;
- Type: Number
```css
$table-padding: 10px;
```

##### $table-stripe-background-color
- Set table stripe background color.
- Default: #EEE;
- Type: Color
```css
$table-stripe-background-color: #000;
```

##### $table-row-hover-color
- Set table row hover color.
- Default: #DDD;
- Type: Color
```css
$table-row-hover-color: #333;
```

##### $table-border-color
- Set table border color.
- Default: #999;
- Type: Color
```css
$table-border-color: #999;
```

##### $table-border-size
- Set table border size.
- Default: 1px;
- Type: Color
```css
$table-border-size: 3px;
```

##### $table-sort-none-image
- Set table sorting none image.
- Default: url('../images/table-sort-none.svg');
- Type: String
```css
$table-sort-none-image: svg-load('table-sort-none.svg');
```

##### $table-sort-desc-image
- Set table sorting desc image.
- Default: url('../images/table-sort-desc.svg');
- Type: String
```css
$table-sort-none-image: svg-load('table-sort-desc.svg');
```

##### $table-sort-none-asc
- Set table sorting asc image.
- Default: url('../images/table-sort-asc.svg');
- Type: String
```css
$table-sort-none-image: svg-load('table-sort-asc.svg');
```

##### $table-sort-right-pos
- Set how far from the right you want the sort icon/image to be.
- Default: 12px;
- Type: Number
```css
$table-sort-right-pos: 14px;
```

##### $table-sort-top-pos
- Set how far from the top you want the sort icon/image to be.
- Default: 12px;
- Type: Number
```css
$table-sort-top-pos: 14px;
```

##### $table-sort-desc-bg-color
- Set what color you'd like the active desc table header to be.
- Default: black;
- Type: Color
```css
$table-sort-desc-bg-color: gray;
```

##### $table-sort-asc-bg-color
- Set what color you'd like the active asc table header to be.
- Default: black;
- Type: Color
```css
$table-sort-asc-bg-color: gray;
```

### Modifier Variables

##### $table--bordered
- Turn on/off table borders for your application. If set to true you can use the class .table--bordered.
- Default: false;
- Type: Boolean
```css
$table--bordered: true;
```
Usage
```html
<table class="table  table--bordered">
    <colgroup>
        <col>
        <col>
        <col>
    </colgroup>
    <thead>
        <tr>
            <th>Lorem</th>
            <th>Ipsum</th>
            <th>Sit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
    </tbody>
</table>
```

##### $table--outer-bordered
- Turn on/off tables with outside borders for your application. If set to true you can use the class .table--outer-bordered.
- Default: false;
- Type: Boolean
```css
$table--outer-bordered: true;
```
Usage
```html
<table class="table  table--outer-bordered">
    <colgroup>
        <col>
        <col>
        <col>
    </colgroup>
    <thead>
        <tr>
            <th>Lorem</th>
            <th>Ipsum</th>
            <th>Sit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
    </tbody>
</table>
```

##### $table--striped
- Turn on/off striped tables for your application. If set to true you can use the class .table--striped.
- Default: false;
- Type: Boolean
```css
$table--striped: true;
```
Usage
```html
<table class="table  table--bordered  table--striped">
    <colgroup>
        <col>
        <col>
        <col>
    </colgroup>
    <thead>
        <tr>
            <th>Lorem</th>
            <th>Ipsum</th>
            <th>Sit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
    </tbody>
</table>
```

##### $table--numerical
- Turn on/off numeric tables for your application. If set to true you can use the class .table--numerical.
- Default: false;
- Type: Boolean
```css
$table--numerical: true;
```
Usage
```html
<table class="table">
    <colgroup>
        <col>
        <col>
        <col>
        <col>
    </colgroup>
    <thead>
        <tr>
            <th>Lorem</th>
            <th>Ipsum</th>
            <th class="table--numerical">Dolor</th>
            <th>Sit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td class="table--numerical">3.788</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td class="table--numerical">32.210</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td class="table--numerical">47.797</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td class="table--numerical">9.640</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td class="table--numerical">12.117</td>
            <td>Lorem</td>
        </tr>
    </tbody>
</table>
```

##### $table--responsive
- Turn on/off responsive tables for your application. If set to true you can use the class .table--responsive.
- Default: false;
- Type: Boolean
```css
$table--responsive: true;
```
Usage
```html
<table class="table  table--bordered  table--responsive">
    <colgroup>
       <col>
       <col>
       <col>
       <col>
    </colgroup>
    <thead>
        <tr>
            <th>Lorem</th>
            <th>Ipsum</th>
            <th>Dolor</th>
            <th>Sit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">3.788</td>
            <td data-th="Sit">Lorem</td>
        </tr>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">32.210</td>
            <td data-th="Sit">Lorem</td>
        </tr>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">47.797</td>
            <td data-th="Sit">Lorem</td>
        </tr>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">9.640</td>
            <td data-th="Sit">Lorem</td>
        </tr>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">12.117</td>
            <td data-th="Sit">Lorem</td>
        </tr>
    </tbody>
</table>
```

##### $table--row-hover
- Turn on/off tables with row hovers for your application. If set to true you can use the class .table--row-hover.
- Default: false;
- Type: Boolean
```css
$table--row-hover: true;
```
Usage
```html
<table class="table  table--bordered  table--row-hover">
    <colgroup>
       <col>
       <col>
       <col>
       <col>
    </colgroup>
    <thead>
        <tr>
            <th>Lorem</th>
            <th>Ipsum</th>
            <th>Dolor</th>
            <th>Sit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">3.788</td>
            <td data-th="Sit">Lorem</td>
        </tr>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">32.210</td>
            <td data-th="Sit">Lorem</td>
        </tr>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">47.797</td>
            <td data-th="Sit">Lorem</td>
        </tr>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">9.640</td>
            <td data-th="Sit">Lorem</td>
        </tr>
        <tr>
            <td data-th="Lorem">Sit</td>
            <td data-th="Ipsum">Dolor</td>
            <td data-th="Dolor">12.117</td>
            <td data-th="Sit">Lorem</td>
        </tr>
    </tbody>
</table>
```

##### Table Sorting
You can add some UI to the table headers if you are going to enable sorting of the tables. Note that Assemble doesn't come with any javascript to do the actual sorting. You can look at [Stupid Table] for a jQuery solution.
- Turn on/off tables that can sort their contents
- Default: false;
- Type: Boolean
```css
$table--sort: true;
```

Usage
```html
<table class="table  table--sort">
    <colgroup>
        <col class="t-15">
        <col>
        <col>
    </colgroup>
    <thead>
        <tr>
            <th>Lorem</th>
            <th class="table--sort__desc">Ipsum</th>
            <th>Sit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
    </tbody>
</table>
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
Usage
```html
<table class="table  table--bordered  table--striped">
    <colgroup>
        <col class="t-15">
        <col>
        <col>
    </colgroup>
    <thead>
        <tr>
            <th>Lorem</th>
            <th>Ipsum</th>
            <th>Sit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
        <tr>
            <td>Sit</td>
            <td>Dolor</td>
            <td>Lorem</td>
        </tr>
    </tbody>
</table>
```
