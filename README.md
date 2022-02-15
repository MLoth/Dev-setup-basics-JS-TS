**Pull requests are welcome: anything that helps to create a good environment for JS-development.**

# Dev setup basics

Some guidelines to start working with JavaScript based tools. This should help you to set up your environment.

## Node

An asynchronous event-driven JavaScript runtime. Allows you to run JS.

## NPM / Yarn

With npm or yarn, we can install node-packages.
Differences are minor - I mostly use npm at the moment (yarn is very similar, but not documented here). Some useful notes on frequently used commands and terms:

- `npm i` (same as `npm install`): installs all the packages from the package.json file.
- There are two types of packages:
  1. Packages for during development.
     Install packages for development use with `-D` or also `--save-dev` -> `npm i -D a-package`.
  2. Packages that are used in the app are installed with `npm i`.
     Be consistent with this difference. This is mostly documented.
- The folder `/node_modules`: contains all the installed packages. **Should always be git-ignored!** Always feel free to delete this folder; `npm i` will get the folder back.
- NPM is installed along Node.js. So it is also linked to the current node.js version.

## NVM - Node version manager

Allows you to easy switch between different versions of Node.js.

**TODO:** Go to the [nvm repo](https://github.com/nvm-sh/nvm). Install the tools _(only for unix, macOS & Windows WSL)_.

I'd recommend the use of WSL on Windows. **Make sure you use a WSL-terminal inside VS Code!**

When a `.nvmrc`-file is present, nvm will find the correct node-version for the current project. This will work with the command: `nvm use`.

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

_There is also an alternative. [Editorconfig](https://editorconfig.org) has a very similar approach and fuctionality. I never really liked it as much as Prettier however... When working with a different programming language, this could be your best option, eg. Python._

## ESLint

Linting vs formatting: Prettier will format the document, ESLint will lint it. Formatting only makes the code consistent with indentation, tabs, spaces, etc. Linting will interpret the code and make sure it is correct; correct use of let, const, etc.

**TODO:** Make sure ESLint & Prettier are not conflicting! [ESLint config for Prettier](https://github.com/prettier/eslint-config-prettier#installation) tries to resolve these conflicts.

I always start looking at the docs for my specific needs on the technology I'm working on at the moment.

## VS Code extensions

Some useful VS code extensions. Your workflow might differ.

### Recommended

- [ES Lint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier Code Formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Import Cost](https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost) see the impact of the bundles / modules you are importing.

### Optional

- [Non breaking space highlighter](https://marketplace.visualstudio.com/items?itemName=viktorzetterstrom.non-breaking-space-highlighter) On macOS you might accidentaly typ a space with `option + space`. This shows that _hidden_ error.
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) Check Git.
- [File Utils](https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils)
- [BundlePhobia](https://marketplace.visualstudio.com/items?itemName=crewsycrews.bundlephobia-support) Quickly check the size of a npm-package.

## Git

A good way of working with .git can be gitflow.
Use 1. [Gitkraken](https://www.gitkraken.com) (you have a student license by using your Howest email address) or 2. [Fork](https://git-fork.com), for an easier approach.
