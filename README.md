Navigation Bar Widget
-------------------
A custom NavigationBar widget for Titanium Alloy.

Example Usage
-------------

###### Alloy View (XML)

	<Require type="widget" src="com.mcongrove.navigationBar" id="NavigationBar" image="/images/logo.png" />

###### Alloy Controller (JS)

	$.NavigationBar.setBackgroundColor("#35ABFF");

	$.NavigationBar.showBack(
		function(_event) {
			closeWindow();
		}
	);

	$.NavigationBar.showRight({
		image: "/images/myRightButton.png",
		callback: function() {
			doSomething();
		}
	});

Options
-------
Parameter | Type    | Default |
----------|---------|---------|
image     | `String` | null    |
text      | `String` | null    |

Methods
-------
Function           | Parameters   | Description
-------------------|--------------|------------
addNavigation      | `View`       | Adds [detail navigation widget](https://github.com/mcongrove/com.mcongrove.detailNavigation)
removeNavigation   |              | Removes [detail navigation widget](https://github.com/mcongrove/com.mcongrove.detailNavigation)
setBackgroundColor | `String`, `String`     | Background color, Theme color ("black" | "white") _(optional)_
setTitle           | `String`     | Title bar text
showLeft           | `Object`     | `callback`: Click callback, `image`: Image to add _(optional)_, `text`: Text to add _(optional)_, `font`: Font for label _(optional)_
showRight          | `Object`     | `callback`: Click callback, `image`: Image to add _(optional)_, `text`: Text to add _(optional)_, `font`: Font for label _(optional)_
showBack           | `Function`   | Click callback
showNext           | `Function`   | Click callback
showMenu           | `Function`   | Click callback
showSettings       | `Function`   | Click callback
showAction         | `Function`   | Click callback

Changelog
---------
* 1.2
	* Improvements by [Stephen Woodford](https://github.com/swoodford5)
	* Ability to manually set theme
	* Android title view fixes
	* Image path improvements
* 1.1
	* Initial commit as separate module; see [ChariTi](https://github.com/mcongrove/ChariTi/tree/master/app/widgets) for previous versions

License
-------

Copyright 2013 Matthew Congrove

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
