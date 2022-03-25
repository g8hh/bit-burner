<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [bitburner](./bitburner.md) &gt; [NS](./bitburner.ns.md) &gt; [scp](./bitburner.ns.scp_1.md)

## NS.scp() method

Copy file between servers.

<b>Signature:</b>

```typescript
scp(files: string | string[], source: string, destination: string): Promise<boolean>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  files | string \| string\[\] | Filename or an array of filenames of script/literature files to copy. |
|  source | string | Host of the source server, which is the server from which the file will be copied. This argument is optional and if it’s omitted the source will be the current server. |
|  destination | string | Host of the destination server, which is the server to which the file will be copied. |

<b>Returns:</b>

Promise&lt;boolean&gt;

True if the script/literature file is successfully copied over and false otherwise. If the files argument is an array then this function will return true if at least one of the files in the array is successfully copied.

## Remarks

RAM cost: 0.6 GB

Copies a script or literature (.lit) file(s) to another server. The files argument can be either a string specifying a single file to copy, or an array of strings specifying multiple files to copy.

## Example 1


```ts
// NS1:
//Copies foo.lit from the helios server to the home computer:
scp("foo.lit", "helios", "home");

//Tries to copy three files from rothman-uni to home computer:
files = ["foo1.lit", "foo2.script", "foo3.script"];
scp(files, "rothman-uni", "home");
```

## Example 2


```ts
// NS2:
//Copies foo.lit from the helios server to the home computer:
await ns.scp("foo.lit", "helios", "home");

//Tries to copy three files from rothman-uni to home computer:
files = ["foo1.lit", "foo2.script", "foo3.script"];
await ns.scp(files, "rothman-uni", "home");
```

## Example 3


```ts
//ns2, copies files from home to a target server
const server = ns.args[0];
const files = ["hack.js","weaken.js","grow.js"];
await ns.scp(files, "home", server);
```
