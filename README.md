# Type safe React & Redux Snippets in TypeScript

Opinionated snippets with best practises we use at Sandstorm.

## Features

Fully Typed:
- Redux store
    - state
    - actions
    - reducers
    - selectors
    - epics
- React component
    - props
    - defaultProps
    - state
    - defaultState
    - test
    - storybook
- React Redux container
    - mapStateToProps
    - mapDispatchToProps

## Example (Component with defaultProps)

> Look, ma! Intellisense!

![Component with defaultProps](images/Component&defaultProps.gif)

## Requirements

**Important:** We use a type definition for picking default props that doesn't come with react's typings.
You'll either have to include this declaration somewhere in your code base or define your default props in another way. If you finde a better, more elegant or just cooler way to type defaultProps, let us know :)

> Put this somewhere in your code base (e.g. `/types/defaultProps.d.ts`)
```ts
// Type definition for React component's defaultProps
// TypeScript Version: 3.0

export type PickDefaultProps<Props, defaultPropsKeys extends keyof Props> = Readonly<Required<{
  [P in defaultPropsKeys]: Props[P]
}>>;
```

## Known Issues

* Redux-Saga does not work with `'@@martin_hotell/rex-tils'`'s action creator. But you can make it work though.

## Release Notes

Users appreciate release notes as you update your extension.

### 1.0.0

Initial release
