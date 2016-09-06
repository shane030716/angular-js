# Tutorial 4

### Directives

AngularJS directives are used to extend HTML. These are special attributes starting with `ng-` prefix.

* **ng-app** - This directive starts an AngularJS application.
* **ng-init** - This directive initializes application data.
* **ng-model** - This directive defines the model that is a variable to be used in AngularJS.
* **ng-repeat** - This directive repeats html elements for each item in a collection.

#### `ng-app` directive

* starts an AngularJS Application.
* defines the root element.
* initializes or bootstraps the AngularJS application which a web page contains
* Loads variable AngularJS modules in the application.

Default AngularJS application on a `div` element. *(Note that it doesn't have to have a name?)*
```
<div ng-app = "">
...
</div>
```

#### `ng-init` directive

* initializes an AngularJS application **data**.
* puts values to variables to be used in the application.

Initialize an array of contries using JSON
```
<div ng-app = "" ng-init = "countries = [{locale:'en-CA',name:'Canada'}, {locale:'en-US',name:'United States'}, {locale:'en-GB',name:'United Kingdom'}, {locale:'fr-FR',name:'France'}, {locale:'fr-CA',name:'Canada'}]">
	...
</div>
```

#### `ng-model` directive

* defines the model/variable to be used in an AngularJS application.

Defining a model named `"name"`.
```
<div ng-app = "">
   ...
   <p>Enter your Name: <input type = "text" ng-model = "name"></p>
</div>
```

#### `ng-repeat` directive

* repeats html elements for each item in a collection.
* Similar with `<s:iterator>` in Struts and `{% for item in collection %}` in Jinja2

Iterating over the array of countries
```
<div ng-app = "">
   ...
   <p>List of Countries with locale:</p>
   
   <ol>
      <li ng-repeat = "country in countries">
         {{ 'Country: ' + country.name + ', Locale: ' + country.locale }}
      </li>
   </ol>
   
</div>
```

See [testAngularJS.html](testAngularJS.html)

[List of Tutorials](https://github.com/shane030716/angular-js#list-of-tutorials)