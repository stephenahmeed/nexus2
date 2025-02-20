# Nexus Network CLI For Mobile/PC

## Installation Guide

### Step 1: Create and Navigate to Directory
```sh
mkdir nexus-cli
cd nexus-cli
```

### Step 2: Install Rust
```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustup target add riscv32i-unknown-none-elf
source $HOME/.cargo/env
```

### Step 3: Install Dependencies
```sh
sudo apt update
sudo apt install pkg-config libssl-dev
sudo apt install protobuf-compiler
```

### Step 4: Install Nexus CLI
```sh
curl https://cli.nexus.xyz/ | sh
```

### Step 5: Get Node ID
Retrieve your Node ID from the Node section: [Nexus Beta](https://beta.nexus.xyz/)

---

## Restarting Nexus CLI
To restart, simply run:
```sh
curl https://cli.nexus.xyz/ | sh
```

---

## Troubleshooting

### Error: `=proto -- experimental_allow_proto3_optional orchestrator.proto`
If you encounter this error, run the following commands one by one:

```sh
sudo apt-get remove -y protobuf-compiler
wget https://github.com/protocolbuffers/protobuf/releases/download/v30.0-rc1/protoc-30.0-rc-1-linux-x86_64.zip
sudo unzip protoc-30.0-rc-1-linux-x86_64.zip -d /usr/local/
sudo chmod +x /usr/local/bin/protoc
```

---

## Multi-Device Usage
You can use Nexus CLI on multiple devices without issues.

---

## License
This repository is open-source and follows the MIT License.
