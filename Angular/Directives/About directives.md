# About directives

## What is directive in general

Directives is akin to a fully-fledged component, but only without the view
Directive is defined by a @Directive decorator
## What is structural directives

Structural directives are different from attribute ones just by wrapping an element to which they are applied with ng-template:

- Syntactic sugar: 
	``` HTML
	<element
		*structuralDirective
	>
		// Some text
	</element>
	```
- What actually happens:
	``` HTML
	<ng-template
		structuralDirective
	>
		<element>
			// Some text
		</element>
	</ng-template>
	```

## How to use

See:
- [[Angular/Directives/Create and apply|Create and apply]]
- [[Angular/Directives/Access to an element|Access to an element]]
- Directives can use data binding like components [[Angular/Components/Data binding|Data binding]]
