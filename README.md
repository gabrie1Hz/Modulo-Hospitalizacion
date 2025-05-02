# Sistema de Administración Hospitalaria

Este repositorio contiene el código fuente para un **sistema de administración hospitalaria** diseñado para gestionar los aspectos administrativos y clínicos de un hospital. El sistema tiene como objetivo optimizar procesos como el registro de pacientes, programación de citas, gestión de historiales médicos, facturación y más. El sistema está desarrollado utilizando **ASP.NET Core Blazor**, **C#**, **SQL Server**, **HTML/CSS** y **JavaScript**.

## Documentación

### Tabla de Contenidos

1. [Introducción](#introducción)
2. [Características](#características)
3. [Arquitectura](#arquitectura)
4. [Tecnologías Utilizadas](#tecnologías-utilizadas)
5. [Guía de Instalación](#guía-de-instalación)
6. [Instrucciones de Uso](#instrucciones-de-uso)
7. [Capturas de Pantalla](#capturas-de-pantalla)
8. [Contribuciones](#contribuciones)
9. [Licencia](#licencia)

## Introducción

El **Sistema de Administración Hospitalaria** es una aplicación web completa diseñada para gestionar todos los aspectos administrativos y clínicos de un hospital. Su objetivo es agilizar procesos como el registro de pacientes, la programación de citas, la gestión de historiales médicos, la facturación y mucho más. Este sistema mejora la eficiencia, reduce el papeleo y mejora la atención al paciente mediante el acceso rápido a información crítica.

## Características

### Gestión de Pacientes
- Registrar nuevos pacientes.
- Actualizar información del paciente.
- Ver el historial médico de los pacientes.

### Gestión de Médicos
- Añadir y gestionar los perfiles de los médicos.
- Programar citas médicas.
- Asignar médicos a pacientes.

### Programación de Citas
- Reservar citas para los pacientes.
- Ver y gestionar el calendario de citas.
- Enviar recordatorios de citas por correo electrónico/SMS.

### Gestión de Registros Médicos
- Registros Electrónicos de Salud (EHR).
- Almacenamiento seguro de datos de los pacientes.
- Control de acceso a la información sensible.

### Facturación y Generación de Facturas
- Generar facturas por los servicios prestados.
- Procesar pagos.
- Gestión de reclamaciones de seguros.

### Gestión del Personal
- Gestionar los detalles del personal del hospital.
- Asignar roles y permisos.
- Sistema de asistencia y nómina.

### Gestión de Inventarios
- Rastrear suministros y equipos médicos.
- Gestionar niveles de inventario.
- Generar órdenes de compra.

### Informes y Análisis
- Generar informes de operaciones hospitalarias.
- Dashboards de visualización de datos.
- Exportar informes en varios formatos (PDF, Excel).

### Autenticación y Autorización de Usuarios
- Sistema de inicio de sesión seguro.
- Control de acceso basado en roles (Administrador, Médico, Enfermero, Recepcionista).

### Diseño Responsivo
- Accesible en escritorios, tabletas y dispositivos móviles.
- Compatibilidad entre navegadores.

## Arquitectura

El sistema se construye utilizando una **arquitectura en capas** para separar responsabilidades y mejorar la escalabilidad.

### Capas

- **Capa de Presentación**:
  - Descripción: Componentes de la interfaz de usuario que interactúan con los usuarios.
  - Tecnologías: HTML5, CSS3, JavaScript, Bootstrap.

- **Capa de Lógica de Negocios**:
  - Descripción: Lógica central de la aplicación que procesa datos entre la UI y las capas de datos.
  - Tecnologías: C#, ASP.NET MVC.

- **Capa de Acceso a Datos**:
  - Descripción: Maneja todas las operaciones con la base de datos.
  - Tecnologías: Entity Framework, LINQ.

- **Capa de Base de Datos**:
  - Descripción: Almacena todos los datos persistentes requeridos por la aplicación.
  - Tecnologías: Microsoft SQL Server.

## Tecnologías Utilizadas

- **Frontend**:
  - HTML5
  - CSS3
  - JavaScript
  - Bootstrap

- **Backend**:
  - C#
  - ASP.NET MVC Framework
  - Entity Framework (ORM)

- **Base de Datos**:
  - Microsoft SQL Server

- **Herramientas de Desarrollo**:
  - Visual Studio 2019 o superior
  - SQL Server Management Studio
  - Git para control de versiones

## Guía de Instalación

### Requisitos Previos

- Sistema Operativo: Linux (Arch Linux recomendado), Windows 10 o superior.
- Software:
  - Visual Studio 2019 o superior
  - SQL Server 2017 o superior
  - SQL Server Management Studio
  - .NET Framework 9.0 o superior
  - Git

### Pasos

#### Clonar el Repositorio

1. Clona este repositorio a tu máquina local:

   ```bash
   git clone https://github.com/tu_usuario/Medical-Facility-Management-System.git

    Accede al directorio del proyecto:

    cd Medical-Facility-Management-System

Restaurar Dependencias

Ejecuta el siguiente comando para restaurar las dependencias del proyecto:

dotnet restore

Configurar la Base de Datos

    Abre el archivo appsettings.json y configura la cadena de conexión de tu base de datos:

{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=HospitalDB;User Id=your_user;Password=your_password;"
  }
}

Asegúrate de reemplazar your_user y your_password por las credenciales de tu base de datos.

Crea la base de datos ejecutando las migraciones:

    dotnet ef migrations add InitialCreate
    dotnet ef database update

Compilar y Ejecutar la Aplicación

    Para compilar el proyecto, usa el siguiente comando:

dotnet build

Para ejecutar la aplicación, usa:

    dotnet run

Esto debería iniciar el servidor en http://localhost:5000 (o el puerto que se haya configurado).
Instrucciones de Uso
Acceder a la Aplicación

    URL: http://localhost:[puerto]/

        Reemplaza [puerto] con el número de puerto mostrado en Visual Studio cuando se ejecute la aplicación.

Credenciales Predeterminadas

    Administrador

        Usuario: admin@hospital.com

        Contraseña: Admin@123

    Médico

        Usuario: doctor@hospital.com

        Contraseña: Doctor@123

    Personal

        Usuario: staff@hospital.com

        Contraseña: Staff@123

Navegación en la Aplicación

    Dashboard: Visualiza las estadísticas generales del hospital y enlaces rápidos a diferentes módulos.

    Módulo de Pacientes: Añade nuevos pacientes, actualiza la información y ve los historiales médicos.

    Módulo de Citas: Programa nuevas citas, ve y gestiona citas existentes y envía recordatorios.

    Módulo de Médicos: Gestiona perfiles de médicos, asigna médicos a pacientes y organiza su calendario.

    Módulo de Facturación: Genera facturas, procesa pagos y gestiona reclamaciones de seguros.

    Módulo de Informes: Genera y exporta informes operativos y visualiza dashboards de análisis.



¡Gracias por usar el Sistema de Administración Hospitalaria!


Este `README.md` proporciona una guía completa para entender, instalar y usar tu proyecto, desde la clonación del repositorio hasta la configuración de la base de datos y el uso del sistema.
