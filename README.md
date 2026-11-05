# Grupo1-Fernandez-Bitacora-4-4-2026-AyE
Hoy hice toda la conexion a base de datos y lo guarde en un archivo json. Para guardarlo en la base de datos, cree la 
carpeta BaseDeDatos con las clases con sus respectivas variables: 
- CartaDB <kbd>
  - public int ID { get; set; }
  - public int partida_id { get; set; }
  - public int fila { get; set; }
  - public int columna { get; set; }
  - public int id_valor { get; set; }
  - public int esta_descubierta { get; set; }
  - public int esta_emparejada { get; set; }
  </kbd>
- JugadorDB <kbd>
  - public int ID { get; set; }
  - public string Nombre { get; set; }
     </kbd>
- Modo_JuegoDB <kbd>
  - public int ID { get; set; }
  - public string nombre { get; set; }
  - public string descripcion { get; set; }
  - public bool disponible { get; set; }
  - public int cantidad_jugadores { get; set; }
  - public bool guarda_records { get; set; }
     </kbd>
- MovimientoDB <kbd>
  - public int ID { get; set; }
  - public int partida_id { get; set; }
  - public int fila1 { get; set; }
  - public int columna1 { get; set; }
  - public int fila2 { get; set; }
  - public int columna2 { get; set; }
  - public int acierto { get; set; }
  - public DateTime momento { get; set; }
     </kbd>
- PartidaDB <kbd>
  - public int ID { get; set; }
  - public int Jugador_id { get; set; }
  - public int Nivel_id { get; set; }
  - public int Tematica_id { get; set; }
  - public DateTime Fecha { get; set; }
  - public int Intentos { get; set; }
  - public int Aciertos { get; set; }
  - public int Fallos { get; set; }
  - public int Tiempo_segundos { get; set; }
  - public int Puntuacion { get; set; }
  - public int Gano { get; set; }
     </kbd>
- Par_descubiertoDB <kbd>
  - public int ID { get; set; }
  - public int Partida_id { get; set; }
  - public int Id_valor { get; set; }
  - public int Puntos { get; set; }
     </kbd>
- RecordDB <kbd>
  - public int ID { get; set; }
  - public int Partida_id { get; set; }
  - public int Jugador_id { get; set; }
  - public int Nivel { get; set; }
  - public int Intentos { get; set; }
  - public int Aciertos { get; set; }
  - public int Fallos { get; set; }
  - public int Tiempo_segundos { get; set; }
  - public int Puntuacion { get; set; }
  - public DateTime Fecha { get; set; }
     </kbd>
- TematicaDB
