# How to bind a class to a child element

## A single-class bind controlled by a boolean

Use attribute with [data binding]:
``` HTML
<element
	[class.className]="boolean"
>
	<!-- Some text -->
</element>
```

## A multiple-class bind controlled by an object

Use attribute with [data binding]:
```TypeScript
<element
	[class]="{class-name-1: true, class-name-2: false}"
>
	<!-- Some text -->
</element>
```

## A multiple-class bind controlled by an array

Use attribute with [data binding]:
```TypeScript
<element
	[class]="[class-name-1, class-name-2]"
>
	<!-- Some text -->
</element>
```

## A multiple-class bind controlled by a string

Use attribute with [data binding]:
```TypeScript
<element
	[class]="'class-name-1 class-name-2 class-name-3'"
>
	<!-- Some text -->
</element>
```

