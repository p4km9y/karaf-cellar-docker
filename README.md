```{r, engine='bash', local notes}
docker build -t p4km9y/karaf-cellar:4.0.4 -t p4km9y/karaf-cellar -t kacel .
docker run --name="kacel1" -h kacel -d -e JAVA_MAX_MEM=256m -v /home/projects/udp/infrastructure/karaf-cellar/deploy:/opt/deploy kacel
docker push p4km9y/karaf-cellar
docker-compose up -d
```