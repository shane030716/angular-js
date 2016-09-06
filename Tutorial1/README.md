# Tutorial 1

### Set up Angular.js

Visit [https://angularjs.org/](https://angularjs.org/), there are various options for downloading. We will choose AngularJS 1.5.x Stable and Minified Version

See [myfirstexample.html](myfirstexample.html)

Some key notes:

* Include the `angular.min.js` script in `<head>`
* Add `ng-app = "myapp"` to tell which part of the HTML contains an AngularJS app.
* The whole div `<div id="myview" ng-controller = "HelloController"> ... </div>` is the view of this app.
* The controller is inside the `<script>` tag, `angular.module(app_name, []).controller(controller_name, function($scope) {});`.
* In the controller: 
	* `angular` is the global variable
	* `angular.module(app_name, [])` creates a module with `app_name`, which is `"myapp"` in this example.
	* Not sure what `[]` is yet.
	* Chaining to `.controller(controller_name, function($scope){})`, which registers a controller called `controller_name` (`"HelloController"` in the example). And the callback with the `$scope` variable, which is considered the model
	* The objects in `$scope` can then be passed to the variables inside the syntax `{{ ... }}` in the html, which will be rendered with their values.


When the page is loaded in the browser, following things happen:

* HTML document is loaded into the browser, and evaluated by the browser. AngularJS JavaScript file is loaded, the angular global object is created. Next, JavaScript which registers controller functions is executed.

* Next AngularJS scans through the HTML to look for AngularJS apps and views. Once view is located, it connects that view to the corresponding controller function.

* Next, AngularJS executes the controller functions. It then renders the views with data from the model populated by the controller. The page is now ready.

[List of Tutorials](https://github.com/shane030716/angular-js#list-of-tutorials)