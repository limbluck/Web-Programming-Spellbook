# How to bind a style to a child element

## A single-style bind controlled by a boolean

Use attribute with [data binding]:
``` HTML
<element
	[style.propety-name]="value"
>
	<!-- Some text -->
</element>
```

## A multiple-style bind controlled by a string

Use attribute with [data binding]:
```TypeScript
<element
	[style]="'property-name: value; property-name: value'"
>
	<!-- Some text -->
</element>
```

## A multiple-class bind controlled by an object

Use attribute with [data binding]:
```TypeScript
<element
	[style]="{property-name: value, property-name: value}"
>
	<!-- Some text -->
</element>
```
