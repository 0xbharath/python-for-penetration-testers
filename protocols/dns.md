# Domain Name Service(DNS)


## Tools

1. [dnspython](http://www.dnspython.org/)
2. [dnsknife](https://github.com/Gandi/dnsknife)


## dnspython

**Querying for A records**

```python
import dns.resolver
answers = dns.resolver.query('github.com', 'A')

for rdata in answers:
    print rdata
```

**Querying PTR(reverse-dns) records for a IP**

```python
from dns import resolver,reversename
addr=reversename.from_address("8.8.8.8")
print str(resolver.query(addr,"PTR")[0])
```

**Querying for TXT records**

```python
import dns.resolver
answers = dns.resolver.query('icann.org', 'TXT')

for rdata in answers:
    print rdata
```


**Querying multiple records**

```python
import dns.resolver
name = 'iana.org'
for qtype in 'A', 'AAAA', 'MX', 'CNAME','NS', 'TXT', 'SOA':
    answer = dns.resolver.query(name,qtype, raise_on_no_answer=False)
    if answer.rrset is not None:
        print(answer.rrset)
```


**Zone transfer(AXFR)**

```
import dns.query
import dns.zone

z = dns.zone.from_xfr(dns.query.xfr('nsztm1.digi.ninja', 'zonetransfer.me'))
names = z.nodes.keys()
names.sort()
for n in names:
    print z[n].to_text(n)
```

## dnsknife


**Querying for A records**

```
from dnsknife import resolver
ans = resolver.query('example.com', 'A', dnssec=True)
for answer in ans.rrset:                                      
    print answer
```

## Query shortcuts