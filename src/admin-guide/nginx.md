# Serving frontend with Nginx

This is a basic Nginx configuration for the frontend. Place all build output files from `dist` directory in `/var/www/rabit`
and change the value of `server_name` to your domain.

Please note that there is no HTTPS or any other forms of security in this configuration. It is strongly recommended that
you use HTTPS in your instance, especially for public-facing ones. You can get free HTTPS certificates using 
[Certbot](https://certbot.eff.org).

```nginx
server {
    listen         80;
    listen         [::]:80;
    # Replace example.com with your domain.
    server_name    example.com;
    root           /var/www/rabit;
    index          index.html;

    access_log /var/log/nginx/rabit_frontend_access.log combined;
    error_log /var/log/nginx/rabit_frontend_error.log error;

    gzip             on;
    gzip_comp_level  3;
    gzip_types       text/plain text/css application/javascript image/*;

    location / {
        try_files $uri $uri/ /index.html =404;
    }
}
```