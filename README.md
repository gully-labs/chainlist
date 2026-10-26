<!-- gully-header:start -->
<a href="https://gullychain.xyz"><img src="https://gullychain.xyz/brand/repos/chainlist.svg" alt="GullyChain · Chainlist" width="100%"></a>

<p align="center">
  <a href="https://gullychain.xyz"><img src="https://img.shields.io/badge/gullychain.xyz-01D9FA?style=for-the-badge&labelColor=000000&logo=googlechrome&logoColor=000000" alt="Website"></a>
  <a href="https://app.gullychain.xyz"><img src="https://img.shields.io/badge/App-0A0F1A?style=for-the-badge&labelColor=000000&logo=googlechrome&logoColor=01D9FA" alt="App"></a>
  <a href="https://docs.gullychain.xyz"><img src="https://img.shields.io/badge/Docs-0A0F1A?style=for-the-badge&labelColor=000000&logo=readthedocs&logoColor=01D9FA" alt="Docs"></a>
  <a href="https://x.com/Gully_Labs"><img src="https://img.shields.io/badge/@Gully__Labs-0A0F1A?style=for-the-badge&labelColor=000000&logo=x&logoColor=white" alt="X"></a>
  <a href="https://t.me/GullyChain"><img src="https://img.shields.io/badge/Telegram-0A0F1A?style=for-the-badge&labelColor=000000&logo=telegram&logoColor=26A5E4" alt="Telegram"></a>
  <a href="https://discord.com/invite/tY2ErsNNBp"><img src="https://img.shields.io/badge/Discord-0A0F1A?style=for-the-badge&labelColor=000000&logo=discord&logoColor=5865F2" alt="Discord"></a>
  <a href="https://github.com/gully-labs"><img src="https://img.shields.io/badge/GitHub-0A0F1A?style=for-the-badge&labelColor=000000&logo=github&logoColor=white" alt="GitHub"></a>
</p>

<p align="center"><b>Chainlist: Chain and RPC registry, including GullyChain.</b></p>

<p align="center"><sub>Maintained by <a href="https://gullylabs.xyz">Gully Labs</a> as part of <a href="https://gullychain.xyz">GullyChain</a>. Fork of <a href="https://github.com/DefiLlama/chainlist">DefiLlama/chainlist</a>, used under its GPL-3.0 licence. Not affiliated with or endorsed by DefiLlama.</sub></p>

---
<!-- gully-header:end -->

# Chainlist

## Add a chain

Submit a PR that adds a new file to the [constants/additionalChainRegistry folder](https://github.com/DefiLlama/chainlist/tree/main/constants/additionalChainRegistry). The new file should be named `chainid-{chainid_number}.js` and the contents should follow this structure:
```
{
  "name": "Ethereum Mainnet",
  "chain": "ETH",
  "rpc": [
    "https://eth.llamarpc.com",
  ],
  "faucets": [],
  "nativeCurrency": {
    "name": "Ether",
    "symbol": "ETH",
    "decimals": 18
  },
  "features": [{ "name": "EIP155" }, { "name": "EIP1559" }],
  "infoURL": "https://ethereum.org",
  "shortName": "eth",
  "chainId": 1,
  "networkId": 1,
  "icon": "ethereum",
  "explorers": [{
    "name": "etherscan",
    "url": "https://etherscan.io",
    "icon": "etherscan",
    "standard": "EIP3091"
  }]
}
```

## Add an RPC to a chain that is already listed

If you wish to add your RPC, please submit a PR modifying [constants/extraRpcs.js](https://github.com/DefiLlama/chainlist/blob/main/constants/extraRpcs.js) to add your RPC to the given chains.

## API
The following API returns all the data in our website, including chain data along with all of their RPCs:

https://chainlist.org/rpcs.json
