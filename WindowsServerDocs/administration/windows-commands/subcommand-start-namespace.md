---
title: Subcommand start-Namespace
description: Reference article for Subcommand start-Namespace, which starts a Scheduled-Cast namespace.
ms.prod: windows-server
ms.technology: manage-windows-commands
ms.topic: article
ms.assetid: 2dd1c11e-6ab7-4129-9e3a-3f80e0ba59c0
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/16/2017
---
# Subcommand: start-Namespace

> Applies to: Windows Server (Semi-Annual Channel), Windows Server 2019, Windows Server 2016, Windows Server 2012 R2, Windows Server 2012

Starts a Scheduled-Cast namespace.

## Syntax
```
wdsutil /start-Namespace /Namespace:<Namespace name[/Server:<Server name>]
```
### Parameters

|          Parameter          |                                                                                                                                                                                             Description                                                                                                                                                                                             |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /Namespace:<Namespace name| Specifies the name of the namespace. Note that this is not the friendly name, and it must be unique.<p>-   **Deployment Server**: The syntax for namespace name is /Namspace:WDS:<Image group>/<Image name>/<Index>. For example: **WDS:ImageGroup1/install.wim/1**<br />-   **Transport Server**: This name must match the name given to the namespace when it was created on the server. |
|   [/Server:<Server name>]   |                                                                                                           Specifies the name of the server. This can be either the NetBIOS name or the fully qualified domain name (FQDN). If no server name is specified, the local server will be used.                                                                                                           |

## Examples
To start a namespace, type one of the following:
```
wdsutil /start-Namespace /Namespace:Custom Auto 1
wdsutil /start-Namespace /Server:MyWDSServer /Namespace:Custom Auto 1
```
## Additional References
- [Command-Line Syntax Key](command-line-syntax-key.md)
[Using the get-AllNamespaces Command](using-the-get-allnamespaces-command.md)
[Using the new-Namespace Command](using-the-new-namespace-command.md)
[Using the remove-Namespace Command](using-the-remove-namespace-command.md)
