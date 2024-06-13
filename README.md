# Matomo NewDimensionPlugin Plugin

## Description

Add your plugin description here.

# MatomoCampNordics-PluginDevelopment

MatomoCampNordics-PluginDevelopment

Matomo provides a list of commands that you can use to scaffold your plugin. You can find the list of commands here: https://developer.matomo.org/guides/getting-started-part-1

```bash
./console development:enable

Development mode enabled
```

```bash
 generate
  generate:api                    Adds an API to an existing plugin
  generate:archiver               Adds an Archiver to an existing plugin
  generate:command                Adds a command to an existing plugin
  generate:controller             Adds a Controller to an existing plugin
  generate:dimension              Adds a new dimension to an existing plugin. This allows you to persist new values during tracking.
  generate:menu                   Adds a plugin menu class to an existing plugin
  generate:plugin                 [generate:theme] Generates a new plugin/theme including all needed files
  generate:report                 Adds a new report to an existing plugin
  generate:scheduledtask          Adds a tasks class to an existing plugin which allows you to specify scheduled tasks
  generate:settings               Adds a SystemSetting, UserSetting or MeasurableSetting class to an existing plugin
  generate:system-check           Adds a new system check to an existing plugin
  generate:test                   Adds a test to an existing plugin
  generate:test-action            Generates a github action workflow file for a plugin. The file can be auto-updating based on the parameters supplied.
  generate:update                 Adds a new update to an existing plugin or "core"
  generate:visualizationplugin    Generates a new visualization plugin including all needed files
  generate:vue-component          Generates a vue component for a plugin.
  generate:widget                 Adds a plugin widget class to an existing plugin
```

```bash
./console generate:plugin --name="MyPlugin"
Enter a plugin description: A new plugin
Enter a plugin version number (default to 0.1.0):
```


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

```bash
./console generate:plugin --name="NewDimensionPlugin"
Enter a plugin description: Plugin to demonstrate a new dimension
Enter a plugin version number (default to 0.1.0):

We have updated the required Piwik version from ">=5.0.0-b1,<6.0.0-b1" to ">=5.1.0-stable,<6.0.0-b1" in "/var/www/html/plugins/NewDimensionPlugin/plugin.json".

Plugin NewDimensionPlugin 0.1.0 generated.
Our developer guides will help you developing this plugin, check out https://developer.matomo.org/guides
To see a list of available generators execute ./console list generate
Enjoy!
./console plugin:activate NewDimensionPlugin
```

```bash

```


log_action

name: a string describing the action type. Can be a URL, a page title, campaign name or anything else. The meaning is determined by the type field.

hash: a hash value calculated using the name.

type: the action type's category. Can be one of the following values:
Piwik\Tracker\Action::TYPE_PAGE_URL = 1: the action is a URL to a page on the website being tracked.
Piwik\Tracker\Action::TYPE_OUTLINK = 2: the action is a URL is of a link on the website being tracked. A visitor clicked it.
Piwik\Tracker\Action::TYPE_DOWNLOAD = 3: the action is a URL of a file that was downloaded from the website being tracked.
Piwik\Tracker\Action::TYPE_PAGE_TITLE = 4: the action is the page title of a page on the website being tracked.
Piwik\Tracker\Action::TYPE_ECOMMERCE_ITEM_SKU = 5: the action is the SKU of an ecommerce item that is sold on the site.
Piwik\Tracker\Action::TYPE_ECOMMERCE_ITEM_NAME = 6: the action is the name of an ecommerce item that is sold on the site.
Piwik\Tracker\Action::TYPE_ECOMMERCE_ITEM_CATEGORY = 7: the action is the name of an ecommerce item category that is used on the site.
Piwik\Tracker\Action::TYPE_SITE_SEARCH = 8: the action type is a site search action.
Piwik\Tracker\Action::TYPE_EVENT_CATEGORY = 10: the action is an event category (see Tracking Events user guide)
Piwik\Tracker\Action::TYPE_EVENT_ACTION = 11: the action is an event action
Piwik\Tracker\Action::TYPE_EVENT_NAME = 12: the action is an event name
Piwik\Tracker\Action::TYPE_CONTENT_NAME = 13: the action is a content name (see Content Tracking user guide and developer guide)
Piwik\Tracker\Action::TYPE_CONTENT_PIECE = 14: the action is a content piece
Piwik\Tracker\Action::TYPE_CONTENT_TARGET = 15: the action is a content target
Piwik\Tracker\Action::TYPE_CONTENT_INTERACTION = 16: the action is a content interaction

url_prefix: if the name is a URL this refers to the prefix of the URL. The prefix is removed from actual URLs so the protocol and www. parts of a URL are ignored during analysis. Can be the following values:
0: 'http://'
1: 'http://www.'
2: 'https://'
3: 'https://www.'


1. Add a controller

Linking to a controller action

<a href="https://matomo.local:8444/index.php?module=NewDimensionPlugin&action=index&idSite=1&period=day&date=2013-10-10">Link</a>


2. Add a view
3. Add a model
4. Add a template



https://github.com/jorgeuos/MatomoCampNordics-PluginDevelopment.git


