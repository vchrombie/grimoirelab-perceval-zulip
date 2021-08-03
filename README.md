# perceval-zulip [![Build Status](https://github.com/vchrombie/grimoirelab-perceval-zulip/workflows/tests/badge.svg)](https://github.com/vchrombie/grimoirelab-perceval-zulip/actions?query=workflow:tests+branch:master+event:push) [![Coverage Status](https://img.shields.io/coveralls/vchrombie/grimoirelab-perceval-zulip.svg)](https://coveralls.io/r/vchrombie/grimoirelab-perceval-zulip?branch=master) [![PyPI version](https://badge.fury.io/py/perceval-zulip.svg)](https://badge.fury.io/py/perceval-zulip)

Bundle of Perceval backends for Zulip.

## Backends

The backends currently managed by this package support the next repositories:

* Zulip

## Requirements

* Python >= 3.6
* python3-requests >= 2.7
* grimoirelab-toolkit >= 0.2
* perceval >= 0.17.4

## Installation

### Getting the source code

Clone the repository
```
$ git clone https://github.com/vchrombie/grimoirelab-perceval-zulip
```

### Prerequisites

#### Poetry

We use [Poetry](https://python-poetry.org/docs/) for managing the project.
You can install it following [these steps](https://python-poetry.org/docs/#installation).

### Installation and configuration

Install the required dependencies (this will also create a virtual environment)
```
$ poetry install
```

Activate the virtual environment
```
$ poetry shell
```

## Examples

### Zulip

**Note:** You need the `email` and the `api_token` from the server. You can create a bot and use it for the authentication,
please read the docs at [About bots (Zulip Help Center)](https://zulip.com/help/bots-and-integrations).

Fetch messages from the `importlib` stream of the [Python Zulip Server](https://python.zulipchat.com)
```
$ perceval zulip https://python.zulipchat.com importlib -e bot@zulipchat.com -t xxxx
```

## Contributing

This project follows the [contributing guidelines](https://github.com/chaoss/grimoirelab/blob/master/CONTRIBUTING.md)
of the GrimoireLab.

Adhering to the guidelines, the work is started in this external repository. But, this can be merged
([chaoss/grimoirelab-perceval/#/667](https://github.com/chaoss/grimoirelab-perceval/pull/667)) into the 
[Perceval](https://github.com/chaoss/grimoirelab-perceval) repository in the future.

## License

Licensed under GNU General Public License (GPL), version 3 or later.
