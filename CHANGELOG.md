# Change Log
All notable changes to the "vscode-awesome-ts-react-redux-snippets" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [2.1.1] - 2019-03-18
- Bugfix:
    - use comma instead of semi-colon in type definitions

## [2.1.0] - 2019-03-15
- Use synthetic default exports, e.g.:
    ```ts
    import * as React from 'react';
    ```
    to
    ```ts
    import React from 'react';
    ```
- Use `type` rather than `interface` when applicable
- Slightly update `test` snippet

## [2.0.0] - 2019-03-01
- **breaking:** now using `@sandstormmedia/react-redux-ts-utils` instead of `@martin_hotell/rex-tils`
- removed `readonly` keywords in `interface` definitions
- added newlines at the end of snippet
- some code style enhancements

## [1.0.1..5] - 2018-09-24
### Added
- fixed typos
- improved clarity in Readme
- license file

## [1.0.0] - 2018-09-23
- Initial release