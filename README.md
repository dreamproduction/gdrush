# gdrush

Run drush commands on multiple sites, matching a pattern to the existing site aliases.
Example:
```
vendor\bin\gdrush dev cr
```
This will run `drush cr` on all aliases that match `dev`

Alternatively, you can declare commonly used commands in `composer.json` in the `scripts` object:
```
...
    "scripts": {
        "drush-local": "vendor/bin/gdrush local",
        "drush-dev": "vendor/bin/gdrush dev",
        "drush-stage": "vendor/bin/gdrush stage",
        "drush-live": "vendor/bin/gdrush live"
    },
...
```
Then, you can use them like this:
```
composer drush-dev cr
```

