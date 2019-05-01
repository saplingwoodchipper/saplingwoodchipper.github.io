# Sapling Woodchipper

## Zcash Protocol-Level Denial-of-Service (CVE-2019-11636)

![Sapling Woodchipper](https://saplingwoodchipper.github.io/sapling-woodchipper.png)

The Sapling Woodchipper is a protocol-level Denial-of-Service against any cryptocoin which implements the Zcash 2.x Sapling protocol, most notably Zcash (ZEC) itself.

The exact severity of the DoS depends on the exact chain parameters of each coin, but the following is a partial list of coins known
to support Sapling transactions and lack mitigations:

* Zcash (ZEC)

Coins known to have Sapling enabled and have mitigations in-place:

* Hush (HUSH)
* Pirate (ARRR)

Please note these are not exhaustive lists. It's currently estimated that there are many dozens of blockchains which have Sapling
transactions enabled and various older Zcash forks with Sprout technology planning to upgrade.

The Sapling Woodchipper is spiritually similar to the [Slowloris attack](https://en.wikipedia.org/wiki/Slowloris_(computer_security)),
in that one or a few machines can completely disable much more powerful entity in a vastly asymmetric attack. In this analogy, long-lived HTTP connections become extremely large transactions, and instead of taking down a webserver, making it unable to process requests, a blockchain is completely filled to the point that no normal users can make transactions. This is a very focused attack, like the Slowloris.

Sapling Woodchipper has been assigned [CVE-2019-11636](https://nvd.nist.gov/vuln/detail/CVE-2019-11636).

## 

## References

...

## Updating this website

This website is very easy to update. You can use the [editor on GitHub](https://github.com/saplingwoodchipper/saplingwoodchipper.github.io/edit/master/README.md) to maintain and preview the content of this website. Patches welcome!

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

## LICENSE

GPLv3

## Author

Duke Leto https://keybase.io/dukeleto
