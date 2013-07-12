Linear gradient mixin for LESS
==============

A really, really comprehensive mixin for generating linear gradients in [LESS](http://lesscss.org/).

For a simple, two colour linear gradient the mixin can be used as so:

	.linear-gradient(top,  #eee, #aaa); // arguments go [direction, first colour, second colour]

You can also pass in an angle in for the direction

	.linear-gradient(50deg,  #eee, #aaa);

If supported, your gradient will observe the angle, for unsupported browsers (cough IE), the mixin determins the closest top, bottom, left, right value to use instead.

rgba values? No problem, even IE gets support as it's converted to aRGB

	.linear-gradient(left, rgba(0,0,0,0.5), #aaa);

For multi-stop gradients call the `.linear-gradient-multi` version of the gradient with valid CSS values (escaped so LESS doesn't freak out), followed by the `.linear-gradient-ie` version with your single stop fallback.

	.linear-gradient-multi(~'top, #eee 0%, #aaa 50%, #eee 100%');
	.linear-gradient-ie(top, #eee, #aaa);
