# core.loader.imports

loads 3rd party modules from plugin definition

```js
let core = new require('core.constructor')();
 
core.plugin(
    require('core.loader.imports')
);

// plugins can now declare actions on the plugin definition object:
core.plugin({
    name: 'test',
    imports: {
        React: require('react')
    }
});

// exists on core.imports
core.imports.React;

// can be required
core.require(['imports.React'], (React) => { ... })
```
