# Rust-OS-Study-Note
# 2023年秋季开源操作系统训练营学习笔记
## 10月23日
成功晋级第二阶段，现在我的Arch Linux上搭建环境，qemu在Arch的Extra仓库中有包：`qemu-full`。
遇到了rustsbi的版本问题，经过大佬帮助，更新了rustsbi的版本(将最新版本的rustsbi-qemu.bin替换掉了`/bootloader/rustsbi-qemu.bin`)(感谢"Misonoi"大佬)

## 10月24日
开始正式学习，在跟着手册敲的过程中，遇到了工具链的问题，error如下：
```
error[E0463]: can't find crate for `core`
  |
  = note: the `riscv64gc-unknown-none-elf` target may not be installed
  = help: consider downloading the target with `rustup target add riscv64gc-unknown-none-elf`

```
解决方法：
```
rustup target add riscv64gc-unknown-none-elf
rustup default nightly
rustup update
```
(Arch仓库中的rustup包禁止的是`rustup self update`，即其自身的更新需要通过pacman管理，而`rustup update`不受影响)  
(感谢“福如东海”大佬)

## 10月25日
遇到了一些困难，由于零基础，看资料和看视频都感觉很吃力  
有时候跟着简化版本的资料敲代码，明明代码都一样，还是会出错，最后需要去看一眼仓库中的源码或者换成复杂一点的资料
