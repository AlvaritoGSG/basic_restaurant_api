<p align="end">
    <figure align="end">
        <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="150" alt="Laravel Logo">
    </figure>
</p>

# Acerca del proyecto

<h1 align="center" style="color:coral; font-size:35px";>
    Restaurente API - Flujo de Caja
</h1>

Este proyecto consiste en una API RESTful construida con Laravel v12.0.4 para gestionar el flujo de caja de un restaurante. Su objetivo es ofrecer un sistema centralizado para el registro de ingresos, egresos y seguimiento de saldo, permitiendo una mejor gestión financiera de las operaciones diarias del restaurante.
La API está diseñada para ser utilizada por los usuarios con roles de admin y vendedor. Estos roles permitirán realizar diversas acciones sobre el flujo de caja, incluyendo la configuración del saldo inicial, registro de ventas y compras, y la ejecución de arqueos de caja.

## Tecnologías Utilizadas

-   **Laravel v12.0.4:** Framework PHP para el desarrollo de la API.

-   **MySQL:** Base de datos relacional para el almacenamiento de información.

-   **Autenticación con Bearer Token:** Utilizado para proteger las rutas de la API, garantizando que solo los usuarios autenticados puedan acceder a ciertas funciones.

## Funcionalidades Principales

La API permite la gestión de los siguientes procesos para un restaurante:

1. **Configuración de Saldo Inicial**.-
   Se establece un saldo inicial de caja desde el cual se gestionan los ingresos y egresos.

2. **Registro de Ingresos**.-
   Permite registrar las ventas realizadas, sumando el monto al saldo de caja.

3. **Registro de Egresos**.-
   Permite registrar las compras y otros gastos del restaurante, restando el monto del saldo de caja.

4. **Arqueo de Caja**.-
   Realiza un arqueo de caja, comparando el saldo registrado con el saldo efectivo, para asegurar que ambos coincidan.

5. **Seguimiento de Flujo de Efectivo**.-
   Monitorea el saldo acumulado de la caja y permite realizar consultas sobre el flujo de efectivo en cualquier momento.

## Usuarios y Roles

La API tendrá dos tipos de usuarios predeterminados:

**Admin:** Usuario con permisos completos para gestionar todos los aspectos del sistema.

**Vendedor:** Usuario con permisos limitados para registrar ventas.

## Autenticación

La API utiliza autenticación basada en Bearer Tokens para proteger las rutas. Los usuarios deben autenticarse mediante un endpoint de login para obtener un token, que luego deben incluir en el encabezado de autorización `(Authorization: Bearer {token})` para acceder a las rutas protegidas.

### Login

Permite a los usuarios obtener un Bearer Token al proporcionar sus credenciales (email y password).

### Acceso a Endpoints Protegidos

Las solicitudes posteriores deben incluir el token JWT en el encabezado `Authorization` con el prefijo `Bearer`.

## Endpoints Principales

1.
2. `//pass`
3.

## Modelo de Datos

El archivo: diagramaER.dbml describe las relaciones entre los diferentes componentes del sistema (productos, ventas, gastos, etc.); está disponible para su revisión y contiene la estructura detallada de las tablas y relaciones de la base de datos.

## Instalación y Configuración

### Requisitos

-   PHP (>= 8.1)
-   Composer
-   MySQL

### Pasos para Iniciar

#### Clona el repositorio:

```
git clone https://github.com/alvaritogsg/restaurant-basic-api.git
```

```
cd restaurant-basic-api
```

#### Instala las dependencias del proyecto:

    composer install

#### Configura tu archivo .env con los detalles de la base de datos:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=flujo_caja
DB_USERNAME=usuario
DB_PASSWORD=contraseña
```

#### Ejecuta las migraciones para crear las tablas:

    php artisan migrate

#### Crea los usuarios predeterminados (admin y vendedor):

    php artisan db:seed

#### Inicia el servidor:

    php artisan serve

Ahora puedes acceder a la API en http://localhost:8000.

## License

API-restaurant es un software de código abierto licenciado bajo la [Licencia MIT](https://opensource.org/licenses/MIT).
