## How Does Elliptical Curve Cryptography Work?
There are many modern encryptions algorithms. Each of which have their own strengths. Elliptical curve cryptpgraphy is a family of algorithms that are based upon elliptical curves. Most commonly these algorithms are seen in blockchains in the forms of private keys and public keys.

### What is Elliptical Curve Cryptography?

The elliptical curve is used by Bitcoin, Ethereum, and many other cryptocurrencies. Specifically they use the secp256k1 curve, which has the equation basic equation:  

<a href="https://www.codecogs.com/eqnedit.php?latex=y^2=x^3&plus;7" target="_blank"><img src="https://latex.codecogs.com/gif.latex?y^2=x^3&plus;7" title="y^2=x^3+7" /></a>

This equation is used to find the public key based upon a value (your private key) multiplied by a point on a curve. Which for Bitcoin that point is: 

x-coordinate: 55066263022277343669578718895168534326250603453777594175500187360389116729240

y-coordinate: 32670510020758816978083085130507043184471273380659243275938904335757337482424

Then in order to make sure the resulting values can fit in 512-bit public keys, both sides of the equation are modded by the largest prime number below 2^256, being 1.15792089237316195423570985008687907853269984665640564039457584007913129639747 × 10^77, meaning the reminder is found by dividing both sides by the previous number.
