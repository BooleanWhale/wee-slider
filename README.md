# Wee Slider

Wee Slider is a lightweight, performant class-based web component that allows you to create sliders with ease. It focuses on performance and small file sizes, with the minified JavaScript file (wee-slider.min.js) being less than 2kb in size.

See the slider in action: <a href="https://codepen.io/ash_s_west/full/bGmOEyP" target="_blank">Wee Slider on CodePen</a>

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Dev notes](#dev-notes)

## Features

- Lightweight and performant
- Optional 'looping' functionality to progress position to first or last slide
- Configurable alignment of slides (start, center, or end)
- Show/hide navigation buttons on hover
- Customizable CSS variables for easy style customization
- Naming conventions ensure no conflicts with existing CSS
- No redundancy, maximize performance by reducing iterations and DOM calls to a minimum.

For information on additional features, refer to [Dev notes](#dev-notes).

## Installation

You can include the Wee Slider component in your project by downloading the minified JavaScript file ```wee-slider.min.js``` and CSS file ```wee-slider.css```, and linking to them in the ```<head>``` of your HTML.

```html
<link rel="stylesheet" href="wee-slider.css">
<script src="path/to/wee-slider.min.js"></script>
```

## Usage

To use Wee Slider, you need to include the necessary HTML structure and attributes in your markup.

```
<wee-slider data-loop="true" data-align="center" data-buttons-on-hover="true">
  <div class="wee-slider">
    <ul class="wee-slider__slides">
      <!-- Add your slides here -->
      <li class="wee-slider__slide"></li>
    </ul>
    <div class="wee-slider__buttons">
      <button class="wee-slider__button-prev">Prev</button>
      <button class="wee-slider__button-next">Next</button>
    </div>
  </div>
  <!-- Navigation dots element is optional -->
  <ul class="wee-slider__navdots">
    <!-- Add your navigation dots here -->
    <li class="wee-slider__navdot"></li>
  </ul>
</wee-slider>
```

## Configuration

#### Data attrubutes

Wee Slider provides configuration options through data-attributes on the <wee-slider> element.

- data-loop: Enables looping through slides (default: true)
- data-align: Sets the alignment of slides (start, center, or end) (default: center)
- data-buttons-on-hover: Shows the navigation buttons on hover (true or false) (default: true)
    
```
<wee-slider 
  data-loop="true" 
  data-align="center"
  data-buttons-on-hover="true">
  <!-- Slider content -->
</wee-slider>
```

#### CSS Variables

Wee Slider uses CSS variables to control its appearance. You can override these variables in your own CSS or edit the CSS file to customize the slider.

```
wee-slider {
  /* Edit these variables for easy customisability */
  --wee-visible-slides-mobile: 1.5;
  --wee-visible-slides-desktop: 3.5;
  --wee-slide-gap: 10px;
  --wee-navdot-color: rgb(0,0,0);
  /* Rest of code... */
}
```
For multiple sliders with different appearances, add a class to specific `<wee-slider>` elemement and overwrite the above variable under that class.

## Dev Notes

Wee Slider prioritizes lightweightness and performance to address the common issues associated with sliders, such as performance degradation and large file sizes. In order to achieve this goal, some of the less essential features commonly found in popular sliders have been omitted. While features like true looping (instead of position jumps) and click/drag functionality on desktop are under consideration, their inclusion will be evaluated based on their impact on performance.

The primary objectives of Wee Slider are to deliver a seamless and efficient slider experience while maintaining a minimal file size. By focusing on core functionalities and optimizing performance, Wee Slider aims to provide a reliable and efficient solution for creating sliders in web projects.

## License

Wee Slider is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

---

That's it! You now have the basic information on how to use and configure Wee Slider. Feel free to contribute to the project, report any issues, or suggest improvements. Your feedback is greatly appreciated!
