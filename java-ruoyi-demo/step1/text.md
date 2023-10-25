## 安装 Metrics-Server
```plain
kubectl apply -f components.yaml
```{{exec}}

## 安装 DataKit Operator
```plain
kubectl create ns datakit
kubectl apply -f datakit-operator.yaml
```{{exec}}

## 安装 DataKit
- 更新 datakit.yaml 中的 ENV_DATAWAY
> 获取方式：登陆观测云空间 --> 集成 --> DataKit

```plain
vim datakit.yaml
```{{exec}}

找到 ENV_DATAWAY 并修改
``` shell
- name: ENV_DATAWAY
  value: https://openway.guance.com?token=<your-token> # 此处填上 您的 DataWay 和 token 信息
```

- 安装
```plain
kubectl apply -f datakit.yaml
```{{exec}}

- 验证：登陆观测云空间，查看基础设施里是否有集群信息，若有即为数据上报成功。若无数据，请按照指引进行 [无数据排查](https://docs.guance.com/datakit/why-no-data/)。
```plain
kubectl get pod -n datakit
```{{exec}}