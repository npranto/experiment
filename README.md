# experiment
An experimental static site project for use

## Adding `Commitizen` to a project
- run `npm install -g commitizen` to install the package globally onto your machine
- run `commitizen init cz-conventional-changelog --save-dev --save-exact` to initialize your project to use the cz-conventional-changelog
- adds the config.commitizen key to the root of your package.json as shown here:
```
"config": {
  "commitizen": {
    "path": "cz-conventional-changelog"
  }
}
```