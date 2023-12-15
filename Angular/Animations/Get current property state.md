# How to make animation from current state
``` TypeScript
style({
      transform: '*', // Get the current state
    }),
animate('1s 0s ease-out',
	style({
		transform: 'translate(-50%, -50%) scale(1.5)' // Transform to this state
	})
)
```