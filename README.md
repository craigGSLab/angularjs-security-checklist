# Angularjs security checklist

AngularJS is a javascript framework for building web clients.

Given below is a list of things you could keep in mind that would help you write more secure client-side code with AngularJS.

1. Be careful when using user input as expressions. Avoid using untrusted user input with the following:

- $eval
- $watch
- $apply
- $parse
- $compile
- $interpolate

   (..and also in other similar situations where expressions are evaluated.)
