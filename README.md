--comando apra subir linode/lemp image on docker
		https://www.linode.com/docs/applications/containers/how-to-install-docker-and-deploy-a-lamp-stack/

		sudo docker run -p 80:80 -t -i linode/lamp /bin/bash

		-- inicio de servicios 

		service apache2 start

		service mysql start

		-- permisos de admin mysql 	

		grant all on exampleDB.* to 'example_user' identified by 'Admin2015';

		-- instalacion de git 

		sudo apt-get update

		sudo apt-get install git

		--creacion de imagenes 
				 sudo docker commit 9c04d30b5b2d lamp-git


		--remover imagenes
				sudo docker rmi --force nombre_image

		--import database proyect 

			create database pedidos;
			use pedidos;
			select datbase();
			exit

		-- bajando el backup base datos
			cd /tmp
			git init
			git remote add origin  https://github.com/hanmiton/BackUpPedidosDB.git
			git pull origin master

		--importan dentro de mysql
			mysql -u root - p 
					"Admin2015"	
			use pedidos
			source /tmp/pedidos.sql
			exit

			





