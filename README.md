# Prueba Técnica (Dinámica: Aseguradora)

## Descripción de la prueba

Esta prueba técnica consta de un backend desarrollado con .NET Core Web API en la versión .NET 8. y de un frontend que se ha desarrollado utilizando React con Vite, Tailwind, NextUI, Redux y Axios. La versión de Node.js utilizada es v20.11.1. Ademas de usar como Base de Datos, MySQL en la version 8.0.36

para clonar este repo usar: ```git clone --recurse-submodules ...```

Ejemplo: 

    git clone --recurse-submodules https://github.com/MarckJrquin/prueba_tecnica_aseguradora.git


## Tecnologías Utilizadas

### Base de Datos
- **Nombre de BD**: aseguradora
- **Gestor de BD**: MySQL
- **Versión de Node.js**: 8.0.36
- **Revisar conexión**: (Puerto:  3306; Usuario: root; Pass: 12345)

### Backend
- **Framework**: .NET Core Web API
- **Versión**: .NET 8

### Frontend
- **Librería**: React
- **Herramientas**: Vite, Tailwind, NextUI, Redux, Axios
- **Versión de Node.js**: v20.11.1

## Instrucciones

### Frontend

Para iniciar el proyecto frontend, seguir estos pasos:

1. Instala las dependencias:
    ```sh
    npm install
    ```

2. Ejecuta el proyecto:
    ```sh
    npm run dev
    ```

### Base de Datos

Hay una exportación de la base de datos con data demo

#### Usuario tipo admin
- **Username**: marckjrquin
- **Contraseña**: ABC123abc

#### Usuario tipo user
- **Username**: gatiuska
- **Contraseña**: ABC123abc

Si no deseas utilizar los usuarios demo, puedes registrar un usuario utilizando Swagger con el endpoint: ```/api/Auth/signup```

El formato de registro es el siguiente:

```json
{
  "username": "string",
  "email": "string",
  "password": "string",
  "firstName": "string",
  "lastName": "string",
  "dateOfBirth": "2024-07-30",
  "role": "string"
}
```
En el campo role, puede colocar "User" o "Admin".

### Migracion de Base de Datos (Alternativa de Cero)
Para preparar y migrar la base de datos a MySQL, puedes utilizar los siguientes comandos:

1. Crear Base de datos en MySQL:
    ```sql
    CREATE DATABASE aseguradora;
    ```

2. Agregar migraciones:
    ```sh
    dotnet ef migrations add InitialCreate
    ```

3. Actualizar la base de datos:
    ```sh
    dotnet ef database update
    ```



