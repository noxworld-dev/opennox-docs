---
title: "Remote SSH console"
menuTitle: "SSH / RCON"
weight: 3
---

Vanilla Nox supported a telnet-based remote console (RCON) which allowed controlling Nox server remotely.

OpenNox has dropped telnet support in favor of SSH-based remote console.

{{% notice info %}}
OpenNox only _emulates_ SSH protocol. It **does not** allow accessing the host machine via SSH.
{{% /notice %}}

To enable RCON, OpenNox must be started with an additional argument:

```shell
opennox --rcon=:18522 --rcon-pass=my-secret-password
```

This will allow SSH connections on port `18522` with a password `my-secret-password`:

{{< tabs >}}
{{% tab title="Linux" %}}
```shell
ssh -p 18522 127.0.0.1
```
{{% /tab %}}
{{% tab title="Windows" %}}
See [this tutorial](https://learn.microsoft.com/en-us/windows/terminal/tutorials/ssh)

```shell
ssh -p 18522 127.0.0.1
```

Or install [PuTTY](https://putty.org/) and connect to `127.0.0.1:18522` with any username and password `my-secret-password`.
{{% /tab %}}
{{< /tabs >}}

```

  /888888                                /88   /88           /88   /88
 /88__  88                              | 888 | 88          | 88  / 88
| 88  \ 88  /888888   /888888  /8888888 | 8888| 88  /888888 |  88/ 88/
| 88  | 88 /88__  88 /88__  88| 88__  88| 88 88 88 /88__  88 \  8888/
| 88  | 88| 88  \ 88| 88888888| 88  \ 88| 88  8888| 88  \ 88  >88  88
| 88  | 88| 88  | 88| 88_____/| 88  | 88| 88\  888| 88  | 88 /88/\  88
|  888888/| 8888888/|  8888888| 88  | 88| 88 \  88|  888888/| 88  \ 88
 \______/ | 88____/  \_______/|__/  |__/|__/  \__/ \______/ |__/  |__/
          | 88
          | 88        Version: v1.9.x (xxxxxxxxx)
          |__/

user@opennox:~$
```

From here, all [console commands]({{% relref "opennox/dev/console" %}}) will work the same way as via in-game console.
A good starting point is a `help` command.
