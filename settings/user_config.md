---
layout: default
parent: Settings
---

# User settings

You can set a number of settings through toml files in Blackwall protocol. Like disabling emojis.

## Location of the toml file

In the .config folder in your user folder you will have to create a folder called "blackwall", if the .config folder does not already exist create it. In your newly created folder put the user_config.toml file.

Example path:

```txt
/u/sperva/.config/blackwall/user_config.toml
```

## Example of a user config

```toml
[display]
logo = true #valid values: true or false
emojis = true #valid values: true or false
system_label = true #valid values: true or false
system_clock = true #valid values: true or false
short_system_label = true #valid values: true or false
theme = "cynosure"

[tabs]
default_tab = "user" #valid values are: search, user, group, dataset, resource, options, and commands

[commands]
clear_on_submission = true #valid values: true or false

[locale]
date_format = "ymd" #valid values are mdy, dmy, or ymd

[notifications]
use_modal = true #valid values: true or false
```

## All available parameters

### Display section

| Setting | Description | Default value |
|---------|-------------|---------|
| logo    | Can be used to disable or enable the logo on the welcome screen, if the image version is installed            | true        |
| emojis   | Can be used to disable or enable emojis | true        |
| system_label  | Can be used to turn the system label at the top off the screen on or off | true        |
| system_clock  | Can be used to turn the system clock at the top off the screen on or off | true        |
| short_system_label | When enabled this will make the system name and LPAR name easier to read at a glance | false        |
| theme        | You can use this to set the default theme when opening up the application, can still be changed manually inside of the application | cynosure        |

### Tabs section

| Setting | Description | Default value |
|---------|-------------|---------|
| default_tab | You can use this to set which tab the program should initially start on when opening up the program, see example for options. | None        |

### Commands section

| Setting | Description | Default value |
|---------|-------------|---------|
| clear_on_submission        | If this option is set to false then the command field will retain the input after submitting the command, by default it will clear the field | true        |

### Locale section

| Setting | Description | Default value |
|---------|-------------|---------|
| date_format | This can be used to set the formatting of dates handled by Blackwall. Please note that it will not affect dates in command output. | dmy        |

### Notifications

| Setting | Description | Default value |
|---------|-------------|---------|
| use_modal | When this is enabled a modal will pop up when things fail, which you will have to dismiss, this makes it harder to miss mistakes. | false        |
