# How to make a parent and a child components communicate

## Input

### 1. Set the input in a child's component file:

Use @Input decorator:
``` TypeScript
@Input() variable: type = 'default value'
```

The set function is also available for use:
``` TypeScript
@Input()
  set setFunction (value: string) {
	  if (value === 'good') {
		  // Execute some code
	  }
  }
```
### 2. Use the input in a parent's template:

Use variable-named attribute in HTML with [data binding]:
``` HTML
<child-element
	[variable]="'another string value'"
>
	<!-- Some text -->
</child-element>
```

The usage of a set function is similar to that of a regular variable:
``` HTML
<child-element
	[setFunction]="'good'"
>
	<!-- Some text -->
</child-element>
```

## Output

### 1. Set the output in a child's component

Use @Output decorator and create an event emitter: 
``` TypeScript
@Output() event: EventEmitter<string> = new EventEmitter<string>();
```

### 2. Trigger the event in a child's component

Use event.emit() function:
``` TypeScript
event.emit('some string value')
```

### 3. Catch the child's output in a parent's template:

Use event-named attribute in HTML with (event binding):
``` TypeScript
<child-element
	(event)="foo($event)"
>
	<!-- Some text -->
</child-element>
```

## Two-way binding
### 1. In child Component create Input() and Output()
``` TypeScript
@Input()
set getFromParent(value: any) {
	// Some code and value confirmation
	this.sendToParent.emit(valueConfirmed)
	// Some code
}

@Output()
sendToParent: EventEmitter<any> = new EventEmitter<any>();
```
### 2. In parent Component receive, modify and send the value
``` TypeScript
// Recieve
recievedValue: any;
recieveValue(value) {
	this.recievedValue = value;
}

// Modify
changeValue() {
	this.sendValue = this.recievedValue;
	// Some code to change sendValue
}

// Send
sendValue: any;
```
###  3. In parent Template bind to the received value
``` HTML
<element (click)=changeValue() [class]=recievedValue>
  // Some text
</element>
```