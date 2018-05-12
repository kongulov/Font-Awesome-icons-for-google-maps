Font Awesome icons for google maps markers
=========

This code for use Font Awesome with Google Maps API and Google Places API using SVG markers and icon labels

## Quick start

There are 2 ways to quickly download and use the code

- [Download the latest release](https://github.com/Ramiz4ik/Font-Awesome-icons-for-google-maps/archive/master.zip).
- Clone the repo: `git clone https://github.com/Ramiz4ik/Font-Awesome-icons-for-google-maps.git`.

## Usage
This code extends the [Google Maps Marker](https://developers.google.com/maps/documentation/javascript/reference#Marker) Object to enable either an image or SVG marker to be used with the icon placed on top as a label.

### Include

First, install the Font Awesome CDN and Google maps Api and map-font-icons.js
```html
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.0.13/css/all.css">
<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY"></script>
<script src="map-font-icons.js"></script>
```

### Classes

All classes you can find on the site [Font Awesome](https://fontawesome.com/icons?d=gallery)

```html
<i class="fas fa-heart"></i>
```
### Styling the Icon

Explict styles to icons being used on a Google Map should be applied with `.map-icon-label i` CSS selector.

```css
.map-icon-label i {
    font-size: 24px;
    color: #FFFFFF;
    line-height: 55px;
    text-align: center;
    white-space: nowrap;
}
```

### Creating a Marker

Markers are created just like a normal Google Maps Marker, however, the class is extended for the `map_icon_label` property to add in markup for marker labels.


```js
var marker = new Marker({
    map: map,
    position: new google.maps.LatLng(40.394508, 49.7148762),
    icon: {
        path: MAP_PIN,
        fillColor: '#9C27B0',
        fillOpacity: 1,
        strokeColor: '',
        strokeWeight: 0
    },
    map_icon_label: '<i class="fas fa-home"></i>'
});
```
