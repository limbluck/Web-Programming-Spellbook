# Subjects in RxJs
Every Subject is an Observable with the methods `next(v)`, `error(e)`, and `complete()`.
```TypeScript
const subject = new [Subject];

subject.subscribe({
next: (v) => console.log(`observerA: ${v}`),
});
subject.subscribe({
next: (v) => console.log(`observerB: ${v}`),
});

subject.next(1);
subject.next(2);
```
