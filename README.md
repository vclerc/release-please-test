# Monorepo sandbox

This projects allows experimentation with monorepo architecture and workflows without embarking heavy code.

## Architecture

The current architecture is naive, having to main components (back and front) being separated from one another.
To reflect different possible configuration, not all packages.json have version (denoted with `*` below)
````
| back
|  | - packages
|  |       | - lib
|  |       |    | lib-1
|  |       |    |   | - package.json *
|  |       |    | lib-2
|  |       |    |   | - package.json *
|  |       |    | lib-2
|  |       |    |   | - package.json *
|  |       | - service
|  |       |      | - service-1
|  |       |      |       | - package.json *
|  |       |      | - service-2
|  |       |      |       | - package.json *
|  |       | - package.json
|  | - package.json
| front
|  | - packages
|  |       | - front-1
|  |       |      | - package.json
|  |       | - front-2
|  |       |      | - package.json
|  |       | - front-3
|  |       |      | - package.json
|  |       | - package.json *
````