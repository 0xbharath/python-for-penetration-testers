# WHOIS service 

## Tools

1. [ipwhois](https://ipwhois.readthedocs.io/)
2. [cymruwhois](https://github.com/JustinAzoff/python-cymruwhois)


## ipwhois

### Simple WHOIS query for an IP

```python
from ipwhois import IPWhois
from pprint import pprint
obj = IPWhois('8.8.8.8')
results = obj.lookup_rdap(depth=1)
pprint(results)
```

### Finding ASN number for an IP

```
from ipwhois.net import Net
from ipwhois.asn import IPASN
from pprint import pprint

net = Net('8.8.8.8')
obj = IPASN(net)
results = obj.lookup()
pprint(results)
```

### Finding the netblocks that belong to an ASN

```python
from ipwhois.net import Net
from ipwhois.asn import ASNOrigin
from pprint import pprint

net = Net('8.8.8.8')
obj = ASNOrigin(net)
results = obj.lookup(asn='AS36459')

for i in results['nets']:
    #print i['cidr'], ' -- ' ,i['maintainer']
    print "{0:<30} -- {1:>30}".format(i['cidr'],i['maintainer'])

```


### Finding IPv4 & IPv6 addresses(with count) in text


```
from ipwhois.utils import unique_addresses
from pprint import pprint
input_data = (
'You can have IPs like 74.125.225.229, or 2001:4860:4860::8888'
'Put a port at the end 74.125.225.229:80 or for IPv6: '
'[2001:4860:4860::8888]:443 or even networks like '
'74.125.0.0/16 and 2001:4860::/32.'
)
results = unique_addresses(data=input_data, file_path=None)
pprint(results)
```


## cymruwhois

- Enumerating ASN details from IP

```python
import socket
ip = socket.gethostbyname("github.com")
from cymruwhois import Client
c=Client()
r=c.lookup(ip)
str(r)
```