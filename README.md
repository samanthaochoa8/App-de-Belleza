# App-de-Belleza
Plataforma para personas interesadas en mejorar su estética personal de manera sencilla y personalizada. 
![belleza](https://sp-ao.shortpixel.ai/client/to_auto,q_glossy,ret_img,w_540,h_540/https://fusionhairsalonspa.com/wp-content/uploads/2022/09/cuidar-tu-balayage-cabello-rubio-brillo-suave-consejos-doce.jpg).

# INTRODUCCIÓN
Bienvenidos a nuestra App-de-Belleza estamos encantados de presentarte una herramienta creada especialmente para realzar tu estilo y cuidar de tu imagen personal. En nuestra app, encontrarás una amplia galería de peinados y maquillajes, tutoriales prácticos para aprender nuevas técnicas, y la opción de agendar citas con estilistas de manera rápida y sencilla.

# CONTEXTO DEL PROBLEMA
El sector de la belleza y el peinado enfrenta desafíos relacionados con la personalización y la accesibilidad. Los usuarios a menudo pierden tiempo buscando estilos adecuados o gestionando citas de manera ineficiente. Además, los estilistas enfrentan problemas al organizar su agenda y promocionar sus servicios. Esta app resuelve estos problemas mediante una plataforma centralizada, intuitiva y accesible desde cualquier dispositivo.

# ANALISIS DE REQUERIMIENTO
* Gestión de usuarios: Registro, inicio de sesión, y administración de perfiles.
* Catálogo de estilos: Visualización de peinados y maquillajes, con filtros personalizables.
* Planificación de citas: Reservas en tiempo real con horarios disponibles de estilistas.
* Favoritos: Posibilidad de guardar estilos preferidos.
# MODELO RELACIONAL

![modelo relacional](https://github.com/user-attachments/assets/65c52d6f-1e4e-47ff-9990-0209aba52db8)
El modelo relacional de nuestra App de belleza está diseñado para que permitir a los usuarios agendar citas con estilistas, establecer preferencias relacionadas con estilos, y mantener información personal y de contacto.

# Tablas Principales y Relaciones 
* 1. Usuario
Atributos:
* id_usuario (PK): Identificador único del usuario.
* nombre: Nombre del usuario.
* gmail: Correo electrónico del usuario.
* contraseña: Contraseña del usuario.
* telefono: Teléfono del usuario.
* cita_id_cita (FK): Relación con la tabla Cita.
* PreferenciaUsuario_id_usuario (FK): Relación con la tabla PreferenciaUsuario.

* 2. Cita
Atributos:
* id_cita (PK): Identificador único de la cita.
* fecha_hora: Fecha y hora de la cita.
* id_usuario: Usuario que reservó la cita.
* id_estilista: Estilista asignado a la cita.
* estado: Estado de la cita (confirmada, cancelada, etc.).
* citacol: Información adicional sobre la cita.

* 3. Estilista
Atributos:
* id_estilista (PK): Identificador único del estilista.
* nombre: Nombre del estilista.
* especialidad: Especialidad del estilista (corte, color, etc.).
* telefono: Teléfono del estilista.
* correo: Correo electrónico del estilista.
* cita_id_cita (FK): Relación con la tabla Cita.

* 4. Estilo
Atributos:
* id_estilo (PK): Identificador único del estilo.
* nombre: Nombre del estilo.
* categoria: Categoría del estilo (peinado, maquillaje, etc.).
* descripcion: Descripción del estilo.
* imagen: Imagen representativa del estilo.
* PreferenciaUsuario_id_usuario (FK): Relación con la tabla PreferenciaUsuario.

* 5. PreferenciaUsuario
Atributos:
* id_usuario (PK, FK): Usuario al que pertenece la preferencia.
* id_estilo (FK): Estilo preferido por el usuario.
* Relaciones
* 1. Usuario - Cita
* Relación: Uno a muchos.
* Clave foránea: cita_id_cita en Usuario.
* Descripción: Cada usuario puede tener múltiples citas asociadas.

* 2. Cita - Estilista
* Relación: Muchos a uno.
* Clave foránea: id_estilista en Cita.
* Descripción: Una cita está vinculada a un estilista específico.

* 3. Usuario - PreferenciaUsuario
* Relación: Uno a muchos.
Clave foránea: PreferenciaUsuario_id_usuario en Usuario.
Descripción: Un usuario puede tener múltiples preferencias.
* 4. PreferenciaUsuario - Estilo
Relación: Muchos a uno.
Clave foránea: id_estilo en PreferenciaUsuario.
Descripción: Una preferencia está asociada con un estilo específico.
* 5. Estilo - PreferenciaUsuario
Relación: Uno a muchos.
Clave foránea: PreferenciaUsuario_id_usuario en Estilo.
Descripción: Un estilo puede ser preferido por múltiples usuarios.




