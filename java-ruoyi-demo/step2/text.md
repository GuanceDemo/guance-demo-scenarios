## 准备物料包
```plain
git clone https://github.com/GuanceDemo/guance-java-ruoyi-demo.git
```{{exec}}

## 修改镜像地址
> 因网络限制，需修改应用镜像地址
```plain
vim guance-java-ruoyi-demo/deployment/helm/values.yaml
```{{exec}}

``` shell
docker_registry: ghcr.io
docker_namespace: harlonhuang
```

## 去掉污点设置
> 因安装资源较大，取消 master 节点的污点

```plain
kubectl taint node controlplane node-role.kubernetes.io/control-plane-
```{{exec}}


## 安装部署
```plain
cd guance-java-ruoyi-demo
helm upgrade -i ruoyi -n ruoyi --create-namespace ./deployment/helm
```{{exec}}

## 查看状态
```plain
kubectl get pod -n ruoyi
```{{exec}}

## 访问地址
[ruoyi-java-demo]({{TRAFFIC_HOST2_30001}})