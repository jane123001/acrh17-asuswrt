## 编译

1. 首先装好 Ubuntu 64bit，推荐  Ubuntu  18 LTS x64 /  Mint 19.1

2. 命令行输入 `sudo apt-get update` ，然后输入
`
sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch python3.5 python2.7 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib antlr3 gperf wget libncurses5:i386 libelf1:i386 lib32z1 lib32stdc++6 gtk-doc-tools intltool binutils-dev cmake lzma liblzma-dev lzma-dev uuid-dev liblzo2-dev xsltproc dos2unix libstdc++5 docbook-xsl-* sharutils autogen shtool gengetopt libltdl-dev libtool-bin
`

3. 使用 `git clone https://github.com/SWRT-dev/acrh17-asuswrt` 命令下载好源代码

4. 使用 `git clone https://github.com/SWRT-dev/qca-toolchains` 命令下载toolchains

5. 分别执行 `cd qca-toolchains`

    `sudo mkdir -p /opt/toolchains/`

    `sudo ln -sf $(pwd)/openwrt-gcc463.arm /opt/toolchains/`

    `chsh -s /bin/bash`

    `sudo ln -sf /bin/bash /bin/sh`

6. 然后 `cd ../acrh17-asuswrt/release/src-qca-dakota` 进入目录

7. 输入 `make rt-acrh17` 即可开始编译你要的固件了。

8. 编译完成后输出固件路径：acrh17-asuswrt/release/src-qca-dakota/image


