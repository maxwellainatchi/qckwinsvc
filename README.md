# ![logo](asset/logo/32.png) Quick Windows Service

[![dependencies](https://david-dm.org/maxwellainatchi/qckwinsvc.png)](https://david-dm.org/maxwellainatchi/qckwinsvc)
[![devDependencies](https://david-dm.org/maxwellainatchi/qckwinsvc/dev-status.png)](https://david-dm.org/maxwellainatchi/qckwinsvc#info=devDependencies)

CLI utility that installs/uninstalls a windows service.

This is a wrapper around [node-windows](https://github.com/coreybutler/node-windows).

## Installing your service

### Interactively

```
> qckwinsvc
prompt: Service name: Hello
prompt: Service description: Greets the world
prompt: Node script path: C:\my\folder\hello.js
prompt: Should the service get started immediately? (y/n): y
Service installed.
Service started.
```

### Non-interactively

```
> qckwinsvc --name "Hello" --description "Greets the world" --script "C:\my\folder\hello.js" --startImmediately
Service installed.
Service started.
```

## Uninstalling your service

### Interactively

```
> qckwinsvc --uninstall
prompt: Service name: Hello
prompt: Node script path: C:\my\folder\hello.js
Service stopped.
Service uninstalled.
```

### Non-interactively

```
> qckwinsvc --uninstall --name "Hello" --script "C:\my\folder\hello.js"
Service stopped.
Service uninstalled.
```
