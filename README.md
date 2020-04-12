# APM

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.1.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).


# Repository Content

* Angular CLI
* Components
* Templates, data binding and directives
* Services and dependency injection
* Http and observables
* Navigation and routing

## NOTES: COMPONENTS

### Component: Class

###### Clear Name
* Use PascalCasing
* Append "Component" to the name

### Component: Interface

###### Creating Interface
* interface keyword
* export it

###### Implementing interface
* _**implements**_ keyword and interface name
* Write code for each property and method in implementing class

###### export keyword

###### Data in properties
* Appropriate data type
* Appropriate default value
* camelCase

###### Logic in Methods
* camelCase

### Component: Metadata

###### Component Decorator
* Prefix with @; Suffix with ()
* selector: Component name in HTML
* template: View's HTML

### Component: Import

###### Module path
* Enclose in quotes
* Correct spelling/casing

### Lifecycle Hooks

* Import the lifecycle hook interface
* Implement the lifecycle hook interface
* Write code for the hook method

###### _OnInit_
* Perform component initialization, retrieve data from backend

###### _OnChanges_
* Perform action after change to input properties


## NOTES: TEMPLATES, INTERPOLATION and DIRECTIVES

### Template

###### Inline Template
* For short templates
* Specify the template property
* Use the ES2015 back ticks for multiple lines

###### Linked Template
* For longer templates
* Specify the templateUrl property
* Define the path to the HTML file

### Interpolation

###### One way binding
* From component class property to an element property
* Defined with double curly braces
* Contains a template expression
* No quotes needed
* _{{ 'Page Title: ' + title }}_
* _{{ 2 * 10 + 1 }}_
* _{{ 'Page Title: ' + getTitle() }}_


### Structural Directives

###### *ngIf and *ngFor
* Prefix with an asterisk(*)
* Assign to a quoted string expression

###### *ngIf
* Expression is evaluated as a true or false value

###### *ngFor
* Define the local variable with _**let**_
* Specify '_**of**_': to get the value of each item
* Specify '_**in**_': to get the index of each item


## NOTES: Data Binding and Pipes

### Data Binding

######
* Interpolation: _{{ title }}_
* Property Binding: _IMG-tag [src]='product.imageUrl'_
* Event Binding: _<BUTTON-tag (click)='toggleImage()'>_
* Two-way Binding: _INPUT-tag [(ngModel)]='listFilter'_

### Pipes

###### 
* Pipe character |
* Pipe name
* Pipe parameter: Separated with colon (:)
* _{{ product.price | currency : 'USD' : 'symbol' : '1.2-2' }}_

###### Building a Custom Pipes
* Import Pipe and PipeTransform
* Create a class that implements PipeTransform - export the class
* Write code for the Transform method
* Decorate the class with the Pipe decorator

###### Using a Custom Pipes
* Import the custom pipe
* Add the pipe to the declaration array of on Angular module
* Any template associated with a component is also declared in that Angular module can use that pipe
* Use the pipe in the template: Pipe character (|) - Pipe Name - Pipe Arguments (separeted by colons)


## NOTES: Nested Component

### Input Decorator
* Attached to a property of any type
* Prefix with @; Suffix with ()

### Output Decorator
* Attached to a property declared as an EventEmitter
* Use the generic argument to define the event payload type
* Use the new keyword to create and instance of the EventEmitter
* Prefix with @; Suffix with ()

### Container Component

###### Use the directive
* Directive name -- nested component's selector
* Use property binding to pass data to the nested component
* Use event binding to respond to events from the nested component
* Use _$event_ to access the event payload passed from the nested component


## NOTES: Services and Dependency Injection

### Creating a Service

###### Service Class
* Clear name
* Use PascalCasing
* Append "Service" to the name
* export keyword

###### Service Decorator
* Use Injectable
* Prefix with @; Suffix with ()

### Registering a Service

###### Appropriate level of hierarchy
* Root application injector if the service is used throughout the application
* Specific component's injector if only that component uses the service

###### Service injectable decorator
* Set the _providedIn_ property to 'root'

###### Component decorator
* Set the providers property to the service

### Dependency Injection
* Specify the service as a dependency
* Use a constructor parameter
* Service is injected when component is instantiated


## NOTES: Retrieving Data using HTTP

### Http Service

###### 
* Define a dependency for the HttpClient service: Use constructor parameter
* Create methods for each http request
* Call the desired http method, such as get: Pass in the URL
* Use generics to specify the returned type
* Add error handling

###### Subscribing
* Call the subscribe method of the returned Observable
* Provide a function to handle an emitted item: Normally assigns a property to the returned JSON object
* Provide an error function to handle any returned errors


## NOTES: Navigation and Routing Basics

### Displaying Components

###### Nest-able Components
* Define a selector
* Nest in another component
* No route

###### Routed Component
* No selector
* Configure routes
* Tie routes to action
* Place the view

### Configuring Routes

###### Define the base element

###### Add RouterModule
* Add each route (RouterModule.forRoot([]))
* Order of the routing paths matters

###### path: Url segment for the route
* No leading slash ('/')
* '' for default route
* '**' for wildcard route: implement 404 not found page

###### component
* Not string name; So not enclosed in quotes

### Tying Routes to Actions

###### Add the routerLink directive as an attribute
* Clickable eleement
* Enclose in square brackets

###### Bind to a link parameters array
* First element is the path
* All other elements are route parameters

### Placing the view

###### Add the router-outlet directive
* Identifies where to display the routed component's view
* Specified in the host component's template
