# Pumpfun-Farming-Bot
The most eficient & fastest farming bot in the solana ecosystem, capable of snipping from 200 different wallets not linked in ms using Jito.


https://github.com/solanatoolsbots/pumpfun-farming-bot/assets/175059128/8170c847-e941-4120-886c-b7e6c0ec57e9

**TELEGRAM** for purchases or questions:

[@solanatoolsbots](https://t.me/solanatoolsbots)

Price is 15 SOL

User guide and installation help is included. Be aware of scammers trying to sell fake software created by our team impersonating us!

Other bots we offer:

+ Volume BUNDLE (full pack)
+ Fast JITO VolumeBot
+ Slow Non-Jito VolumeBot
+ Pump.Fun VolumeBot
+ Pump.Fun Bumper
+ Raydium Bundler
+ Pump.Fun FarmingBot
+ Raydium Freeze Bundler
+ DexSc. ReactionSpammer
+ Sniper Bot

[@solanatoolsbots](https://t.me/solanatoolsbots)
#
# FEATURES

+ Available as Web Console and Desktop CLI. The Desktop CLI is provided open source!
+ Create and Manage your token launches all from a convenient console.
+ nipe & Farm: buy without being front run and sell by using “exit liquidity”, literally harvest liquidity from the token by selling into buy orders until the market cap drops below a threshold.
+ Stealth Mode: use the build-in SOL mixer to obfuscate the flow of your SOL. Avoid blockchain analysis and bubble maps that could reveal your central dev wallets.
+ Remove LP: Remove the liquiduity pool and sell all your sniped bags automatically at a defined marketcap, random in between range or manually.
+ Multiple Wallets: Your bots can buy and sell from several wallets, hiding your entry prices in the web statistics. After buying your token are transferred to another wallet for selling.
+ Quick Airdrops: Distribute your token to lists of wallets, making it possible to airdrop to over 100 wallets in one transaction. A great marketing method to spread your token!
+ Dedicated / Private SOL nodes with dynamic fee adjustments guarantee the fastest execution time for trades and to avoid EVM bots.
+ Personal Support: Our team has years of experience with token launches and we help you to optimize your bots and settings.
+ Video Tutorials & Guides are member-only and are currently being updated to v4.

#
# FAQ

**Does it work with any SOL token?**

While our videos focus mostly on token creators, it is totally possible to use it with any token from pump.fun and raydium. Choose "Farm Token" from the console and enter the CA addresse, if the token is not yet trading you can snipe some initial supply on launch, and farming a token is always possible with already launched token.

## Overview
This guide outlines the process for managing market creation and transactions using Solana Bundler.

Below are detailed instructions for setting up your environment and executing prompts in a sequential manner.

### Initial Setup

1. **Install Dependencies**
   ```bash
   npm install

2. **Configuration**
    - Place your Blockengine keypair in `blockengine.json`.
    - Modify `config.ts`:
      - It includes two keypairs:
        1. One for handling SOL distribution fees.
        2. Another for creating the pool.
      - These keypairs can be the same if desired.
    - Modify RPC URL with one that supports JITO(e.g. Helius)

3. **Run script**
   ```bash
   npx ts-node main.ts

## Script Functions

Execute these steps in sequential order. After executing each step, verify the transaction bundle has landed by checking the first included transaction on [Jito Explorer](https://explorer.jito.wtf/).

### A) Create Keypairs
Run this step as needed, not necessarily for every launch. Ensure the existent keypairs hold no SOL before proceeding because this will override them with new keypairs.

### B) Premarket
Execute steps 2 through 6 in order. If a bundle does not land, re-execute the step with a higher tip. Step 1 is optional because you can create a market through other methods as well.

### C) Create Pool
Repeatedly invoke the pool creation & bundling function. Increasing the tip and repeated attempts are recommended due to Solana congestion at peak times.

### D) Sell Features
After the pool is live, proceed to either:
  - Sell all keypairs at once and reclaim SOL in the subsequent step.
  - Gradually sell portions of the token supply on demand. This process involves transferring a percentage of each keypair's token balance to the fee payers and selling it all in one bundle.

### E) LP Removal
This step removes liquidity from the market(if LP tokens are not burned)

## Notes

- Ensure you maintain a minimal SOL balance in your fee wallet so you can cover all the network fees.
- Monitor each transaction bundle to confirm landing using the suggested link to the explorer before proceeding to the next step.
- Consider adjusting the tip to ensure transactions land promptly.

### Main Menu

```bash
Menu:
1. Create Token
2. Manage Token
3. Send Airdrop
4. Farm Token
5. Import Accounts
6. Settings
BACK
```

### Buyer UI
```
1. Create Market (0.3 SOL)
2. Create LUT and SOL ATAs Solfarmer
3. Extend LUT Solfarmer
4. Create ATAs and Send SOL Solfarmer
5. Simulate LP Buys (Get exact amounts)
6. Send SOL Solfarmer
7. Close SOL Accounts to deployer
```

  
