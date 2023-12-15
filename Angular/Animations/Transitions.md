# Transition properties

## style

Define a style to apply instantly
If used with animate() will transit an element into defined style

How to use:
``` TypeScript
style({
 property: value,
 ThreeWordsProperty: 'string value'
})
```
## animate

Define a time to transit into a next state

How to use:
``` TypeScript
animate() // - instant transit
animate(500) // - 500ms duration
animate('500ms 1s ease') // - 500ms duration, 1s delay, ease timig function

// Can be used with style()
animate(duration, style({property: value}))
```

Important clarifications: 
- Several animate()s can't exist together
- Can use cubic-bezier for timing fuction 
## sequence

Make a sequence of animations

How to use:
``` TypeScript
sequence([
	animate(duration, style({property: value})),
	animate(duration)
])
```
To make a sequence or a group with children elements see [[Angular/Animations/Children' animations|Children' animations]]
