---
title: "Modding"
weight: 6
---

OpenNox provides a lot of tooling for modding the game. Some of it is still in development.

The `noxtools` binary provides useful commands for modding the game and extracting assets. It is located in the [opennox/libs](https://github.com/opennox/libs) repository under the `noxtools` folder. To build it, run `go build ./cmd/noxtools` from the root of the repository. To install the `noxtools` binary to `~/go/bin`, `go install github.com/opennox/libs/cmd/noxtools@latest` can be run.

{{% children sort="weight" %}}
