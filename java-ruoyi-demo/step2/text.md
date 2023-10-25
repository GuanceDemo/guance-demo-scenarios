## 准备物料包
```plain
git clone https://github.com/GuanceDemo/guance-java-ruoyi-demo.git
```{{exec}}

## 安装部署
```plain
cd guance-java-ruoyi-demo
helm upgrade -i ruoyi -n ruoyi --create-namespace ./deployment/helm
```{{exec}}

## 访问
[ruoyi-java-demo]({{TRAFFIC_HOST1_30001}})