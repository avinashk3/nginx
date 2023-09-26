docker run --name nginx --hostname ng1 -p 80:80 -v F:\Learn\NGINX\webpage:/usr/share/nginx/html -d nginx


docker build -t nodeapp .

docker network create backendnet
docker run --hostname nodeapp1 --name nodeapp1 -d --rm --network backendnet nodeapp
docker run --hostname nodeapp2 --name nodeapp2 -d --rm --network backendnet nodeapp
docker run --hostname nodeapp3 --name nodeapp3 -d --rm --network backendnet nodeapp
docker run --hostname nginx --name nginx -d --rm -v f:\Learn\NGINX\nginx:/etc/nginx/ -p 80:8080 --network backendnet nginx
