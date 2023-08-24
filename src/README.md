# esplora.js
A flexible backend for browser-based Bitcoin clients. The unofficial JavaScript library for Blockstream's Esplora API. 

## Demo
[You can find the demo here](https://coins.github.io/esplora-js/src/demo.html)


## Features: 
  - Mainnet & Testnet supported
  - Documented with JSDocs
  - High-level API for error handling
  - Promise-based / compatible with `async/await`
  - Most Esplora endpoints implemented
  - Good auditability
    - Simple code
    - No dependencies
    - Compatible with tree shaking ( reduce your code size to the minimum )

## Example Code

### Mainnet 
```html
<script type="module">
import * as Esplora from 'https://coins.github.io/esplora-js/esplora.js'

Esplora.fetchBalance('1K9zQ8f4iTyhKyHWmiDKt21cYX2QSDckWB').then(console.log)
Esplora.fetchTransactions('3QYFDVHdb8voaTyzPxWeAuP5bgqA92vk4w').then(console.log)
Esplora.fetchUnspentOutputs('1K9zQ8f4iTyhKyHWmiDKt21cYX2QSDckWB').then(console.log)
Esplora.fetchBlockAtHeight(200002).then(hash => Esplora.fetchBlock(hash)).then(console.log)
Esplora.fetchLatestBlockHash().then(console.log)
Esplora.fetchLatestBlockHeight().then(console.log)
Esplora.fetchMempool().then(console.log)
</script>
```

### Testnet
```html
<script type="module">
import * as Esplora from 'https://coins.github.io/esplora-js/esplora.js'

Esplora.useTestnet()
Esplora.fetchAddressInfo('2NAZGp2t955uwYsBCoUawbf2cWafgnVhQjm').then(console.log)
</script>
```

#### Demo in your Dev Tools via a Data URL 
```
data:text/html;base64,PHRpdGxlPkVzcGxvcmEgQVBJIEphdmFTY3JpcHQgUGxheWdyb3VuZDwvdGl0bGU+CjxzY3JpcHQgdHlwZT0ibW9kdWxlIj5pbXBvcnQgKiBhcyBFc3Bsb3JhIGZyb20gJ2h0dHBzOi8vY29pbnMuZ2l0aHViLmlvL2VzcGxvcmEtanMvZXNwbG9yYS5qcyc7d2luZG93LkVzcGxvcmEgPSBFc3Bsb3JhO2NvbnNvbGUubG9nKCdUeXBlICJFc3Bsb3JhLiInKTwvc2NyaXB0PjxoMz5PcGVuIENvbnNvbGU8L2gzPg==
```

## Official API Documentation 
Here you can find Blockstream's official [Esplora API Documentation](https://github.com/Blockstream/esplora/blob/master/API.md). 


## CoinThx

[<img src="https://coins.github.io/thx/logo-color-large-pill-320px.png" alt="CoinThx" width="200"/>](https://coins.github.io/thx/#1K9zQ8f4iTyhKyHWmiDKt21cYX2QSDckWB?label=Coins%20Project&message=Thank%20you%20for%20your%20contribution!)

