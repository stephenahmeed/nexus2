# Nexus Network CLI For Mobile/PC

## Installation Guide

### Step 1: Create and Navigate to Directory
```sh
mkdir nexus-cli
```
```sh
cd nexus-cli
```

### Step 2: Install Rust
```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
```sh
rustup target add riscv32i-unknown-none-elf
```
```sh
source $HOME/.cargo/env
```

### Step 3: Install Dependencies
```sh
sudo apt update
```
```sh
sudo apt install pkg-config libssl-dev
```
```sh
sudo apt install protobuf-compiler
```

### Step 4: Install Nexus CLI
```sh
curl https://cli.nexus.xyz/ | sh
```

### Step 5: Get Node ID
Take your Node ID from the Node section: [Nexus Beta](https://app.nexus.xyz/nodes)

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
```
```sh
wget https://github.com/protocolbuffers/protobuf/releases/download/v30.0-rc1/protoc-30.0-rc-1-linux-x86_64.zip
```
```sh
sudo unzip protoc-30.0-rc-1-linux-x86_64.zip -d /usr/local/
```
```sh
sudo chmod +x /usr/local/bin/protoc
```
### Error 2: If this error coming Killed or memory allocation of 8606711792 bytes failed Aborted (core dumped).

Then use this command

```sh
sudo fallocate -l 10G /swapfile && sudo chmod 600 /swapfile && sudo mkswap /swapfile && sudo swapon /swapfile && echo ‘/swapfile none swap sw 0 0’ | sudo tee -a /etc/fstab
```
---

### Another Way

## Update and Install Dependencies
```sh
sudo apt update && sudo apt upgrade -y
sudo apt install build-essential curl git pkg-config libssl-dev protobuf-compiler unzip -y
```

## Install Protobuf Compiler
```sh
PROTOC_ZIP=protoc-21.12-linux-x86_64.zip
curl -OL https://github.com/protocolbuffers/protobuf/releases/download/v21.12/$PROTOC_ZIP
sudo unzip -o $PROTOC_ZIP -d /usr/local bin/protoc
sudo unzip -o $PROTOC_ZIP -d /usr/local 'include/*'
rm -f $PROTOC_ZIP
```

## Install Rust
```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source $HOME/.cargo/env
rustup update
```

## Set Up Environment Variables
```sh
echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

## Clone Nexus Repository
```sh
rm -rf ~/.nexus
git clone https://github.com/nexus-xyz/nexus-zkvm ~/.nexus
cd ~/.nexus
```

## Install Nexus CLI
```sh
curl https://cli.nexus.xyz/ | sh
```
Then type `2` and enter your CLI code.

## Fix Byte Error (If Needed)
If you encounter a byte error, run the following command:
```sh
sudo fallocate -l 10G /swapfile && sudo chmod 600 /swapfile && sudo mkswap /swapfile && sudo swapon /swapfile && echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
```




## Multi-Device Usage
You can use Nexus CLI on multiple devices without issues.

---

## License
This repository is open-source and follows the MIT License.
