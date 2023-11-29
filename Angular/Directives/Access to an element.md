# How to access an HTML element to which a directive is applied

Define a variable to reference an ElementRef type in constructor:
``` TypeScript
@Directive({
  selector: '[appDirective]'
})
export class Directive {
  constructor (host: ElementRef) { }
```

Important note: This will work different with structural directives, because constructor will get an ng-template element without the view 
(see [[Angular/Directives/About directives#About directives#What is structural directives|About directives]])