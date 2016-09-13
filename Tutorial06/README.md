# Tutorial 6

### Controllers

AngularJS application mainly relies on controllers to control the flow of data in the application. A controller is defined using `ng-controller` directive. A controller is **a JavaScript function** which accepts the `$scope` parameter, which contains properties, objects or functions. The `$scope` parameters refers to the application/module that controller is to controll.

Here we declare a controller "studentController" for this `<div>`, which will be the view of this controller. ** *(Note that the `ng-app` and the `ng-controller` directives are in the same `<div>`, which is different from Tutorial 1)* **
```
<div ng-app = "" ng-controller = "studentController" >
	...
</div> 
```

Now we can write a function for the "studentController", which we can then use when registering the controller in the module

```
<script>
	function studentController($scope) {
		$scope.student = {
			firstname: "Justin",
			lastname: "Trudeau",

			fullname: function() {
				return $scope.student.firstname + " " + $scope.student.lastname;
			}
		};
	}
</script>
```
Some key notes for the above function

* studentController is defined as a function with the `$scope` argument.
* `$scope` refers to the application which is to use the "studentController" controller .
* `$scope.student` is property of "studentController" controller
* firstname and lastname are two properties of the `$scope.student` object.
* `fullname` is a function/closure of the `$scope.student` object which returns the combined first and last names.
* Inside the `fullname` function, we need to access student's other properties from `$scope`, cannot access them using `firstname` or `lastname` directly. i.e. `return firstname + " " + lastname` will get an error


See [testAngularJS.html](testAngularJS.html)

Note that the import of angular.js `<script src = "angular.min.js"></script>` must be before the rest of AngularJS related scripts.

[List of Tutorials](https://github.com/shane030716/angular-js#list-of-tutorials)