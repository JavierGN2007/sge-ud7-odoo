# Errores y Comprobaciones de Instalación

## 1. Comprobaciones
Para evitar fallos durante la instalación con Docker, se hicieron las siguientes verificaciones:
* **Estado de Docker:** Se comprobó que Docker estuviera iniciado y funcionando correctamente.
* **Disponibilidad de puertos:** Se verificó que el puerto `8069` estuviera libre.
* **Revisión del archivo de configuración:** Se revisó el archivo `docker-compose.yml`, asegurando que las credenciales de usuario y contraseña coincidieran tanto en el servicio de Odoo como en el de la base de datos PostgreSQL.

---

## 2. Documentación y resolución de error típico simulado

| Error o mensaje | Causa | Solución aplicada | Fuente consultada |
| :--- | :--- | :--- | :--- |
| `Bind for 0.0.0.0:8069 failed: port is already allocated` | El puerto `8069` del equipo anfitrión está ocupado por otro proceso o contenedor en ejecución. | Cambiar el puerto del host en el archivo `docker-compose.yml` a `"8070:8069"`, reiniciar el contenedor con `docker compose up -d` y acceder a Odoo a través de `http://localhost:8070`. | [Documentación oficial de Docker - Port binding](https://docs.docker.com/network/) |