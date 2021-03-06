# IOTA swarm-like Node
A IOTA swarm-like node proof of concepts (POC)

## Pre-Installation:
Dependency packages:

```$ sudo apt-get install python-pip python-setuptools python-dev python3-dev build-essential libssl-dev libffi-dev```

Official Python library for the IOTA Core:

```
$ pip install pyota
```

IOTA transaction POW utilities:

```
$ git clone https://github.com/chenweiii/dcurl.git
$ cd dcurl
$ make check
$ cp ./libdcurl.so iota_swarm_like_node/
```

## How to use:

* Swarm-like node (server side):
```
$ python server.py 
Server start at: 0.0.0.0:8080
wait for connection...
```

* Generate a unused address:
```
$ python exanples/gen_a_unused_address.py
Generating a unused address ... 
{u'addresses': [Address('OMAEMGRMASNBLYVFCRG9UARBBCWDIC9RGCOFTVAVJZDWISOHVMFLSW9ZL9FIJIHVVRYQLIMYBWEYP9WSX')]}
Duration: 73.5027749538 seconds
``` 

* Get tips from full node
```
$ python examples/get_tips.py
Getting tips ...
{u'duration': 484, u'branchTransaction': TransactionHash('QCPNKOXJXFERNNLTZZG9LBWDJQRLFIWDYNYQBHZJANJGXAADKNFTPWBWVDGHROVVVQWBKP9ROKRMZ9999'), u'trunkTransaction': TransactionHash('GEPJNFUNQGPDSFECJZGEWYYWYMGVWDCOELBKZQWILEUGGVHPNWFRLHNQHYKHCHPQWSQAXGYG9AIBA9999')}
Duration: 0.960033893585 seconds
``` 

* Send data (0 value transaction)
```
$ python examples/send_data.py
Send send transfer command ... 
WIAEHXJUVO9IDZXROJEDBQLFHVFLZCIQKPLLXCGWLNZFIUJZLBZACVLZPWAKUBYLDYRZKFIDKLSAHJHEY
Duration: 1.91658091545 seconds

```

## TODO
* Attache a signed bundle to Tangle (Send value transaction)
* Support HTTP protocol
