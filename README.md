# App-de-Belleza
Plataforma para personas interesadas en mejorar su estética personal de manera sencilla y personalizada. 
             ![belleza](https://sp-ao.shortpixel.ai/client/to_auto,q_glossy,ret_img,w_540,h_540/https://fusionhairsalonspa.com/wp-content/uploads/2022/09/cuidar-tu-balayage-cabello-rubio-brillo-suave-consejos-doce.jpg).

# INTRODUCCIÓN
Bienvenidos a nuestra App-de-Belleza estamos encantados de presentarte una herramienta creada especialmente para realzar tu estilo y cuidar de tu imagen personal. En nuestra app, encontrarás una amplia galería de peinados y maquillajes, tutoriales prácticos para aprender nuevas técnicas, y la opción de agendar citas con estilistas de manera rápida y sencilla.

# PROPÓSITO
El propósito de mi app de belleza es ofrecer una experiencia personalizada para el cuidado y mejora de la apariencia, brindando recomendaciones, productos y servicios adaptados a las necesidades de cada usuario.

# OBJETIVOS
**Objetivos de mi app de belleza:**  
1. **Personalización** – Ofrecer recomendaciones y servicios adaptados a cada usuario según sus necesidades y preferencias.  
2. **Accesibilidad** – Facilitar el acceso a productos y servicios de belleza en un solo lugar.  
3. **Interactividad** – Permitir a los usuarios interactuar con expertos y recibir asesoría personalizada.  
4. **Innovación** – Integrar herramientas tecnológicas como inteligencia artificial para mejorar la experiencia del usuario.  
5. **Comunidad** – Fomentar una comunidad donde los usuarios puedan compartir experiencias, consejos y opiniones.

# CONTEXTO DEL PROBLEMA
El sector de la belleza y el peinado enfrenta desafíos relacionados con la personalización y la accesibilidad. Los usuarios a menudo pierden tiempo buscando estilos adecuados o gestionando citas de manera ineficiente. Además, los estilistas enfrentan problemas al organizar su agenda y promocionar sus servicios. Esta app resuelve estos problemas mediante una plataforma centralizada, intuitiva y accesible desde cualquier dispositivo.

# ANALISIS DE REQUERIMIENTO
* Gestión de usuarios: Registro, inicio de sesión, y administración de perfiles.
* Catálogo de estilos: Visualización de peinados y maquillajes, con filtros personalizables.
* Planificación de citas: Reservas en tiempo real con horarios disponibles de estilistas.
* Favoritos: Posibilidad de guardar estilos preferidos.

# FUNCIONALIDAD CLAVE
Mi app de belleza ofrece un diagnóstico personalizado para recomendar productos y rutinas adaptadas a cada usuario. Permite agendar citas con expertos, probar looks con realidad aumentada y comprar productos en una tienda integrada. Además, brinda un espacio para compartir experiencias y seguir el progreso en el cuidado personal.

# MODELO RELACIONAL

![modelo relacional](https://github.com/user-attachments/assets/65c52d6f-1e4e-47ff-9990-0209aba52db8)
El modelo relacional de nuestra App de belleza está diseñado para que permitir a los usuarios agendar citas con estilistas, establecer preferencias relacionadas con estilos, y mantener información personal y de contacto.

# Tablas Principales y Relaciones 
**1. Usuario**
- Atributos clave: id_usuario (PK), nombre, gmail, telefono.

**Relaciones:**
- Uno a muchos con Cita (cita_id_cita).
- Uno a muchos con PreferenciaUsuario.
--------------------------------------------------------------------------------------------
**2. Cita**
- Atributos clave: id_cita (PK), fecha_hora, id_usuario, id_estilista.

**Relaciones:**
- Muchos a uno con Usuario.
- Muchos a uno con Estilista.
-------------------------------------------------------------------------------------------
**3. Estilista**
- Atributos clave: id_estilista (PK), nombre, especialidad, telefono.

**Relaciones:**
- Uno a muchos con Cita.
-------------------------------------------------------------------------------------------
**4. Estilo***
- Atributos clave: id_estilo (PK), nombre, categoria, descripcion.

**Relaciones:**
- Uno a muchos con PreferenciaUsuario.
-----------------------------------------------------------------------------------------
**5. PreferenciaUsuario**
- Atributos clave: id_usuario (FK, PK), id_estilo (FK).

**Relaciones:**
- Muchos a uno con Usuario y Estilo
----------------------------------------------------------------------------------------
# MODELO FISICO


