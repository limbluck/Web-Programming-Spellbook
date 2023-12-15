# How to use AnimationBuilder
Base structure in TypeScript looks like this:
``` TypeScript
private readonly animationBuilder: AnimationBuilder = inject(AnimationBuilder);

playAnimation() {
	const animation: AnimationPlayer = this.animationBuilder
	.build([
		style({
			// Some styles before
		}),
		animate(`150ms ease`,
			style({
				transform: `translate(${translateValue})` // Implement variable
			})),
		style({
			// Some more styles after
		})
	])
	.create(this.host.nativeElement);
	animation.onDone( () => {
		// Code to apply when animation done
		animation.destroy() // To unlock CSS properties setted by the animation
	})
	animation.play(); // To play the animation
}

```