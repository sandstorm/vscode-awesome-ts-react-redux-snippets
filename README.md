# Type safe React & Redux Snippets in TypeScript

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

These snippets may only make sense if used in the opinionated dev environment described in our [Kickstart guide](https://sandstorm.github.io/typescript-react-app-kickstart-guide/).

>**Important:** We use a type definition for picking default props that doesn't come with react's typings.
>You'll either have to include this declaration somewhere in your code base or define your default props in another way. If you finde a better, more elegant or just cooler way to type defaultProps, let us know :)
>
> Put this somewhere in your code base (e.g. `/types/defaultProps.d.ts`)
```ts
// Type definition for React component's defaultProps
// TypeScript Version: 3.0

export type PickDefaultProps<Props, defaultPropsKeys extends keyof Props> = Readonly<Required<{
  [P in defaultPropsKeys]: Props[P]
}>>;
```

## Known Issues

* Redux-Saga does not work with `'@martin_hotell/rex-tils'`'s action creator. You can fix this by not using Redux-Saga or by unfreezing your actions for Redux-Saga. (https://github.com/Hotell/rex-tils/issues/21)

## License
MIT
