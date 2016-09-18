# Components

- Manage templates
- Teach the browser new tags that have new functionality
- Every app has at least one component, the root component. They are the basic building blocks of applications.
- Controls a portion of the screen, a view, through it's associated template
- You define a component's application logic—what it does to support the view—inside a class. The class interacts with the view through an API of properties and methods.

A basic component has 2 parts

1. A `Component` annotation
2. A component definition class

- `selector` and `template`/`templateUrl` are mandatory properties
- Annotations start with `@` and create an annotations array. They add metadata to the class immediately following it.
- When I annotate a class (really just a newable function), the compiler creates an attribute on that class called "annotations", stores an array in it, then tries to instantiate an object with the same name as the annotation, passing the metadata into the constructor. The annotated object can then make any use of this 'annotations' array that it likes.

```
@Component ({
  selector: 'hello-world',
  template: `
  <div>
      Hello World
  </div>        
  `
})

class HelloWorld {}

@NgModule({
    declarations: [HelloWorld],
    imports: [BrowserModule],
    bootstrap: [HelloWorld],
})

class HelloWorldAppModule {}

platformBrowserDynamic().bootstrapModule(HelloWorldAppModule);

```

- Typical `@Component` configuration options:
- *selector* - CSS selector that tells Angular to create and insert an instance of this component where it finds a <selector_name> tag in parent HTML. 
- *templateUrl* - address of this component's HTML template
- *directives* - array of the components or directives that this template requires. 
- *providers* - array of dependency injection providers for services that the component requires. 
