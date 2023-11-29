# How to define routing paths

In routing module create variable before @NgModule decorator:
``` TypeScript
import { Component } from 'path to component.ts';

const routes: Routes = [
	{ path: 'pathName', component: Component },
];
```