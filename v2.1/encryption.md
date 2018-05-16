---
title: Encryption At Rest
summary: Encryption At Rest encrypts node data on local disk transparently.
toc: false
---

<span class="version-tag">New in v2.1:</span>
Encryption At Rest provides transparent encryption for node data on local disk.

<div id="toc"></div>

## Terminology

## Example

Create store key:
{% include copy-clipboard.html %}
~~~ shell
$ openssl rand -out /path/to/my/aes-128.key 48
~~~

Start node in AES-128 mode:
{% include copy-clipboard.html %}
~~~ shell
$ cockroach start --store=cockroach-data --enterprise-encryption=path=cockroach-data,key=/path/to/my/aes-128.key,old-key=plain
~~~

## See Also

