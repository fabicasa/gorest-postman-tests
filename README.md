# GoRest API Tests con Postman + GitHub actions

Este proyecto automatiza pruebas sobre la API pública de la siguiente url- ( https://gorest.co.in/) 
utilizando "Postman" para definir los endpoints y "Newman" para su ejecución automática a través de "GitHub Actions" (CI/CD).

------------------------------------------------------------------------------------------------------------------------------

# Requisitos

Antes de ejecutar el proyecto, asegurarse de tener instalado lo siguiente:

- [Postman](https://www.postman.com/downloads/)
- [Node.js + npm](https://nodejs.org/)
- [Newman](https://www.npmjs.com/package/newman)
- Git
Instalar Newman:
bash
npm install -g newman
-------------------------------------------------------------------------------------------------------------------------------
# Contenido del proyecto

- Colección de Postman con los endpoints automatizados y la variable de entorno-->GoRestAPItests.postman_collection.json / GoRestEnv.postman_environment.json	
- Flujo de GitHub Actions para ejecutar pruebas en cada push --> .github/workflows/postman.yml	
- Instrucciones y detalles del proyecto-->README.md
--------------------------------------------------------------------------------------------------------------------------------
# Token de autenticación
Se debe configurar como una variable de entonrno llamada ACCESS_TOKEN
--------------------------------------------------------------------------------------------------------------------------------
# Enpoints automatizados
- Listado de usuarios
- Crear new user
- Actualizar un user
- Eliminar un User
----------------------------------------------------------------------------------------------------------------------------------
# Ejecutar pruebas localmente
Ejecutar colección con Newman en el Git: newman run gorest-api.postman_collection.json
# Integración continua con Github
Se ejecuta automáticamente la colección cada que se hace push a la rama: .github/workflows/testApi.yml

---------------------------------------------------------------------------------------------------------------------------------
NOTA ADICIONAL:
El email de los usuario incluye (timestamp) para evitar errores por duplicidad.
