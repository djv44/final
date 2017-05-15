1.	Go to github.com
2.	Click repositories
3.	Click new
4.	Name it and create with a README
5.	Create repository 
6.	Go to command line
7.	Cd into directory where you want repository 
8.	git clone https://github.com/djv44/final.git
9.	cd into cloned repository 
10.	git checkout-b start
11.	create Dockerfile with a capital D
a.	Dockerfile helps build container for project
12.	Added prometheus_metrics file to build monitoring capabilities
13.	Run_tests.sh to run unit tests
14.	Add unh698.py which is the python files to call pages and where the apps are routed 
15.	Added unh698_test.py file which tests each case for the pages
16.	Added docker-compose.test.yml runs the ren-tests.py script
17.	Use and ansible playbook to run everything in container.
18.	Templates folder to for the web pages
19.	Git add . to add all docs to git
20.	Git status to see that everything is green 
21.	Git commit -m “first commit on start”
22.	Git push origin start
23.	Go to docker cloud account
24.	Go to repositories 
25.	Click on create
26.	Name same as github repository 
27.	Public
28.	Click connected
29.	Select github id
30.	Select github repository name
31.	https://cloud.docker.com/swarm/djv44/repository/registry-1.docker.io/djv44/final/builds/a508db3e-b8e3-4660-a90d-24c0501c1e99Click create
32.	In github click on settings
33.	Integration and services  
34.	Docker
35.	After a successful test in Docker merge 
36.	Git checkout master to change to master branch
37.	Git pull origin master to make local master same as git hub
38.	Change tags in production/staging to tag 0.0.1 for testing
39.	git checkout master
40.	git pull origin master
41.	git tag 0.0.1
42.	Push your tags to github and verify through the UI that they exist.
43.	git push --tags origin master
44.	ssh -i C:/Users/danie/.ssh/dbeitel-xxxxxxxxxx.key dbeitel@54.183.112.17 to log into aws instance
45.	git clone https://github.com/djv44/final.git
46.	cd final
47.	sudo apt install docker.io
48.	sudo apt-get update if the daemon doesn’t work….
a.	sudo usermod -aG docker $(whoami)
49.	logout
50.	log in
51.	docker build -t test .
52.	docker pull djv44/final – pulls latest public docker image
53.	docker images – shows image ID
54.	sudo docker run -d -p 8080:8080 djv44/final python3 unh698.py -get a container up and running and keeps it running in the background
55.	wget http:// 54.183.112.17:8080 confirms connectivity
56.	http:// 54.183.112.17:8080 in web browsers shows image/container
57.	to use tag image
a.	docker ps
b.	docker stop (name of instance being run)
c.	docker run -d -p 8080:8080 djv44/final:release-0.0.1 python3 unh698.py
58.	log out
59.	on local machine create new branch
60.	add links to pages and update deploy-website-production.yml page with image version of 0.0.2 to get ready for next tag
61.	git add .
62.	git commit -m
63.	git push origin pages
64.	on AWS git pull –tags origin master
65. docker run -d -p 8080:8080 djv44/final:release-0.0.x changes depending on the current release
