NIP for storage of Grapevine or web of trust scores as csv files in nostr
=====

```json
{
  "kind": [ 39903 ],
  "tags": [
    ["p",pk], // only use if the score is being stored for an individual pubkey
    ["scoreType", ""], // a string used as an indicator of the type of the WoT score being stored
  ],
}
```

```csv
sample,pk1,pk2,pk3,pk4
averageScore,0.4,0.6,0.4.0
certainty,0.5,0.7.0.02,0.5
```
