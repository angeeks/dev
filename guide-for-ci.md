# Guide for CI setup

## Dependenices

- `direnv`
- `rbenv`
  - `travis`
- `nvm`
  - `@angular/cli`
- `git`
  - `hub`

## Commands

- new_lib [lib name]

## Explains

### step 1 - init

```
npx ng new [project-name]
```

- Github: create a repo
- [Travis](https://travis-ci.org/)
  - (sync, then) link repo
  - config & add tokens
- repo
  - update readme/contributing
  - add/update travis.yml
  - `npm i -D puppeteer @angeeks/{testing,gh-layout,globals,gtags} hoek@4.2.1`
  - setup karma with `ChromeHeadless` with `puppeteer`
  - lint/test/build
  - commit & push

### step 2 - release

```
npx ng g library @angeeks/[lib]
```

- repo
  - update project/package.json
  - update apis
  - lint/test/build
  - commit & push
- git
  - g checkout branch release
  - update .travis.yml
  - push

- check package published

