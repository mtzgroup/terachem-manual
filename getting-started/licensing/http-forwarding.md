# HTTP Forwarding

There are many proxy servers currently available free of charge or by payment, and here we use one, called **nginx**, as an example. It is a lightweight web server with low memory usage that can sustain heavy load through parallelism and load balancing. nginx can be downloaded from&#x20;

```
http://nginx.org/en/download.html
```

and installed by running

{% code fullWidth="true" %}
```
./configure --prefix=install_directory --without-http_rewrite_module


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

worker_processes 1;

# each worker can process up to 1024 connections
events {
   



   server {
   
   
   # provided the proxy is running on localhost:8080,
   # TeraChem license.key file should contain ’server localhost:8080’ line
      server_name localhost;
      listen 8080;
   
   
      # commented out in license.key
      location / {
         proxy_pass http://54.208.252.40:8877;
      }
   }

```
{% endcode %}
