## Restful API for XDC Web3 Domains

### Get Resolve .xdc domain
Resolve .xdc domain to get the address of the owner.

Contract Address (Mainnet): xdc295a7ab79368187a6cd03c464cfaab04d799784e

Contract Address (Testnet): xdc41da23dfaf3990f7831c838b54a7f734efcc5971

Endpoint: https://app.xdcdomains.xyz/api/domains/getOwner?domain=domain.xdc&network=mainnet

**Method: GET**

**Param:**

domain: 'xdc.xdc'

network: 'testnet' // mainnet default

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

Endpoint: https://app.xdcdomains.xyz/api/domains/getDomain?address=xdc3c16183c1c0e28f1a0cb9f8ee4b21d0db2&network=mainnet

**Method: GET**

**Param**

address: xdc3c16183c1c0e28f1a0cb9f8ee4b21d0db2 ... // wallet address

network: 'testnet' // mainnet default

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

Endpoint: https://app.xdcdomains.xyz/api/domains/getDomains?address=xdc3c16183c1c0e28f1a0cb9f8ee4b21d0db2&network=mainnet

**Method: GET**

**Param**

address: xdc3c16183c1c0e28f1a0cb9f8ee4b21d0db2 ...

network: 'testnet' // mainnet default

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

Endpoint: https://app.xdcdomains.xyz/api/domains/getMetadata?key=website,twitter&domain=xdc.xdc&network=mainnet

**Method: GET**

**Param**

keys: 'website,social:twitter'

domain: 'xdc.xdc'

network: 'testnet' // mainnet default

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


