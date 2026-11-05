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
- MovimientoDB
- PartidaDB
- Par_descubiertoDB
- RecordDB
- TematicaDB
