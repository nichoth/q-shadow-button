# quiet shadow button

Sass mixin for button made with css `text-shadow`.

## install

    $ bower install q-shadow-button

## example

[Demo](https://34b5031f563032f046bb058392d8b33863f946d1.htmlb.in)

Markup:
```html
<body>
  <h1 class="my-button">ham party</h1>

  <script>
    var elmt = document.querySelector('h1');
    elmt.addEventListener('click', function(ev) {
      ev.target.classList.toggle('my-button-depressed');
    });
  </script>
</body>
```

Sass:
```sass
@import "bower_components/q-shadow-button/q-shadow-button";

// make it pretty
.my-button {
  letter-spacing: 0.1em;
  font-family: 'Avenir Next', sans-serif;
  font-weight: 900;
  text-transform: uppercase;
  font-size: 5em;
  transition: all 0.12s ease;
  cursor: pointer;
}

// use this component
.my-button {
  @include q-shadow-button;
}

// compiles to:
// .my-button {
//   position: relative;
//   top: 0px;
//   left: 0px;
//   text-shadow: rgba(0, 0, 0, 0.4) 7px 7px 0px; }
// .my-button.my-button-depressed {
//   top: 7px;
//   left: 7px;
//   text-shadow: rgba(0, 0, 0, 0.4) 0px 0px 0px; }
```

Configure shadow color and offset:
```sass
.my-button {
  @include q-shadow-button(5px, pink)
}
```
