# esplora.js
A flexible backend for browser-based Bitcoin clients. The in-official JavaScript library for Blockstream's Esplora API. 

## Demo
[You can find the demo here](https://coins.github.io/esplora.js/demo.html)


## Features: 
  - Mainnet & Testnet supported
  - Documented with JSDocs
  - High-level API for error handling
  - Promised-based / compatible with `async/await`
  - Most Esplora endpoints implemented
  - Good auditability
    - Simple code
    - No dependencies
    - Compatible with tree shaking ( reduce your code size to the minimum )

## Example Code

```
import {Esplora} from './esplora-api.js';

Esplora.useTestnet();
Esplora.fetchAddressInfo('2NAZGp2t955uwYsBCoUawbf2cWafgnVhQjm').then(console.log);

Esplora.useMainnet();
Esplora.fetchBalance('1K9zQ8f4iTyhKyHWmiDKt21cYX2QSDckWB').then(console.log);
Esplora.fetchTransactions('1K9zQ8f4iTyhKyHWmiDKt21cYX2QSDckWB').then(console.log);
Esplora.fetchTransactions('3QYFDVHdb8voaTyzPxWeAuP5bgqA92vk4w').then(console.log);
Esplora.fetchUnspentOutputs('1K9zQ8f4iTyhKyHWmiDKt21cYX2QSDckWB').then(console.log);
Esplora.fetchBlockAtHeight(200002).then(hash => Esplora.fetchBlock(hash)).then(console.log)
Esplora.fetchLatestBlockHash().then(console.log)
Esplora.fetchLatestBlockHeight().then(console.log)
Esplora.fetchMempool().then(console.log)
```

## Official API Documentation 
Here you can find Blockstream's official [Esplora API Documentation](https://github.com/Blockstream/esplora/blob/master/API.md). 
