## API for XDC Web3 Domains

dApp Mainnet: https://xdcdomains.xyz/app

dApp Testnet: https://xdcdomains.xyz/apptest

Use NPMJS: https://github.com/XDCWeb3Domains/xdcdomainjs/blob/main/README.md

Contract Address (Mainnet): xdc295a7ab79368187a6cd03c464cfaab04d799784e - https://explorer.xinfin.network/tokens/xdc295a7ab79368187a6cd03c464cfaab04d799784e

Contract Address (Testnet): xdc41da23dfaf3990f7831c838b54a7f734efcc5971 - https://apothem.xinfinscan.com/tokens/xdc41da23dfaf3990f7831c838b54a7f734efcc5971

### Get Resolve .xdc domain
Resolve .xdc domain to get the address of the owner.


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
This will designate one of your domain to represent your account and act as your cross-platform Web3 username and profile. You can only have one Primary Domain per wallet address and can change it at any time. Steps to "Set Primary" domains:
1. Goto dApp: xdcdomains.xyz/app
2. Connect wallet, show the list of created domains, click the Set Primary button below each domain (you need a gas fee to complete the transaction), reload the dapp to see the results shown above.

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
            "domain": "xdc.xdc"
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
    data: ["xdcnetwork.xdc","xxxxxx.xdc" ..]
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


