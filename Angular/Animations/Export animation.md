# How to export animation
## 1. Define an exportable animation class (AnimationMetadata)
``` TypeScript
export const animations = {
  animationOne: trigger('animationOne', [
      // Cool animationOne code
    ]),
  animationTwo: trigger('animationTwo', [
      // Cool animationTwo code
    ]),
  animationThree: trigger('animationThree', [
      // Cool animationThree code
    ])
}
```
## 2. Import animation in Component
``` TypeScript
@Component({
  // Component stuff
  animations: [
    animations.animationOne,
    animations.animationTwo,
    animations.animationThree
  ]
})
export class Component {
	// Another component stuff
}
```
## 3. Apply animation in Component template
``` HTML
<element [@animationOne]="animationOneStatus">
	// Some text
</element>
<element [@animationTwo]="animationTwoStatus">
	// Some text
</element>
<element [@animationThree]="animationThreeStatus">
	// Some text
</element>
```