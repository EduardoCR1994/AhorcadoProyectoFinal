# Proyecto Ahorcado - Programación Avanzada SC-601

## Integrantes

- Castro Rojas Eduardo (FI13005258)
- Cespedes Morales Brandon Steven (FH22012992)
- Flores Carmona Jimena (FH23014559)
- Hidalgo de la O Mariana (FH23015127)

## Tecnología

- ASP.NET Web Application (.NET Framework 4.8.1)
- Entity Framework 6 (Code First)
- SQL Azure

## Diagrama de Base de Datos (Mermaid)

```mermaid
erDiagram
    Jugadores {
        int IdJugador PK
        bigint Cedula UNIQUE
        nvarchar Nombre
    }
    Palabras {
        int IdPalabra PK
        nvarchar PalabraTexto UNIQUE
    }
    Partidas {
        int IdPartida PK
        int IdJugador FK
        int IdPalabra FK
        nvarchar Nivel
        nvarchar Resultado
        datetime FechaHora
    }
    Jugadores ||--o{ Partidas : "tiene"
    Palabras ||--o{ Partidas : "asociada"
