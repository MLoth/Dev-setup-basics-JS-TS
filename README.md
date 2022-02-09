Pull requests are welcome.

# Dev setup basics

Some guidelines to start working with JavaScript based tools. This should help you to set up your environment.

## Node

An asynchronous event-driven JavaScript runtime. Allows you to run JS.

## NVM - Node version manager

Allows you to easy switch between different versions of Node.js.

**TODO:** Go to the [nvm repo](https://github.com/nvm-sh/nvm). Install the tools _(only for unix, macOS & Windows WSL)_.

I'd recommend the use of WSL on Windows. **Make sure you use a WSL-terminal inside VS Code!**

## Prettier

Allows you to automatically format files for consistency across developers in development-teams.

See [default config file](/.prettierrc). This is a config that works best in my opinion. The main reasons are: 1. as little git differences as possible and 2. some generic conventions.

**TODO:**

1. Install the prettier extension.
2. Check how prettier looks for a config (it is best to use a `.prettierrc` file in the root).

### Troubleshooting:

- Prettier might not work at first:
  1. Hit `ctrl + shift + p` or `⌘ + shift + p`
  2. Choose `Format Document`
  3. Choose Prettier as default formatter.

## ESLint

Linting vs formatting: Prettier will format the docuement, ESLint will lint it. Formatting only makes the code consistent with indentation, tabs, spaces, etc. Linting will interpret the code and make sure it is correct; correct use of let, const, etc.

**TODO:** Make sure ESLint & Prettier are not conflicting! [ESLint config for Prettier](https://github.com/prettier/eslint-config-prettier#installation) tries to resolve these conflicts.

## VS Code extensions

Some useful VS code extensions. Your workflow might differ.

- [ES Lint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Import Cost](https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost) see the impact of the bundle you are importing.
- [Prettier Code Formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
