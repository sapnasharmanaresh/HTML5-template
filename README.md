HTML5-template
==============

Standard HTML5-based template for HTML24.

This is the standard HTML5-based template for HTML24, which is to be used for every project. 
To use this, simply make a clone of this GitHub Repository to the wanted folder directory. 


Special Fonts
-------------

If you need to use a special font for your project, then use the css-way with font-face. To generate the correct css-syntax and get the correct file formats for the font-face, use a font-face generator. Use the [FontSquirrel generator](fontsquirrel.com/fontface/generator) for this. If fontsquirrel doesn't work, then use either [Code and More](http://fontface.codeandmore.com/index.php) or [Font2Web](http://www.font2web.com/).


CSS3
----

Rounded corners, box shadows and other CSS3 stylings should always be discussed with the project manager for each project, before choosing a solution.


Standard coding in the CSS-file
-------------------------------

The styling in the CSS-files should be indented like in the HTML-file. 


Inline styling
--------------

Do whatever you can to avoid using inline styling as this is not semantic code. Even if you use jQuery.

If you need to add styling with jQuery add a class to the element instead of adding inline styling with jQuery.css(). 


Hover Image
-----------

When you create a button or another project, that uses a background image and also has a hover effect, then use a sprite image instead of two separate images. Two separate images will sometimes cause a delay on the hover effect, that's why we use a sprite image for hover images.


Script.js
---------

In the js-folder there is a script.js file, where all the custom jQuery code should be written. This means that we should stop writing javascript codes in the HTML-files, and start writing them in separate files.


HTML5
-----

As this is a HTML5 template you are allowed to use HTML5-tags. To make them recognized in old browsers (mostly Internet Explorer) we are using the javascript plugin [HTML5shiv](https://github.com/aFarkas/html5shiv). 


Favicon
-------

For every project we will make a favicon. There is already a reference to this favicon in the head of the HTML-file.


Optional Header References
--------------------------

There are a lot of other header references as touch icons, Google Analytics and so on, which aren't needed in all projects. Therefore we've made a list of all these optional references here, to get the right code and get it faster:

- Google Analytics:

		<script type="text/javascript">

		  var _gaq = _gaq || [];
		  _gaq.push(['_setAccount', 'UA-XXXXX-X']);
		  _gaq.push(['_trackPageview']);

		  (function() {
		    var ga = document.createElement('script'); ga.type = 'text/javascript'; ga.async = true;
		    ga.src = ('https:' == document.location.protocol ? 'https://ssl' : 'http://www') + '.google-analytics.com/ga.js';
		    var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(ga, s);
		  })();

		</script>
- Piwik:

		<script type="text/javascript">
			var pkBaseURL = (("https:" == document.location.protocol) ? "https://{$PIWIK_URL}/" : "http://{$PIWIK_URL}/");
			document.write(unescape("%3Cscript src='" + pkBaseURL + "piwik.js' type='text/javascript'%3E%3C/script%3E"));
		</script><script type="text/javascript">
			try {
				var piwikTracker = Piwik.getTracker(pkBaseURL + "piwik.php", {$IDSITE});
				piwikTracker.trackPageView();
				piwikTracker.enableLinkTracking();
			} catch( err ) {}
		</script>
		
- [Placeholder javascript plugin](https://github.com/danielstocks/jQuery-Placeholder)
- Touch icons (if you need to add a icon for Android phones, then create the icon as a ["apple-touch-icon-precomposed"](http://mathiasbynens.be/notes/touch-icons) - this removes the fancy effects on the Home Screen such as rounded corners and reflective shine):

		<link rel="apple-touch-icon" href="" /> <!-- iPhone -->
		<link rel="apple-touch-icon" sizes="72x72" href="apple-touch-icon-ipad.png" /> <!-- iPad -->
		<link rel="apple-touch-icon" sizes="114x114" href="apple-touch-icon-iphone4.png" /> <!-- high-resolution iPhone and iPod -->
		<link rel="apple-touch-icon" sizes="144x144" href="" /> <!-- high-resolution iPad -->
		
- Viewport meta tag:

		<meta name="viewport" content="width=device-width, initial-scale=1">
	