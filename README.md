# Pantalla-de-Crystal-Liquido-LCD

## 1. Liquid Crystal Display (LCD)

- Consiste en un en una capa de moléculas alineadas y con un cambio de voltaje se logra visualizar en pantalla

### 1.1 Pantallas dot-matrix

 - Se muestran caracteres establecidos y personalizados con el limite de puntos de nuestra matriz

<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/Liquid-Crystal-Display-16x2-1.png" width="20%">

### 1.1.1 Tipos de pantallas dot-matrix

- Tenemos distintos formatos 8x2, 16x2, 20x4
- Se numera de acuerdo a sus filas y sus columnas
- Cada caracter esta separado por cada matriz de pixeles o matriz de puntos
  
<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/D_NQ_NP_844791-MCO48762011723_012022-O.webp" width="20%">

<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/RC0802A1-BIW-2.png" width="20%">

### 1.2 Controlador de la Pantalla
 
 - Viene dotada con un tarjeta el cual es un microcontrolador que ya trae unas conexiones para limitar voltajes y asi evitar tener que hacer protecciones

### 1.3 Controlador Hitachi 44780

 - En este viene precargado con los caracteres mas usados como alfabeto, numero, signos

<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/Screenshot%202025-04-12%20223020.png" width="20%">

### 1.4 Memoria de la LCD

 - Es la memoria ROM viene precargado caracteres y si se llega a borrar esta memoria ya no seria funcional
 - En la ROM podemos personalizar nuestros caracteres

### 1.5 Memoria de la LCD - Características físicas de la LCD HD44780

   - 14 pines
    
   - 16 pines si el display tiene Backlight
   
   - Compatible con niveles de tension TT2
   
   - Controlador maneja 3 tipos de señales

     - Alimentación

     - Control

     - Datos
       
   - Contiene bits de estados, para identificar si hay información pendiente, los bits cambian el funcionamiento de la pantalla

### 1.6 Señales de Alimentación

| PINES |            FUNCIÓN           |
|:-----:|:----------------------------:|
|   1   | Corresponde a la referencia  |
|   2   | positiva (normalmente +5Vdc) |
|   3   | Ajuste del Contraste         |

### 1.7 Señales de Control

| PINES |                                                       FUNCIÓN                                                      |
|:-----:|:------------------------------------------------------------------------------------------------------------------:|
|   4   | (RS) sirve para seleccionar; El registro de Datos (DR) - RS=1; Registro de Instrucciones (IR) - RS=0               |
|   5   | Permite leer (𝑅/𝑊ഥ = 1) o escribir (𝑅/𝑊ഥ = 0) en el modulo LCD datos como instrucciones                         |
|   6   | (E) Permite habilitar con E=1, o deshabilitar el Display (E=0), solo cuando esta habilitado nos  comunicar con el  |

### 1.7 Señales de Datos

|  PINES  |                      FUNCIÓN                     |
|:-------:|:------------------------------------------------:|
| 7 al 14 | Bus de datos bidireccional de 8 bits (DB7 - DB0) |

- El LCD también puede ser gobernado con un bus de datos de 4 bits
- Se recomienda usar resistencia externa para proteger
  
## 2.Memorias y registros de la LCD

### 2.1 DDRAM (Display Dara RAM)

- Su capacidad es de 80 Bits
- Cada caracter tiene asignado un espacio de memoria
  
<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/Screenshot%202025-04-12%20230639.png" width="30%">

### 2.2 CGRAM (Character Generator RAM)

- Es el área de memoria RAM interna del LCD donde elusuario puede definir sus propios caracteres o gráficos
- Es el area de memoria RAM 8*5 espacio de trabajo
  
### 2.3 CGROM (Character Generator ROM)

- Es el area de memoria donde esta precargado los caracteres como:
- Número
- Caracteres latinos
- griegos
- Caracteres japoneses “Kanji”

### 2.4 Registros internos

 - El HD44780 tiene dos registros internos de 8 bits, un registro de datos (DR) y un registro de instrucciones (IR), que se pueden leer 
   y escribir
 - Registro de instrucciones
 - Registro de datos
   
### 2.5 Busy Flag (BF)
 
 - Nos avisa si la pantalla esta haciendo una operación y no puede atender la siguiente instrucción

### 2.6 Address Counter (AC)

 - Nos sirve para el control de la DDRAM, nos permite desplazarnos entre posiciones en la pantalla


## 3. Inicialización de la pantalla LCD

### 3.1 Inicialización por reset interno

- Se le quita la alimentacion y el automaticamente se reinicia y enciende la pantalla, se debe esperar un tiempo entrre 0.1 ms < 10 ms

### 3.2 Inicialización por instrucciones

<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/Screenshot%202025-04-12%20232111.png" width="30%">

### 3.3 Set de instrucciones

 - Son instrucciones predeterminadas
 - Implementado en el Data Sheet y siempre vamos a trabajar directamente con los pines de la pantalla
   
<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/Screenshot%202025-04-12%20232553.png" width="30%">

## 4. Como usar la pantalla?

### 4.1 Como enviar instrucciones
 
 - Usar comandos necesarios para la pantalla
 - Diferenciar si se usara en 8 Bits o 4 Bits
 - El Enable debe estar activo un minimo de **10 segundos** parac poder usar la pantalla

### 4.2 Proceso Configuración inicial

 - Configurar modo de trabajo a 4 u 8 bits
 - Configurar numero de lineas y tipo de Fuente
   - Se repiten los bits mas significativos y se agregan los menos significativos
- Configurar dezplazamiento de caracteres
- Encendido del Display y configuración de cursor
- Limpiar Display (Buenas Practicas)
- Configuración posición Inicial

## 5. Caracteres de la pantalla LCD

## 5.1 Para imprimir caracteres
