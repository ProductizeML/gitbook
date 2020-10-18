---
description: Install Python in MacOS systems
---

# MacOS

To follow this guide, you will need to install [Homebrew](https://brew.sh/) first.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

After Homebrew is installed, let's install pyenv:

```bash
brew update
brew install pyenv
```

This command will show a list of Python versions:

```text
pyenv install --list
```

Now let's install the latest Python version \(3.8.5 as of this writing\):

```text
pyenv install 3.8.5
```

Now that Python 3 is installed through pyenv, we want to set it as our global default version for pyenv environments:

```text
$ pyenv global 3.8.5
# and verify it worked
$ pyenv version
```

The power of pyenv comes from its control over our shell's path.   
In order for it to work correctly, we need to add the following to our configuration file \(**.zshrc**  or  **.bash\_profile**\) depending on your terminal version:

```text
$ echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc
```

```text
$ echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile
```

Now create a new terminal session and run:

```text
python -V
```

You should see the 3.8.5 version showing up. 



Sources:

* [https://brew.sh/](https://brew.sh/)
* [https://github.com/pyenv/pyenv](https://github.com/pyenv/pyenv)
* [https://opensource.com/article/19/5/python-3-default-mac](https://opensource.com/article/19/5/python-3-default-mac)

