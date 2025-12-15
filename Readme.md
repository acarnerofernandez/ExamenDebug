# Examen de Depuración en PyCharm

---

## **Instrucciones:**

1. Realiza un fork de este repositorio y clónalo.
1. Las respuestas a las preguntas realízalas en este Readme
2. Cada pregunta vale un punto
<img width="866" height="154" alt="Captura desde 2025-12-15 13-53-05" src="https://github.com/user-attachments/assets/e28f427e-0f74-4513-943b-0b50b786c05e" />

### Apartado 1

- Coloca un punto de interrupción **normal** en la línea donde se inicializa la lista de la serie: `serie = [0, 1]`. 
- Inicia el modo *Debug*.

**Pregunta**

1. Si la función es llamada con `n=10`, ¿cuál es el valor de la variable `n` que se visualiza en la ventana de variables del debugger justo antes de que se ejecute la línea `serie = [0, 1]`?

N sera igual a 10

!(<img width="629" height="258" alt="imagen" src="https://github.com/user-attachments/assets/46a89503-dd47-48c8-84ab-5bf54862defc" />)

---

### Apartado 2

-  Asegúrate de que la llamada a la función es `print(funcion_bucle(10))`.
-  Inicia el modo *Debug* y avanza hasta que la ejecución se detenga en la línea `siguiente_numero = calcular_siguiente(serie)`.
-  Utiliza la opción de depuración adecuada para **entrar dentro** de la función `calcular_siguiente`.

**Preguntas**

1. Justo cuando el debugger se detiene dentro de la función `calcular_siguiente` por **primera vez**, ¿cuál es el valor que tiene la variable local `aux` *después* de que se ejecute la línea `aux = serie[-1] + serie[-2]`?
**(Indica el valor numérico exacto de la variable `aux` en ese momento y el nombre de la herramienta de *debugging* que utilizaste para entrar en la función).**

el valor de aux es 1 y la herramienta fue step into

!(<img width="1346" height="832" alt="Captura desde 2025-12-15 14-05-43" src="https://github.com/user-attachments/assets/b2cf4396-1fa2-41da-882f-89be296caf12" />)

2. Si estuvieras dentro de la función `calcular_siguiente` y quisieras salir rápidamente sin ejecutar el resto de las líneas, volviendo al punto de llamada en `funcion_bucle`, ¿qué función del debugger deberías usar?

para salir usaria step out 

!(<img width="835" height="810" alt="Captura desde 2025-12-15 14-24-09" src="https://github.com/user-attachments/assets/d8a83242-cd42-4cd1-8e8e-0f1119f19c68" />)


3. ¿Qué diferencia fundamental existe entre usar *Step Over* y *Step Into* en la línea `siguiente_numero = calcular_siguiente(serie)`?

La diferencia es clara, el step into te manda a la funcion para que se ejectue linea por linea, step over lo que hace es ejecutar esa linea en concreto,
haciendo asi la funcion directamente

---

### Apartado 3

-  Cambia la llamada a la función para que el número de elementos sea mayor: `print(funcion_bucle(1000))`.
-  Establece un **Breakpoint Condicional** para que la ejecución se detenga solo cuando `siguiente_numero` sea **mayor que 20000**.

<img width="781" height="250" alt="Captura desde 2025-12-15 14-12-01" src="https://github.com/user-attachments/assets/fc55fd1d-0f32-4138-ae5e-01bc343b9b09" />

**Pregunta**

1. Cuando el *Breakpoint Condicional* se activa por **primera vez** (la primera vez que `siguiente_numero` es mayor que 20000), ¿qué longitud tiene `serie`?

La longitud de serie seria 2584

!(<img width="1040" height="286" alt="Captura desde 2025-12-15 14-14-29" src="https://github.com/user-attachments/assets/6a2761b2-5026-4da9-ba00-b9e2db83571f" />)

---
