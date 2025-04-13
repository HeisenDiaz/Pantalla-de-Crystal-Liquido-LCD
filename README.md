# Pantalla-de-Crystal-Liquido-LCD

## 1. Liquid Crystal Display (LCD)

- Consiste en un en una capa de moléculas alineadas y con un cambio de voltaje se logra visualizar en pantalla

## 1.1 Pantallas dot-matrix

 - Se muestran caracteres establecidos y personalizados con el limite de puntos de nuestra matriz

<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/Liquid-Crystal-Display-16x2-1.png" width="20%">

### 1.1.1 Tipos de pantallas dot-matrix

- Tenemos distintos formatos 8x2, 16x2, 20x4
- Se numera de acuerdo a sus filas y sus columnas
- Cada caracter esta separado por cada matriz de pixeles o matriz de puntos
  
<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/D_NQ_NP_844791-MCO48762011723_012022-O.webp" width="20%">

<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/RC0802A1-BIW-2.png" width="20%">

## 1.2 Controlador de la Pantalla
 
 - Viene dotada con un tarjeta el cual es un microcontrolador que ya trae unas conexiones para limitar voltajes y asi evitar tener que hacer protecciones

## 1.3 Controlador Hitachi 44780

 - En este viene precargado con los caracteres mas usados como alfabeto, numero, signos

<img src="https://github.com/HeisenDiaz/Pantalla-de-Crystal-Liquido-LCD/blob/main/Screenshot%202025-04-12%20223020.png" width="20%">

## 1.4 Memoria de la LCD

 - Es la memoria ROM viene precargado caracteres y si se llega a borrar esta memoria ya no seria funcional
 - En la ROM podemos personalizar nuestros caracteres

## 1.5 Memoria de la LCD - Características físicas de la LCD HD44780

   - 14 pines
    
   - 16 pines si el display tiene Backlight
   
   - Compatible con niveles de tension TT2
   
   - Controlador maneja 3 tipos de señales

     - Alimentación

     - Control

     - Datos
       
   - Contiene bits de estados, para identificar si hay información pendiente, los bits cambian el funcionamiento de la pantalla

## 1.6 Señales de Alimentación

| PINES |            FUNCIÓN           |
|:-----:|:----------------------------:|
|   1   | Corresponde a la referencia  |
|   2   | positiva (normalmente +5Vdc) |
|   3   | Ajuste del Contraste         |

## 1.7 Señales de Control

| PINES |                                                       FUNCIÓN                                                      |
|:-----:|:------------------------------------------------------------------------------------------------------------------:|
|   4   | (RS) sirve para seleccionar; El registro de Datos (DR) - RS=1; Registro de Instrucciones (IR) - RS=0               |
|   5   | Permite leer (𝑅/𝑊ഥ = 1) o escribir (𝑅/𝑊ഥ = 0) en el modulo LCD datos como instrucciones                         |
|   6   | (E) Permite habilitar con E=1, o deshabilitar el Display (E=0), solo cuando esta habilitado nos  comunicar con el  |

## 1.7 Señales de Datos

|  PINES  |                      FUNCIÓN                     |
|:-------:|:------------------------------------------------:|
| 7 al 14 | Bus de datos bidireccional de 8 bits (DB7 - DB0) |

- El LCD también puede ser gobernado con un bus de datos de 4 bits
- Se recomienda usar resistencia externa para proteger
  
## 2.Memorias y registros de la LCD

## 2.1 DDRAM (Display Dara RAM)

- Su capacidad es de 80 Bits
- Cada caracter tiene asignado un espacio de memoria


