# kubeadm 重制版本

## 支持版本

- 签名证书有效时间:99年

| 版本 | 证书有效 99 年|
| 1.20 | 支持|
| 1.21 | 不支持|
| 1.22 | 不支持|
| 1.23 | 不支持|
| 1.24 | 不支持|
| 1.25 | 不支持|
| 1.26 | 不支持|
| 1.27 | 不支持|
| 1.28 | 不支持|
| 1.29 | 不支持|
| 1.30 | 不支持|

## 下载安装

```sh
wget -O kubeadm https://raw.githubusercontent.com/yezihack/k8s-example/kubeadm/kubeadm-1.20.15-linux-$(uname -m)

cp kubeadm /usr/bin/kubeadm

# 测试 

kubeadm --help
```

- 看到黄色框的字体表示是重制版本

![20240407195701](https://cdn.jsdelivr.net/gh/yezihack/assets/b/20240407195701.png)

## 使用

```sh
# 查看证书有效期
kubeadm certs check-expiration

# 更新所有证书（前提是 etcd 是内置的）
kubeadm certs renew all

# 更新指定组件的证书（etcd 是外置情况）
kubeadm certs renew apiserver

```

![20240407200026](https://cdn.jsdelivr.net/gh/yezihack/assets/b/20240407200026.png)
