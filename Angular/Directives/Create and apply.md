# How to create and apply a directive

## 1. Create a direcive

Use Angular CLI:
``` Node.js
ng generate directive directive-name
```

## 2. Declare the directive in module or make it standalone and import in one

In module.ts:
``` TypeScript
import { directiveClassName } from 'path';
import { directiveClassNameStandalone } from 'path';

@NgModule({
	 declarations: [
		directiveClassName
	],
	import: [
		directiveClassNameStandalone
	]
})
export class AppModule { }
```

## 3. Define the directive's selector

In directive.ts:
``` TypeScript
@Directive({
	selector: '[appDirectiveClassName]'
})
export class DirectiveClassName { 
	// Some Code
}
```

## 4. Apply the directive in a component's template

In component's template:
``` HTML
<element
	appDirectiveClassName
>
	// Some text
</element>
```

