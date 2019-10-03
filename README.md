# Data Compression Primitives

This is my attempt to start mapping out the various data structures
and algorithms in Data Compression - what would be absolutely
right to have - for people to start using and writing out
their large data systems with the right primitives.

There has been plenty of code around, why isn't all of it in *ONE*
usable library? It is time for us, as people who write software, to think
about how we should build and get people to start using Data Compression
all the way at source.

## Call for Volunteers

As a person willing to implement it in a language of your choice, you should be
able to take that language, and implement all the functionality in this list to
be considered a useful library. This is a checklist, so tick off items
as and when you finish it.

When you are starting to implement your library, Clone/Fork this
repository as well. Create your repository for the language,
then link to it in this file in your fork, and send a pull-request.
I'll merge it.

## Plea for Readability

Code, at the end of the day should be easy to call AND easy to
read. The idea is not looking for the fastest implementation, but
for the most readable / modifiable implementation.

Surely there are enough fast implementations in the world, why
don't people write this kind of code?

## Thanks in Advance

Bless you for caring about the environment and making data
compression accessible to most programmers.

## List of Implementations - Status

- [DCP Java](https://github.com/DataCompressionPrimitives/DCP-Java) - WIP

## Checklist

### Bit I/O Library

- Read/Write to files or streams bit by bit.
   - [Example](https://github.com/naoya/perl-BitIO)

### Basic Primitives

- Bit
   - [Example](https://github.com/DataCompressionPrimitives/DCP-Java/blob/master/src/main/java/org/dcp/entities/bit/Bit.java)
- Bit Buffer
   - [Example](https://github.com/DataCompressionPrimitives/DCP-Java/blob/master/src/main/java/org/dcp/entities/bit/BitBuffer.java)
- Unsigned Integer
   - [Example](https://github.com/DataCompressionPrimitives/DCP-Java/blob/master/src/main/java/org/dcp/entities/primitives/UnsignedInteger.java)
- Integer
   - [Example](https://github.com/DataCompressionPrimitives/DCP-Java/blob/master/src/main/java/org/dcp/entities/primitives/Integer.java)
- Decimal
   - [Example](https://github.com/DataCompressionPrimitives/DCP-Java/blob/master/src/main/java/org/dcp/entities/primitives/Decimal.java)

### Variable Length Code Primitives

- Var Integer
   - [Example](https://github.com/DataCompressionPrimitives/DCP-Java/blob/master/src/main/java/org/dcp/entities/primitives/VarUnsignedInteger.java)
- Unary Integer
   - [Example](https://github.com/syohex/go-unary-coding/blob/master/unary.go)
- Elias Coded Integer (Gamme, Delta, Omega)
   - [Example](https://github.com/naoya/perl-integer-elias)
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/Omega.pm)
- Even Rodeh Coded Integer
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/EvenRodeh.pm)
- Golomb Coded Integer (Regular, Gamma, Exponential)
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/Golomb.pm)
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/GammaGolomb.pm) 
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/ExponentialGolomb.pm)
- Rice Coded Integer (Regular, Adaptive)
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/Rice.pm)
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/ARice.pm)
- Fibonacci Coded Integer
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/Fibonacci.pm)
- Boldi Vigna Zeta Coded Integer
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/BoldiVigna.pm)
- Taboo Coded Integer
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/Taboo.pm)
- Levenstein Coded Integer
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/Levenstein.pm)
- Comma Coded Integer
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/Comma.pm)
- Escape Coded Integer
   - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/Escape.pm)

### Large Integer Primitives

- Big Unsigned Integer
- Big Integer
- Big Decimal

### Array Primitives

- Array
  - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/BLVec.pm)
- Indexed Array
- Sparse Array

### Symbol Primitives

- Smaz Coded String
  - [Example](https://github.com/antirez/smaz)
- Varicode String
  - [Example](https://github.com/argilo/gr-ham/blob/master/python/varicode_rx.py)
- Morse Coded String
  - [Example](https://github.com/SeunMatt/morsecodetranslator/blob/master/src/main/java/com/smatt/morse/MorseCodeTranslator.java)
- Variable Name Coded String
- Symbol Table
- Trie

### Object Primitives

- Map SerDe
- Object SerDe

### Statistical and Adaptive Encoding

- Shannon Fano Coding and SerDe
  - [Example](https://github.com/jigar23/Entropycoding/tree/master/EntropyCoding/src/ShannonFano)
- Tunstall Coding and SerDe
- Huffman Tree Coding and SerDe
  - [Example](https://github.com/jigar23/Entropycoding/tree/master/EntropyCoding/src/Huffman)
- Arithmetic Encoding and SerDe
  - [Example](https://github.com/nayuki/Reference-arithmetic-coding/blob/master/java/src/ArithmeticCoderBase.java)
- ANS Encoding and SerDe
  - [Example](https://github.com/EhomeBurning/Asymmetric-Numeral-Systems/blob/master/main.cpp)
- Start-Stop Encoding and SerDe (Regular and Start-Step-Stop)
  - [Example](https://github.com/danaj/BitStream/blob/master/lib/Data/BitStream/Code/StartStop.pm)
- Delta Encoding and SerDe
  - [Example](https://en.wikipedia.org/wiki/Delta_encoding)
- Range Encoding and SerDe
  - [Example](https://github.com/apronchenkov/RangeCode/blob/master/coder.h)
- Roaring Bitmaps and SerDe
  - [Example](https://github.com/RoaringBitmap/RoaringBitmap)

### Contextual Encoding

- CABAC and SerDe
  - [Example](https://github.com/jigar23/CABAC)
- BWT and SerDe (Regular, SuffixTree)
  - [Example](https://github.com/egonelbre/fm-index/blob/master/src/bwt.py)
- ACB and SerDe
  - [Example](http://www.stringology.org/DataCompression/acb/index_en.html)
- DMC and SerDe
  - [Example](https://github.com/sporkmonger/squish/blob/master/src/lib/state.ml)
- CTW and SerDe
  - [Example](https://github.com/gabeschamberg/context-tree-weighting/blob/master/ctw.py)
- PPM and SerDe
  - [Example](https://github.com/gosoares/ITI-PPM/blob/master/PpmEncoder.kt)
- RLE and SerDe
  - [Example](https://github.com/powturbo/TurboRLE)
- MTF and SerDe
  - [Example](https://github.com/liam60/MTFEncoder/blob/master/WordList.java)

### Dictionary Encoding

- Byte Pair Encoding and SerDe
  - [Example](https://github.com/soaxelbrooke/python-bpe)
- N-Gram Coding and SerDe + Variants
  - [Example](https://github.com/yassineameur/one_hot_encoder)
- LZ Encoding and SerDe + Variants
  - [Example](https://github.com/gusrsilva/Lempel-Ziv-Welch-Compression/blob/master/src/ZivLempel.java)
- ZStandard and SerDe + Variants
  - [Example](https://github.com/noop-dev/Zstandard/blob/master/java/src/main/java/rtmath/zstd/ZstdDecompressor.java)
- Snappy Encoding and SerDe
  - [Example](https://github.com/dain/snappy/blob/master/src/main/java/org/iq80/snappy/SnappyCompressor.java)
- Brotli and SerDe + Variants
  - [Example](https://github.com/dominikhlbg/BrotliHaxe/blob/master/python/brotli.py)

### Iterators

- ZigZag Iterator
- Slurm Iterator
- Interleaving Iterator

### Lossy Encoding

- Dimensional Sampler and SerDe
- Eigenvalue Sampler and SerDe
- HyperLogLog Sampler and SerDe
- Dynamic Range Transformer and SerDe
- Differencial Transformer and SerDe
- Exponential Range Transformer and SerDe
- Clustering Transformer and SerDe
- Banding Transformer and SerDe
- Scalar Quantizer and SerDe
- Vector Quantizer and SerDe
- Fractal Transformer and SerDe
- Periodic Wave Transformers (Fourier, DCT, etc) and SerDe
- Polynomial Equation Quantizer and SerDe
- Bloom Filter Quantizer and SerDe
- Regression / Learning Transformer and SerDe

### Specialized Data Encoding

- Color Format Convertor (Frequency/Intensity, HSV, RGV etc)
- Wave Generator (Sample, Frequency, Intensity)
- Motion Predictor (Video)
- Background Value Finder (DJVU)
- Shape Binner (DJVU, Potrace)
- Stream Delta Encoder
  - [Example](https://github.com/eerimoq/detools)

## References for Reading

- [The Data Compression Book](https://www.amazon.com/Data-Compression-Book-Mark-Nelson/dp/1558514341)
- [Data Compression: The Complete Reference](https://www.amazon.com/Data-Compression-Reference-David-Salomon/dp/1846286026)
- [Understanding Compression: Data Compression for Modern Developers](https://www.amazon.com/Understanding-Compression-Data-Modern-Developers-ebook/dp/B01IE1C9B4)
- [Introduction to Data Compression](https://www.amazon.com/Introduction-Compression-Kaufmann-Multimedia-Information/dp/0128094745)
- [Introduction to Information Theory and Data Compression](https://archive.org/details/introductiontoin0000hank)
- [Managing Gigabytes](https://www.amazon.com/Managing-Gigabytes-Compressing-Multimedia-Information/dp/1558605703)
- [Data Compression Explained](http://mattmahoney.net/dc/dce.html)
- [Wikipedia](https://en.wikipedia.org/wiki/Data_compression)

## Conclusion

It is my idea that we should get enough people to implement these
in multiple languages, and eventually that we get wire-readability
across these implementations. I thank you for your time and effort spent in
reading through this. I would really appreciate any help I can get in spreading
the word.
