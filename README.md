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
- TematicaDB <kbd>
    - public int ID { get; set; }
    - public string Nombre { get; set; }
    - public string Carpeta { get; set; }
    </kbd>
Sumado a esto, añadi las respectivas funciones las cuales se encargan de añadir los datos a cada tabla de la base.
<img width="3357" height="306" alt="image" src="https://github.com/user-attachments/assets/f7db7cb0-04ba-4737-bf33- c47dc2bdf0cb" /> FUNCION PARA GUARDAR LOS DATOS EN LA TABLA JUEGO

<img width="1581" height="966" alt="image" src="https://github.com/user-attachments/assets/a8955cab-d2cc-4bfc-bda4-6aa009d8dfc5" /> DOS FUNCIONES PARA GUARDAR LOS DOS JUGADORES QUE VAN A JUGAR. EL PRIMERO ES EL USUARIO Y EL OTRO ES POR SI
EL USUARIO DECIDE JUGAR AL MODO MULTIJUGADOR

<img width="2394" height="747" alt="image" src="https://github.com/user-attachments/assets/974e93b1-250d-4314-b23e-235e45a93dc4" /> FUNCION LA CUAL DIBUJA PARA PODER INGRESAR EL NOMBRE AL INICIO

<img width="2076" height="1341" alt="image" src="https://github.com/user-attachments/assets/204df26a-f063-4849-928a-54ea2782e549" /> DOS FUNCIONES: INITIALIZE PARA PODER EJECUTAR LAS FUNCIONES Y QUE SE GUARDEN LOS DATOS EN LA BASE DE DATOS Y
CARGARTEMATICAS PARA CARGAR LOS DATOS DE TEMATICA EN LA BASE

- Tambien añadi lineas a funciones ya creadas para que funcione todo: <kbd>         
        - case EstadoJuego.IngresarNombre: DibujarIngresarNombre(); break;
        - case EstadoJuego.IngresarNombre2: DibujarIngresarNombre2(); break;
 </kbd> 
 - Añadi estas dos lineas en en el switch (_estado) en Draw, basicamente si la pantalla es la de ingresar el nombre de
 alguno de los dos usuarios dibuja lo necesario en la pantalla. <kbd>    
        - case EstadoJuego.IngresarNombre:
        - ActualizarIngresarNombre(Tecla);
        - break;
        - case EstadoJuego.IngresarNombre2:
        - ActualizarIngresarNombre2(Tecla);
        - break;
</kbd> Otras lineas que tambien añadi a un switch (_estado), pero esta vez en la funcion Update. Esto se encarga de determinar que botones tiene la pantalla correspondiente (en este caso IngresarNombre, la cual solo tiene para ingresar nombre osea Tecla).

<img width="2574" height="348" alt="image" src="https://github.com/user-attachments/assets/cdbadde4-8b99-4181-b2ef-9888ad2bbd77" /> Lo añadi en la funcion IniciarPartida, sirve para que en el modo Multijugador muestre los nombres ingresados
y no "Jugador 1","Jugador 2".

<img width="3153" height="891" alt="image" src="https://github.com/user-attachments/assets/f17b723a-a275-44a4-b9a7-f877e367104a" /> Si hay mas de un usuario, se pone en la pantalla de ingresar nombre (multijugador), ademas, esta
la funcion GuardarModoJuego(), esto para que cada vez que el usuario elija un modo se guarde en la base de datos.

bool enMenu = _estado == EstadoJuego.IngresarNombre || _estado == EstadoJuego.IngresarNombre2 || _estado == EstadoJuego.Inicio || _estado == EstadoJuego.SeleccionModo || _estado == EstadoJuego.ElegirNivel; Lo añadi en la funcion
ActualizarMusica, basicamente se encarga de que en las pantallas IngresarNombre suene la musica del menu.

<img width="2745" height="291" alt="image" src="https://github.com/user-attachments/assets/fde3303c-07ee-4163-9e82-1b4bd0cb6913" /> El juego empieza en la pantalla ingresar nombre y lo que el usuario ingrese se guarda en la variable
_nombreJugador.

public enum EstadoJuego { IngresarNombre, Inicio, SeleccionModo, IngresarNombre2, ElegirNivel, Jugando, Gano, Perdio }
Añado dos nuevas pantallas; IngresarNombre (para el inicio) y IngresarNombre2 (para el multijugador)




