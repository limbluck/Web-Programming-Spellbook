# Component lifecycle event sequence
## `ngOnChanges`
Respond when Angular sets or resets data-bound input properties. The method receives a `[SimpleChanges](https://angular.io/api/core/SimpleChanges)` object of current and previous property values.
Called before `ngOnInit()` (if the component has bound inputs) and whenever one or more data-bound input properties change.
## `ngOnInit()`
Initialize the directive or component after Angular first displays the data-bound properties and sets the directive or component's input properties.
Called once, after the first `ngOnChanges()`. `ngOnInit()` is still called even when `ngOnChanges()` is not (which is the case when there are no template-bound inputs).
## `ngDoCheck()`
Detect and act upon changes that Angular can't or won't detect on its own.
Called immediately after `ngOnChanges()` on every change detection run, and immediately after `ngOnInit()` on the first run.
## `ngAfterContentInit()`
Respond after Angular projects external content into the component's view, or into the view that a directive is in.
Called _once_ after the first `ngDoCheck()`.
## `ngAfterContentChecked()`
Respond after Angular checks the content projected into the directive or component.
Called after `ngAfterContentInit()` and every subsequent `ngDoCheck()`.
## `ngAfterViewInit()`
Respond after Angular initializes the component's views and child views, or the view that contains the directive.
Called _once_ after the first `ngAfterContentChecked()`.
## `ngAfterViewChecked()`
Respond after Angular checks the component's views and child views, or the view that contains the directive.
Called after the `ngAfterViewInit()` and every subsequent `ngAfterContentChecked()`.
## `ngOnDestroy()`
Cleanup just before Angular destroys the directive or component. Unsubscribe Observables and detach event handlers to avoid memory leaks.
Called immediately before Angular destroys the directive or component.