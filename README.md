# webserver-log-template
Brief templates to make web server logging based on nginx server


## Configuration

Here is small configuration that need to be updated according to your service

### NGINX Proxy
Go to `./nginx/conf/nginx.conf` and update the `SERVICE_IP` and `SERVICE_PORT`  variable on the configuration

```angular2
 proxy_pass http://{SERVICE-IP}:{SERVICE-PORT};
```

Update the variable and make the NGINX Proxy route to your service

### Update Elasticsearch Host

Go to `./logstash/conf/logstash.conf` and go to output section. Change the elasticsearch host according to yours

```angular2
output {
  elasticsearch {
      hosts => "SERVICE_IP:SERVICE_PORT"
      index => "nginx"
  }
```
