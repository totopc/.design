---
title: Colors
layout: app
toc: false
---

<script>
function getColor() {
  /* Get the text field */
  var copyText = document.getElementById("pillColor");

  /* Select the text field */
  copyText.select();
  copyText.setSelectionRange(0, 99999); /* For mobile devices */

   /* Copy the text inside the text field */
  navigator.clipboard.writeText(copyText.value);

}
</script>

<div class="container-fluid p-0">
<p>Color distinguishes our brand and helps us create consistent experiences across products. </p>
<h3 class="m-bottom-2 t-bold">Primary Colors</h3>
<p>Colors that represent our brand, used as primary color and accents. Our primary palette is comprised of purple, white, and blue to bring boldness to our brand and is used in logical ways throughout product and marketing to guide the eye and highlight the important bits.</p>

{% comment %} 
 Start of primary color pills
{% endcomment %}

<div class="row ">
{% for colors in site.data.colors %}
{% for color in colors.primary %}
<span onClick="getColor()" type="button" class=" col-12 col-md-4 m-bottom-4  ">
<div class="row m-0 {{color.bg}} t-c-w100 p-0 m-0 t-left p-left-4 rounded-pill no-scroll shadow-default colorpill">
<a class='copy col-8 {% if color.text-color=="white"%} t-c-w100{% else %}t-black{% endif %} m-top-2'>
<b class="t-bold">{{color.name}}</b><br/>
{{color.hex}}</a>
<span class="col-4 col-md-4 p-left-4 p-left-3__m p-3 bg-c-b300">
<svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 viewBox="0 0 22 24" style="enable-background:new 0 0 22 24;" xml:space="preserve">
<style type="text/css">
	.st0{fill:#FFFFFF;}
</style>
<g>
	<path class="st0" d="M20.8,3.1l-2.4-2.4C18,0.2,17.4,0,16.8,0H8.8C7.5,0,6.5,1,6.5,2.3v2.3H2.8c-1.2,0-2.3,1-2.3,2.3v15
		c0,1.2,1,2.3,2.3,2.3h10.5c1.2,0,2.3-1,2.3-2.3v-2.3h3.8c1.2,0,2.3-1,2.3-2.3V4.7C21.5,4.1,21.3,3.5,20.8,3.1z M17,1.5
		c0.1,0,0.3,0.1,0.3,0.2l2.4,2.4c0.1,0.1,0.2,0.2,0.2,0.3h-3V1.5z M14,21.8c0,0.4-0.3,0.8-0.8,0.8H2.8c-0.4,0-0.8-0.3-0.8-0.8v-15
		C2,6.3,2.3,6,2.8,6h3.8v11.3c0,1.2,1,2.3,2.3,2.3H14V21.8z M20,17.3c0,0.4-0.3,0.8-0.8,0.8H8.8C8.3,18,8,17.7,8,17.3v-15
		c0-0.4,0.3-0.8,0.8-0.8h6.8v3.4C15.5,5.5,16,6,16.6,6H20V17.3z"/>
</g>
</svg>
</span>
</div>
<input class="l-none" type="text" value="#000000"  id="pillColor">
</span>
{% endfor %}
{% endfor %}
</div>
{% comment %} 
 End of primary colour pils
{% endcomment %}


</div>

<h3 class ="t-bold t-right m-0">  Next: <a href="">Color →</a></h3>
