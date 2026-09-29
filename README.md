# Horario de Transporte Escuela Guadalupe

Proyecto Spring Boot + Thymeleaf + MySQL para registrar los horarios semanales y las lecciones acumuladas.

## Estructura

- `com.guadalupe` - aplicación principal
- `com.guadalupe.controller` - páginas y API
- `com.guadalupe.domain` - entidades JPA
- `com.guadalupe.repository` - acceso a datos
- `com.guadalupe.service` - lógica del sistema
- `com.guadalupe.config` - datos iniciales
- `templates` - HTML
- `static/css` - estilos
- `static/js` - JavaScript
- `database` - script SQL opcional

## Base de datos remota

La aplicación está preparada para usar una base MySQL remota mediante variables de entorno:

- `DB_URL`
- `DB_USERNAME`
- `DB_PASSWORD`

Ejemplo de `DB_URL`:

`jdbc:mysql://HOST:PUERTO/horario_guadalupe?sslMode=REQUIRED&serverTimezone=America/Costa_Rica`

No coloque las credenciales reales dentro del código si el proyecto se va a subir a GitHub.

## Pasos

1. Crear una base MySQL remota.
2. Ejecutar `database/horario_guadalupe.sql` si se desea crear las tablas manualmente.
3. Configurar `DB_URL`, `DB_USERNAME` y `DB_PASSWORD` en el entorno de ejecución.
4. Abrir el proyecto como Maven en NetBeans.
5. Ejecutar `ZonaGuadalupeApplication`.
6. Entrar a `http://localhost:8080` durante las pruebas locales. La información sigue guardándose en la base remota configurada.

## Nota

`spring.jpa.hibernate.ddl-auto=update` está activo para que Hibernate pueda crear o actualizar las tablas. Si las tablas ya fueron creadas con el script SQL, la aplicación las utilizará.
