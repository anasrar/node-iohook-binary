Temporary solution for installing iohook for electron and node js due to iohook unmaintained prebuild binary for latest Electron and Node.js.

# Version

Current Version : v0.9.3

# Installation

Install iohook

```text
npm install iohook --ignore-scripts
```

Add few lines below to `package.json`

```text
"iohook": {
  "targets": [
    "node-72",
    "electron-85"
  ],
  "platforms": [
    "win32",
    "darwin",
    "linux"
  ],
  "arches": [
    "x64",
    "ia32"
  ]
}
```

Change `node-72` and `electron-85` to fit your version node and electron on your project.

Further information on [https://wilix-team.github.io/iohook/usage.html#electron](https://wilix-team.github.io/iohook/usage.html#electron)

Change few lines in `node_modules/iohook/install.js`

From

```text
  let downloadUrl =
    'https://github.com/wilix-team/iohook/releases/download/v' +
    pkgVersion +
    '/' +
    currentPlatform +
    '.tar.gz';
```

To

```text
  let downloadUrl =
    'https://github.com/anasrar/node-iohook-binary/releases/download/ci' +
    '/' +
    currentPlatform +
    '.tar.gz';
```

Run

```text
node node_modules/iohook/install.js
```

# Support

## Electron

- 4.0.4 (ABI 69)
- 5.X.X (ABI 70)
- 6.X.X (ABI 73)
- 7.X.X (ABI 75)
- 8.X.X (ABI 76)
- 9.X.X (ABI 80)
- 10.X.X (ABI 82)
- 11.X.X (ABI 85)
- 12.X.X (ABI 87)
- 13.X.X (ABI 89)
- 14.X.X (ABI 89)
- 15.X.X (ABI 98)
- 16.X.X (ABI 99)
- 17.X.X (ABI 101)
- 18.X.X (ABI 103)

## Node.js

- 8.9.X (ABI 57)
- 9.2.X (ABI 59)
- 10.X.X (ABI 64)
- 11.X.X (ABI 67)
- 12.X.X (ABI 72)
- 13.X.X (ABI 79)
- 14.X.X (ABI 83)
- 15.X.X (ABI 88)
- 16.X.X (ABI 93)
- 17.X.X (ABI 102)
- 18.X.X (ABI 108)
