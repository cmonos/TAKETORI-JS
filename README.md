About taketori.js
===============

What's this ?
----------------

"taketori.js" is a javascript library to make text vertical.

###Browser Support
InternetExplorer5.5+ / Firefox3.5+ / Safari3.2+ / Chrome3.0+ / Opera10.5+

###Language
Chinese, Japanese, Korean

###License
MIT License

How To Use
---------------

###Preparation

Upload these two files same directory.

* taketori.js
* taketori.css

###Sample

	<script type="text/javascript" src="taketori.js" charset="UTF-8"></script>
	<script type="text/javascript">
	//<![CDATA[
	(new Taketori()).set({key : value}).element('target element ID').toVertical([waiting for load or not]);
	//]]>
	</script>

###Parameters

lang

* 'ja-jp' = Japanese
* 'zh-tw' = Taiwanese

fontFamily

* 'serif'
* 'sans-serif'
* 'cursive'
* 'kai'

height（'em'|'px'|'width'=height of parent node.）

maxHeight（'em'|'px'）

multiColumnEnabled

* false(default)
* 'auto'
* true(too slow)

gap（'em'|'px'）(=column-gap)

togglable(true|false)

cacheDisabled(true|false)

####Tips

You can set these parameters as class name.

> class="taketori-maxHeight-30em taketori-fontFamily-sans-serif"

###How to set target elements.

* 'element ID'
* 'tagName.className'
* '=auto'
* '=dblclick'

###Button Sample

	<div class="tategaki">
	縦書き　直排
	</div>
	<a href="#" id="toggle">Toggle</a>
	<script type="text/javascript" src="taketori.js" charset="UTF-8"></script>
	<script type="text/javascript">
	//<![CDATA[
	var taketori = (new Taketori()).set({fontFamily:'sans-serif'}).element('div.tategaki').toVertical();
	taketori.document.element('toggle').addEventListener('click',function (e) {
		taketori.toggleAll();
		taketori.document.stopPropagation(e);
		taketori.document.preventDefault(e);
		return false;
	});
	//]]>
	</script>
