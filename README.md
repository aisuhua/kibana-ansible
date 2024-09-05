# kibana-ansible

以简单的方式快速搭建 Kibana。

## 安装

```sh
git git@github.com:aisuhua/kibana-ansible.git
cd kibana-ansible

# 按需修改 inventory 、安装目录、用户等信息
vim hosts.yaml

ansible-playbook playbook.yaml
```

## 卸载

```sh
ansible-playbook remove.yaml
```

## 测试

浏览器打开 https://172.31.96.151:15603

或者将证书 `/path/to/kibana-ansible/roles/kibana/files/certs/ca.pem` 导入到浏览器后，用类似 https://kibana1.wildcard.net:15603 的域名（kibana1 随意）可以以信任的方式访问。

## 特点

- 可离线安装
- 支持在单机上安装多个不同版本的实例
- 卸载简单，方便来回测试
- 自带 100 年 SSL 证书，可简单替换成自签名证书
- 定制简单，该 role 保持了简单
