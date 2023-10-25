## 准备物料包
```plain
git clone https://github.com/GuanceDemo/guance-java-ruoyi-demo.git
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
[ruoyi-java-demo]({{TRAFFIC_HOST1_30001}})