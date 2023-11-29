# How to listen events by Renderer2

## 1. Inject Renderer2 in a component

Use inject method
``` TypeScript
private readonly renderer: Renderer2 = inject(Renderer2);
```
## 2. Listen to DOM event

Use listen() method: 
``` TypeScript
this.renderer.listen(HTMLElement, 'DOM event', functionToExecute)
```