#vue-animate
*Cross-browser CSS3 animation library*

[![Version](https://img.shields.io/npm/v/vue-animate.svg?style=flat-square)](https://www.npmjs.com/package/vue-animate)
[![License](https://img.shields.io/npm/l/vue-animate.svg?style=flat-square)](LICENSE)

A [Vue.js](http://vuejs.org/ "Vue.js") port of [Animate.css](https://github.com/daneden/animate.css "Animate.css"). For use with Vue's built-in transitions.

##Installation
####HTML
Include the stylesheet:

  ```html
  <head>
    <link rel="stylesheet" href="vue-animate.min.css">
  </head>
  ```
####npm
  If you're on webpack and using the [css-loader](https://github.com/webpack/css-loader "css loader"), you can use something like this:
  ```shell
  npm install --save vue-animate
  ```
  ```js
  require('vue-animate/dist/vue-animate.min.css')
  ```
####Less
  ```less
  @import "<PATH_TO_SOURCE>/src/vue-animate.less";
  ```

####Building
  ```shell
  git clone https://github.com/haydenbbickerton/vue-animate.git
  cd vue-animate
  npm install
  npm run build #Compiled .css files go to the dist folder
  ```

##Usage

  Use [Vue.js transitions](http://vuejs.org/guide/transitions.html "Vue.js Transitions") as you normally would, but for the transition name you will use one of [Animate.css animations](https://github.com/daneden/animate.css#basic-usage "animations") **removing** the ***In/Out*** from the name.

  For example, if I want to use *fadeInLeft* and *fadeOutLeft* on my element, I'll write:
  ```html
  <div v-if="show" transition="fadeLeft">hello</div>
  ```
  enter/leave is already written in the stylesheet, so just remove *In/Out* from the name and you're golden.

####Custom Transition Classes
  As of 0.0.3, Animate.css's original classnames are supported on enter/leave transitions. So if you're going to use [Custom Transition Classes](http://vuejs.org/guide/transitions.html#Custom-Transition-Classes "Custom Transition Classes"), you can either add *-enter/-leave* to the classes:

  ```js
  Vue.transition('bounce', {
    enterClass: 'bounceLeft-enter',
    leaveClass: 'bounceRight-leave'
  })
  ```
  Or use the regular *In/Out* syntax:

  ```js
  Vue.transition('bounce', {
    enterClass: 'bounceInLeft',
    leaveClass: 'bounceOutRight'
  })
  ```

####Supported Animations
  Not all [Animate.css animations](https://github.com/daneden/animate.css#basic-usage "animations") are supported at the moment. Here is a list of what's in vue-animate (aka - *what you can put in the transition="x"* attribute) as of right now:

#####Bounce
  * `bounce`
  * `bounceDown`
  * `bounceLeft`
  * `bounceRight`
  * `bounceUp`

#####Fade
  * `fade`
  * `fadeDown`
  * `fadeDownBig`
  * `fadeLeft`
  * `fadeLeftBig`
  * `fadeRight`
  * `fadeRightBig`
  * `fadeUp`
  * `fadeUpBig`

#####Rotate
  * `rotate`
  * `rotateDownLeft`
  * `rotateDownRight`
  * `rotateUpLeft`
  * `rotateUpRight`

#####Slide
  * `slideDown`
  * `slideLeft`
  * `slideRight`
  * `slideUp`

#####Zoom
  * `zoom`
  * `zoomDown`
  * `zoomLeft`
  * `zoomRight`
  * `zoomUp`

# License

[MIT](http://opensource.org/licenses/MIT)

## Contributing

Pull requests are welcome :)
