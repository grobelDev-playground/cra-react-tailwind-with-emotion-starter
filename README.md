## Explanation

This project shows how you can use: <br />
Create-React-App (CRA) combined with Emotion + Tailwind CSS.

## 1. Installation

1.1: Create React App in the chosen directory. <br />
`npx create-react-app MY_PROJECT_NAME`

1.2: cd into the directory and execute these commands.

```
npm i @emotion/styled @emotion/core && npm install tailwindcss && npm install --save-dev tailwind.macro@next && npm install eslint-plugin-react-hooks --save-dev && npm audit fix

```

## 2. Create a file named 'babel-plugin-macros.config.js' at root (where the package.json is).

Put this code inside it: <br />

```
module.exports = {
  tailwind: {
    styled: "@emotion/styled"
  }
};
```

## 3. Done! Try using this App.js code to test installation.

```
import React from "react";

import tw from "tailwind.macro";
import styled from "@emotion/styled";

// Style 1: Only requires the tw import.
const Paragraph = tw.p`flex justify-center text-white items-center bg-gray-500`;

// Style 2: Requires both the styled and tw imports.
const Button = styled.button`
  ${tw`bg-blue-300 hover:bg-blue-700 text-white p-2 rounded`};
`;

function App() {
  return (
    <div className="App">
      <Paragraph>Hello CRA-Tailwind-StyledComponents!</Paragraph>
      <Button>Hover Button</Button>
    </div>
  );
}

export default App;
```

<br />

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `yarn build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
