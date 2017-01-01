Centos-6.8_redsat <=> Docker
============================

## Example start

Clone my Docker projects repo:

	git clone https://github.com/ZigFisher/MyDocker.git

Go to project dir:

	cd MyDocker/project_centos-6.8_red-sat

Create image:

	docker build -t centos-6.8_redsat .

Start container with "normal" name and hostname:

	docker run -d --restart=always -p 2054:22/tcp --name centos-6.8_redsat --hostname centos-6.8_redsat centos-6.8_redsat

If you need connect to container run this command:

	docker exec -it centos-6.8_redsat bash

Quick uninstall:

	docker stop centos-6.8_redsat && docker rm centos-6.8_redsat && docker rmi centos-6.8_redsat
