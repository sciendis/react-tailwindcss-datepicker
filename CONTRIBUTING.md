# Contributing

Thanks for your interest in contributing to `react-tailwindcss-datepicker`! Please take a moment to
review this document **before submitting a pull request**.

-   [Installation](#installation)
-   [Coding standards](#coding-standards)
-   [Running playground](#running-playgrounds)
-   [Before you make a Pull Request](#before-you-make-a-pull-request)
-   [Publish the updated Datepicker](#publish-the-updated-datepicker)

## Installation

You only require a `npm install` in the root directory to install everything you need.

```sh
npm install
```

## Coding standards

We use `prettier` for making sure that the codebase is formatted consistently. To automatically fix
any style violations in your code, you can run:

```sh
npm pret:fix
```

## Running playground

We currently use `next.js` as server for live testing.

You can run the `dev` script and open your browser to `http://localhost:8888`.

See complete `props` usage in `pages/index.js` file.

```sh
npm dev
```

## Before you make a Pull Request

We recommend to run these scripts in sequence before you make your commit message amd open a Pull
Request

**Let's clean the code first**

```sh
npm pret:fix
```

**Test a build of your changes**

```sh
npm build

```

**Add a changeset**

Everytime you make a change you should add a changeset. Changesets hold two key bits of information:
a version type (following semver), and change information to be added to a changelog. For details,
check out the
[documentation](https://github.com/changesets/changesets/blob/main/docs/intro-to-using-changesets.md)

```sh
npx changeset
```

Follow the prompts to document your changes.

**Commit your changes**

It is generally advised to create a feature branch for your changes and open a merge request.

Create a commit, preferrably using [Commitizen](https://commitizen-tools.github.io/commitizen/).

```sh
git cz commit
git push
```

# Publish the updated Datepicker

**Update npm package**

To release a new version use

```sh
npx changeset version
```

This consumes all changesets, and updates to the most appropriate semver version based on those
changesets. It also writes changelog entries for each consumed changeset.

Make sure to review all changes. Once you are confident that these are correct, and have made any
necessary tweaks to changelogs, you can publish your packages:

```sh
npx changeset publish
```

**Update github repo**

Make sure to also commit und push the updated package and changelogs to github.

```sh
git commit -m <message>
git push
```

Add a tag with the latest version number to mark a new release. The tag name should reflect the
updated version property in the `package.json` file.

```sh
git tag <tagname>

```

Note that tags are not automatically pushed. You will have to explicitly push tags to a shared
server after you have created them.

```sh
git push origin <tagname>
```
