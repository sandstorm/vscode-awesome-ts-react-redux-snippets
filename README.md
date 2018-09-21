# Type safe React & Redux Snippets in TypeScript

This is the README for your extension "vscode-awesome-ts-react-redux-snippets". After writing up a brief description, we recommend including the following sections.

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

// TODO 3 animations (store, component, test)

Describe specific features of your extension including screenshots of your extension in action. Image paths are relative to this README file.

For example if there is an image subfolder under your extension project workspace:

\!\[feature X\]\(images/feature-x.png\)

> Tip: Many popular extensions utilize animations. This is an excellent way to show off your extension! We recommend short, focused animations that are easy to follow.

## Requirements

**Important:** We use a type definition for picking default props that is not part of the react standard.
You'll either have to include this declaration somewhere in your code base or define your default props in another way. If you finde a better, more elegant or just cooler way to type defaultProps, let us know :)

> Put this somewhere in your code base
`defaultProps.d.ts`
```ts
// Type definition for React component's defaultProps
// TypeScript Version: 3.0

export type PickDefaultProps<Props, defaultPropsKeys extends keyof Props> = Readonly<Required<{
  [P in defaultPropsKeys]: Props[P]
}>>;
```

// TODO: show anymation with no default props -> with default props with `const test = () => <Test/>` where test needs a property for wich we then define a default.

## Known Issues

* Declaring defaultProps: At the time of writing the intellisense breaks after the first property key.

// Show animation of broken intellisense

## Release Notes

Users appreciate release notes as you update your extension.

### 1.0.0

Initial release of ...
