# Pruebas de API con Postman y JSONPlaceholder

Este repositorio contiene documentación práctica para aprender y practicar el uso de Postman realizando pruebas de tipo CRUD (Crear, Leer, Actualizar, Eliminar) utilizando la API pública [JSONPlaceholder](https://jsonplaceholder.typicode.com/).

## 🛠 Herramientas necesarias

- [Postman](https://www.postman.com/downloads/) (versión de escritorio o en navegador)
- Conexión a internet
- Cuenta gratuita en Postman (opcional pero recomendable)

---

## 🌐 Qué es JSONPlaceholder

JSONPlaceholder es una API REST gratuita de prueba que simula un servidor real con datos falsos, ideal para practicar solicitudes HTTP como `GET`, `POST`, `PUT`, y `DELETE`.

---

## 🔍 Pruebas CRUD realizadas

### ✅ GET - Leer un post

- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Método:** `GET`
- **Descripción:** Recupera los datos del post con ID 1.
- **Respuesta esperada:**

```json
{
  "userId": 1,
  "id": 1,
  "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
  "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"
}
```

---

### 📝 POST - Crear un nuevo post

- **URL:** `https://jsonplaceholder.typicode.com/posts`
- **Método:** `POST`
- **Headers:**  
  `Content-Type: application/json`
- **Body (raw > JSON):**

```json
{
  "title": "Mi primer post",
  "body": "Este es el contenido del post",
  "userId": 1
}
```

- **Respuesta esperada:**

```json
{
  "title": "Mi primer post",
  "body": "Este es el contenido del post",
  "userId": 1,
  "id": 101
}
```

---

### ✏️ PUT - Actualizar un post existente

- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Método:** `PUT`
- **Headers:**  
  `Content-Type: application/json`
- **Body (raw > JSON):**

```json
{
  "id": 1,
  "title": "Título actualizado por mí",
  "body": "Este post ha sido modificado con éxito.",
  "userId": 1
}
```

- **Respuesta esperada:** El mismo JSON enviado.

---

### ❌ DELETE - Eliminar un post

- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Método:** `DELETE`
- **Headers:** No requiere
- **Body:** No requiere
- **Respuesta esperada:** Estado 200 OK o 204 No Content (sin cuerpo)

---

## 🧪 Recomendaciones adicionales

- Siempre verificar que `Content-Type: application/json` esté presente al usar `POST` o `PUT`.
- JSONPlaceholder **no guarda cambios reales**, por lo que cada solicitud de escritura es simulada.
- Puedes usar la función de **colecciones de Postman** para guardar estas pruebas.

---

## 🗂 Estructura sugerida del repositorio

```
/postman-api-practice
├── README.md
└── JSONPlaceholderCRUD.postman_collection.json
```

---

## 📚 Recursos útiles

- Postman: https://www.postman.com/
- JSONPlaceholder: https://jsonplaceholder.typicode.com/
- Documentación oficial de Postman: https://learning.postman.com/

---

**Autor:** *[Tu Nombre]*  
**Propósito:** Documentación para práctica personal de pruebas de APIs con Postman.

### MIT License
### Copyright (c) 2025 Jose Magariño
### See LICENSE file for more details.
