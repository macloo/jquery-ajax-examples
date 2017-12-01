# jQuery Ajax examples

Some files for easy reference. 

[`$.ajax()` example with `$.map()`](https://macloo.github.io/jquery-ajax-examples/ajax-and-map.html) — gets a JSON file with 65 Harry Potter characters in it and formats all the text and writes it into the HTML.

[`$.getJSON()` example with `$.map()`](https://macloo.github.io/jquery-ajax-examples/getJSON-and-map.html) — this is the same as the previous file, but using the `$.getJSON` method instead of `$.ajax`.

[Ajax/jQuery.getJSON Simple Example](https://www.sitepoint.com/ajaxjquery-getjson-simple-example/) is a nice explainer about `$.getJSON`.

[`$.ajax()` example with `$.each()`](https://macloo.github.io/jquery-ajax-examples/ajax-and-each.html) — no Harry Potter here. U.S. presidential portraits instead. Whereas `$.map()` returns a new array, containing all the stuff you requested from the server — `$.each()` just loops and does whatever you say — no new array. Here jQuery detects which president you clicked, finds his data on the server, and gives you a pop-up card full of facts about him. **Things that work poorly** in this version (fixed in the next version, *presidents.html*): (1) The modal info box does not center correctly. (2) The modal info box looks awful on mobile.

[U.S. Presidents](https://macloo.github.io/jquery-ajax-examples/presidents.html) — this is the same as the previous file, but with NO AJAX — because we can just load the JSON file as an array. However, a tweak is needed: `var presData = []`. Now you have an array of objects, but it's formatted exactly the same as the pure JSON version. This version also fixes **the centering of the modal info box,** which is off in the previous version because jQuery `width()` does not account for padding and border, but jQuery `outerWidth()` does. Yay! Also fixed responsive (mobile) in this version (the JavaScript tests for width < 550 pixels).
