# answer from instructor
# -e refers to a enviromental variable == ?foo=bar
docker container run -d -p 3306:3306 --name db \
-e MYSQL_RANDOM_ROOT_PASSWORD=yes \
mysql



# grabs the generated password from the mysql logs
docker logs db 2>/dev/null | grep "GENERATED ROOT PASSWORD"

# runs the apache container
docker container run -d \
--name webserver \
#on8080:forward80
-p 8080:80 \
httpd

#runs the ngnix container
docker container run -d \
--name proxy \
-p 80:80 \
nginx

#check to make sure everything went smooth
curl localhost
curl localhost:8080
