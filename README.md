## Ingress-nginx Benchmark

通过wrk测试Ingress性能
```bash
wrk -t8 -c1000 -d100s --latency http://my.nginx.svc/1kb.bin
```

- [ingress-nginx.yaml](./ingress-nginx.yaml): ingress-nginx configmap
- [nginx-server.yaml](./nginx-server.yaml): proxy server, 作为代理服务器对比ingress-nginx
- [my-nginx.yaml](./my-nginx.yaml): backend web server, 作为后端服务，用于压测

测试结果见https://qingwave.github.io/ingress-benchmark/
