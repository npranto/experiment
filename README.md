# experiment
An experimental static site project for use

## Adding `Commitizen` to a project
- run `npm install --save-dev commitizen` to install the package as a dev dependency
- run `npx commitizen init cz-conventional-changelog --save-dev --save-exact` to initialize your project to use the cz-conventional-changelog
- add the following script to package.json:
```
"scripts": {
  "commit": "cz"
}
```
- adds the config.commitizen key to the root of your package.json as shown here:
```
"config": {
  "commitizen": {
    "path": "cz-conventional-changelog"
  }
}
```
- now, instead of running `git commit -m "..."`, run `npm run commit` to start creating a detailed commit message through a prompt

### Add `Commitizen` as part of `husky` commit hook
- run `npm install husky --save-dev` to install the package as a dev dependency
- run `npx husky install`
- run `npx husky add .husky/prepare-commit-msg "exec < /dev/tty && node_modules/.bin/cz --hook || true"`
- run `git add .husky/prepare-commit-msg`
- now, whenever you run `git commit`, it would run you through the commitizen prompter