# Cavos Labs

Embedded wallet SDK for Starknet, Solana, and Stellar. Hardware-isolated, non-custodial.

[cavos.xyz/embedded-wallet](https://cavos.xyz/embedded-wallet) · [Docs](https://docs.cavos.xyz) · [Pricing](https://cavos.xyz/pricing)

## How it works

- Users sign in with Google, Apple, GitHub, Telegram, or an email code. No seed phrase and no browser extension.
- Signing always happens on the user's device. The hardware-isolated enclave and the passkey only keep an encrypted copy of the master key, used to restore on a new device.
- Each chain uses its native account: the audited OpenZeppelin account contract on Starknet, a native Ed25519 system account on Solana, and a classic G account on Stellar.
- Gas Sponsorship in Any Token, so users can transact without holding the chain's native coin.
- Connect never deploys. The first execute deploys the account and runs your calls atomically.

## SDK

[`@cavos/kit`](https://www.npmjs.com/package/@cavos/kit) includes `@cavos/kit/react` and `@cavos/kit/react-native`.

```ts
import { Cavos } from "@cavos/kit";

const wallet = await Cavos.connect({
  chain: "solana",
  network: "testnet",
  appSalt: "my-app",
  identity: { userId: "user-123", email: "user@example.com" },
  appId: "your-app-id",
});

if (wallet.status === "undeployed" || wallet.status === "ready") {
  await wallet.execute(1_000_000n, recipient);
}
```

## Pricing

Free up to 1,000 wallets. Essential $59/month. Complete $139/month. Details at [cavos.xyz/pricing](https://cavos.xyz/pricing).

## Repositories

- [kit](https://github.com/cavos-labs/kit): the `@cavos/kit` SDK
- [cavos-recovery](https://github.com/cavos-labs/cavos-recovery): hardware-isolated social recovery in an AWS Nitro Enclave, opt-in and non-custodial
- [reserve](https://github.com/cavos-labs/reserve): Stellar reserves and fees paid in a held token

## Links

- Website: [cavos.xyz](https://cavos.xyz)
- Dashboard: [cavos.xyz/dashboard](https://cavos.xyz/dashboard)
- Docs: [docs.cavos.xyz](https://docs.cavos.xyz)
- X: [@cavosxyz](https://x.com/cavosxyz)
