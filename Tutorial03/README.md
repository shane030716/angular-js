# Tutorial 3

### First Application

Before we start, we need to know that an AngularJS application consists of three important parts:

* **ng-app** - This directive defines and links an AngularJS application to HTML
* **ng-model** - This directive binds the values of AngularJS application data to HTML input controls. 
* **ng-bind** - This directive binds the AngularJS application data to HTML tags.

## Steps to create an AngularJS Application

### Step 1 - Load framework
With CDN (content delivery network)
```
<script src = "http://ajax.googleapis.com/ajax/libs/angularjs/1.3.14/angular.min.js">
</script>
```
Or local file:
```
<script src = "angular.min.js">
</script>
```

### Step2 - Define AngularJS Application using `ng-app` directive
```
<div ng-app = "">
   ...
</div>
```

### Step 3 - Define a model name using `ng-model` directive
```
<p>Enter your Name: <input type = "text" ng-model = "name"></p>
```

### Step 4 - Bind the value of the above model defined using `ng-bind` directive.
```
<p>Hello <span ng-bind = "name"></span>!</p>
```

## Steps to run an AngularJS Application

Create and See [testAngularJS.htm](testAngularJS.htm). *(Note that `angular.min.js` in included at the end of the html file.)*

Open it on a web browser.

## How AngularJS integrates with HTML

* `ng-app` directive indicates the start of AngularJS application.

* `ng-model` directive then creates a model variable named `"name"` which can be used with the html page and within the div having ng-app directive.

* `ng-bind` then uses the `name` model to be displayed in the html span tag whenever user input something in the text box.

* Closing`</div>` tag indicates the end of AngularJS application.


[List of Tutorials](https://github.com/shane030716/angular-js#list-of-tutorials)