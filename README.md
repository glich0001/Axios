# Integración de Axios en una Aplicación Next.js

## Scripts Disponibles

En el directorio del proyecto, puedes ejecutar:

### `npm install`

Para instalar las todas dependecias en la carpeta /nodemodules

### `npm run dev`

Ejecuta la aplicación en modo de desarrollo.
Abra [http://localhost:3000](http://localhost:3000) para verlo en su navegador.

### `code .`
Para abrir la carpeta de proyecto

## Detalles
integracion de axios en el proyecto
Conexión a una API Externa:

![Agregar]
// Obtain User by ID
export const getUserByID = (id) => {
    return axios.get(`https://reqres.in/api/users/${id}`);
} 

// Create User
export const createUser = (name, job) => {
    let body = {
        name: name,
        job: job
    }

    // Returns the response with a Promise
    return axios.post('https://reqres.in/api/users', body)
}

// Update User
export const updateUserByID = (id, name, job) => {
    let body = {
        name: name,
        job: job
    }

    // Returns the response with a Promise
    return axios.put(`https://reqres.in/api/users/${id}`, body)
}

// Delete User
export const deleteUserByID = (id) => {
    return axios.delete(`https://reqres.in/api/users/${id}`);
} 


Visualización de Datos:



Gestión de Errores y Excepciones:

 //En caso de un error genera una ventana emergente de alerta 
 
Integrar Axios en tu proyecto es un proceso sencillo. Aquí te dejo los pasos a seguir:

1. **Instalación**: Primero, necesitas instalar Axios en tu proyecto. Puedes hacerlo utilizando npm o yarn. Aquí te dejo los comandos para ambos:

```bash
npm install axios
# o
yarn add axios
```

2. **Importación**: Una vez que Axios esté instalado, puedes importarlo en cualquier archivo donde quieras hacer solicitudes HTTP. Aquí te dejo un ejemplo de cómo hacerlo:

```javascript
import axios from 'axios';
```

3. **Uso**: Ahora puedes usar Axios para hacer solicitudes HTTP. Aquí te dejo un ejemplo de cómo hacer una solicitud GET:

```javascript
axios.get('https://api.example.com/data')
  .then(response => {
    console.log(response.data);
  })
  .catch(error => {
    console.error('Error:', error);
  });
```

4. **Configuración**: Axios también te permite configurar instancias de Axios con valores predeterminados. Esto puede ser útil si estás haciendo muchas solicitudes al mismo servidor, por ejemplo:

```javascript
const api = axios.create({
  baseURL: 'https://api.example.com',
  timeout: 1000,
  headers: {'X-Custom-Header': 'foobar'}
});
```


