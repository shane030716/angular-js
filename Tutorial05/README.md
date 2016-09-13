# Tutorial 5

### Expressions

`{{ expression }}`. So the double braces are called **Expression**

Expressions are used to **bind** application data to html. It behaves in the same way as the `ng-bind` derective does. AngularJS application expressions are **pure javascript expressions** and output the data where they are used.

* Numbers:
   `<p> Expense on books: ${{ cost * quantity }}</p>`

* Strings:
   `<p> Hello {{ student.firstname + " " + student.lastname }}!</p>`

* Object:
   `<p> Roll No.: {{ student.rollNo }}</p>`

* Array:
   `<p> Marks: {{ marks[3] }} </p>`

See [testAngularJS.html](testAngularJS.html)

[List of Tutorials](https://github.com/shane030716/angular-js#list-of-tutorials)