# Angularjs security checklist

AngularJS is a javascript framework for building web clients.

Given below is a list of things you could keep in mind that would help write more secure client-side code with AngularJS.

### 1. Use the latest Angular possible.

### 2. Be careful when using user input in  Angular expressions. Avoid using untrusted user input with the following:

###### Methods:
- $eval
- $evalAsync
- $watch
- $watchGroup
- $apply
- $applyAsync
- $watchCollection

###### Filters:
- expressions used with the 'orderBy' filter.

###### Services:
- $parse
- $compile
- $interpolate


### 3. Avoid generating templates on the server based on user generated input.
This could open up the applciation to an XSS attack.

### 4. Avoid dynamically generating templates on the sever. 
Templates should be defined on the client and can be populated via data bindings.


### 5. Do not write user input to the DOM before Angular runs on the webpage.

### 6. Be careful when inserting HTML into the DOM.
- Avoid diabling escaping for user input - $sce.enabled(false)
- Avoid using element.html() to insert HTML.
- Avoid using ng-bind-html and 'trustAsHtml'.
- Use ng-bind-html along with the NGSanitize module.

### 7. Don't use user input in url based directives:
This includes ngSrc, ngInclude, ngHref


___


References:
--------------
- https://docs.angularjs.org/guide/security
- https://www.owasp.org/images/6/6e/Benelus_day_20161125_S_Lekies_Securing_AngularJS_Applications.pdf
- https://www.owasp.org/images/4/46/OWASPLondon20170727_AngularJS.pdf

General security references:
-------------------------------
- https://www.owasp.org/index.php/AJAX_Security_Cheat_Sheet
