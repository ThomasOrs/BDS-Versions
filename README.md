# Minecraft BDS versions

This repository acts as an automatic archive of BDS versions.
You can consume the `versions.json` file to get the stable build
and a history of versions.

An example to get the latest stable build:

```bash
#!/bin/bash

LATEST_VERSION=`curl -s https://raw.githubusercontent.com/ScriptAPIOSS/BDS-Versions/main/versions.json | jq -r '.linux.stable'`

echo "The latest Linux BDS is [${LATEST_VERSION}]"

DOWNLOAD_URL=`curl -s https://raw.githubusercontent.com/ScriptAPIOSS/BDS-Versions/main/linux/${LATEST_VERSION}.json | jq -r '.download_url'`

wget ${DOWNLOAD_URL}
```
Latest Linux: `1.19.30.04`

Latest Windows: `1.19.30.04`
