# github-action-fpm

Github action to build packages for multiple platforms using [fpm](https://github.com/jordansissel/fpm).

## Example

```
name: Example workflow yml

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v1
    - name: Package
      uses: bpicode/github-action-fpm@master
      with:
        fpm_args: 'file=/usr/local/bin/file'
        fpm_opts: '--debug -n mypackage -t deb -s dir'
```
## Inputs and Outputs

| argument | required | description                                                    |
| :------- | :------: | :------------------------------------------------------------- |
| fpm_args | no       | Arguments to pass to the fpm command (e.g. file=/usr/bin/file) |
| fpm_opts | no       | Options to pass to the fpm command (e.g. --verbose)            |

## Feedback, Suggestions, Contributions, Known Limitations

Feel free to file an issue, open a pull request, etc.
