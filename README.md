# Remote Video YouTube Lite Embed Drupal Recipe

Configures Remote Video Media entity to use Lite YouTube Embed.

## Configuring Drupal for Recipes

See https://www.drupal.org/files/issues/2023-10-01/Configuring%20Drupal%20to%20Apply%20Recipes.md


## Installing this Recipe

`composer require kanopi/remote-video-youtube-lite`

NOTE:

This recipe requires the [YouTube Lite Embed](https://github.com/paulirish/lite-youtube-embed)
 npm packages that needs to be saved in Drupal libraries.

Be sure your project's composer.json file is set up like this:

```
"extra": {
    "installer-types": [
        "npm-asset"
    ],
    "installer-paths": {
        "web/libraries/{$name}": [
            "type:drupal-library",
            "type:npm-asset"
        ],
    }
}
```


## Applying this Recipe

From your webroot run:

`php core/scripts/drupal recipe recipes/contrib/remote-video-youtube-lite`

 and `drush cr`

If you have our Docksal command in your project, run:

`fin recipe-apply remote-video-youtube-lite`


## Unpacking this Recipe

To unpack this recipe's dependencies to your site's composer.json, in the root 
of your project run:

`composer unpack kanopi/remote-video-youtube-lite`

If you have our Docksal command in your project, run:

`fin recipe-unpack kanopi/remote-video-youtube-lite`


## Known Issues

N/A
