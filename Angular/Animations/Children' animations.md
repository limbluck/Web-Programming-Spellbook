# How to make children animations work

Parent's animation always blocks children' ones, but you can call child's animation from parent's one

To do so you can use:
``` TypeScript
query('@childAnimationTrigger', animateChild())
```

To make a parent and a child animate at the same time use:
``` TypeScript
group[
	animate(duration),
	query('@childAnimationTrigger', animateChild())
]
```
Important clarifications: 
- The next animation state will only be activated once all animations of both the child and parent elements in the group have finished