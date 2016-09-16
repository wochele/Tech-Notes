# Modules (NgModules)

- [Module plunkr](https://angular.io/resources/live-examples/ngmodule/ts/plnkr.html)
- [Modules In Depth](https://angular.io/docs/ts/latest/guide/ngmodule.html)

- Every Angular app has at least one module, the root module, conventionally named `AppModule`
- While the root module may be the only module in a small application, most apps have many more feature modules, each a cohesive block of code dedicated to an application domain, a workflow, or a closely related set of capabilities.
- An Angular module, whether a root or feature, is a class with an `@NgModule` decorator.

`@NgModule` is a decorator function that takes a single metadata object whose properties describe the module. The most important properties are:

- *declarations* - the view classes that belong to this module. Angular has three kinds of view classes: components, directives, and pipes.
- *exports* - the subset of declarations that should be visible and usable in the component templates of other modules.
- *imports* - other modules whose exported classes are needed by component templates declared in this module.
- *providers* - creators of services that this module contributes to the global collection of services; they become accessible in all parts of the app.
- *bootstrap* - the main application view, called the root component, that hosts all other app views. Only the root module should set this bootstrap property.
