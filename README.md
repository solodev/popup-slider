# popup-slider

We've written numerous times about ways you can preserve space within your design while simultaneously showcasing valuable content. Within the world of web design, some prefer to create content sliders while others prefer content overlays or popups. What is also feasible is to combine both techniques into a popup slider.

Popup sliders combine the best elements of each namesake. Information is only displayed upon user interaction and is overlayed on top of your body content, thus preserving crucial space within your design. Further, the slider allows you to include numerous sections that would otherwise have to be trimmed in traditional popup settings.

In this tutorial, [Solodev](https://www.solodev.com/) will show you how to add a popup slider to your website.

## Tutorials

For detailed instructions, view Solodev's [Adding a Popup Slider to your Website](https://www.solodev.com/blog/web-design/adding-a-popup-slider-to-your-website.stml) article.

## Demo

Try out a working example on [JSFiddle](https://jsfiddle.net/solodev/1f0jqr90/).

## HTML

The popup slider has the following HTML markup.

```
<section class="culture-section">
  <div class="container">
    <div class="col-md-8 col-md-offset-2">
      <h2>Slider Popup</h2>
      <h3>Easily Customized to Meet Your Needs</h3>
      <p>Create a unique slider embedded in a popup. Include valuable information while perserving space and optimizing your deisgn.</p>
    </div>
    <span class="btn btn-slider">Are You Ready?</span>
  </div>
</section>
                                              
<div class="sliderPop" style="display:none;">
  <div class="ct-sliderPop-container">
    <div class="ct-sliderPop ct-sliderPop-slide1 open">
      <div class="inner">
        <i class="fa fa-code" aria-hidden="true"></i>
        <h1>Code</h1>
        <div class="map-white-border"></div>
        <h2>Programming Not Required</h2>
        <p>WebCorpCo enables marketers to manage their entire stack in one place without needing the ability to program as all code is automatically written by webcorpco.</p>
        <a class="ct-newsletter-close ct-sliderPop-close" href="#">
        <img alt="close" src="https://www.solodev.com/assets/popup-slider/popup-close.png"></a>
      </div>
    </div>
    <div class="ct-sliderPop ct-sliderPop-slide2">
      <div class="inner">
        <i class="fa fa-paint-brush" aria-hidden="true"></i>
        <h1>Design</h1>
        <div class="map-white-border"></div>
        <h2>A Touch of Detail</h2>
        <p>With a team of award-winning designers behind every possible design and layout, you are sure to find success in our automated design process.</p>
        <a class="ct-newsletter-close ct-sliderPop-close" href="#">
        <img alt="close" src="https://www.solodev.com/assets/popup-slider/popup-close.png"></a>
      </div>
    </div>
    <div class="ct-sliderPop ct-sliderPop-slide3">
      <div class="inner">
        <i class="fa fa-users" aria-hidden="true"></i>
        <h1>Marketing</h1>
        <div class="map-white-border"></div>
        <h2>Marketing in Alignment</h2>
        <p>There is no 'one size fits all' approach to marketing. Every business is unique, customers are unique, and your marketing should be as well.</p>
        <a class="ct-newsletter-close ct-sliderPop-close" href="#">
        <img alt="close" src="https://www.solodev.com/assets/popup-slider/popup-close.png"></a>
      </div>
    </div>
    <div class="ct-sliderPop ct-sliderPop-slide1">
      <div class="inner">
        <i class="fa fa-life-ring" aria-hidden="true"></i>
        <h1>Support</h1>
        <div class="map-white-border"></div>
        <h2>Available 24/7</h2>
        <p>WebCorpCo offers state of the art support and training to enable users to make the most out of the platform and learn all of the functionality under the hood.</p>
        <a class="ct-newsletter-close ct-sliderPop-close" href="#">
        <img alt="close" src="https://www.solodev.com/assets/popup-slider/popup-close.png"></a>
      </div>
    </div>
    <div class="ct-sliderPop ct-sliderPop-slide2">
      <div class="inner">
        <i class="fa fa-university" aria-hidden="true"></i>
        <h1>Training</h1>
        <div class="map-white-border"></div>
        <h2>Take Control Yourself</h2>
        <p>Training can be "as requested" although there are regular webinars, code tutorials, and training courses offered for free on our website.</p>
        <a class="ct-newsletter-close ct-sliderPop-close" href="#">
        <img alt="close" src="https://www.solodev.com/assets/popup-slider/popup-close.png"></a>
      </div>
    </div>
  </div>
</div>
```
## CSS

All required CSS is in popup-slider.css

## JavaScript

This tutorial utilizes the JavaScript below.

```
$( document ).ready(function() {
	$('.btn-slider').on('click', function() {
	  $('.sliderPop').show();
	  $('.ct-sliderPop-container').addClass('open');
	  $('.sliderPop').addClass('flexslider');
	  $('.sliderPop .ct-sliderPop-container').addClass('slides');

	  $('.sliderPop').flexslider({
		selector: '.ct-sliderPop-container > .ct-sliderPop',
		slideshow: false,
		controlNav: false,
		controlsContainer: '.ct-sliderPop-container'
	  });
	});

	$('.ct-sliderPop-close').on('click', function() {
	  $('.sliderPop').hide();
	  $('.ct-sliderPop-container').removeClass('open');
	  $('.sliderPop').removeClass('flexslider');
	  $('.sliderPop .ct-sliderPop-container').removeClass('slides');
	});
});

```

## External Includes

This tutorial utilizes the following third party resources.

```
<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" rel="stylesheet">
<link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
<link href="https://cdnjs.cloudflare.com/ajax/libs/flexslider/2.5.0/flexslider.min.css" rel="stylesheet">
<link href="popup-slider.css" rel="stylesheet">
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/flexslider/2.5.0/jquery.flexslider-min.js"></script>
<script src="popup-slider.js"></script>
```
