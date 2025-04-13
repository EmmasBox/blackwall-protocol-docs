---
layout: page
nav_exclude: false
---

# User settings

You can set a number of settings through toml files in Blackwall protocol. Like disabling emojis.

## Location of the toml file

In the .config folder in your user folder you will have to create a folder called "blackwall", if the .config folder does not already exist create it.

Example path:

```txt
/u/sperva/.config/blackwall/user_config.toml
```

## Example of a user config

```toml
[display]
logo = true
emojis = true
```

## All available parameters

### Display section

| Setting | Description | On by default |
|---------|-------------|---------|
| logo    | Can be used to disable or enable the logo on the welcome screen, if the image version is installed            | true        |
| emojis        | Can be used to disable or enable emojis | true        |
