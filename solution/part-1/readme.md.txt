
ran the container with cmd

docker run -d --name csvserver infracloudio/csvserver:latest

container statte with below cmd

---->ps -a

container is exided with and error Exited (1)

-----> dokcer log  csvserver
output :  2024/08/10 17:44:59 error while reading the file "/csvserver/inputdata": open /csvserver/inputdata: no such file or directory


mounting the file of inputfile in container with below cmd

docker run -d --name csvserver-4 -p 9393:9300 -v "/root/inputFile:/csvserver/inputdata" infracloudio/csvserver:latest
b0ccc954014bd4e90ed940ae59da89db6238cc82f2e9267e29ce0185bf2898d6

passing env variable from cmd 

docker run -d --name csvserver-5 -p 9393:9300 -v "/root/inputFile:/csvserver/inputdata" -e CSVSERVER_BORDER=Orange infrac
loudio/csvserver:latest