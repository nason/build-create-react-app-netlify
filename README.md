build-create-react-app-netlify
===========

A utility to help make Netlify build variables available to `create-react-app` builds, without ejecting.

More information and context around this tool can be found here: https://medium.com/@nasonosan/free-robust-and-collaborative-create-react-app-deployments-on-netlify-59a3f5feda9e

To use:

```
yarn add build-create-react-app-netlify
```

Add a new script to your `package.json`:

```
{
  ...,
  "scripts": {
    "build-netlify": "build-create-react-app-netlify"
  }
}
```

And then configure your Netlify project to run `yarn build-netlify` instead of `yarn build`.

### Running Tests

This script can also run your `create-react-app` project's tests before running the build. Pass the `--withTests` flag to enable this behavior, for example:

```
{
  ...,
  "scripts": {
    "build-netlify": "build-create-react-app-netlify --withTests"
  }
}
```


