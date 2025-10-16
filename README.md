# Random-

## Level-0 Block Diagram
```mermaid
graph TD
    A[SW11_0  12-bit Binary Input] -->|Binary to BCD Conversion| B[bin12_to_bcd16.v]
    B -->|4-Digit BCD Output| C[mux4_nibble.v  4-to-1 Nibble Multiplexer]
    C -->|Selected BCD Digit| D[bcd7seg.v  BCD to 7-Segment Decoder]
    D -->|7-Segment Cathode Signals| E[Seven-Segment Display Cathodes a-g]
    C -->|Digit Select| F[refresh_gen.v  Refresh Generator]
    F -->|Time-Division Multiplexing| G[Anode Control AN3-AN0]
    E -->|Display Output| H[Basys3 4-Digit Display]
    G --> H

```



