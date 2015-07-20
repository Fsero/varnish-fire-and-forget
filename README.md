How to launch fire and forget demo
----------------------------------

docker run --name varnish --link web:web -v $PWD/etc/varnish:/etc/varnish/ -i -p 80:80 -d jacksoncage/varnish

docker run -d -P --name web  -v  $PWD/varnish-docker/html1:/usr/share/nginx/html:ro -d nginx 
