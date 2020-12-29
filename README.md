# tpintegradorm3y4
TP Integrador N° 1 - Grupo P

Errores detectados

En la base de datos:

	> En la tabla "personas" en ninguno de los campos deberían aceptarse los valores null porque está especificado en el TP (me di cuenta de esto cuando termine la API POST/libro)


En app.js:

	> La siguiente línea de código, de conexión al servidor, no permite a Postman enviar las consultas:

		app.listen(app.get('port'),()=>{
    			console.log('Server listening on port', port);
		});

	En su lugar se solucionó con la siguiente (actualmente):

		app.listen(port, () => {
    			console.log("Server listening on port:", port);
		});


	> La siguiente linea de código tenia escrito el puerto en la misma palabra que PORT:

	const port = process.env.PORT3000 ? process.env.PORT3000 : 3000;

	Se modificó por: (Por lo visto en la última clase)

	const port = process.env.PORT ? process.env.PORT : 3000;



