# mp42mcap

## 设置源
```sh
export RUSTUP_DIST_SERVER=https://rsproxy.cn
export RUSTUP_UPDATE_ROOT=https://rsproxy.cn/rustup
```

## 环境安装
```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

## 依赖安装
```sh
sudo apt-get update
sudo apt-get install protobuf-compiler
sudo apt-get install libavutil-dev pkg-config
sudo apt-get install libavformat-dev pkg-config
echo 'export PKG_CONFIG_PATH=/usr/lib/x86_64-linux-gnu/pkgconfig:$PKG_CONFIG_PATH' >> ~/.bashrc
source ~/.bashrc

export RUST_BACKTRACE=1
apt-get install libavfilter-dev
apt-get install libavdevice-dev
apt-get install clang libclang-dev llvm-dev
```

## 编译
```sh
cargo clean
cargo build
```

Convert MP4 video files to MCAP format with H.264/H.265 compression.

AI wrote this code so no guarantees.

## Usage

```sh
$ cargo run -- --help

Converts MP4 videos to MCAP

Usage: mp42mcap [OPTIONS] <INPUT> <OUTPUT>  --topic="/test/abc" --initial-timestamp=1736850000000

Arguments:
  <INPUT>   Input MP4 file
  <OUTPUT>  Output MCAP file

Options:
      --topic <TOPIC>        Topic name for the video messages [default: video]
      --frame-id <FRAME_ID>  Frame ID for the video messages [default: video]
  -h, --help                 Print help
  -V, --version              Print version
```



