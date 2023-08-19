# HTTP Forwarding

There are many proxy servers currently available free of charge or by payment, and here we use one, called **nginx**, as an example. It is a lightweight web server with low memory usage that can sustain heavy load through parallelism and load balancing. nginx can be downloaded from&#x20;

```
http://nginx.org/en/download.html
```

and installed by running

{% code fullWidth="true" %}
```
./configure --prefix=install_directory --without-http_rewrite_module
make build
make install
```
{% endcode %}

To start nginx, simply

```
cd install_directory
sbin/nginx
```

Below is a simple configuration file that should be placed in install\_directory/conf directory:

{% code title="nginx.conf" %}
```
# number of CPU processes
# can be increased, CPU affinity can be specified
worker_processes 1;

# each worker can process up to 1024 connections
events {
   worker_connections 1024;
}

http {
   server {
   # proxy is running on host localhost
   # proxy is listening on port 8080
   # provided the proxy is running on localhost:8080,
   # TeraChem license.key file should contain ’server localhost:8080’ line
      server_name localhost;
      listen 8080;
      # all traffic is forwarded to PetaChem license server 54.208.252.40:8877
      # when proxy is used, ’server 54.208.252.40:8877’ setting should be
      # commented out in license.key
      location / {
         proxy_pass http://54.208.252.40:8877;
      }
   }
}
```
{% endcode %}

