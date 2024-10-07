# An indepedent ethereum execution client contributor

I have been actively involved in the Ethereum execution clients and ecosystem for more than 6 years as an independent contributor. Since 2018, I have been involved in various projects within the Ethereum ecosystem. During that time, I created a Chinese guide called [Hitchhikers-guide-to-the-Ethereum](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum), which serves as a valuable resource for beginners to understand the inner workings of Ethereum using the [go-ethereum](https://github.com/ethereum/go-ethereum) implementation. This guide covers a wide range of topics, including:

- [From the perspective of transactions, Ethereum's functionality and features](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/00.from-transaction-to-ethereum.md)
- [An introduction to EVM and smart contracts](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/01.evm-and-contract.md)
- [A collection of internal data structures in Ethereum](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/02.data-struct-in-ethereum.md)
- [Applications of RLP and MPT structures in Ethereum](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/03.rlp-and-mpt.md)
- [Knowledge about Ethereum wallets and implementation of built-in keystore wallets](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/04.wallet-and-keystore.md)
- [Matters related to blockchain block synchronization](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/05.block-syncing.md)
- [Matters related to Ethereum account synchronization](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/06.state-syncing.md)
- [Miners and block sealing in the Ethereum network](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/07.miner-and-seal.md)
- [What is blockchain consensus](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/10.what-is-consensus.md)
- [RPC in Ethereum and its implementation](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/11.rpc-in-ethereum.md)
- [Analysis of the P2P Kademlia protocol](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/60.p2p-kademlia.md)
- [Analysis of Ethereum block synchronization using Fast Sync](https://github.com/jsvisa/Hitchhikers-guide-to-the-Ethereum/blob/master/71.fast-sync-101.md)

## My contributions

Here is my contributions to the Ethereum ecosystem in the past years:

The raw data is available at [data](./data) directory.

| year | [erigon](https://github.com/erigontech/erigon) | [go-ethereum](https://github.com/ethereum/go-ethereum) | [prysm](https://github.com/prysmaticlabs/prysm) | [reth](https://github.com/paradigmxyz/reth) | others                | total merged PRs |
| ---: | :--------------------------------------------- | :----------------------------------------------------- | :---------------------------------------------- | :------------------------------------------ | :-------------------- | ---------------: |
| 2018 | 0                                              | Closed: 12, Merged 31                                  | 0                                               | 0                                           | 0                     |               31 |
| 2019 | 0                                              | Merged: 1                                              | 0                                               | 0                                           | 0                     |                1 |
| 2022 | 1                                              | Closed: 2, Merged: 9                                   | Merged: 2                                       | 0                                           | Closed: 1             |               11 |
| 2023 | 4                                              | Closed: 22, Merged: 72                                 | Merged: 8                                       | Merged: 4                                   | Closed: 1, Merged: 4  |               88 |
| 2024 | 4                                              | Closed: 1, Merged: 6                                   | 1                                               | Closed: 13, Merged: 75                      | Closed: 4, Merged: 18 |              100 |

Hints the `others` including the below projects:

- [alloy](https://github.com/alloy-rs): Alloy implements high-performance, well-tested & documented libraries for interacting with Ethereum and other EVM-based chains.
- [brownie](https://github.com/eth-brownie/brownie): Brownie is a Python-based development and testing framework for smart contracts targeting the Ethereum Virtual Machine.
- [DeFiHackLabs](https://github.com/SunWeb3Sec/DeFiHackLabs): A collection of DeFi security tools and resources.
- [optimism](https://github.com/ethereum-optimism/optimism): Optimistic Ethereum is an L2 scaling solution for the Ethereum blockchain.
- [revm](https://github.com/bluealloy/revm): A Rust implementation of the Ethereum Virtual Machine.
- [revm-inspectors](https://github.com/paradigmxyz/revm-inspectors): A collection of tools for inspecting and debugging EVM bytecode.
- [web3.py](https://github.com/ethereum/web3.py): A Python library for interacting with Ethereum.

From the past contributions, I have a deep understanding of the Ethereum execution client, and I have proposed some useful features, optimizations, and bug fixes to the Ethereum execution clients

### Features

- [eth/tracers: add diffMode to prestateTracer ethereum/go-ethereum#25422](https://github.com/ethereum/go-ethereum/pull/25422): This PR adds a new mode to the `prestateTracer` for emitting the modified parts of state within a transaction. It can be enabled by passing in `diffMode: true` as option.
- [eth/tracers: add withLog to callTracer ethereum/go-ethereum#25991](https://github.com/ethereum/go-ethereum/pull/25991): This PR adds logs along with callTracers, it can be enabled by passing in `withLog: true` as option.
- [cmd/evm: t8n support native tracers ethereum/go-ethereum#28557](https://github.com/ethereum/go-ethereum/pull/28557): This PR adds native tracers support for the `evm` command, it can be enabled by passing in `--tracers` option.

- [feat(rpc): implement eth_getTransactionBySenderAndNonce by jsvisa · Pull Request #10540 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/10540): This PR implements the `eth_getTransactionBySenderAndNonce` RPC to get the transaction by the sender and nonce.
- [feat(rpc/ots): implement ots_getContractCreator by jsvisa · Pull Request #9236 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/9236): This PR implements the `ots_getContractCreator` RPC to get the contract creator address.
- [feat(rpc/ots): implement ots_traceTransaction RPC by jsvisa · Pull Request #9246 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/9246): This PR implements the `ots_traceTransaction` RPC to trace the transaction.

### Optimizations

- [rpc: improve the realtime notify performance by 30% by jsvisa · Pull Request #28328 · ethereum/go-ethereum](https://github.com/ethereum/go-ethereum/pull/28328): This PR improves the realtime notify performance by 30%, by reducing the number of objects allocated and the number of times the `json.Marshal` is called.
- [cmd: use errrors.New instead of empty fmt.Errorf by jsvisa · Pull Request #27329 · ethereum/go-ethereum](https://github.com/ethereum/go-ethereum/pull/27329): This PR uses `errors.New` instead of empty `fmt.Errorf` to reduce the number of allocations.

- [beacon-chain/execution: use pointer instead of value to reduce copy by jsvisa · Pull Request #12818 · prysmaticlabs/prysm](https://github.com/prysmaticlabs/prysm/pull/12818): This PR uses a pointer instead of value to reduce the copy of the data.
- [beacon-node/state: alloc 1more item for append case by jsvisa · Pull Request #12832 · prysmaticlabs/prysm](https://github.com/prysmaticlabs/prysm/pull/12832): This PR allocates one more item for the append case to reduce the number of allocations.

- [feat(trie): hash post state in parallel by jsvisa · Pull Request #7190 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/7190): This PR hashes the post state in parallel to improve the performance.
- [chore(stages/metrics): use Counter instead of Gauge for mgas_processed by jsvisa · Pull Request #7234 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/7234): This PR uses `Counter` instead of `Gauge` for those value can only increase metrics, so the metrics will be more accurate.

### Bugfixes

- [eth/filters: exit early if topics-filter has more than 4 topics by jsvisa · Pull Request #28494 · ethereum/go-ethereum](https://github.com/ethereum/go-ethereum/pull/28494): This PR fixes the issue that the topics-filter has more than 4 topics, it will exit early.
- [eth/filters: eth_getLogs fast exit for invalid block range by jsvisa · Pull Request #28386 · ethereum/go-ethereum](https://github.com/ethereum/go-ethereum/pull/28386): This PR fixes the issue that the `eth_getLogs` will fast exit for invalid block range.
- [graphql: fix an issue of nil pointer panic by jsvisa · Pull Request #28416 · ethereum/go-ethereum](https://github.com/ethereum/go-ethereum/pull/28416): This PR fixes an issue of nil pointer panic in the GraphQL module when the request is invalid.
- [internal/ethapi: ethSendTransaction check baseFee by jsvisa · Pull Request #27834 · ethereum/go-ethereum](https://github.com/ethereum/go-ethereum/pull/27834): This PR fixes the issue that the `eth_sendTransaction` does not check the baseFee.
- [eth/downloader: fix rare crash when parent header missing in db by jsvisa · Pull Request #27945 · ethereum/go-ethereum](https://github.com/ethereum/go-ethereum/pull/27945): This PR fixes the rare crash when the parent header is missing in the database.

- [beacon-chain/execution: no need to reread and unmarshal the eth1Data twice by jsvisa · Pull Request #12826 · prysmaticlabs/prysm](https://github.com/prysmaticlabs/prysm/pull/12826): This PR fixes the issue that the `eth1Data` is read and unmarshaled twice, no need to re-read it.
- [beacon-chain/execution: fix a data race in testcase by jsvisa · Pull Request #13016 · prysmaticlabs/prysm](https://github.com/prysmaticlabs/prysm/pull/13016): This PR fixes some data race in the test case.
- [fix(rpc/trace): include block rewards in trace_filter rpc by jsvisa · Pull Request #8868 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/8868): This PR includes block rewards in the trace_filter RPC response.
- [fix(rpc/trace): wrong calculate of block ommer rewards by jsvisa · Pull Request #8767 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/8767): This PR fixes the wrong calculation of block ommer rewards in the trace response.

- [fix(rpc/trace): trace_filter filting with trace's address by jsvisa · Pull Request #9722 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/9722): This PR fixes the issue that the `trace_filter` does not filter the trace with the trace's address, likewise, it uses transaction's instead.
- [fix(rpc/eth): remove cache when reorg occured by jsvisa · Pull Request #9775 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/9775): This PR fixes the issue that the cache is not removed when reorg occurred.
- [fix(txpool/blob): make blob delete failed more accurate by jsvisa · Pull Request #9846 · paradigmxyz/reth](https://github.com/paradigmxyz/reth/pull/9846): This PR makes the blob delete failed metric more accurate.
