### Technical Requirements

To operate as a validator, nodes must meet the following minimum specifications:

Hardware Requirements:
- CPU: 8+ core processor
- RAM: 16GB minimum
- Network: 100Mbps stable connection
- For GPU mode: Nvidia GPU with at least 4GB VRAM

Software Requirements:
- Linux-based operating system
- CUDA for GPU mode

If you want to compile the binary by yourself and test it locally:
- Docker environment
- Rust, cargo and Risc0 installed

Other Requirements:
- RPC url for Holesky network
- websocket url for Holesky network
- Beacon chain API url for Holesky network (available on chainstack for free)
- Private key with funds on Holesky

Security Requirements:
- Hardware security module (HSM) for key management
- DDoS protection
- Redundant network connectivity
- Regular security audits
