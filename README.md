# AplicacionWebFlask

Esto es una aplicacion web echa con Flask que sirve para mantener un registro de los cumpleaños de nuestros amigos o personas cercanas a nosotros.

La aplicacion cuenta de dos archivos importantes el app.py y el index.html junto con este tambien esta el de estilos.css para que el html tenga un estilo adecuado.

El index.html es lo que ve y usa el usuario para insertar y visualizar los cumpleaños que ha guardado mientras que el app.py se encarga de hacer las funcionas logicas y conectar el index.html con la base de datos 
para guardar esa informacion.
![image](https://github.com/toniroigchulia/AplicacionWebFlask/assets/114684509/97a7830a-0b0e-4f8d-925b-71c0b2fcfe84)

Para completar la practica en el index.html he creado un formulario donde el usuario inserta los datos de nombre, dia, para que despues el app.py pueda cojer estos datos y usarlos. Aparte de este formulario en el body
tambien hay un bucle for para que cuando el app.py manda al index.html la informacion de la basee de datos usando el for recorremos esa informacion y creamos una tabla para ver todos los cumpleaños.

En el app.py tenemos una funcion importante la que se encarga de cargar la informacion a la base de datos y despues otra que se encarga de devolver dicha informacion. Para insertar la informacion usamos la funcion de
request.form.get("") para conseguir los datos del apartado en cuestion y lo guardamos en una variable, despues usando esa variable ejecutamos un Insert de Sql con esas variables y lo guardamos en la base de datos.
Despues para cargar la base de datos solo hacemos una Select de toda la base de datos y lo guardamos en la variable birthadays, despues el html recorrera el birthadys con el FOR mencionado anteriormente y creara una tabla para
mostrar toda la informacion.
