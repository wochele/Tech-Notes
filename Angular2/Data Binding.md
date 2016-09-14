# Data Binding

## Interpolation

`<h3>{{story.name}}</h3>`

## 1 Way Binding

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
