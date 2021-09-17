Pure PHP UUID generator

Dual-licensed under BSDL (2-clause) or Apache 2.0 license 

# Important Note (Mario DE WEERD):

The original library incorrectly generates random UUIDs.
The [RFC4122](https://datatracker.ietf.org/doc/html/rfc4122#section-4.4) requires that the two most significant bits of `clock_seq_hi...` are as in `0b10xx_xxxx`, but the original code generated a random number for that byte in the range 0..177.

As a result half of the generated random UUIDs (Version 4) were not compliant.
This is fixed in this version.
