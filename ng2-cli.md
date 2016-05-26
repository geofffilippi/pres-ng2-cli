## Geoff Filippi

### Application Architect

---

# [Oildex](www.oildex.com)

A cloud service company for oil and gas

* 1 year

---

Formerly:

# [Time Warner Cable](www.timewarnercable.com)

(now Charter)

* 12 years

---

## Experience

<i class="fa fa-phone"></i>

* Worked on streaming media (Voice over IP), 6 years
* 5 million phone customers

---

## Experience

<i class="fa fa-video-camera"></i>

* Worked on video and streaming video, 4 years

---

## Projects

[twctv.com](twctv.com)

* Video streaming website
 * backbone.js
* Video streaming Set-Top Box (STB) web application

---

## Oildex Projects

* Rewrite 10+-year-old apps
* Angular 1.5
 * Component Router
 * ES5
* Angular 2 Prototype
 * Typescript
* Some ES6 in tests

---

---

# We will cover

* `angular-cli`
* Code Walkthrough
* Tools

---

---

## `angular-cli`

---

### [`angular-cli`](https://github.com/angular/angular-cli)

* Based on `ember-cli`
* beta

---

### Angular 2 code generator

 * Applications
 * Components
 * Directives
 * Pipes
 * Services
 * Routes
 * Unit Tests
 * Protractor Tests

---

### Angular 2 Tools

 * Build
 * Unit Tests
 * Protractor Tests
 * Deployment
 * Lint
  * Style Guide Checker
 * Type Definitions
 * Code Formatter
 * CSS Preprocessors

---

### Install

<pre><code data-trim contenteditable class=bash>
npm install -g angular-cli
</pre></code>

---

## Help

<pre><code data-trim contenteditable class=bash>
ng --help
</pre></code>

---

## Generate New App

<pre><code data-trim contenteditable class=bash>
ng new PROJECT_NAME
cd PROJECT_NAME
</pre></code>

---

## Serve

<pre><code data-trim contenteditable class=bash>
ng serve
</pre></code>

---

---

# Code Walkthrough

---

### Application

<pre><code data-trim contenteditable class="no-highlight">
./src/app/
         /angular2-kickstart.component.css
         /angular2-kickstart.component.html
         /angular2-kickstart.component.spec.ts
         /angular2-kickstart.component.ts
         /environment.ts
         /index.ts
         /shared/
                /index.ts
</pre></code>

---

### Bootstrapping

<pre><code data-trim contenteditable class="no-highlight">
./src/index.html
     /main.ts
</pre></code>

---

### Config

<pre><code data-trim contenteditable class="no-highlight">
./angular-cli.json
./package.json
./tslint.json
./typings.json
./config/
</pre></code>

---

## `index.html`

### Base

<pre><code data-trim contenteditable class=html>
<base href="/">
</code></pre>

---

## `index.html`

### Root Component

<pre><code data-trim contenteditable class=html>
<angular2-kickstart-app>Loading...</angular2-kickstart-app>
</code></pre>

---

## `index.html`

### System Loader

<pre><code data-trim contenteditable class=javascript>
System.import('system-config.js').then(function () {
  System.import('main');
}).catch(console.error.bind(console));
</code></pre>

---

## Bootstraping

`/src/main.ts`

<pre><code data-trim contenteditable class=typescript>
import { bootstrap } from '@angular/platform-browser-dynamic';
import { enableProdMode } from '@angular/core';
import { Angular2KickstartAppComponent, environment } from './app/';

if (environment.production) {
  enableProdMode();
}

bootstrap(Angular2KickstartAppComponent);
</code></pre>

---

## Root Component

`src/app/angular2-kickstart.component.ts`

<pre><code data-trim contenteditable class=typescript>
import { Component } from '@angular/core';

@Component({
  moduleId: module.id,
  selector: 'angular2-kickstart-app',
  templateUrl: 'angular2-kickstart.component.html',
  styleUrls: ['angular2-kickstart.component.css']
})
export class Angular2KickstartAppComponent {
  title = 'angular2-kickstart works!';
}
</code></pre>

---

---

# Tools

---

## Tools

* Build
* Unit Tests
* Protractor Tests
* Lint
  * Style Guide Checker
* Type Definitions
* CSS Preprocessors
* Deployment

---

## Build

```
ng build
```

---

## Unit Tests

```
ng test
```
---

## Protractor Tests

```
ng e2e
```
---

## Lint and Style Guide Checker

```
ng lint
```
---

## Generate Another Component

```
ng generate component my-new-component
```
---

## Hook Up Component

* `import` into root component
* Put a selector in the root template
* Add to root component's `directive` array

---

## Generate A Service

```
ng generate service my-new-service
```
---

## Generate A Route

```
ng generate route first-route
```
---
---

# Questions?
