A reproduction case of <noscript> running in the visual editor when it shouldn't.

The component `global/hero` is used on the homepage, and has this noscript tag as part of its contents:

```html
...

<noscript>
  <style>
    body {
      background-color: red;
    }

    .hero-test {
      background-color: purple !important;
      color: white;
    }
  </style>
</noscript>

<section class="hero-test relative isolate pt-24 bg-primary/5 overflow-hidden">

....
```

The noscript applies the styles in the visual editor, but not the live site preview. On disabling JS in the browser, the live site preview correctly applies the noscript styles.
