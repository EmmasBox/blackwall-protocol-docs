---
layout: page
nav_exclude: false
---

# Site settings

You can set a number of settings through toml files in Blackwall protocol. Like a company logo.

## Location of the toml file

In the /etc/ folder you will have to create a folder called "blackwall", in here you can put the site_config.toml file.

Example path:

```txt
/etc/blackwall/site_config.toml
```

## Example of a site config

```toml
[meta]
company = "Wilford Industries"

[welcome]
logo_path = "cool_logo.png"
```

## All available parameters

### Meta section

| Setting | Description | Default value |
|---------|-------------|---------|
| company | Can be used to supply a company name, this will be used in a variety of places such as the program header | None        |

### Welcome section

| Setting | Description | Default value |
|---------|-------------|---------|
| logo_path | Can be used to supply a company logo to the welcome screen, if the image version is installed. Note it only accepts png images | None        |
