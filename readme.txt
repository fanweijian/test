使用git远程仓库时
需要将你当前的电脑添加到github远程仓库的信任目录中
通过git生成安全证书 $ ssh-keygen -t rsa -C "2874304856@qq.com"
输入命令后直接按回车就会生成一个安全证书
    Generating public/private rsa key pair.
    Enter file in which to save the key (/c/Users/user/.ssh/id_rsa):
    Created directory '/c/Users/user/.ssh'.
    Enter passphrase (empty for no passphrase):
    Enter same passphrase again:
    Your identification has been saved in /c/Users/user/.ssh/id_rsa.
    Your public key has been saved in /c/Users/user/.ssh/id_rsa.pub.
    The key fingerprint is:
    SHA256:B/Tr3SPow3HHeILC2QRi7nUBdkIGhHPK4oCGD5aWHDM 2874304856@qq.com
    The key's randomart image is:
    +---[RSA 2048]----+
    |     oooB..      |
    | E  o ++.+.      |
    |+ *. * .....     |
    |=B. o . ..o.     |
    |+= . . oS=o. o   |
    |  o   . +o+o+.+  |
    |         oooo+o  |
    |         .o  . . |
    |          ..     |
    +----[SHA256]-----+
根据返回的结果,找到对应的证书文件id_rsa.pub 用记事本打开该文件,复制其内容
打开github账号 -> settings -> SSH and GPG keys -> New SSH key
   创建一个新的SSH key 这里title可以自由设置key值就是id_rsa.pub文件的文本内容