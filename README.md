# EmailBot

A historical 2016 Microsoft Bot Framework experiment, retained as reference.
There is no verified supported runtime or account-connected operating baseline.
Repository age alone is not a claim that the code is broken or vulnerable.

## Inspect safely

- `app.js` contains the application; `package.json`'s `main` field points to
  `index.js`, which is not present. Do not treat it as a working package entry point.
- `package.json` declares Bot Builder 0.6 and Restify 4 era dependencies.
  `node_modules/` is tracked historical content, not a reproducible clean install.
- `npm test` deliberately exits with an error placeholder. There is no automated
  behavioral test suite or root dependency lockfile.
- Review source without launching the bot or supplying account credentials.
  Do not run the vendored dependencies against real email or bot accounts.

## Before any revival

Confirm the intended bot behavior and account owner, choose a supported runtime
and SDK, replace vendored dependencies with a reviewed manifest and lockfile,
correct the entry point, and add mocked message-processing tests. Establish a
local-only smoke test before requesting a separate account-connected trial.
No account connection or dependency modernization is part of this handoff.
