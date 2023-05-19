# 02MASW - POSTGRESQL
[![N|Solid](C:\Users\johan\PycharmProjects\pythonProject1\img.png)]
Apellidos y nombres de los integrantes del equipo/grupo:
1) Barrios Rivera, Juan Pablo
2) Hernández Durá, Raquel
3) Ospina Alzate, Johan David
* Índice del contenido.


* Tabla de Ilustraciones
1. Introducción
2. Obtención de los datos
3. Diseño de la base de datos
4. Despliegue de la base de datos
5. Consultas a base de datos
6. Conclusiones

***
<p>
Descripción empresa (cliente): Es una nueva empresa dedicada a prestar servicios de control, seguimiento y gestión de seguros, de flotas de vehículos pertenecientes a empresas del sector de la construcción.

La empresa facilita el control de los seguros de los vehículos de construcción, alertando cuando estos estén próximos a vencer y facilitando la comunicación con los brokers o aseguradoras, para la renovación o ampliación de estos.

Cabe mencionar que su foco de clientes, son las empresas constructoras, las cuales cuentan con flotas de vehículos menores, de carga y de maquinaria pesada. El rango de vehículos por empresa es de 10 a 100, por ello la necesidad de contar con este tipo de servicios, que son la información de los vehículos, sus seguros, inspecciones recurrentes y control de las fechas de vencimiento.
</p>

***

<h3>Actividad 01_BD</h3> 
<ol>
<li>Necesidades y requisitos del usuario (análisis de requisitos)</li>
<li>Tabla con los requisitos finales entregados en la Actividad 2 03MASW Ingeniería del Software Web.  
El sistema debe contemplar </li>
</ol>


3 tipos de roles: Administrador, Gestor y Conductor
El registro del rol Administrador, se deben ingresar de forma obligatoria los siguientes datos: nombres, apellidos, email, nombre de usuario, contraseña, fecha de nacimiento y documento de identidad.  
El registro del rol Gestor, se deben ingresar de forma obligatoria los siguientes datos: nombres, apellidos, email, nombre de usuario, contraseña, fecha de nacimiento, documento de identidad.  
Se deben agregar los datos de la empresa (nombre de empresa a la que pertenece, RUC de la empresa) habría que tener en cuenta que, desde el gestor y el conductor, se pueda dar de alta la empresa - como funcionalidad.  
El registro del rol Conductor, se deben ingresar de forma obligatoria los siguientes datos: nombres, apellidos, email, nombre de usuario, contraseña, fecha de nacimiento, documento de identidad.  
Se deben agregar los datos de la empresa (nombre de empresa a la que pertenece, RUC de la empresa).  
Se debe registrar su código de licencia de conducir.  

Se debe agregar la categoría de licencia y fecha de vencimiento de la licencia.  

Se debe adjuntar licencia de conducir en formato PDF.  

   

El sistema debe enviar al nuevo usuario un correo de confirmación, con su nombre completo, nombre de usuario y el link de validación al aplicativo web.  

 El link de validación tendrá un token que validará el alta del usuario nuevo.  

   

Para ingresar al sistema, se debe ingresar el usuario (email) y contraseña.   

 El usuario inicia sesión en la aplicación, accediendo a la dirección web de la aplicación.  

 La primera vez que el usuario acceda al sistema, deberá modificar su contraseña.  

 El sistema permitirá recuperar contraseña.  

 El sistema enviará un email con un link para realizar el cambio de contraseña.  

  

El sistema mostrará un menú lateral con las acciones vinculadas al rol del usuario en el sistema.  

 El rol administrador visualizará en el menú lateral: usuarios, obras, vehículos y empresas.  

 El rol gestor visualizará en el menú lateral: conductores de la empresa, obras de la empresa, vehículos de la empresa.  

El gestor visualizará las obras a las que tiene permisos.  

 El conductor visualizará en el menú lateral vehículos de la obra.  

   

El sistema permitirá realizar un registro de una empresa, se deben ingresar: RUC, razón social, dirección, nombre, persona, contacto, correo, teléfono.  

El rol administrador realizará la acción de registro para una empresa.  

El rol administrador realizará la acción de modificar para una empresa.  

El rol administrador realizará la acción de eliminar para una empresa.  

El rol administrador realizará la acción de listar las empresas.  

   

El sistema permitirá realizar un alta de un vehículo, se deben ingresar: placa, número de bastidor, tipo de vehículo y fotografía del vehículo.  

 El sistema permitirá cargar imágenes del vehículo arrastrando el elemento desde el ordenador del usuario.  

 El sistema tendrá opcional el asignar un conductor a un vehículo.  

 El vehículo pertenecerá a la empresa del usuario en sesión que crea el vehículo.  

   

El sistema permitirá realizar un registro de Tipo de vehículos.  

 El sistema tendrá los tipos de vehículos: menores, de carga y de maquinaria pesada.  

   

El sistema creará un nuevo Subtipo de Vehículo,   

 El sistema tendrá los tipos de subvehículos: auto, SUV  

 El tipo de vehículo de carga debe tener 1 subtipos: volquete.  

 El tipo de vehículo de maquinaria pesada debe tener 5 subtipos: minicargador, cargador, retroexcavadora, excavadora y rodillo.  

  

El sistema permitirá registrar pólizas con los siguientes datos: Número de póliza, Fecha de inicio, Fecha de fin, Aseguradora, Número de contacto de la aseguradora, Número de contacto de bróker (intermediario), Costo de póliza, Cronograma de pago, si la compra de póliza se realizó en cuotas, Póliza adjunta (PDF), Tipo de póliza, Estado (Activo / Vencido)  

   

El usuario gestor asignará el tipo de póliza que tiene asociado el vehículo, seleccionando entre: SOAT, Póliza de seguro vehicular, SAT, TREC y RC.  

   

El usuario debe poder visualizar dentro del detalle del vehículo las pólizas en formato PDF.  

   

El usuario debe poder descargar dentro del detalle del vehículo las pólizas en formato PDF.  

   

El sistema debe permitir el actualizar la información de las pólizas cuando se está editando un vehículo.  

   

El sistema debe permitir adjuntar nuevas pólizas a un vehículo.  

El sistema permitirá cargar pólizas del vehículo arrastrando el elemento desde el ordenador del usuario. ￼  

   

El sistema debe permitir registrar Obras al usuario gestor. Los datos que se deben colocar son: Nombre de la Obra, Dirección y el Identificador de la empresa.  

   

El usuario en sesión podrá ver su perfil.  

   

El sistema permitirá editar los campos del usuario en sesión en la sección de mi perfil.  

El usuario editará los campos: Nombre, Apellido, Teléfono.  

   

En el rol de administrador se permitirá activar un usuario.  

   

En el rol de administrador se permitirá desactivar un usuario.  

   

El rol gestor puede visualizar la información de todos los vehículos de su empresa.  

   

El rol gestor podrá modificación de los datos de los vehículos registrados en su empresa.  

   

El rol gestor podrá borrado de los datos de los vehículos registrados en su empresa.  

   

El usuario gestor debe poder registrar en la aplicación los datos de los vehículos pertenecientes a su empresa.  

   

El sistema permitirá que el rol Administrador agregue nuevas obras.  

El sistema habilitará un selector de empresa para la nueva alta de obras.  

El sistema habilitará un selector de gestor para la nueva obra.  

El sistema permitirá ver solo los posibles gestores de una determinada empresa seleccionada.  

   

El sistema tendrá un listado de todas las empresas para el rol administrador.  

El sistema tendrá en este listado un buscador por nombre de empresa.  

El sistema tendrá un paginador para el listado de empresa.  

El sistema podrá ver el detalle de la empresa.  

El sistema permitirá al rol administrador eliminar la empresa.  

   

El sistema tendrá un listado de los vehículos gestionados por un gestor.  

El gestor podrá buscar por nombre de vehículo.  

El gestor tendrá un filtro por tipo de vehículo.  

El gestor tendrá un filtro por subtipo de vehículo.  

El listado de los vehículos tendrá un paginado.  

   

El sistema tendrá un listado de las obras gestionadas por un gestor.  

   

El sistema permitirá ver la última ubicación del conductor.  

El sistema mostrará un mapa con la ubicación de los vehículos.  

El sistema permitirá cambiar la ubicación de un vehículo.  

El sistema permitirá cambiar un vehículo de obra.  

El sistema enviará email con la actualización de vehículo.  

   

El sistema alertará sobre las fechas de terminación de las pólizas de seguro.  

El sistema debe brindar alertas a los usuarios, cuando sus pólizas estén próximas a vencer.  

El sistema, cuando salga una alerta de fecha próxima de vencimiento, debe permitir a los gestores ingresar los días que se desea ampliar.   

El sistema brindará la opción de enviar de manera automática un correo al bróker/asegurador.  

   

El sistema debe permitir adjuntar la documentación técnica de los vehículos en formato PDF.  

El aplicativo debe permitir imprimir la documentación técnica de los vehículos.  

El aplicativo debe permitir descargar una copia de la documentación técnica de los vehículos en formato PDF.  

   

El sistema debe alertar sobre las cuotas del seguro próximo a vencer.  

   

El rol conductor solo debe contar con permisos de lectura para ver las pólizas.  

   

El usuario debe cerrar sesión.  

  

  

  

4.3.   Diseño de la base de datos  

  

3.1 Diseño Conceptual:   

  

Paso 1: Identificar las entidades del modelo de datos. Las que hemos identificado son:  

Usuario: son los perfiles que interactúan con el sistema.  

Vehículo: son los vehículos que tienen las empresas.  

Póliza: contiene la información de los datos de las pólizas de los vehículos.  

Obra: contiene la información de las obras en las que intervienen los vehículos.  

Empresa: son las empresas que están registradas en el servicio de gestión de seguros.  