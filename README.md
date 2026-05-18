# H2Ledger: Privacy-Preserving Green Hydrogen Credits

## Overview

H2Ledger is a decentralized marketplace using zero-knowledge proofs (Groth16) to enable suppliers to prove they hold sufficient green hydrogen credits without revealing the actual volume.

## Quick Start

### Verify the Example Proof

```bash
npm install -g snarkjs
snarkjs groth16 verify keys/verification_key.json proofs/public_pass.json proofs/proof_pass.json
```

Expected output: `OK`

## Files

- `circuits/credit_proof.circom` - Main ZK circuit source
- `circuits/credit_proof.r1cs` - Compiled constraints
- `contracts/Verifier.sol` - Auto-generated Solidity verifier
- `keys/verification_key.json` - Public verification key
- `proofs/` - Example proofs and metrics

## Performance

- Verifier Deployment: 2,850,000 gas
- Per-Verification: ~300,000 gas
- Proof Size: 256 bytes

## References

- Circom: https://docs.circom.io
- SnarkJS: https://github.com/iden3/snarkjs

## License

MIT
