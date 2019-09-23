# TEST STYLELINT

this repo is used to reproduce the issues [#4289](https://github.com/stylelint/stylelint/issues/4289).

## Step

1. open terminal

2. install node_modules

```bash
npm i

# or

yarn
```

3. run scripts

```bash
yarn lint:style
```

will got

```bash
yarn run v1.17.3
$ stylelint '**/*.scss'

index.scss
 10:5  ✖  Expected "display" to come before "color" in group "Box Model"
 13:5  ✖  Expected "overflow" to come before "line-height" in group "Box Model"

error Command failed with exit code 2.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```

```bash
yarn lint-fix:style
```

will got

```bash
yarn run v1.17.3
$ stylelint '**/*.scss' --fix
✨  Done in 0.94s.
```