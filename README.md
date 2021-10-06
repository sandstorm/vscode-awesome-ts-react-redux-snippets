> DEPRECATED! This hasn't been state of the art for some years now. Use functional components and hooks instead.

# Type safe React & Redux Snippets in TypeScript
[![VSCode Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/Sandstorm.vscode-awesome-ts-react-redux-snippets.svg?label=VSCode%20Marketplace&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=Sandstorm.vscode-awesome-ts-react-redux-snippets)

Opinionated snippets with best practices we use at Sandstorm.

> This extension complements our [Kickstart guide](https://sandstorm.github.io/typescript-react-app-kickstart-guide/) for React-Redux-Apps written in TypeScript. We highly recommend to check it out!

## Snippets

Below is a list of all available snippets and the triggers of each one. The **`→`** means the `TAB` key.

| Trigger  | Content |
| -------: | ------- |
| `component→` | `Type safe PureComponent` |
| `story→`| `Type safe story for Storybook` |
| `test→`| `Type safe component test` |
| `container→` | `Type safe container component` |
| `store→` | `Type safe Redux store` |

## Example (Component with defaultProps)

> Look, ma! Intellisense!

![Component with defaultProps](images/Component&defaultProps.gif)

## Requirements

These snippets expect the usual package to be installed (e.g. `react`, `redux`, ect.). 
One of them is `@sandstormmedia/react-redux-ts-utils` wich is a little library that provides some useful types and utilities (available on [npm](https://www.npmjs.com/package/@sandstormmedia/react-redux-ts-utils)). You can of course change the relevant code.

These snippets may only make sense if used in the opinionated dev environment described in our [Kickstart guide](https://sandstorm.github.io/typescript-react-app-kickstart-guide/).

## License
MIT
