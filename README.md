# Pas2JS Widgetset
Pas2JS Widgetset is a RAD Framework to develop Web Applications like to develop Windows Applications originally started by Hélio S. Ribeiro and Anderson J. Gado da Silva.

### Thanks
This project is only possible thanks to [Free Pascal](https://www.freepascal.org/ "Free Pascal"), [Lazarus](https://www.lazarus-ide.org/ "Lazarus") and the fabulous compiler [Pas2JS](http://wiki.freepascal.org/pas2js "Pas2JS")

### Help Please
This project is under development.
This version is an basic implementation and many bugs need to be corrected.
Please help us to take this project forward.

### Install
This was tested with Lazarus 2.0.6 and Lazarus 2.1.
* make sure that the _pas2jsdsgn_ package is installed
* the _pas2js_rtl_ package should have been opened (so that the IDE knows about it)
* install the _pas2js_designer_package_ package from _design/package_
* open the _pas2js_widget_ package in _widgets_ (again so that the IDE knows about it)

### Usage
* create a new _Web Browser Application_ (this is provided by the Pas2JS package; the _Application (Pas2JS)_ template is currently not useable)
* add _-JRhtml_ to the custom compiler options
* change the code of the main project to the following:

      program YourProject;

      {$mode objfpc}

      uses
        Forms, Interfaces;

      begin
        Application.Initialize;
        Application.Run;
      end.

* add forms by using the _Web Form (Pas2JS)_ template (frame and data module are not yet tested)

### Notes
* you need to manually add the `Application.CreateForm(TWFormX, WForm1);` statement for now
* you can only use components from the _Pas2JS_ tab
* when you add a component you need to remove the _pas2js_designer_package_ and _LCL_ packages from the project again before compiling
* after each compile copy the resource `link`-entries from the generated _*-res.html_ file in front of the `script` entry in the project's HTML file

### Further plans
* fix project template
* test frame and data module templates
* implement support for DB controls
* implement a Lazarus compatible grid
* better maintenance of the project's HTML file
* better maintenance of the project's main program file
* more dynamic layouting of the components
