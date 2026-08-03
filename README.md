# React Tailwindcss Datepicker

<p align="center">
    <a href="https://react-tailwindcss-datepicker.vercel.app/" target="_blank">
      <img alt="React Tailwindcss Datepicker" width="100" style="border-radius: 100%;" src="https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/calendar_logo.svg?raw=true">
    </a><br><br>
    A modern date range picker component for React using Tailwind 4 and dayjs. </br>
    Forked from   <a href="https://github.com/onesine/react-tailwindcss-datepicker" target="_blank">React Tailwindcss Datepicker</a>.
</p>

## Contents

-   [Features](#features)
-   [Documentation](#documentation)
-   [Installation](#installation)
-   [Publishing](#publishing)
-   [Simple Usage](#simple-usage)
-   [Theming Options](#theming-options)
-   [Playground](#playground)
-   [Contributing](#contributing)

## Features

-   ✅ Theming options
-   ✅ Dark mode
-   ✅ Single Date
-   ✅ Single date use Range
-   ✅ Shortcuts
-   ✅ TypeScript support
-   ✅ Localization(i18n)
-   ✅ Date formatting
-   ✅ Disable specific dates
-   ✅ Minimum Date and Maximum Date
-   ✅ Custom shortcuts

## Documentation

Go to [full documentation](https://react-tailwindcss-datepicker.vercel.app/)

## Installation

⚠️ React Tailwindcss Datepicker uses Tailwind CSS 4 (with the
[@tailwindcss/forms](https://github.com/tailwindlabs/tailwindcss-forms) plugin) &
[Dayjs](https://day.js.org/en/) under the hood to work.

### Install via npm

```sh
npm install @sciendis/react-tailwindcss-datepicker
```

### Install via yarn

```sh
yarn add @sciendis/react-tailwindcss-datepicker
```

Make sure you have installed the peer dependencies as well with the below versions.

```
"dayjs": "^1.11.6",
"react": "^17.0.2 || ^18.2.0"
```

## Publishing

The GitHub repository is mirrored to
[Sciendis GitLab project 198](https://gitlab.sciendis.eu/Development/react-tailwindcss-datepicker-mirror).
GitLab publishes the package from release tags using `CI_JOB_TOKEN`; no npmjs token is required.

1. Update `version` in `package.json` and add the release notes to `CHANGELOG.md`.
2. Merge the release commit into `main` on GitHub.
3. Create and push a matching tag, for example `v1.8.6` for package version `1.8.6`.
4. Wait for the mirror pipeline to validate, build, inspect, and publish the package.

The pipeline rejects a tag that does not match the package version or a version that already exists
in the GitLab Package Registry. Historical releases through `1.8.5` have already been migrated.

## Simple Usage


### Configure the GitLab Package Registry

The package is published in the Sciendis GitLab Package Registry. Configure the Sciendis group registry in the consuming project's `.npmrc`:

```ini
@sciendis:registry=https://gitlab.sciendis.eu/api/v4/groups/8/-/packages/npm/
//gitlab.sciendis.eu/api/v4/:_authToken=${GITLAB_NPM_TOKEN}
```

Use a GitLab token with `read_package_registry` access. The broad `/api/v4/` authentication path is
required because package metadata may refer to tarballs under the owning project.

#### Tailwindcss Configuration

Add the datepicker to your tailwind configuration using this code

```css
/* in your styles.css */
@import 'tailwindcss';
@source './node_modules/@sciendis/react-tailwindcss-datepicker/dist/index.esm.js';
```

Then use react-tailwindcss-datepicker in your app:

```jsx
import React, { useState } from "react";
import Datepicker from "@sciendis/react-tailwindcss-datepicker";

const App = () => {
    const [value, setValue] = useState({
        startDate: new Date(),
        endDate: new Date().setMonth(11)
    });

    const handleValueChange = newValue => {
        console.log("newValue:", newValue);
        setValue(newValue);
    };

    return (
        <div>
            <Datepicker value={value} onChange={handleValueChange} />
        </div>
    );
};

export default App;
```

## Theming options

**Light Mode**

![Light Mode](https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/Screen_Shot_2022-08-04_at_17.04.09_light.png?raw=true)

**Dark Mode**

![Dark Mode](https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/Screen_Shot_2022-08-04_at_17.04.09_dark.png?raw=true)

**Supported themes**
![Theme supported](https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/Screen_Shot_2022-08-04_at_17.04.09_theme.png?raw=true)

**Teal themes example**
![Theme supported](https://raw.githubusercontent.com/onesine/react-tailwindcss-datepicker/master/assets/img/Screen_Shot_2022-08-04_at_17.04.09_teal.png?raw=true)

You can find the demo at [here](https://react-tailwindcss-datepicker.vercel.app/demo)

> **Info**
>
> 👉 To discover the other possibilities offered by this library, you can consult the
> [full documentation](https://react-tailwindcss-datepicker.vercel.app/).

## PlayGround

Clone the `main` branch and run commands:

```sh
# Using npm
npm install && npm dev

# Using yarn
yarn install && yarn dev

```

Open a browser and navigate to `http://localhost:8888`

## Contributing

See
[CONTRIBUTING.md](https://github.com/sciendis/react-tailwindcss-datepicker/blob/main/CONTRIBUTING.md)

## Official Documentation repo

Onesine's original documentation is still valid for this fork:
[https://github.com/onesine/react-tailwindcss-datepicker-doc](https://github.com/onesine/react-tailwindcss-datepicker-doc)

## Thanks to

-   [React Tailwindcss Datepicker ](https://github.com/onesine/react-tailwindcss-datepicker).
-   [Vue Tailwind Datepicker](https://vue-tailwind-datepicker.com/)
-   [React](https://reactjs.org/)
-   [Tailwind CSS](https://tailwindcss.com/)
-   [dayjs](https://day.js.org/)

I thank you in advance for your contribution to this project.

## License

[MIT](LICENSE) Licensed.
