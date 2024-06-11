# MatomoCampNordics-PluginDevelopment

MatomoCampNordics-PluginDevelopment

Matomo provides a list of commands that you can use to scaffold your plugin. You can find the list of commands here: https://developer.matomo.org/guides/getting-started-part-1

To create a new plugin, you can use the following command:

```
./console generate:plugin --name="NewDimensionPlugin"
```
```bash
./console generate:plugin --name="NewDimensionPlugin"
Enter a plugin description: A new dimension
Enter a plugin version number (default to 0.1.0): 

We have updated the required Piwik version from ">=5.0.0-b1,<6.0.0-b1" to ">=5.0.2-stable,<6.0.0-b1" in "/var/www/html/plugins/NewDimensionPlugin/plugin.json".

Plugin NewDimensionPlugin 0.1.0 generated.
Our developer guides will help you developing this plugin, check out https://developer.matomo.org/guides
To see a list of available generators execute ./console list generate
Enjoy!
```


And don't forget to enable the plugin:

```bash
./console plugin:activate MyPlugin
```




