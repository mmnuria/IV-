# Errores frecuentes - Objetivo 4

El código se debe desarrollar siguiendo la metodología que se ha venido
comentando desde el objetivo 2. Si no se hace así, el código es incorrecto. Eso
quiere decir que todos los issues deben estar relacionados con una historia de
usuario, y deben estar también asignados a un milestone. Olvidar hacerlo así
indica que el estudiante no se preocupa por la metodología, simplemente de hacer
código para "pasar el objetivo". Y este objetivo va *de usar la metodología*, no
de producir código.

- No se debe usar *ninguna* biblioteca externa aparte de las de test. Se trata
  de testear el código propio. Ni siquiera se debe usar como parte del test
  aparte de las propias bibliotecas de test; si lo haces, tendrás que mostrar,
  como cualquier otra herramienta, que conoces las alternativas y que tienes los
  criterios apropiados para seleccionarla.

## Sobre las diferentes herramientas

- Hablar de "herramientas de test" sin especificar qué es lo que hacen esas
  herramientas de test. No existen las herramientas de test, existen
  herramientas que llevan a cabo diferentes funcionalidades relacionadas con los
  tests. El tipo de esas herramientas, para las funcionalidades que se requieren
  en el objetivo, es lo que hay que hay que reflejar aquí.

- En muchos casos, esto se debe a que se ha usado ChatGPT para generar los
  criterios. Los criterios son algo que debe establecer la persona, no un modelo
  de IA. Como se detecte el uso de herramientas de IA tanto en los criterios
  como en la lista de posibles herramientas, se dejará de corregir y se
  retrasará la corrección de la siguiente versión.

- Listar ventajas y desventajas no es un proceso objetivo, y sobre todo no tiene
  nada que ver con los criterios que se hayan elegido. Si las desventajas son
  razones para descartarlo, se debe incluir un criterio que permita descartarlos
  por esa razón.

- En general, sólo se debe incluir la información que permita entender por qué
  se ha elegido una u otra.

- Conviene confundir el comando que ejecuta los test, que es un comando
  *externo* al lenguaje, aunque puede ser también un subcomando del toolchain
  del lenguaje, y que *se llama test runner* porque ejecuta los tests, de la
  biblioteca que agrupa los tests y que permite crear *fixtures*. Como se ve,
  son funciones muy diferentes.

## Sobre el código

- Los issues deben plantear problemas, igual que en el objetivo 2. El código
  resuelve el problema, y para ver si se ha resuelto, deben usarse los tests.
  - Un issue no puede ser "hacer tests"
  - No se puede plantear "escribir código que haga esto" como issue. Debe
    plantearse el problema que debe resolverse.
- Un poco de trabajo a la hora de plantear los issues evita mucho trabajo más
  adelante escribiendo tests y por supuesto revisando el código.

- TDD no sólo es una metodología para escribir tests, es una para modularizar el
  código de forma que sea fácil de testear y para que sea más fácil de entender,
  refactorizar y evolucionar. Para hacer esto lo más importante, entre los
  principios SOLID, es la S de *Separation of concerns*: se trata de que cada
  función haga una cosa y solo una. Eso hace más fácil testear esa única cosa.
  - Si te preguntas si una función hace una sola cosa y solo una, en el momento
    que tengas más de un bucle o más de un `if` y sobre todo `if`s anidados, ya
    estás haciendo más de una cosa.

- Los tests deben estar *siempre* relacionados con las historias de usuario. Un
  PMV debe testear *solo* los diferentes problemas de la historia de usuario. Si
  te pones a testear todos los aspectos del programa como si hace una suma bien
  o si es capaz de llamar a un constructor correctamente estás solamente creando
  ruido para la persona que revisa.
