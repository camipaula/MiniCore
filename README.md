# MiniCore - Backend API

## Descripción
MiniCore es una API RESTful construida con ASP.NET Core que gestiona clientes, contratos y genera reportes personalizados basados en un rango de fechas. Este backend maneja la lógica de negocio y el acceso a los datos utilizando Entity Framework Core y una base de datos SQL Server.

## Características
- Gestión de Clientes y Contratos (CRUD).
- Generación de reportes personalizados de montos por cliente en un rango de fechas.
- Implementación de CORS para facilitar la interacción con el frontend.
- Uso de Entity Framework Core para la manipulación de datos.
  
## Tecnologías Utilizadas
- **ASP.NET Core 6.0**
- **Entity Framework Core**
- **SQL Server**
- **Newtonsoft.Json** para la serialización JSON

## Configuración del Proyecto

### Requisitos Previos
- **.NET 6 SDK** o superior.
- **SQL Server** (local o remoto).
- **Visual Studio** o cualquier IDE compatible con .NET.

### Instalación

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/camipaula/MiniCore.git
Configurar la cadena de conexión: En el archivo appsettings.json, configura la cadena de conexión a tu base de datos SQL Server:

json
Copiar código
"ConnectionStrings": {
  "Conexion": "Server=DESKTOP-4469NNS\\SQLEXPRESS;Database=MiniCore;User Id=sa;Password=1234;TrustServerCertificate=True;"
}
Aplicar migraciones a la base de datos: Abre la consola del administrador de paquetes (Package Manager Console) o la terminal y ejecuta:

bash
Copiar código
dotnet ef database update
Ejecutar el proyecto:

bash
Copiar código
dotnet run
Acceder a la documentación de la API con Swagger: La API estará disponible en https://localhost:7220/swagger.

Endpoints Principales
Clientes
GET /api/Clientes: Obtener todos los clientes.
GET /api/Clientes/{id}: Obtener un cliente específico.
POST /api/Clientes: Crear un nuevo cliente.
PUT /api/Clientes/{id}: Actualizar un cliente existente.
DELETE /api/Clientes/{id}: Eliminar un cliente.

Contratos
GET /api/Contratos: Obtener todos los contratos.
GET /api/Contratos/{id}: Obtener un contrato específico.
POST /api/Contratos: Crear un nuevo contrato.
PUT /api/Contratos/{id}: Actualizar un contrato existente.
DELETE /api/Contratos/{id}: Eliminar un contrato.

Reportes
GET /api/Reporte/Resultado: Generar un reporte de contratos entre fechas (fechaDesde, fechaHasta).
