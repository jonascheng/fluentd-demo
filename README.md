
# Install random log generator in K8S

kubectl run random-logger --image=chentex/random-logger --generator=run-pod/v1

# Start fluentd server

docker run -d -p 24224:24224 -p 24224:24224/udp -v /data:/fluentd/log fluent/fluentd:v1.3-debian-1

