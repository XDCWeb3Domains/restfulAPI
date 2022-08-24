## Restful API for XDC Web3 Domains

### Get Resolve .xdc domain
Resolve .xdc domain to get the address of the owner.

Endpoint: https://app.xdcdomains.xyz/api/domains/getOwner?domain=domain.xdc

**Method: GET**

**Param:**

domain: 'xdc.xdc'

metadata: true // false default return metadata along with domain information

**Return:** 
```
{
    "status": true,
    "message": "Success",
    "data": { 
        "owner": "xdc37Jrh74Jdff...",
        "owner0x": "0x37Jrh74Jdff...",
        "metadata": [
        ]
    }
}
```
### Get a domain default from address
Get a domain default from a user's address, requiring the user to set the default domain name initially.

Endpoint: https://app.xdcdomains.xyz/api/domains/getDomain?address=xdc3c16183c1c0e28f1a0cb9f8ee4b21d0db2

**Method: GET**

**Param**

address: xdc3c16183c1c0e28f1a0cb9f8ee4b21d0db2 ... // wallet address

**Return:** 
```
{
    status: true,
    message: "Success",
    data:
        { 
            "domain": "xdc.xdc",
            "setDefault":true
        }
    ]
}
```

### Get all domains owned by address
This GET method gets all the domains owned by an wallet address.

Endpoint: https://app.xdcdomains.xyz/api/domains/getDomains?address=xdc3c16183c1c0e28f1a0cb9f8ee4b21d0db2

**Method: GET**

**Param**

address: xdc3c16183c1c0e28f1a0cb9f8ee4b21d0db2 ...

**Return:** 
```
{
    status: true,
    message: "Success",
    data: [
        { 
            "domain": "xdcnetwork.xdc",
            "setDefault":true
        },
        { 
            "domain": "xdc.xdc",
            "setDefault":false
        },
    ]
}
```


### Get Metatada
Get a value of metadata from the domain name

Endpoint: https://app.xdcdomains.xyz/api/domains/getMetadata?key=website,twitter&domain=xdc.xdc

**Method: GET**

**Param**

keys: 'website,social:twitter'
domain: 'xdc.xdc'

**Return:** 
```
{
    status: true,
    message: "Success",
    data:
        { 
            "metadata": [
                {"key": "social:twitter","value":"https://twitter.com/xdcdomains"},
                {"key": "website","value":"https://xdcdomains.xyz"}
            ]
        }
}
```


