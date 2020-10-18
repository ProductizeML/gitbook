---
description: Install Python in Linux OS systems
---

# Linux

Pyenv builds Python from source, which means you’ll need build dependencies to actually use it. The build dependencies vary by platform. If you are on **Ubuntu/Debian** and want to install the build dependencies, you could use the following:

```text
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl
```

After you’ve installed the build dependencies, you’re ready to install `pyenv` itself. We recommend using the [pyenv-installer project](https://github.com/pyenv/pyenv-installer):

```text
curl https://pyenv.run | bash
```

At the end of the installation you will see something similar to:

```text
WARNING: seems you still have not added 'pyenv' to the load path.

# Load pyenv automatically by adding
# the following to ~/.bashrc:

export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

Follow the instructions that will appear to add the paths to your /.bashrc file and then start a new shell session.:

```text
exec "$SHELL" # Or just restart your terminal
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

Run this command to see the system Python's version after the change:

```text
python -V
```



Sources:

* [https://realpython.com/intro-to-pyenv/](https://realpython.com/intro-to-pyenv/)
* [https://github.com/pyenv/pyenv](https://github.com/pyenv/pyenv)

