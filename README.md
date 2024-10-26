# EDge-Bridge

<p align="center">
  <img src="https://cloudflare-ipfs.com/ipfs/bafybeigd6i5aavwpr6wvnwuyayklq3omonggta4x2q7kpmgafj357nkcky" alt="edgetunnel" style="margin-bottom: -50px;">
</p>

A fork of [https://github.com/zizifn/edgetunnel](https://github.com/zizifn/edgetunnel)

[![Repository](https://img.shields.io/badge/View%20on-GitHub-blue.svg)](https://github.com/zizifn/edgetunnel)
## Deploy in pages.dev

1. See YouTube Video:

   [https://www.youtube.com/watch?v=8I-yTNHB0aw](https://www.youtube.com/watch?v=8I-yTNHB0aw)

2. Clone this repository deploy in cloudflare pages.

## Deploy in worker.dev

1. Copy `_worker.js` code from [here](https://github.com/rti2/edge-bridge/blob/main/_worker.js).

2. Alternatively, you can click the button below to deploy directly.

   [![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/rti2/ED)

## Lazy to deploy

`https://edge-bridge.pages.dev/sub/1f489b96-80a3-44eb-b32a-b454341e200c` (free v2ray subscription link)

## UUID Setting (Optional)

1. When deploy in cloudflare pages, you can set uuid in `wrangler.toml` file. variable name is `UUID`. `wrangler.toml` file is also supported. (recommended) in case deploy in webpages, you can not set uuid in `wrangler.toml` file.

2. When deploy in worker.dev, you can set uuid in `_worker.js` file. variable name is `userID`. `wrangler.toml` file is also supported. (recommended) in case deploy in webpages, you can not set uuid in `wrangler.toml` file. in this case, you can also set uuid in `UUID` enviroment variable.

Note: `UUID` is the uuid you want to set. pages.dev and worker.dev all of them method supported, but depend on your deploy method.

### UUID Setting Example

1. single uuid environment variable

   ```.environment
   UUID = "uuid here your want to set"
   ```

2. multiple uuid environment variable

   ```.environment
   UUID = "uuid1,uuid2,uuid3"
   ```

   note: uuid1, uuid2, uuid3 are separated by commas`,`.
   when you set multiple uuid, you can use `https://edtunnel.pages.dev/uuid1` to get the clash config and vless:// link.

## subscribe vless:// link (Optional)

1. visit `https://edtunnel.pages.dev/uuid your set` to get the subscribe link.

2. visit `https://edtunnel.pages.dev/sub/uuid your set` to get the subscribe content with `uuid your set` path.

   note: `uuid your set` is the uuid you set in UUID enviroment or `wrangler.toml`, `_worker.js` file.
   when you set multiple uuid, you can use `https://edtunnel.pages.dev/sub/uuid1` to get the subscribe content with `uuid1` path.(only support first uuid in multiple uuid set)

3. visit `https://edtunnel.pages.dev/sub/uuid your set/?format=clash` to get the subscribe content with `uuid your set` path and `clash` format. content will return with base64 encode.

   note: `uuid your set` is the uuid you set in UUID enviroment or `wrangler.toml`, `_worker.js` file.
   when you set multiple uuid, you can will use `https://edtunnel.pages.dev/sub/uuid1/?format=clash` to get the subscribe content with `uuid1` path and `clash` format.(only support first uuid in multiple uuid set)

## multiple port support (Optional)

   <!-- let portArray_http = [80, 8080, 8880, 2052, 2086, 2095];
	let portArray_https = [443, 8443, 2053, 2096, 2087, 2083]; -->

For a list of Cloudflare supported ports, please refer to the [official documentation](https://developers.cloudflare.com/fundamentals/reference/network-ports/).

By default, the port is 80 and 443. If you want to add more ports, you can use the following ports:

```text
80, 8080, 8880, 2052, 2086, 2095, 443, 8443, 2053, 2096, 2087, 2083
http port: 80, 8080, 8880, 2052, 2086, 2095
https port: 443, 8443, 2053, 2096, 2087, 2083
```

If you deploy in Cloudflare pages, https port is not supported. Simply add multiple ports node drictly use subscribe link, subscribe content will return all Cloudflare supported ports.

## Reason for Creating a New Repository
The decision to create a new repository, rather than forking from the original repository Kmfi6HP/EDtunnel, was due to the first source repository being unavailable. Since the GitHub account 'Kmfi6HP' is deleted, Cloudflare can't deploy from that repository. For Cloudflare access and deployment, it had to be a new repository; thus, it is the most viable option considering the situation.

## What improvements have been made ?
Some clean IPs for Iranian users has been added.

The early data (ed) value has been changed and is now set to 2560.

The path has changed to EDge-Bridge.

Thai texts in the code, have been translated to English (Google translate).

The formatting of configuration names has been updated.


