# How to create and apply an observable for DOM Events

Important clarifications: Unlike Renderer2, observables can handle touch events
## 1. Declare the observable object for event

In constructor or onInit)():
``` TypeScript
let observable$: Observable<EventType> = fromEvent(element, 'event');
```

## 2. Subscribe on the observable and use the data

In constructor or onInit)():
``` TypeScript
observable$.subscribe( (event) => {
	// Some code
}
```
## 3. Unsubscribe when it's job is done
Don't forget to unsubscribe.
It's possible to use array and while cycle:
``` TypeScript
let activeOvservers: Subscription[] = [];              // - Declare an array

activeOvservers.push(observer$.subscribe( (value) => { // - Push observable 
   // Some code                                        //   to an array
}
													  
while (activeMouseObservers.length > 0) {              // - Unsubscribe from all
  activeMouseObservers[0].unsubscribe();               //   the observables in
  activeMouseObservers.shift()                         //   the array
}
```
