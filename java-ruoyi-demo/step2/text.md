## 安装部署
```plain
kubectl create ns ruoyi-demo
kubectl apply -f ruoyi-demo.yaml
```{{exec}}

## 查看状态
```plain
kubectl get pod -n ruoyi-demo
```{{exec}}

## 访问地址
[ruoyi-demo]({{TRAFFIC_HOST2_30000}})