#command to run normal container

docker run -d -t infracloudio/csvserver:latest

#it was stopping immidiatley after starting due to csvserver

bash gencsv.sh

docker run -d -v /home/harish/solution/inputFile:/csvserver/inputdata infracloudio/csvserver:latest

docker ps

docker exec -it 88d44c3d379e /bin/bash

netstat -tulpn | grep LISTEN

found port 9300 running csvserver application

docker run -d -v /home/harish/solution/inputFile:/csvserver/inputdata -p 9393:9300 -e CSVSERVER_BORDER=Orange infracloudio/csvserver



