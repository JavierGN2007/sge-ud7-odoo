# Gestión de Usuarios, Grupos, Roles y Privilegios - Estilo Infantil S.L.

## Clasificación de Tipos de Usuarios de Odoo

* **Usuario Interno:** Miembros de la organización con acceso a la interfaz operativa de gestión. Sus permisos dependen directamente de las aplicaciones y grupos asignados.
* **Usuario Portal:** Clientes externos con acceso autenticado limitado a un área web privada para consultar presupuestos, facturas y pedidos propios, sin visibilidad del backend ni del resto de la empresa.
* **Usuario Público:** Visitantes anónimos sin credenciales que únicamente acceden a la vista pública de la web o catálogo online.

---

## Usuarios
| Nombre y Apellidos | Puesto de Trabajo | Correo de Acceso | Tipo de Usuario | Privilegios por Módulo | Justificación |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Javier Gallego** | Comercial Junior | `comercial@estiloinfantil.es` | Interno | • **Ventas:** Usuario: solo mostrar documentos propios<br>• **Facturación:** Ninguno<br>• **Inventario:** Usuario<br>• **Grupo Propio:** Estilo Infantil / Comercial Junior | Elabora presupuestos y contacta clientes. No debe ver cotizaciones de otros comerciales ni consultar datos financieros de la empresa. |
| **Elena Morales Ruiz** | Responsable de Ventas | `ventas@estiloinfantil.es` | Interno | • **Ventas:** Administrador<br>• **Facturación:** Ninguno<br>• **Inventario:** Usuario | Supervisa al equipo comercial, revisa y aprueba todos los presupuestos emitidos en la compañía. |
| **Javier Nieto Vega** | Administración y Facturación | `administracion@estiloinfantil.es` | Interno | • **Ventas:** Ninguno<br>• **Facturación:** Facturación / Contable<br>• **Inventario:** Ninguno | Emite y valida facturas oficiales y gestiona los cobros, sin intervenir en el ciclo de negociación de ventas. |
| **Laura Martínez Romero** | Cliente Particular | `laura.martinez.romero@gmail.com` | Portal | • **Portal:** Usuario externo | Consulta sus pedidos tramitados y descarga sus documentos en formato digital. |

---

## Grupos
* **Nombre del grupo:** `Estilo Infantil / Comercial Junior`
* **Herencia configurada:** `Ventas / Usuario: solo mostrar documentos propios` (asume la base operativa estándar de ventas).
* **Usuario asignado:** `Javier Gallego`

## 4. Evidencias de Acceso y Restricciones

* **Acceso Comercial (Javier Gallego):** La interfaz muestra el menú de Ventas y Contactos, con ausencia total del módulo de Contabilidad/Facturación. Intento de supresión de presupuestos bloqueado por permisos.
* **Acceso Administración (Javier Nieto Vega):** Interfaz enfocada en Facturación sin acceso a herramientas comerciales de venta.