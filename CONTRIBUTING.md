# Contributing to Himpun

Thanks for your interest! Bug reports, feature ideas, and pull requests are welcome.

## Before you start

- Check the [open issues](https://github.com/MrPrinceAli/himpun/issues) so we don't duplicate work.
- For anything bigger than a small fix, open an issue first so the approach can be agreed on.

## Setting up

Follow [Running locally](README.md#running-locally) in the README. In short:

```bash
npm run install:all
npm run node          # terminal 1: local blockchain
npm run deploy:local  # terminal 2: deploy the contracts
npm run dev           # frontend at http://localhost:4000
```

## Before opening a pull request

Run the same checks as CI:

```bash
npm test          # contract + frontend tests
npm run lint
npm run build
npm run format    # Prettier, including Solidity
```

- After changing a contract, run `npm --prefix smart-contract run compile` so the ABI and rule constants in `frontend/lib/abi/` are refreshed.
- Keep pull requests focused: one change per PR.
- Describe **what** changed and **why** in the PR description.
- User-facing text must be available in both Indonesian and English (`frontend/lib/i18n/`).

## Commit messages

Short imperative summaries, in Indonesian or English, e.g. `Tambah filter provinsi` or `Add province filter`.
