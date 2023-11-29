# How to create and apply a component

## 1. Create a component

Use Angular CLI:
``` Node.js
ng generate component component-name
```

## 2. Declare the component in module or make it standalone and import in one

In module.ts:
``` TypeScript
import { componentClassName } from 'path';
import { componentClassNameStandalone } from 'path';

@NgModule({
	 declarations: [
		componentClassName
	],
	import: [
		componentClassNameStandalone
	]
})
export class AppModule { }
```

## 3. Define the component's selector, template and style

In component.ts:
``` TypeScript
@Directive({
	selector: '[app-component]',
	templateUrl: 'path to .html',
	styleUrl: 'path to .scss'
})
export class ComponentClassName { 
	// Some code
}
```

## 4. Use the component

In app.component.ts:
``` HTML
<app-component></app-component>
```
