[![Disnake Banner](https://raw.githubusercontent.com/DisnakeDev/disnake/master/assets/banner.png)](https://disnake.dev/)

disnake
=======

<p align="center">
    <a href="https://discord.gg/gJDbCw8aQy"><img src="https://img.shields.io/discord/808030843078836254?style=flat-square&color=5865f2&logo=discord&logoColor=ffffff&label=discord" alt="Discord server invite" /></a>
    <a href="https://pypi.python.org/pypi/disnake"><img src="https://img.shields.io/pypi/v/disnake.svg?style=flat-square" alt="PyPI version info" /></a>
    <a href="https://pypi.python.org/pypi/disnake"><img src="https://img.shields.io/pypi/pyversions/disnake.svg?style=flat-square" alt="PyPI supported Python versions" /></a>
    <a href="https://github.com/DisnakeDev/disnake/commits"><img src="https://img.shields.io/github/commit-activity/w/DisnakeDev/disnake.svg?style=flat-square" alt="Commit activity" /></a>
</p>

A modern, easy to use, feature-rich, and async ready API wrapper for Discord written in Python.

Key Features
------------

- Proper rate limit handling.
- Type-safety measures.
- [FastAPI](https://fastapi.tiangolo.com/)-like slash command syntax.

<sup>The syntax and structure of `discord.py 2.0` is preserved.</sup>

Installing
----------

**Python 3.8 or higher is required.**

To install the library without full voice support, you can just run the
following command:

``` sh
# Linux/macOS
python3 -m pip install -U disnake

# Windows
py -3 -m pip install -U disnake
```

Installing `disnake` with full voice support requires you to replace `disnake` here, with `disnake[voice]`. To learn more about voice support (or installing the development version), please visit [this section of our guide](https://guide.disnake.dev/prerequisites/installing-disnake/). 

(You can optionally install [PyNaCl](https://pypi.org/project/PyNaCl/) for voice support.)

Note that voice support on Linux requires installation of `libffi-dev` and `python-dev` packages, via your preferred package manager (e.g. `apt`, `dnf`, etc.) before running the following commands.

Versioning
----------

This project does **not** quite follow semantic versioning; for more details, see [version guarantees](https://docs.disnake.dev/en/latest/version_guarantees.html).

To be on the safe side and avoid unexpected breaking changes, pin the dependency to a minor version (e.g. `disnake==a.b.*` or `disnake~=a.b.c`) or an exact version (e.g. `disnake==a.b.c`).

Quick Example
-------------

### Slash Commands Example

``` py
import disnake
from disnake.ext import commands

bot = commands.Bot(command_prefix=">", test_guilds=[12345])

@bot.slash_command()
async def ping(inter):
    await inter.response.send_message("Pong!")

bot.run("BOT_TOKEN")
```

### Context Menus Example

``` py
import disnake
from disnake.ext import commands

bot = commands.Bot(command_prefix=">", test_guilds=[12345])

@bot.user_command()
async def avatar(inter, user):
    embed = disnake.Embed(title=str(user))
    embed.set_image(url=user.display_avatar.url)
    await inter.response.send_message(embed=embed)

bot.run("BOT_TOKEN")
```

### Prefix Commands Example

``` py
import disnake
from disnake.ext import commands

bot = commands.Bot(command_prefix=">")

@bot.command()
async def ping(ctx):
    await ctx.send("Pong!")

bot.run("BOT_TOKEN")
```

You can find more examples in the [examples directory](./examples).

<br>
<p align="center">
    <a href="https://docs.disnake.dev/">Documentation</a>
    ⁕
    <a href="https://guide.disnake.dev/">Guide</a>
    ⁕
    <a href="https://discord.gg/gJDbCw8aQy">Discord Server</a>
    ⁕
    <a href="https://discord.gg/discord-api">Discord API</a>
</p>
<br>


# disnake Technical Documentation

**Last updated:** 2022-01-20\
_Document generation aided by **Documatic**_

<SHORT PROJECT DESCRIPTION>

* [Introduction](#introduction)
* [Code Overview](#code-overview)

## Introduction

This is a technical document detailing
        at a high-level
        what disnake does, how it operates,
        and how it is built.

The outline of this document was generated
        by **Documatic**.
<!---Documatic-section-group: arch-start--->


## Project Architecture


<!---Documatic-section-group: arch-end--->

<!---Documatic-section-group: helloworld-start--->


## Code Overview

The codebase has a flat structure, with 0 code files.
<!---Documatic-section-helloworld: setup-start--->

No exact compatable Python version has been detected.
Versions below 3.8 are compatable.

Install requirements with `pip install -r requirements.txt`.

Run `pip install -e .` in top-level directory to install
package in local directory.
Install from pypi with `pip install disnake`.



<!---Documatic-section-helloworld: setup-end--->

<!---Documatic-section-helloworld: entrypoints-end--->

<!---Documatic-section-group: concept-start--->
## Concepts
<!---Documatic-section-group: concept-end--->

<!---Documatic-section-group: helloworld-end--->

<!---Documatic-section-group: dev-start--->


## Developers
<!---Documatic-section-dev: setup-start--->
* This project uses `pre-commit` to enforce code style on commit. Run `pre-commit install` in a terminal to setup




<!---Documatic-section-dev: setup-end--->

<!---Documatic-section-dev: ci-start--->
The project uses GitHub Actions for CI/CD.

| CI File | Purpose |
|:----|:----|
| pre-commit | Executes on push for any branch, pull_request for any branch |


<!---Documatic-section-dev: ci-end--->

<!---Documatic-section-group: dev-end--->
