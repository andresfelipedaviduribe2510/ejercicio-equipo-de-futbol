# Ejercicio: Equipo de Fútbol

## El Problema
Una liga local de fútbol necesita digitalizar su operación. Actualmente llevan todo en hojas de Excel y es un caos. El sistema debe permitir gestionar Equipos, Jugadores y los Partidos que se juegan.

## Reglas de Negocio (Para el MER)
- **Equipos:** Cada equipo tiene un nombre único, una ciudad y un director técnico.
- **Jugadores:** Cada jugador pertenece a un solo equipo. Se debe registrar su nombre, número de camiseta (dorsal) y posición (Portero, Defensa, etc.).
- **Partidos:** Un partido ocurre entre dos equipos (Local y Visitante). Se debe registrar la fecha, la hora y el resultado final (goles local e goles visitante).

## Fase 1: Modelado y Normalización
Pídales que entreguen el Modelo Entidad-Relación (MER) y que apliquen las primeras tres formas normales (1FN, 2FN, 3FN).

**Punto clave para evaluar:** ¿Cómo manejan la relación entre Equipos y Partidos? (Un equipo participa en muchos partidos, y un partido tiene exactamente dos equipos).

**Normalización:** Deben asegurarse de que no haya redundancia en los nombres de los equipos dentro de la tabla de jugadores o partidos.

## Fase 2: Implementación en la Base de Datos
Una vez aprobado el diseño, deben llevarlo a SQL (MySQL o PostgreSQL). El script debe incluir:
- Creación de la base de datos.
- Definición de tablas con sus respectivas Primary Keys y Foreign Keys.
- Restricciones (NOT NULL, UNIQUE para nombres de equipos, etc.).
- Un script de "Seed" con al menos 4 equipos y 10 jugadores para probar.

## Fase 3: El CRUD (Capa de Aplicación)
Para cerrar el ciclo, deben desarrollar un pequeño backend (pueden usar Node.js, .NET o el lenguaje que estén viendo) para gestionar la tabla de Jugadores.

### Requerimientos del CRUD:
- **Create:** Registrar un nuevo jugador asignándolo a un equipo existente.
- **Read:** Listar todos los jugadores, mostrando el nombre del equipo al que pertenecen (aquí deben usar un JOIN en la consulta).
- **Update:** Poder cambiar a un jugador de equipo o actualizar su número de camiseta.
- **Delete:** Dar de baja a un jugador del sistema.
