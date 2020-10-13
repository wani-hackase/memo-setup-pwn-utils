# 想定環境

ubuntu 18.04を想定しています。

# netcat

標準で入っているかと。
入ってなかったら
`sudo apt-get install netcat`
?

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
