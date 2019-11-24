
Coin Electron App
===================

Prerequisites
-------------

Make sure you back up your  `wallet.dat` before developing on this app.

You need the following prerequisites to be able to build and develop the project
on your local machine.

- Node.js
- npm

Install
-------


Change directory into the cloned repository:

Install dependencies with npm:

```sh
npm install
```

Place `Coind` and `Coin-cli` binaries in a `bin` directory in the the root
of your repo:

```sh
mkdir bin

```

Development
-----------

Run in development mode:

```sh
npm run dev
```

Before submitting a patch we highly recommend running the linting and formatting
scripts:

```sh
npm run lint-fix && npm run lint-styles-fix
```

Package for Distribution
------------------------


```sh
npm run package
```

After running the package command the executable will be located in the
`release` folder.

Code Signing
------------

To code sign the packaged app you must set the following environment variables
before running `npm run package`.

macOS:

```sh
# macOS - Name of certificate to retrieve from Keychain
export CSC_NAME='Coin Limited'
```

Windows:

```sh
# Windows (PowerShell) - Path to *.pfx certificate relative to root of project
$env:CSC_LINK='build\Coin.pfx'

# Optional - The password to decrypt the certificate given in CSC_LINK
$env:CSC_KEY_PASSWORD='Password123!'
```

Contributing
------------

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of
conduct, and the process for submitting pull requests to us.

License
-------

Licensed under the [MIT](LICENSE.md) License.
