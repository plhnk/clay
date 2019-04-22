---
title: "Importing the JS Component"
weight: 3
---

Clay is available as the `clay` package in [npm](https://www.npmjs.com/). The components are packaged as Component/Metal.js classes that provide a high fidelity component. You can import the Clay components in several ways depending on your Stack.

## Installation from NPM

You can import the entire library of Clay components at once in your application, or you can import them individually as you need them.

* All components - `clay` package on npm.
* Separate components - `clay-` packages on npm.

**All components**

> Using [npm](https://www.npmjs.com/):

```bash
npm install clay --save
```

> Or [yarn](https://yarnpkg.com/lang/en/):

```bash
yarn add clay
```

**Separate components**

> Using [npm](https://www.npmjs.com/):

```bash
npm install clay-badge --save
```

> Or [yarn](https://yarnpkg.com/lang/en/):

```bash
yarn add clay-badge
```

## ES2015

```javascript
import {ClayBadge, ClayButton} from 'clay';
```

## Manual Instantiation

You can render a Clay component on whatever element you want if you are not using a framework.

```html
<div id="my-element"></div>
```

Import the component in your application and manually instantiate the component by passing the required properties and the `id` of the element.

```javascript
import ClayBadge from 'clay-badge';

const badge = new ClayBadge(
    {
        label: 'My Badge'
    }, 
    '#my-element'
);
```

## CDN

Once added to your page, the Clay components are accessible globally on the page with all components.

> See [Introduction](/docs/get-started/introduction.html).

```html
<div id="element"></div>

<script type="text/javascript">
    var clayButton = new clay.ClayButton(
        {
            label: 'My Button'
        }, 
        '#element'
    );
</script>
```

## Using Clay in soy and jsx

For more information see the [advanced guides](/docs/get-started/using-js-components-with-metal.html).
