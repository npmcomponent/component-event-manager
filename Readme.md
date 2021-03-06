*This repository is a mirror of the [component](http://component.io) module [component/event-manager](http://github.com/component/event-manager). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-event-manager`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# EventManager

  __DEPRECATED__: this module is no longer recommended, [component/events](https://github.com/component/events)
  now supports this functionality directly.

  Higher level event management designed to facilitate fluent
  domain-specific event subscriptions.

  For example [component/events](https://github.com/component/events)
  uses `EventManager` to provide fluent dom node event subsciptions,
  while [component/delegates](https://github.com/component/delegates)
  does the same, however for delegated events.

## Installation

    $ component install component/event-manager

## API

  - [EventManager()](#eventmanager)
  - [EventManager.onbind()](#eventmanageronbindfnfunction)
  - [EventManager.onunbind()](#eventmanageronunbindfnfunction)
  - [EventManager.bind()](#eventmanagerbindeventstringmethodstring)
  - [EventManager.unbind()](#eventmanagerunbindeventstringmethodstring)

## EventManager()

  Initialize an `EventManager` with the given
  `target` object which events will be bound to,
  and the `obj` which will receive method calls.

## EventManager.onbind(fn:Function)

  Register bind function.

## EventManager.onunbind(fn:Function)

  Register unbind function.

## EventManager.bind(event:String, [method]:String)

  Bind to `event` with optional `method` name.
  When `method` is undefined it becomes `event`
  with the "on" prefix.

```js
 events.bind('login') // implies "onlogin"
 events.bind('login', 'onLogin')
```

## EventManager.unbind([event]:String, [method]:String)

  Unbind a single binding, all bindings for `event`,
  or all bindings within the manager.

```js
  evennts.unbind('login', 'onLogin')
  evennts.unbind('login')
  evennts.unbind()
```


## License

  MIT
