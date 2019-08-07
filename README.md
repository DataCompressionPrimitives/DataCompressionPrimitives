# Data Compression Primitives

Now you should be able to take a language *A* of choice and
implement all of the functionality in this list to be 
considered a useful library.

What is the process for it? Clone/Fork this repository. Create
your repository for the language, then link to it in this file
in your fork, and send a pull-request. I'll merge it.

Sometimes you don't need to re-invent the wheel, just need to
copy pasta and spice it. Sometimes you need to restructure and
refactor it a bit to support more types, or come up with ideas
on how to support those types. Nevertheless, it's helpful.

Code, at the end of the day should be easy to call AND easy to
read. The idea is not looking for the fastest implementation, but
for the most readable implementation. Surely there are enough fast
implementations in the world, why don't people write this kind
of code?

Bless you for caring about the environment and making data
compression accessible to most programmers.

## List of Implementations

None.

## Bit I/O Libraries

- Read/Write to files bit by bit.
   - Example implementation: https://github.com/naoya/perl-BitIO

## Serialization Format for Elementary Types

- Portable Binary Format on Wire with JumpTo Semantics

## Bit Encoding Symbols

- Shannon Fano Coding and SerDe + Variants
- Huffman Tree Coding and SerDe
- Arithmetic Encoding and SerDe
- ANS Encoding and SerDe
- CABAC Encoding and SerDe
- Range Encoding and SerDe
- Unary Coding and SerDe
- Golomb Coding and SerDe + Variants
- Tunstall Coding and SerDe
- Elias Coding and SerDe + Variants
- Even Rodeh Coding and SerDe 
- Variable Length Coding and SerDe
- Fibonacci Coding and SerDe
- Levenhstein Coding and SerDe

## Dictionary Encoding

- BWT Encoding and SerDe
- Trie Implementation for Symbol Lookups
- Byte Pair Encoding and SerDe
- Byte Offset Encoding and SerDe
- On Wire Format for Symbols, Flush and Add Symbol and SerDe
- N-Gram Coding and SerDe + Variants
- LZ Encoding and SerDe + Variants
- Snappy Encoding and SerDe
- Brotli and SerDe + Variants
- ZStandard and SerDe + Variants

## Range Compression

- Roaring Bitmap Iterator and SerDe
- ZigZag Iterator
- Slurm Iterator
- Sampling Iterator

## Lossy Encoding

- Range Transformer and SerDe
- Exponential Range Transformer and SerDe
- Clustering Transformer and SerDe
- Quantizer Transformer and SerDe
- X Dimensional Sampling and SerDe
- Eigenvalue Sampling and SerDe
- HyperLogLog Sampling and SerDe
- Fractal Transformer and SerDe
- Deep Learning Transformer and SerDe
- Periodic Wave Transformers and SerDe
- Polynomial Equation Quantizer and SerDe
- Bloom Filter Quantizer and SerDe

## Specialized Data Generation

- Color Formats Converter (Frequency/Intensity, HSV, RGV etc) and SerDe
- Color Quantizer and SerDe
- Sound Tone Generator and SerDe (Sample, Frequency, Intensity)
- Sound Wave Quantizer and SerDe

## Conclusion

This is my attempt to start mapping out what would be absolutely
necessary to have, for people to start using, when writing out
their large data systems.

This may look like pie in the sky, but yes, there has been plenty
of code around, why isn't all of it in *ONE* usable library? It
is time for you to think about how we can evangelize this.
