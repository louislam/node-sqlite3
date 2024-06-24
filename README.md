# node-sqlite3 with ARMv7 and CentOS 7 support

Mainly used for my another project - [Uptime Kuma](https://github.com/louislam/uptime-kuma)

## What is the different between TryGhost/node-sqlite3?

The official one is dropped the support for CentOS 7, but my fork supports CentOS 7.

This fork also provides ARMv7 prebuilt.

If you want to build a Node.js application which can be installed on many Linux distributions like Uptime Kuma, this library should be useful.

If your application will be just designed for new Linux distributions, you probably do not need it, just use the official one.


PS: No electron supports

## How to use

```
npm install @louislam/sqlite3
npm remove sqlite3
```

Replace require("@louislam/sqlite") in your source code

## Documentation

https://github.com/TryGhost/node-sqlite3

## (For Maintainers/Developers Only) 

###Prepare Prebuilt

#### glibc & musl

```bash
npm run build-binaries
```

All files in ./build after built.

glibc
- armv7 - npm run build-linux-arm (Support glibc >=2.18 only)
- amd64/arm64 - npm run build-linux

musl (alpine)
- armv7/arm64/amd64 - npm run build-linux-alpine

#### Windows / MacOS
- Get from Github Action

#### Mac ARM64 (M1/M2)
- Get from TryGhost/node-sqlite3
- Rename to `napi-v6-darwin-arm64-unknown.tar.gz`
- Use 7zip to rename the folder inside to `napi-v6-darwin-arm64`
