# Sapling Woodchipper

<table border=1>
<tr>
<th>Name</th>
<th>Symbol</th>
<th>Price (USD)</th>
<th>Price (EUR)</th>
<th>Price (BTC)</th>
<th>Market Cap</th>
<th>Daily Attack Cost (USD)</th>
<th>Daily Attack Cost (EUR)</th>
<th>Daily Attack Cost (BTC)</th>
</tr>
<tr>
<td><a href="https://z.cash">Zcash</a></td>
<td>ZEC</td>
<td id="zecpriceusd"></td>
<td id="zecpriceeur"></td>
<td id="zecpricebtc"></td>
<td id="zecmcap"></td>
<td id="zeccostusd"></td>
<td id="zeccosteur"></td>
<td id="zeccostbtc"></td>
</tr>
</table>

## Zcash Protocol-Level Denial-of-Service (CVE-2019-11636)

![Sapling Woodchipper](https://saplingwoodchipper.github.io/sapling-woodchipper.png)

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.js"> </script>
<script>
    $( document ).ready(function() {
        $.ajax({
            url: "https://api.coingecko.com/api/v3/simple/price?ids=zcash&vs_currencies=BTC%2CUSD%2CEUR&include_market_cap=true&include_24hr_vol=true",
            type: "GET",
            dataType : "json",
        })
        .done(function( json ) {
            console.log(json);
            $('#zecpriceusd').html( "$" + json.zcash.usd.toFixed(2) );
            $('#zecpriceeur').html( "$" + json.zcash.eur.toFixed(2) );
            $('#zecpricebtc').html( json.zcash.btc.toFixed(4) + " BTC" );
            $('#zecmcap').html( "$" + Math.round( json.zcash.usd_market_cap / 1000000 ) + "M" );
            $('#zeccostusd').html( "$" + (json.zcash.usd * 0.0001 * 576).toFixed(2) );
            $('#zeccosteur').html( (json.zcash.eur * 0.0001 * 576).toFixed(2) + " EUR" );
            $('#zeccostbtc').html( (json.zcash.btc * 0.0001 * 576).toFixed(8) + " BTC" );
        })
        .fail(function( xhr, status, errorThrown ) {
            alert( "Ooops, error talking to Coingecko!");
            console.log( "Error: " + errorThrown );
            console.log( "Status: " + status );
            console.dir( xhr );
        })
        .always(function( xhr, status ) {
            console.log("Finished!");
        });
    });
</script>
Sapling Woodchipper Loves Supple Saplings


The Sapling Woodchipper is a protocol-level Denial-of-Service against any
cryptocoin which implements the Zcash 2.x Sapling protocol, most notably Zcash
(ZEC) itself.

The exact severity of the DoS depends on the exact chain parameters of each
coin.

It's currently estimated that there are many dozens of blockchains which have
Sapling transactions enabled and various older Zcash forks with Sprout
technology planning to upgrade.

The Sapling Woodchipper is spiritually similar to the
[Slowloris attack](https://en.wikipedia.org/wiki/Slowloris_(computer_security)),
in that one or a few machines can completely disable much more powerful entity
in a vastly asymmetric attack. In this analogy, long-lived HTTP connections
become extremely large transactions, and instead of taking down a webserver,
making it unable to process requests, a blockchain is completely filled to the
point that no normal users can make transactions. This is a very focused
attack, like the Slowloris. Unlike the Slowloris attack, the Sapling
Woodchipper is very CPU intensive, and as such, the attack benefits greatly
from more powerful CPUs. In this sense, the Sapling Woodchipper takes a lot
more work than Slowloris, which merely waits the maximum time before
successfully ending a request.

Sapling Woodchipper has been assigned [CVE-2019-11636](https://nvd.nist.gov/vuln/detail/CVE-2019-11636).

## Details

More Details Coming Real Soon 

## References

...

## Updating this website

This website is very easy to update. You can use the [editor on GitHub](https://github.com/saplingwoodchipper/saplingwoodchipper.github.io/edit/master/README.md) to maintain and preview the content of this website. Patches welcome!

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

## LICENSE

GPLv3

## Official Site

[https://saplingwoodchipper.github.io](https://saplingwoodchipper.github.io)

## Author

Duke Leto [Keybase](https://keybase.io/dukeleto)

