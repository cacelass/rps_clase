Práctica Axentes Intelixentes
=============================

rps_clase de Alejandro Cancelas Chapela

## Descripcion
Proponse programar un axente intelixente solución ao entorno de tarefas do xogo pedra, papel, tesoiras, seguindo as directrices de modelado propostas no capítulo 2 _Intelligent Agents_ do libro _IA: A modern approach, Russell & Norvig_.

El proyecto sigue los principios SOLID, permitiendo estender a lógica a otras versiónes del juego.

Contorno de tarefas | Observable| Axentes | Determinista | Episódico | Estático | Discreto | Coñecido
:---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
 RPS | No | Multiagente | Estocástico | Secuencial y Estocástico | Estatico |  Discreto |  No |

Este proyecto implementa un Agente Secuencial de Predicción por Frecuencia en Python. El agente está diseñado para jugar y ganar contra un oponente humano detectando y explotando patrones de juego.

El agente transforma el entorno del juego de episódico a secuencial mediante el uso de la memoria (memoria = []), que almacena el historial de las jugadas del usuario.

1. De 1 a 5 rondas elige una acción completamente aleatoria.
2. De la ronda 6 en adelante activa el análisis de frecuencia para buscar patrones.
    1.    Calcula el ** porcentaje** de cada jugada del usuario a partir del historial.
    2. Identifica el porcentaje máximo (max_porcentaje).
    3. Si max_porcentaje > 0.40: El agente predice que el usuario repetirá esa acción y juega la acción que GANA a esa jugada (lógica inversa).
    4. Si max_porcentaje <= 0.40: El patrón es incierto. El agente vuelve a la elección aleatoria para mantener su robustez.

### Mejoras


Unha vez programado o axente para a versión clásica do RPS, extende o súa lóxica para xogar á versión  [pedra, papel, tesoiras, lagarto, Spock](http://www.samkass.com/theories/RPSSL.html)

## Estructura de directorios y archivos resultantes

    rps_clase
    ├── pyproject.toml
    ├── README.md
    └── src
        ├── rps_clase
        │   ├── __init__.py
        │   └── main.py
        └── test
            ├── __init__.py
            └── test_proba.py
