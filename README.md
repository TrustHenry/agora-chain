# Agora Mainnet

- [Abort](#abort)

- [Install Docker Engine](#install-docker-engine)

- [For Linux or MacOS users](#for-linux-or-macos-users)
  - [Install](#install-for-linux-or-macos)
  - [Execution Layer](#execution-layer-for-linux-or-macos)
  - [Consensus Layer](#consensus-layer-for-linux-or-macos)
  - [Using docker-compose](#using-docker-compose-for-linux-or-macos)


- [For Windows users](#for-windows-users)
  - [Install](#install-for-windows)
  - [Execution Layer](#execution-layer-for-windows)
  - [Consensus Layer](#consensus-layer-for-windows)
  - [Using docker-compose](#using-docker-compose-for-windows)

## Abort
[Agora-el](https://github.com/bosagora/agora-el) is an execution client that has an EVM.  
Agora-el was forked from Ethereum's execution client, [ethereum/go-ethereum](https://github.com/ethereum/go-ethereum) version 1.10.23.  
We implemented the function of issuing commons budget in Agora-el.

[Agora-cl](https://github.com/bosagora/agora-cl) is a consensus client with a focus on usability, security, and reliability.  
Agora-cl was forked from Ethereum's consensus client, [prysmaticlabs/prysm](https://github.com/prysmaticlabs/prysm) version 3.1.1.  
We modified the block confirmation rewards in Agora-cl.

## Install Docker Engine

To run the Agora node, you must first install the Docker Engine.  
See [here](https://docs.docker.com/engine/install/) for instructions on how to install the Docker Engine  
https://docs.docker.com/engine/install/

## For Linux or MacOS users

### Install for Linux or MacOS

```shell
wget https://file.bosagora.io/chain/agora-chain-mainnet.zip -O mainnet.zip
unzip mainnet.zip
cd agora-chain-mainnet
```

### Execution Layer for Linux or MacOS

Init execution node

```shell
./agora.sh el-node init
```

Run execution node

```shell
./agora.sh el-node run
```


### Consensus Layer for Linux or MacOS


Run consensus node

```shell
./agora.sh cl-node run
```

### Validator for Linux or MacOS

Import your key stores

```shell
./agora.sh validator accounts import <your key stores folder>
```

List your key stores

```shell
./agora.sh validator accounts list
```

Run validator

```shell
./agora.sh validator run
```

Voluntary exit of the validator

```shell
./agora.sh validator accounts voluntary-exit
```

### Using docker-compose for Linux or MacOS

1. Init the execution node
```shell
./agora.sh el-node init
```

2. Import your key stores
```shell
./agora.sh validator accounts import <your key stores folder>
```

3. Edit wallet password
```shell
nano ./root/config/cl/password.txt
```

4. Edit transaction fee receiving address
```shell
nano ./root/config/cl/proposer_config.json
```

5. Run docker-compose
```shell
./agora.sh docker-compose up
```

6. Stop docker-compose
```shell
./agora.sh docker-compose down
```

### Using docker-compose with monitoring for Linux or MacOS

1. Init the execution node
```shell
./agora.sh el-node init
```

2. Import your key stores
```shell
./agora.sh validator accounts import <your key stores folder>
```

3. Edit wallet password
```shell
nano ./root/config/cl/password.txt
```

4. Edit transaction fee receiving address
```shell
nano ./root/config/cl/proposer_config.json
```

5. Run docker-compose
```shell
./agora.sh docker-compose-monitoring up
```

6. Stop docker-compose
```shell
./agora.sh docker-compose-monitoring down
```

7. Monitoring
   Launch the URL below to view the login page.  
   The initial ID is admin. The password is admin.  
   Please make sure to change your account and password.  
   http://localhost:3000
   The following screens are prepared.  
   http://localhost:3000/d/FDX6YtOiz/geth-node-dashboard-feb-2022?orgId=1&refresh=10s  
   http://localhost:3000/d/bosagora2023/boa-staking-dashboard?orgId=1&refresh=1m  
   http://localhost:3000/d/rYdddlPWk/node-exporter-full?orgId=1&refresh=1m  

## For Windows users


### Install for Windows

```shell
curl https://file.bosagora.io/chain/agora-chain-mainnet.zip --output mainnet.zip
tar -xf mainnet.zip
cd agora-chain-mainnet
```

### Execution Layer for Windows

Init execution node

```shell
agora.bat el-node init
```

Run execution node

```shell
agora.bat el-node run
```


### Consensus Layer for Windows


Run consensus node

```shell
agora.bat cl-node run
```

### Validator for Windows

Import your key stores

```shell
agora.bat validator accounts import <your key stores folder>
```

List your key stores

```shell
agora.bat validator accounts list
```

Run validator

```shell
agora.bat validator run
```

Voluntary exit of the validator

```shell
agora.bat validator accounts voluntary-exit
```

### Using docker-compose for Windows

1. Init the execution node
```shell
agora.bat el-node init
```

2. Import your key stores
```shell
agora.bat validator accounts import <your key stores folder>
```

3. Edit wallet password
```shell
notepad ./root/config/cl/password.txt
```

4. Edit transaction fee receiving address
```shell
notepad ./root/config/cl/proposer_config.json
```

5. Run docker-compose
```shell
agora.bat docker-compose up
```

6. Stop docker-compose
```shell
agora.bat docker-compose down
```

### Using docker-compose with monitoring for Windows

1. Init the execution node
```shell
agora.bat el-node init
```

2. Import your key stores
```shell
agora.bat validator accounts import <your key stores folder>
```

3. Edit wallet password
```shell
notepad ./root/config/cl/password.txt
```

4. Edit transaction fee receiving address
```shell
notepad ./root/config/cl/proposer_config.json
```

5. Run docker-compose
```shell
agora.bat docker-compose-monitoring up
```

6. Stop docker-compose
```shell
agora.bat docker-compose-monitoring down
```

7. Monitoring
   Launch the URL below to view the login page.  
   The initial ID is admin. The password is admin.  
   Please make sure to change your account and password.  
   http://localhost:3000
   The following screens are prepared.  
   http://localhost:3000/d/FDX6YtOiz/geth-node-dashboard-feb-2022?orgId=1&refresh=10s  
   http://localhost:3000/d/bosagora2023/boa-staking-dashboard?orgId=1&refresh=1m  
   http://localhost:3000/d/rYdddlPWk/node-exporter-full?orgId=1&refresh=1m   
