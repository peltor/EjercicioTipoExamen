Ejercicio 2025 Despliegue de Aplicaciones Web

Indicaciones:
- Crear un repositorio nuevo en Github que tenga estos archivos.
- Tiene que tener las siguientes ramas:
	- main
	- develop 
	- feature_primer_cambio
- Se debe hacer un cambio en la rama "feature..." en el archivo html (un cambio que sea notorio, que se pueda identificar de manera sencilla), ese cambio debe integrarse en la rama "develop" pero no en la rama main. Haciendo esto las ramas de "develop" y "feature_primer_cambio" tendrán los mismos cambios.
- Una vez que se realicen los cambios, se deben subir todas las ramas a github, por lo que "main" tendrá los archivos iniciales, y tanto "develop" como "feature_primer_cambio" el cambio que se hizo
- Crear imagen de docker
	- Crear dockerfile con los siguientes comandos:

	FROM httpd:2.4
	ADD public_html /usr/local/apache2/htdocs/
	EXPOSE 80

	- Una vez creado el dockerfile, crear la imagen de docker ejecutando el siguiente comando en la consola:

	docker build -t ejercicio1:v1

- Una vez creada la imagen, inicializar el contenedor con el siguiente comando:
	docker run -d -p 80:80 --name ejercicio ejercicio1:v1

- Si el contenedor ha iniciado correctamente deberías de poder acceder a la web abriendo el navegador y escribiendo en la url la siguiente dirección:
http://localhost:8080

- Crear un docker compose para poder inicializar un contenedor de la imagen hecha.
