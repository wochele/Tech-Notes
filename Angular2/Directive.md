# Directives

'*' is a structural directive which will change something in my view

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
