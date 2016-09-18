# Data Binding

- Mechanism for coordinating parts of a template with parts of a component. Add binding markup to the template HTML to tell Angular how to connect both sides.
- Angular processes all data bindings once per JavaScript event cycle, from the root of the application component tree through all child components.
- Data binding plays an important role in communication between a template and its component.
- Data binding is also important for communication between parent and child components.

## Interpolation

`<h3>{{story.name}}</h3>`

## 1 Way Binding - Property binding

```angular
<h3 [InnerText]="story.name"></h3>
<div [style.color]="color">{{story.name}}</div>
```

## Event Binding

```angular
<button
  (click)="log('click')"
  (blur)="log('blur')">OK</button>
```

## 2 Way binding on an input

```angular
<input [(ngModel)]="story.name">
```

[()] - Bananna in a box - Gives 2 way binding
