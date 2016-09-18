# Directives

- Angular templates are dynamic. When Angular renders them, it transforms the DOM according to the instructions given by directives.
- A directive is a class with directive metadata - `@Directive`
 
### Structural Directives

- Alter layout by adding, removing, and replacing elements in DOM.
- '*' is a structural directive which will change something in my view - `*ngFor`, `*ngIf`

### Atribute Directives

- Alter the appearance or behavior of an existing element. In templates they look like regular HTML attributes, hence the name.
- The ngModel directive, which implements two-way data binding, is an example of an attribute directive. ngModel modifies the behavior of an existing element (typically an <input>) by setting its display value property and responding to change events.

```angular
<ul>
  <li *ngFor="#vehicle of vehicles">
    {{ vehicle.name }}
  </li>
</ul>
<div *ngIf="vehicles.length">
  <h3>You have {{vehicles.length}} vehicles</h3>
</div>
```
