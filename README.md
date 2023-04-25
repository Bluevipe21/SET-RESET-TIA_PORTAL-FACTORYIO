# Ejemplo de un set y reset utilizando TIA PORTAL y Factoryio

This is an example of the use of the set and reset functions in a PLC. The code was created using the ladder language in the tia portal software v15. To verify the operation, the factoryio 3D simulation software was used. Factoryio works as training software for different PLC platforms.  ( [Click here for more information](https://docs.factoryio.com/) ). 

---

## Utilización de factoryio con tia portal

Para conectar factoryio con el tia portal puedes descargar los templates dependiendo de la versión de tia portal que manejes en el siguiente [enlace](https://docs.factoryio.com/tutorials/siemens/setting-up-s7-plcsim-v13/#tia-portal-template-projects). Estos templates contienen un archivo, en este caso llamado __MHJ-PLC-Lab-Function-S71200__, el cuál es el encargado de realizar la conexión con el tia portal como si estuviera conectado de manera física. Este archivo lo copiaremos hacia nuestro proyecto y lo llamaremos dentro de nuestro bloque principal o main. Para hacer que el direccionamiento concuerde con el de factoryio debemos cambiar las propiedades de nuestro proyecto. Para esto realizaremos lo siguiente:

- Hacemos clic derecho sobre la carpeta de nuestro PLC (Donde dice algo como: PLC_1 [CPU 1212C AC/DC/RLY]) y damos clic en propiedades. 
- Luego en la pestaña __General__ damos clic en la sección *Direcciones* *E/S* y donde dice *Direccionamiento inicial* lo cambiamos a 10.
- Luego navegamos a la pestaña de *Protección y seguridad* y navegamos hacia la parte que dice __Mecanismos de conexión__ y damos marcamos o damos clic en: *Permitir acceso vía comunicación PUT/GET del interlocutor remoto*.

Con lo anterior ya tendremos habilitada la comunicación con el factoryio. Por último solo debemos de verificar que el direccionamiento de entradas y salidas sea el correcto, o sea, que concuerde con el establecido en el programa en ladder del PLC.

### [Archivo de la escena creada en factoryio](https://drive.google.com/file/d/1YXIbnCdtQzOsWUAxKyq5qBdlVM4UxTAd/view?usp=sharing)
