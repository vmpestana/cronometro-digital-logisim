# Cronómetro digital en Logisim

Cronómetro con tiempo configurable, selector de velocidad y máquina de estados, diseñado en Logisim-evolution. Muestra minutos y segundos en displays y avisa con un LED cuando llega al tiempo configurado.

Proyecto del tercer parcial (Universidad del Norte).

**Autores:** Victor Mendoza y equipo

## Qué hace

- Cuenta minutos y segundos (`MIN_DEC`, `MIN_UNI`, `SEG_DEC`, `SEG_UNI`).
- Permite configurar el tiempo objetivo antes de empezar.
- Tiene botones de **START** y **RESET**.
- Cambia la velocidad del conteo con un selector.
- Enciende `FINISH_LED` cuando el tiempo actual alcanza el configurado.

## Cómo está construido

| Módulo | Función |
|---|---|
| `main` | Circuito principal |
| `STATE_MACHINE` | Controla los estados del cronómetro con flip-flops |
| `PULSE_DETECTOR` | Convierte la pulsación de un botón en un solo pulso |
| `TICK_GENERATOR` | Genera los pulsos de conteo a partir del reloj |
| `SPEED_SELECTOR` | Elige a qué velocidad avanza el conteo |
| `CHRONOMETER` | Contadores de segundos y minutos |
| `CONFIG_TIME` | Guarda el tiempo objetivo |
| `FINISH_COMPARATOR` | Compara el tiempo actual con el configurado |
| `DISPLAY_BLOCK` | Convierte los valores a BCD para los displays |

## Cómo abrirlo

1. Instala [Logisim-evolution](https://github.com/logisim-evolution/logisim-evolution) 4.1 o superior.
2. Abre `cronometro.circ`.
3. Activa la simulación del reloj (*Simulate → Auto-Tick Enabled*), configura el tiempo y pulsa START.
