# Skeleton Python Package

- [Installation](#Installation)
    - [Clone Repository](#Clone-Repository)
    - [Install Packages](#Install-Packages)
    - [Change Package Name](#Change-Package-Name)
    - [Update doc/conf.py](#Update-doc/conf.py)
    - [Update setup.cfg](#Update-setup.cfg)
- [Usage](#Usage)
    - [Add Code](#Add-Code)
    - [Auto Generate Document](#Auto-Generate-Document)
    - [Build Document](#Build-Document)
- [Developers](#Developers)


## Installation

### Clone Repository
Clone this github repository by following:
```
$ git clone https://github.com/Chanok203/python-sphinx-skeleton.git
```

### Install Packages
Upgrade pip and setuptools and install sphinx and sphinx-rtd-theme via pip by following:
```
$ pip install --upgrade pip setuptools sphinx sphinx-rtd-theme
```

### Change Package Name

Edit directory's name from package_name to your package name by following:
```
$ mv package_name <your_package_name>
```

### Update doc/conf.py

First, uncomment line 13, 14 and 16 in doc/conf.py and edit code at line 16 by following:

```
sys.path.insert(0, os.path.abspath("../<your_package_name>"))
```

Then, update your project information at line 21, 22 and 23

### Update setup.cfg
In [build_sphinx] block, change your proejct information by following:
```
[build_sphinx]
project = <your_project_name>
version = <version>
release = <release_version>
```

## Usage

### Add Code
example skeleton:
```
~/python-sphinx-skeleton
    - doc/
        - ...
    - tests/
        - ...
    - setup.py
    - ...
    - setup.cfg
    - <your_package_name>
        - __init__.py
        - <your_subpackage>/
            - __init__.py
            - ...
        - ...
```

### Auto Generate Document
Generate document using sphinx-apidoc by following:
```
$ sphinx-apidoc -f -o doc <your_package_name>
```

### Build Document
Build document using sphinx and setuptools by following:
```
python setup.py build_sphinx
```

The output of the above command is in build/sphinx/html.

## Developers

Chanok Pathompatai
