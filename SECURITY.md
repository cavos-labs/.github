# Security policy

This policy covers every public repository in the `cavos-labs` organization,
including `@cavos/kit`, the Cavos vault served from `cavos.xyz/vault`, the
Stellar and Solana relayers, and the recovery enclave in
[cavos-recovery](https://github.com/cavos-labs/cavos-recovery).

## Report a vulnerability

Email **hello@cavos.xyz** with the subject `Security:` and include:

- the affected package, version, or URL,
- steps to reproduce or a proof of concept,
- the impact you expect.

Do not open a public issue or pull request for a vulnerability. Do not test
against other users' accounts or funds; use testnet where you can.

## Supported versions

Fixes ship in the latest `@cavos/kit` release on npm. Older versions do not get
backported fixes.

## Security model

How keys are held, signed, and restored is documented at
[docs.cavos.xyz/docs/vault](https://docs.cavos.xyz/docs/vault) and
[docs.cavos.xyz/docs/hardware-isolated-recovery](https://docs.cavos.xyz/docs/hardware-isolated-recovery).
