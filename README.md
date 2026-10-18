# Mastermind P2P Testing

A peer-to-peer implementation of Mastermind with dynamic broadcast discovery, standard TCP gameplay, and reliable UDP cost-cutting transport.

## Build

```bash
make clean && make
```

This compiles cleanly with `-Wall -Wextra -Werror` on Linux (WSL2/Ubuntu) and macOS (Apple Clang).

## Run

### 1. Standard Mode (TCP)
```bash
./mastermind
```

### 2. Cost-Cutting Mode (Reliable UDP)
```bash
./mastermind --cost-cutting
```

### 3. With Logging
```bash
./mastermind --log
# or combine flags:
./mastermind --cost-cutting --log
```

## How to Test
1. Both players run `./mastermind` on the same Wi-Fi network or mobile hotspot.
2. Enter your name when prompted.
3. Once in the lobby, discovered players will appear under **Players Online**.
4. Type `challenge <ID>` to challenge a peer.
5. If challenged, type `yes` to accept.
6. The Codemaker (Mastermind) sets a 5-digit code (digits `0`-`9`).
7. The Codebreaker enters attempts and receives feedback (`x` = correct position, `o` = correct digit wrong position, `-` = absent).
