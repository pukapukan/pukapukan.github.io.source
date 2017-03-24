<template>
  <div id="app">
    <img src="./assets/logo.png">
    <hello/>
  </div>
</template>

<script>
const screen = {
  phone: '480px',
  tablet: '1024px'
}

import Hello from '@/components/Hello'

export default {
  name: 'app',
  data: { screen },
  components: { Hello }
}
</script>

<style>
@import url(http://fonts.googleapis.com/css?family=Lato:300,400|Lobster|Roboto:100);
@custom-media --phone-screen (max-width: 480px);
@custom-media --tablet-screen (max-width: 1024px);

:root {
  --bg-body: #f9f9f9;

  --red: #ee4d4d;
  --blue: #2b2e48;
  --light-blue: rgb(10, 195, 255);
  --black: #2a2a2a;
  --light-gray: color(var(--black) lightness(75%));
  --dark-gray: color(var(--black) lightness(65%));
  --primary-color: var(--black);
  --secondary-color: var(--blue);

  /* Z-index */
  --header-z-index: 999;

  /* Typography */
  --base-font: Roboto, Helvetica, arial, tahoma, verdana;
  --title-font: Dosis, Helvetica, arial, tahoma, verdana;
  --description-font: Roboto, Helvetica, Arial, sans-serif;

  /* Timeline */
  --timeline-color: var(--light-gray);
  --timeline-highlight-color: var(--dark-gray);
}

#app {
  background: #fafafa;
  font-family: Lato, 'Helvetica Neue', Helvetica, 'Nanum Gothic', Arial, sans-serif;
  color: #333;
  &.mobile {
    height: 101vh !important;
  }
}

html, body {
  height: 100%;
  margin: 0;
}

.hidden {
  display: none;
  visibility: hidden;
  opacity: 0;
}

.content {
  padding: 100px;
}

@media only screen and (--phone-screen) {
  html {
    font-size: 14px;
  }
}

.clearfix {
  &:after, &:before {
    content: '';
    display: block;
    width: 100%;
    clear: both;
  }
}

.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
</style>
