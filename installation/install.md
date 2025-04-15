---
layout: default
parent: Installation
---

# Installation

Prior to Blackwall installation, Python and ZOAU must be installed. Ensure the IRRSEQ00, IRRSMO00, and RACF Subsystem Address Space are configured correctly.

If your environment is not airgapped, you can automatically install Blackwall and its dependencies by running the following command:

```sh
pip install blackwall
```

If your environment is airgapped, you will have to download and install [Textual](https://pypi.org/project/textual/) and [RACFU](https://pypi.org/project/racfu/) manually by downloading the wheel/whl files and uploading them to the mainframe. Make sure you get the correct minimum package versions.
After you have [downloaded Blackwall](https://pypi.org/project/blackwall/), upload the .whl package to the machine through Zowe Explorer or SSH and run the pip command in the folder with the .whl file:

```sh
pip install blackwall-<REPLACE WITH VERSION>-py3-none-any.whl
```

## Optional: installing Blackwall with image support

Blackwall has built in support for the [Sixel](https://en.wikipedia.org/wiki/Sixel) format and can use them to display graphics in the terminal.  This could be used for a company logo or other things. This is vastly more complicated to install and does decrease performance, which is why it doesn't come with Blackwall by default. Make sure you have access to zlib on the system. This can be installed from [zopen community](https://zopen.community).

First install pillow with the following command:

```sh
python3 -m pip install --upgrade Pillow -C jpeg=disable
```

Then install textual-image

```sh
pip install textual-image
```

Then install Blackwall with the images dependencies enabled as seen below:

```sh
pip install blackwall[images]
```
