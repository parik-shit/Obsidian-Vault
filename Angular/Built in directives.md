Sure, here are some built-in directives in Angular that you can include in your notes:

1. **ngIf**: Used for conditionally rendering elements based on a boolean expression.
   ```markdown
   ```html
   <div *ngIf="isLoggedIn">
       Welcome, User!
   </div>
   ```

2. **ngFor**: Used for iterating over lists and collections to generate HTML elements.
   ```markdown
   ```html
   <ul>
       <li *ngFor="let item of items">
           {{ item }}
       </li>
   </ul>
   ```

3. **ngSwitch**: Used for conditionally rendering elements based on multiple conditions.
   ```markdown
   ```html
   <div [ngSwitch]="color">
       <div *ngSwitchCase="'red'">Red color</div>
       <div *ngSwitchCase="'blue'">Blue color</div>
       <div *ngSwitchDefault>Other color</div>
   </div>
   ```

4. **ngModel**: Used for two-way data binding, linking form controls to properties in the component class.
   ```markdown
   ```html
   <input type="text" [(ngModel)]="username">
   ```

5. **ngClass**: Used for conditionally applying CSS classes based on expression evaluation.
   ```markdown
   ```html
   <div [ngClass]="{'active': isActive, 'inactive': !isActive}">
       Content
   </div>
   ```

6. **ngStyle**: Used for conditionally applying inline styles based on expression evaluation.
   ```markdown
   ```html
   <div [ngStyle]="{'color': isActive ? 'green' : 'red', 'font-size': isActive ? '16px' : '14px'}">
       Content
   </div>
   ```

7. **ngSubmit**: Used with forms to handle form submissions.
   ```markdown
   ```html
   <form (ngSubmit)="onSubmit()">
       <!-- Form controls here -->
       <button type="submit">Submit</button>
   </form>
   ```

8. **ngTemplateOutlet**: Used for dynamic template rendering.
   ```markdown
   ```html
   <ng-container *ngTemplateOutlet="templateRef"></ng-container>
   ```

These are some of the commonly used built-in directives in Angular. Make sure to check the official Angular documentation for more details and examples.