# egerep-svg-metro


## Dependencies
```
 jquery.panzoom ^3.2.2
```

## Dev dependencies
```
 underscore ^1.8.3
 jquery.panzoom ^3.2.2
```


## Usage

install package
```
bower install --save egerep-svg-metro
```

concat with vendor files
```js
elixir(mix => {
    mix.scripts(jsFromBower([
        'egerep-svg-metro/scripts/svg'
    ]);
});
```
add css/scss to styles
```scss
@import egerep-svg-metro/styles/svg-metro.scss
```

add module as depency to your app
```coffee
angular.module 'some-module', ['svgmap', ...]
```

move svg file to img/svg folder under webroot
```html
cp bower_packages/egerep-svg-metro/views/map.svg public/img/svg/map.svg
```
insert directive to page
```html
<svg-map id='some-id' selected='selected_stations'></svg-map>
```

## Options

`"scalable"` - adds scaling feature
```html
<svg-map id="some-id" selected="[1, 2, 3]" scalable></svg-map> 
```

`"selectable"` -  add selecting stations feature, quick selectes supported

```html
<svg-map id="some-id" selected="[1, 2, 3]" selectable></svg-map> 
```