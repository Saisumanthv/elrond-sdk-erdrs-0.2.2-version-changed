# Dharitri SDK for Rust

[![Crates.io](https://img.shields.io/crates/v/dharitri-sdk-erdrs)](https://crates.io/crates/dharitri-sdk-erdrs)

## Example

```rust
use dharitri_sdk_erdrs::blockchain::rpc::{DharitriProxy, DEVNET_GATEWAY};

#[tokio::test]
async fn get_network_config() {
    let blockchain = DharitriProxy::new(DEVNET_GATEWAY.to_string());
    let network_config = blockchain.get_network_config().await.unwrap();

    println!("network_config: {:?}", network_config)
}
```

More example in `./src/blockchain/tests.rs`