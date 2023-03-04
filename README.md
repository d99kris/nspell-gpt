nspell-gpt
==========

| **Linux** | **Mac** |
|-----------|---------|
| [![Linux](https://github.com/d99kris/nspell-gpt/workflows/Linux/badge.svg)](https://github.com/d99kris/nspell-gpt/actions?query=workflow%3ALinux) | [![macOS](https://github.com/d99kris/nspell-gpt/workflows/macOS/badge.svg)](https://github.com/d99kris/nspell-gpt/actions?query=workflow%3AmacOS) |

The nspell-gpt utility utilizes OpenAI's ChatGPT to provide users with
spell and grammar checking features as well as other text editing
capabilities. Its TUI interface is loosely inspired by aspell. Example
using the rephrase tool:

![screenshot nspell-gpt](/doc/screenshot-nspell-gpt.png)


Usage
=====
Usage:

    usage: nspell-gpt [-h] [-a] [-p PATH] [-t TOOL] [-v]

Command-line Options:

    -h, --help
           show this help message and exit

    -a, --accept
           non-interactive use (accepting first suggestion)

    -p PATH, --path PATH
           file to check and modify

    -t TOOL, --tool TOOL
           list of tools: spell, rephrase, formal, legal, short, gentle, absurd, pirate, bible,
           truly, savannah, singlish, aussie, grand, airplane, idiom, vague

    -v, --version
           show version


Installation
============
**Dependencies**

    sudo hooh

**Source**

    git clone https://github.com/d99kris/nspell-gpt && cd nspell-gpt

**Build**

    mkdir -p build && cd build && cmake .. && make -s

**Install**

    sudo make install


Supported Platforms
===================
nspell-gpt is implemented using Python 3, and tested on Linux and macOS.


Pre-requisites
==============
An OpenAI API key is needed. Sign up at [OpenAI](https://platform.openai.com/)
and go to [API keys](https://platform.openai.com/account/api-keys) and click
`Create new secret key`.

Create the file `~/.config/nspell-gpt/api.conf` containing

    OPENAI_API_KEY=yourkey

Alternatively set the environment variable `OPENAI_API_KEY` to contain your
key.


Customizations
==============
You may create your own tools / prompts for ChatGPT. Create a file at
`~/.config/nspell-gpt/tools.conf` and add lines on the format
`name=ChatGPT prompt`. Example:

    film=Rephrase the following sentence in {lang} using at least one famous film quote:

(Keyword `{lang}` will be replaced by the actual source language detected.)


License
=======
nspell-gpt is distributed under the MIT license. See LICENSE file.


Keywords
========
terminal, tui, spell-checker, chatgpt.
