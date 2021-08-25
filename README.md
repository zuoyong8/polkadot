## 波卡

### 一）build for centos8

#### 安装基本环境并运行

1、**安装clang** 

​     $ sudo yum update

​	$ sudo yum install epel-release 

​	$ sudo yum install clang

2、**安装和配置rustup**

​    $ sudo curl https://sh.rustup.rs -sSf | sh

​    $ sudo source ~/.cargo/env

   $  cargo update -p parity-db

3、**配置Rust toolchain**

​	$ sudo rustup default stable

​    $ sudo rustup update

   $ sudo rustup update nightly

   $ sudo rustup target add wasm32-unknown-unknown --toolchain nightly

4、**配置Node Template**

   $ git clone -b v3.0.0+monthly-2021-05 --depth 1 https://github.com/substrate-developer-hub/substrate-node-template

   $ cd substrate-node-template

   $ cargo build --release

**5、运行**

$ cargo run --release -- --dev --tmp

