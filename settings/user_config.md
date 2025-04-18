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
logo = true
emojis = true
system_label = true
theme = "cynosure"

[commands]
clear_on_submission = true

[locale]
date_format = "ymd" #valid values mdy, dmy, or ymd
```

## All available parameters

### Display section

| Setting | Description | Default value |
|---------|-------------|---------|
| logo    | Can be used to disable or enable the logo on the welcome screen, if the image version is installed            | true        |
| emojis        | Can be used to disable or enable emojis | true        |
| system_label        | Can be used to turn the system label at the top off the screen on or off | true        |
| theme        | You can use this to set the default theme when opening up the application, can still be changed manually inside of the application | cynosure        |

### Commands section

| clear_on_submission        | If this option is set to false then the command field will retain the input after submitting the command, by default it will clear the field | true        |

### Locale section

| date_format        | This can be used to set the formatting of dates handled by Blackwall. Please note that it will not affect dates in command output. | dmy        |
