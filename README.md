# stride-props
These are some attempts by RoboMcGobo to make text proposals on stride to accomplish redelegations.  

We're going to use this repository in the future as a template, once Robo and I (Jacob Gadikian) have figured out how to do it successfully. 



## Fails

### JSON fails

all of the json files in the [JSON](./json/) folder are json fails. 

### Command line fail

```bash
strided tx gov submit-legacy-proposal --title="Signaling Proposal - Redelegate Stride's Osmosis Host Chain Validator Set" --description="This is a signaling proposal to redelegate Stride's Osmosis Validator Set. Over the past two months, the Stride community has been engaged in the process of selecting a new set of Osmosis validators for the purpose of delegating the OSMO deposited with Stride. This process has been open, transparent, and decentralized. \n\\n\\nA set of thirty-two Osmosis validators has been curated, and now it is up to Stride governance to decide whether or not to accept this new set. The proposed weights are:\n\n\n- Cohort 1: {Notional: 5.625%, CryptoCrew Validators: 5.625%, Lavender.Five Nodes: 5.625 %, Hathor Nodes: 5.625%}\n- Cohort 2: {Cosmostation: 4.375%, POSTHUMAN∞DVS: 4.375%, Crypto Assassin: 4.375%, stakely.io: 4.375%}\n- Cohort 3: {binary_holdings: 3.125%, bro_n_bro: 3.125%, Flipside: 3.125%, Interbloc: 3.125%}\n- Cohort 4: {Imperator: 2.875%, S16 Research Ventures: 2.875%, Smart Stake Analytics Hub: 2.875%, Interop: 2.875%}\n- Cohort 5: {Citadel.One: 2.625%, Stakewolle.com |100% Insurance: 2.625%, Crosnest: 2.625%, Autostake Slash Protected: 2.625%}\n- Cohort 6: {Polkachu.com: 2.375%, Forbole: 2.375%, Golden Ratio Staking: 2.375%, in3s.com: 2.375%}\n- Cohort 7: {DSRV: 2.125%, Jabbey: 2.125%, WhisperNode: 2.125%, StakeWithUs: 2.125%}\n- Cohort 8: {Chorus One: 1.875%, Cosmos Spaces: 1.875%, Silk Nodes: 1.875%, Simply Staking: 1.875%}}\n\\n\\nVoting YES indicates that you approve of this validator set, and would like to see OSMO deposited with Stride redelegated to these validators, according to the stated weights.\n\\n\\nVoting NO indicates that you disapprove of this validator set, and would like OSMO deposited with Stride to remain delegated to the default validator set.\n\\n\\nThe full proposal and discussion can be found here: https://commonwealth.im/stride/discussion/13084-redelegate-the-stride-osmosis-validator-set?tab=0\n%22}" --type="Text" --from RoboMcGobo --deposit 1000000000ustrd --chain-id stride-1 --gas 9000000 --gas-prices 0.025ustrd --node https://stride-rpc.polkachu.com:443
```

This fail yeilded: 

https://www.mintscan.io/stride/transactions/C97E448E9CAEC25AA2691D6E0E54138DE407DF20983FEFFA41499824693A92B5?height=5436228


### Command line win?

```bash
strided tx gov submit-legacy-proposal --title="Signaling Proposal - Redelegate Stride's Osmosis Host Chain Validator Set" --description="This is a signaling proposal to redelegate Stride's Osmosis Validator Set.\n\\n\\nThe full proposal and discussion can be found here: https://commonwealth.im/stride/discussion/13084-redelegate-the-stride-osmosis-validator-set?tab=0\n%22}" --type="Text" --from RoboMcGobo --deposit 1000000000ustrd --chain-id stride-1 --gas 9000000 --gas-prices 0.025ustrd --node https://stride-rpc.polkachu.com:443
```



https://www.mintscan.io/stride/transactions/E40DAD268BF61706FBA4DCE5B3C87EB4C0A4C17E7A16453C1DE17F823E6BFA55
