# legos.ctftime

[![Travis](https://img.shields.io/travis/bbriggs/legos.ctftime.svg)](https://travis-ci.org/bbriggs/legos.ctftime) [![PyPI](https://img.shields.io/pypi/pyversions/legos.ctftime.svg)](https://pypi.python.org/pypi/legos.ctftime) [![PyPI](https://img.shields.io/pypi/v/legos.ctftime.svg)](https://pypi.python.org/pypi/legos.ctftime) [![PyPI](https://img.shields.io/pypi/wheel/legos.ctftime.svg)](https://pypi.python.org/pypi/legos.ctftime) [![PyPI](https://img.shields.io/pypi/l/legos.ctftime.svg)](https://pypi.python.org/pypi/legos.ctftime) [![PyPI](https://img.shields.io/pypi/status/legos.ctftime.svg)](https://pypi.python.org/pypi/legos.ctftime)

Interact with CTFtime API via chat to find out information about upcoming CTF events, team rankings, and more.

## Usage

CTFtime has two commands, `upcoming` and `top10`. 

### Upcoming

Displays all upcoming events with start and end times:

```
    nick | !ctftime upcoming
legobot | Name: SHA2017 CTF, Format: Jeopardy, Date 2017-08-05T08:00:00+00:00 - 2017-08-06T20:00:00+00:00
legobot | Name: HackCon 2017, Format: Jeopardy, Date 2017-08-25T21:00:00+00:00 - 2017-08-26T21:00:00+00:00
legobot | Name: Tokyo Westerns CTF 3rd 2017, Format: Jeopardy, Date 2017-09-02T00:00:00+00:00 - 2017-09-04T00:00:00+00:00
legobot | Name: ASIS CTF Finals 2017, Format: Jeopardy, Date 2017-09-08T17:00:00+00:00 - 2017-09-10T17:00:00+00:00
legobot | Name: CSAW CTF Qualification Round 2017, Format: Jeopardy, Date 2017-09-15T16:00:00+00:00 - 2017-09-17T16:00:00+00:00
```

### Top 10

Displays the top ten teams and their curent rankings:

```
nick    | !ctftime top10
legobot | ~~~2017 Results~~~
legobot | 217-----------------------|556.8473095563388
legobot | Plaid Parliament of Pwning|550.9596762103753
legobot | LC↯BC---------------------|441.75300810117955
legobot | Bushwhackers--------------|435.99265313767927
legobot | Dragon Sector-------------|428.0948575325616
legobot | Shellphish----------------|400.5711435966653
legobot | binja---------------------|345.1475045345989
legobot | p4------------------------|336.28870164357625
legobot | dcua----------------------|324.9802695455461
legobot | 0daysober-----------------|317.06964731320085
```

## Installation

`pip3 install legos.ctftime`

This is a Lego designed for use with [Legobot](https://github.com/bbriggs/Legobot), so you'll get Legobot along with this. To deploy it, import the package and add it to the active legos like so:

```python
# This is the legobot stuff
from Legobot import Lego
# This is your lego
from legos.ctftime import CTFtime

# Legobot stuff here
lock = threading.Lock()
baseplate = Lego.start(None, lock)
baseplate_proxy = baseplate.proxy()

# Add your lego
baseplate_proxy.add_child(CTFtime)
```

## Tweaking

While you can use this one as-is, you could also add a localized version to your Legobot deployment by grabbing [ctftime.py](legos/ctftime.py) and deploying is as a local module. [Example of a Legobot instance with local modules](https://github.com/voxpupuli/thevoxfox/)

## Contributing

As always, pull requests are welcome.

