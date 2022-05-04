![image](https://user-images.githubusercontent.com/105896/166617434-046adb58-a6ef-4964-b542-a82906c2f4d5.png)

# perp-collateral-liquidator

## Local Development and Testing

### Requirements

You should have Node v16 installed. Use [nvm](https://github.com/nvm-sh/nvm) to install it.

### Development

Clone this repository, install NodeJS dependencies, and build the source code:

```bash
git clone git@github.com:perpetual-protocol/perp-collateral-liquidator.git
# hardhat-deploy-ethers@0.3.0-beta.11 needs --legacy-peer-deps
# otherwise there would be conflicting peer dependencies during installation
npm i --legacy-peer-deps
npm run build
```

Since there are some runtime environment dependencies, if the installation failed on your machine, please try a vanilla install instead:

```bash
npm run clean
rm -rf node_modules/
rm package-lock.json
npm install
npm run build
```

### Testing

To run all the test cases:

```bash
npm run test
```

### Deploy Contract

Prerequisite:
1. duplicate `.env.build.example`
2. rename it to `.env.build`
3. fill all of the fields

To deploy the contract:

```bash
# to Optimism Kovan (testnet)
npm run deploy-contract-optimism-kovan

# to Optimism (mainnet)
npm run deploy-contract-optimism
```

### Run App

Prerequisite:
1. duplicate `.env.runtime.example`
2. rename it to `.env.runtime.optimism` (or `.env.runtime.optimism-kovan` for testnet)
3. fill all of the fields

```bash
# on Optimism Kovan (testnet)
npm run app:optimism-kovan

# on Optimism (mainnet)
npm run app:optimism
```
