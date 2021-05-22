# 想定環境

ubuntu 18.04を想定しています。

# netcat

標準で入っているかと。
入ってなかったら
`sudo apt-get install netcat`
でインストール。

# strings

```
apt-get install binutils
```

# objdump

stringsと同じbinutils

```
apt-get install binutils
```

# httpie

あると便利なので入れておく

```
apt-get install httpie
```

# python

[htttpie](#httpie)がインストールされているという前提でminicondaのインストール方法を書いておきます。

```
http --download https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
```

# pwntools

minicondaで[python](#python)がインストールされているという前提でpwntoolsのインストール方法を書いておきます。

## pwn用の環境の構築

```
conda create --name pwn python=3.8
conda activate pwn
pip install pwntools
```

## pwn用の環境を抜けるとき

```
conda deactivate
```

## pwn用の環境に入るとき

```
conda activate pwn
```

# ROPgadget

```
conda activate pwn
pip install ropgadget
```

# one_gadget

```
sudo apt-get install ruby
sudo gem update
sudo gem install one_gadget
```

# ghidra

[https://ghidra-sre.org/](https://ghidra-sre.org/)からダウンロードします。

```
http --download https://ghidra-sre.org/ghidra_9.1.2_PUBLIC_20200212.zip
```

javaが必要なのでjavaもインストールします。

```
sudo apt-get install default-jre
```

# Pwndbg + GEF + Peda

- [apogiatzis/gdb-peda-pwndbg-gef: A script to automatically install Peda+pwndbg+GEF plugins for gdb](https://github.com/apogiatzis/gdb-peda-pwndbg-gef)

