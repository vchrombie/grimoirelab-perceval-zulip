# perceval-zulip
[![Build Status](https://github.com/vchrombie/grimoirelab-perceval-zulip/workflows/tests/badge.svg)](https://github.com/vchrombie/grimoirelab-perceval-zulip/actions?query=workflow:tests+branch:master+event:push) [![Coverage Status](https://img.shields.io/coveralls/vchrombie/grimoirelab-perceval-zulip.svg)](https://coveralls.io/r/vchrombie/grimoirelab-perceval-zulip?branch=master) [![PyPI version](https://badge.fury.io/py/perceval-zulip.svg)](https://badge.fury.io/py/perceval-zulip)

Perceval backend for Zulip.

## Requirements

* Python >= 3.6.1
* python3-requests >= 2.7
* grimoirelab-toolkit >= 0.2
* perceval >= 0.17.4

## Installation

### 1. PyPI

Perceval Zulip backend can be installed using [pip](https://pip.pypa.io/en/stable/)
```
$ pip install perceval-zulip
```

### 2. Getting the source code

Clone the repository
```
$ git clone https://github.com/vchrombie/grimoirelab-perceval-zulip
```

### Prerequisites

#### Poetry

We use [Poetry](https://python-poetry.org/docs/) for managing the project.
You can install it following [these steps](https://python-poetry.org/docs/#installation).

### Setup

Install the required dependencies (this will also create a virtual environment)
```
$ poetry install
```

Activate the virtual environment
```
$ poetry shell
```

## Usage

**Note:** You need the `email` and the `api_token` (API key) from the server. You can use the user email and API key
for authentication or create a bot and use the bot email and API key.

Reference: [About bots (Zulip Help Center)](https://zulip.com/help/bots-and-integrations).
```
(.venv) $ perceval zulip --help
[2021-09-20 15:57:22,523] - Sir Perceval is on his quest.
usage: perceval [-h] [--category CATEGORY] [--tag TAG] [--filter-classified] -t API_TOKEN
                [--archive-path ARCHIVE_PATH] [--no-archive] [--fetch-archive]
                [--archived-since ARCHIVED_SINCE] [--no-ssl-verify] [-o OUTFILE]
                [--json-line] -e EMAIL
                url stream

positional arguments:
  url                   Zulip chat URL
  stream                Zulip chat stream name

optional arguments:
  -h, --help            show this help message and exit

authentication arguments:
  -t API_TOKEN, --api-token API_TOKEN
                        backend authentication token / API key

zulip arguments:
  -e EMAIL, --email EMAIL
                        Zulip bot/user email
```

Fetch messages from the `importlib` stream of the [Python Zulip Server](https://python.zulipchat.com) with the
bot email `bot@zulipchat.com` and API key `xxxx`
```
(.venv) $ perceval zulip https://python.zulipchat.com importlib -e bot@zulipchat.com -t xxxx
[2021-09-20 15:59:24,593] - Sir Perceval is on his quest.
{
...
```

## Contributing

This project follows the [contributing guidelines](https://github.com/chaoss/grimoirelab/blob/master/CONTRIBUTING.md)
of the GrimoireLab.

## Acknowledgment

The backend was initially developed by [@vchrombie](https://github.com/vchrombie).

Adhering to the guidelines, the work is started in this external repository. But, this can be merged
([chaoss/grimoirelab-perceval/#/667](https://github.com/chaoss/grimoirelab-perceval/pull/667)) into the 
[Perceval](https://github.com/chaoss/grimoirelab-perceval) repository in the future.

## License

Licensed under GNU General Public License (GPL), version 3 or later.
