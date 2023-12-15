# How to apply animations

## 1. Don't forget to install a package

Type a command in Angular CLI:
``` Node.js
nmp install @angular/animations@latest
```

## 2. Include animations in @Component decorator

Insert an animations property in a decorator in a component.ts file
``` TypeScript
@Component({
	 animations: [
		 // insert code here
	 ]
})
```

## 3. Define a trigger for animations

Insert a trigger property in an animations property of a decorator in a components.ts file
``` TypeScript
trigger('triggerName', [
	// insert code here
]
```

## 4. Define states of animation and styles for them

Insert states in a trigger property of an animations property of a decorator in a components.ts file
``` TypeScript
state('stateName', style({
	property: value,
	property: 'string value'
}))
```

## 5. Define transitions between states

Insert transitions in a trigger property of an animations property of a decorator in a components.ts file
``` TypeScript
transition('styleName => styleName', [
	// type transition properties here
])
```
See also:
- [[Angular/Animations/Transitions|Transitions]] to find transition properties
- [[Angular/Animations/Children' animations|Children' animations]] to find a howto for complex animations

## 6. Apply a trigger to HTML element and bind a state value for it

Insert a trigger into an element in HTML markup
``` HTML
<element
	[@triggerName]="stateName"
>
	<!-- Some marked text -->
</element>
```