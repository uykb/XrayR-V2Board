# XrayR-V2Board
1. 无需每次配置面板URL和TOKEN（一次永久生效）
2. 无需在配置文件中修改节点ID

## 使用指南
1. Fork本仓库，修改 `config.yml` 文件，仅需修改下面两行。
```shell
ApiHost: "YOUR_PANEL_URL" # 修改这里
ApiKey: "YOUR_TOKEN" # 修改这里
```


2. 修改 `install.sh` 文件的203行，将用户名 `missuo` 修改为你自己的GitHub用户名。
```
wget https://cdn.jsdelivr.net/gh/uykb/XrayR-V2Board/config.yml -O /etc/XrayR/config.yml
```

3. 修改下面链接的用户名 `missuo` 为你自己的GitHub用户名，完成配置一键安装脚本命令。
### x86_64
```
bash <(curl -Ls https://raw.githubusercontent.com/uykb/XrayR-V2Board/main/install.sh)
```
### ARM_64
```
bash <(curl -Ls https://cdn.jsdelivr.net/gh/uykb/XrayR-V2Board/install-arm.sh)
```

4. 在 `V2Board` 面板上完成基本节点信息的填写。
![截图](https://files.xiami.com/cpp/07d8ec1a38a5462c3afbfac41413b8af/1622434730321.png)

5. 记录一下你的节点ID。

6. 在VPS上执行上面的一键安装命令，会全自动安装，会提示你输入节点ID。

## 注意事项
由于你Fork本仓库之后，你的仓库可能会是公开的。直接修改配置文件可能会暴露你的面板关键信息。建议下载 `config.yml` ，修改完信息后，上传到你自己的服务器。并在 `install.sh` 中填写你自己的配置文件下载链接。最后上传 `install.sh` 到你自己的服务器，生成自己的一键安装命令。

[![Star History Chart](https://api.star-history.com/svg?repos=missuo/XrayR-V2Board&type=Date)](https://star-history.com/#fanux/missuo/XrayR-V2Board)
