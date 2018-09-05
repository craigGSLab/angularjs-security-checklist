# Angularjs security checklist

AngularJS is a javascript framework for building web clients.

Given below is a list of things you could keep in mind that would help write more secure client-side code with AngularJS.

1. Be careful when using user input in  Angular expressions. Avoid using untrusted user input with the following:

...###### Methods:
...- $eval
...- $evalAsync
...- $watch
...- $watchGroup
...- $apply
...- $applyAsync
...- $watchCollection

...###### Filters:
...- expressions used with the 'orderBy' filter.

...###### Services:
...- $parse
...- $compile
...- $interpolate


2. Avoid generating templates on the server based on user generated input.
3. Avoid dynamically generating templates on the sever. Templates should be defined on the client and can be populated via data bindings.
4. Do not write user input to the DOM before Angular runs on the webpage.



References:
--------------
- https://www.owasp.org/images/6/6e/Benelus_day_20161125_S_Lekies_Securing_AngularJS_Applications.pdf
- https://www.owasp.org/images/4/46/OWASPLondon20170727_AngularJS.pdf

General security references:
-------------------------------
- https://www.owasp.org/index.php/AJAX_Security_Cheat_Sheet
