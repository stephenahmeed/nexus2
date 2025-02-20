# Nexus Prover Node
You earn NEX Points by contributing compute and interacting with the Nexus ecosystem.
---

## --> Create account
* Create an account at https://app.nexus.xyz.
---

## --> Contribute via Web browser
Login into the dashboard and press the button to start your node

https://app.nexus.xyz/

- You can run prover nodes on multiple browser tabs, desktops, laptops, mobile phones.
- Link and manage all your devices from a single Nexus account.
- More computations = More NEX points

### 1. Install Dependecies
```bash
sudo apt update & sudo apt upgrade -y
sudo apt install screen curl libssl-dev pkg-config build-essential git-all protobuf-compiler -y
sudo apt update
```
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
```bash
source $HOME/.cargo/env
```
```bash
rustup target add riscv32i-unknown-none-elf
```
```bash
rustup target add riscv32i-unknown-none-elf
```
```bash
cargo config --global set build.unstable-features true
```

### 2. Run Prover
**1- Start a screen to keep it running in the background**
```bash
screen -S nexus
```
**2- Install and run prover**
```bash
curl https://cli.nexus.xyz/ | sh
```

### 3. Link Node
1- After installation command completes, it asks you if you want to link your node press `2`
![image](https://github.com/user-attachments/assets/603d8a8e-5be5-485d-b4b8-76a9639aa836)

2- Enter you `node-id`
* To find your `node-id`, go  to https://app.nexus.xyz/nodes
* Click `Add Node`, click `Add CLI Node` and copy your `node-id` and paste in terminal

![image](https://github.com/user-attachments/assets/754e4b13-9400-4108-9c3f-b0bba6c40132)


### 4. Manage your Node screen:
* To minimze the screen: `CTRL+A+D`

* To return to screen: `screen -r nexus`

* To kill screen: `screen -XS nexus quit`

---

Showing Error like this  ?  --experimental_allow_proto3_optional, 

Input and try 

```bash
sudo apt-get remove -y protobuf-compiler && \
wget https://github.com/protocolbuffers/protobuf/releases/download/v30.0-rc1/protoc-30.0-rc-1-linux-x86_64.zip && \
unzip protoc-30.0-rc-1-linux-x86_64.zip -d /usr/local/ && \
sudo chmod +x /usr/local/bin/protoc
```
