# experiment

An experimental re-working of Aurelia, oriented around compile-time reflection and code generation.

## Compiler

* [ ] View Precompilation:
  * [x] One Way Bindings
  * [x] Two Way Bindings
  * [x] From View Bindings
  * [x] Listener Bindings
  * [ ] Ref Bindings
  * [ ] Template Controllers
* [ ] AST
  * [x] Centralized AST Registry
  * [ ] Getter / Setter Methods
* [ ] Components
  * [x] Link view / view model
  * [ ] Single File Component
  * [ ] Lifecycle Optimization
  * [x] <import from="..." />

## Runtime

* Core
  * [x] PAL
  * [x] Logging
  * [x] Task Queue
  * [ ] Dependency Injection
* Binding
  * [x] One Way
  * [x] Two Way 
  * [x] One Time
  * [x] From View
  * [x] Trigger
  * [x] Delegate
  * [x] Capture
  * [x] Call
  * [x] Ref
  * [x] Style
  * [x] Text
* Custom Elements
  * [x] Properties
  * [x] Binding
  * [x] Bind Lifecycle
  * [x] Attach Lifecycle
  * [x] Fixed Views
  * [x] Per-instance Views
  * [x] No View
  * [x] Containerless
  * [x] Content Projection
  * [ ] Template Part Replacement
  * [ ] CSS Modules
  * [ ] `compose` Custom Element
* Custom Attributes
  * [x] Binding
  * [x] Bind Lifecycle
  * [x] Attach Lifecycle
* Template Controllers
  * [x] Binding
  * [x] Bind Lifecycle
  * [x] Attach Lifecycle
  * [x] View Factories
  * [x] View Slots
  * [x] Plain Views
  * [x] Linking
    * e.g. if/else and switch/case scenarios
  * [x] `if` Template Controller
  * [x] `else` Template Controller
  * [ ] `repeat` Template Controller
* Application Startup
  * [x] SPA Startup
  * [ ] Progressive Enhancement

## Building & Testing the Compiler

This project has a temporary dependency on `aurelia-path` and `aurelia-dependency-injection`. Those need to be manually `npm install`ed first.

* Build compiler

```shell
npm run build
```

* Test compiler

```shell
npm run test
```

* Build then test

```shell
npm run start
```

## Running the sample App

```shell
au run [--watch]
```

## Running the unit tests

* Single run

```shell
npm run karma
```

* Watch mode

```shell
npm run karma-watch
```

### Debugging the unit tests from VS Code:


```shell
npm run karma-debug
```

- When karma is running, press the `DEBUG` button in the browser (will open a new tab);
- In VS Code start the debugger `Attach Karma Chrome`
- When prompted to select which tab, select `DEBUG`
- In VS Code, set a breakpoint in a `.ts` source file (src or test)
- `ctrl+s` / save to trigger a recompile (works even if there are no changes)
- Refresh the chrome `DEBUG` tab
- Your breakpoint should now be hit

By default no coverage is generated in debug mode.


### Custom options (defaults are shown)

```shell
npm run karma -- --transpile-only=true --no-info=true --coverage=true --tsconfig=tsconfig-karma.json
```

For all standard karma options, see `karma start --help`

Installed browser plugins: `Chrome,ChromeHeadless,Firefox,InternetExplorer`

To see the generated test coverage, open `coverage/index.html` in a browser.
