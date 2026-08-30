# Cavos Labs

Device-native, self-custodial embedded wallets for Starknet, Solana, and Stellar.

## Mission

Remove the friction from Web3. No seed phrases, no wallet popups, just social logins and on-chain execution across Starknet, Solana, and Stellar.

## How it works

The private key is created and used on the user's device. Cavos cannot see it, cannot sign, and cannot move funds. No seed phrase, no browser extension, no MPC, no server-side key shards. Passkeys enroll devices; they do not sign transactions.

- **Starknet and Solana**: on-chain device-signer accounts
- **Stellar**: classic G… account with an encrypted control-key envelope unlocked on the device

Connect never deploys. The first transaction deploys the account. Status is `undeployed`, `ready`, or `needs-device-approval`.

## SDK

[`@cavos/kit`](https://github.com/cavos-labs/kit) — includes `@cavos/kit/react` and `@cavos/kit/react-native`.

```ts
import { Cavos } from "@cavos/kit";

const wallet = await Cavos.connect({
  chain: "solana",
  network: "testnet",
  identity: { userId: "user-123", email: "user@example.com" },
  appId: "your-app-id",
  appSalt: "my-app",
});

if (wallet.status === "undeployed" || wallet.status === "ready") {
  if (wallet.chain === "solana") {
    const tx = await wallet.execute(/* ... */);
  }
}
```

## Repositories

- [kit](https://github.com/cavos-labs/kit) — `@cavos/kit` SDK
- [account-contracts](https://github.com/cavos-labs/account-contracts) — on-chain account contracts
- [cavos-recovery](https://github.com/cavos-labs/cavos-recovery) — hardware-isolated social recovery (AWS Nitro Enclave); opt-in, non-custodial

## Links

- Website: [cavos.xyz](https://cavos.xyz)
- Dashboard: [cavos.xyz/dashboard](https://cavos.xyz/dashboard)
- Docs: [docs.cavos.xyz](https://docs.cavos.xyz)
- X: [@cavosxyz](https://x.com/cavosxyz)
