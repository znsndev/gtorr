# gtorr

**A from-scratch, dependency-free BitTorrent client written in Go (Golang).**

`gtorr` is a pet project created with a single goal: to deeply understand the BitTorrent protocol, network programming, and concurrency patterns in Go by building a complete client without any external dependencies for the core functionality.

## 🚧 Project Status: Early MVP

This project is currently under active development. The current milestone is **MVP**:
- [ ] Bencode decoder
- [ ] .torrent file parser
- [ ] HTTP tracker communication
- [ ] Peer wire protocol handshake
- [ ] Downloading and verifying a single piece
- [ ] Multi-peer download
- [ ] File assembly
- [ ] Seeding (uploading)

## 🛠️ Tech Stack

*   **Language:** Go (aiming for compatibility with the latest stable version)
*   **Philosophy:** Zero external dependencies (only the Go standard library).
*   **Core Packages Used:** `net`, `io`, `crypto/sha1`, `encoding/binary`, `sync`, `context`.

## 📁 Project Structure

```text
gtorr/
├── cmd/
│   └── gtorr/          # CLI application entry point
│       └── main.go
├── internal/           # Private application code
│   ├── torrentfile/    # .torrent file metadata handling
│   ├── tracker/        # HTTP tracker client
│   ├── peer/           # Peer connection and management
│   └── message/        # Peer wire message serialization
├── pkg/                # Publicly reusable libraries (empty for now)
│   └── bencode/        # Bencode decoding/encoding
├── downloads/          # Default directory for downloaded files
├── .gitignore
├── LICENSE
├── README.md
└── go.mod
```

## 🚀 Getting Started

### Prerequisites
- Go 1.21+ (or a recent stable version)


### Installation
1. Clone the repository:
```bash
git clone https://github.com/znsndev/gtorr.git
cd gtorr
```

2. Build the binary:
```bash
go build -o gtorr ./cmd/gtorr
```

## 📚 Learning Resources

This project would not be possible without the excellent documentation of the BitTorrent protocol:

- [BitTorrent Protocol Specification (BEP 3)](https://www.bittorrent.org/beps/bep_0003.html)
- [Theory.org BitTorrent Spec](https://wiki.theory.org/BitTorrentSpecification)
- [BitTorrent Enhancement Proposals (BEPs) Index](https://www.bittorrent.org/beps/bep_0000.html)

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.