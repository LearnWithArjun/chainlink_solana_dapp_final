# Chainlink + Solana combo app

### How to run this project
1. Navigate to the project directory
2. Run `npm install` to install the required dependencies
3. Generate a new wallet: `solana-keygen new -o id.json`
4. Copy the address of the new wallet: `solana-keygen pubkey id.json`
5. Airdrop some SOL into your new wallet: `solana airdrop 2 $(solana-keygen pubkey ./id.json) --url devnet && solana airdrop 2 $(solana-keygen pubkey ./id.json) --url devnet`
6. Build the program: `anchor build`
7. Copy the new program ID from `solana address -k ./target/deploy/chainlink_solana_dapp-keypair.json`, and replace the existing program ID in lib.rs and Anchor.toml
8. Run `anchor test`
