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
        INT IdJugador PK
        BIGINT Cedula
        NVARCHAR Nombre
    }
    Palabras {
        INT IdPalabra PK
        NVARCHAR PalabraTexto
    }
    Partidas {
        INT IdPartida PK
        INT IdJugador FK
        INT IdPalabra FK
        NVARCHAR Nivel
        NVARCHAR Resultado
        DATETIME FechaHora
    }
    Jugadores ||--o{ Partidas : juega
    Palabras ||--o{ Partidas : contiene

