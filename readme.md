# Angular CLI Alias

A little helper utility to allow setting max_old_used_space on the node process that runs the angular cli.

## Usage

1. Add a config option to your project's package.json:

```json
{
    "config": {
        "max_old_used_space": 3072
    }
}
```

2. Change all references in your npm scripts from `ng` to `ng-alias`
3. Ensure that `setup-ng-alias` runs before you try to run `ng-alias`. i.e. with a `prebuild` script:

```json
{
    "scripts": {
        "prebuild": "setup-ng-alias",
        "build": "ng-alias build --prod"
    }
}
```

## Cross platform
This script has been tested on Windows and Unix environments.
