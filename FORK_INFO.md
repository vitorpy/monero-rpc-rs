# Fork Information

## Fork Details
- **Upstream**: https://github.com/monero-rs/monero-rpc-rs
- **Fork**: https://github.com/vitorpy/monero-rpc-rs
- **Purpose**: Add multisig wallet RPC methods for XMR-Solana bridge integration

## Feature Branch
- **Branch**: `feature/multisig-wallet-methods`
- **Base**: `main` from upstream

## Git Remotes
```bash
origin: https://github.com/vitorpy/monero-rpc-rs (fork)
upstream: https://github.com/monero-rs/monero-rpc-rs (original)
```

## Planned Changes

### New Methods to Add
1. `is_multisig()` - Check if wallet is multisig and get configuration
2. `sign_multisig(tx_data_hex)` - Sign a multisig transaction
3. `submit_multisig(tx_data_hex)` - Submit a signed multisig transaction
4. `open_wallet(filename, password)` - Open a wallet file
5. `close_wallet(autosave_current)` - Close the current wallet

### Integration
- Will be used by `xmr-bridge` signer-service via git dependency
- After PR is merged upstream, can switch to crates.io version

## Tracking
- Beads issues: xmr-bridge-43 through xmr-bridge-48
- Related to: xmr-bridge-42 (Complete monero-wallet-rpc integration)

## Local Setup
```bash
cd /home/vitorpy/code/monero-rpc-rs
git remote -v
git checkout feature/multisig-wallet-methods
```
