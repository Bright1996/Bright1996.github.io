---
layout: mypost
title: golang 私有仓库 Git设置
categories: [Git，golang]
---
# 

基于邮箱生成密钥

```jsx
ssh-keygen -t ed25519 -C "workEmail"
```

go env 设置私有仓域名

```jsx
go env -w GOPRIVATE="公司域名"
```

修改 Git 配置，强制对私有仓库使用 SSH
```jsx
git config --global url."ssh://公司域名:23".insteadOf "http:/公司域名"
```

设置Git 全局账户名和邮箱
```jsx
git config --global user.name " username"
git config --global user.email "workEmail"
```