1. **Escriban qué esperan de cada uno de los pasos**  

Paso 1) Pre-procesador: Analiza el código, en qué sentido? Con respecto a la escritua, es decir, semántica, reglas, etc. En caso de cometer errores me avisa lo que anda mal.  
Paso 2) Compilación I: En este paso se genera el código de assembler, aun legible para nosotros. Se hace un análisis semántico y se producen optimizaciones que la maquina cree necesarias.
Paso 3) Compilación II: Genera el pase de código assembler al código binario.
Paso 4) Linkeo: Busca la información necesaria (en librerias, otros códigos) para poder ejecutarse.

2.  **¿Qué agregó el preprocesador?**  

Muchas cosas! Me muestra un listado de cosas externas que va a necesitar mi código (calculator.c). Qué cosas va a necesitar las saca de mi archivo .h. Las cosas externas las va a buscar en el momento del linkeo de los lugares correspondientes. 
Otra cosa muy interesante es que si mi código tiene errores propios (me falta ; o cosas del estilo) el precompilado no me lo muestra! Muestra el código tal cual lo escribí. Si me equivoco en las funciones, como por ejemplo escribir mal el nombre, tampoco me lo muestra. Escribe que va a necesitar la funcion con el nombre mal escrito.  

[Cosas para no olvidar: Dije que no saltan los errores, pero cuando me avisa que algo anda mal? En los pasos 2 y 3. Cuando compila saltan los errores propios como error identificados por la maquina (sale la palabra error), los errores externos (escribir mal una funcion que vaya a utilizar) los identifica con warning, y me deja compilar. Recién cuando pase al último paso van a saltar los errores externos]  

3. **Identificar en la rutina de assembler las funciones**  

Las funciones son main y add_numbers. .LFB0 y LFB1. son etiquetas de las funciones.  
(Llama la atención la cantidad de pasos que hace para sumar dos numeritos, movlmovq)  

4. **Explicar qué quieren decir los símbolos que se crean en el objeto**  

Simbolos, U y T. (comando: nm nombrearchivo.o)  

Si utilizo el comando man nm me dice para que sirve y que significan los simbolos.  

U Simbolo sin definir
T Seccion texto


