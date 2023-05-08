<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [bitburner](./bitburner.md) &gt; [HacknetNodesFormulas](./bitburner.hacknetnodesformulas.md) &gt; [levelUpgradeCost](./bitburner.hacknetnodesformulas.levelupgradecost.md)

## HacknetNodesFormulas.levelUpgradeCost() method

Calculate cost of upgrading hacknet node level.

<b>Signature:</b>

```typescript
levelUpgradeCost(startingLevel: number, extraLevels?: number, costMult?: number): number;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  startingLevel | number | starting level |
|  extraLevels | number | amount of level to purchase (defaults to 1) |
|  costMult | number | player cost reduction (default to 1) |

<b>Returns:</b>

number

The calculated cost.
