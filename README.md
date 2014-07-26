ngSilent
========

Adds silent mode to AngularJS.

How to use
------

1. Add link to ngSilent.js file
2. Connect the module

      var site = angular.module('site', ['module1', 'ngSilent', 'ngRoute']);
	 
**IMPORTANT**
'ngSilent' should be defined before 'ngRoute'.


     var site = angular.module('site', ['module1', 'ngRoute', 'ngSilent']);
	
This will not work.	

3. Add $ngSilentLocation wherever you want:


      function SomeController($ngSilentLocation)
	 
and then

     $ngSilentLocation.silent('/new/path/');
	 
URL will be changed but related controller is not called.	 
