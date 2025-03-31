https://github.com/LValdes2003/Ejercicios-1a3-Redes/tree/main  
Leonardo Valdés Esparza

# Ejercicios-1a3-Redes

### 1. Para un sistema de comunicaciones con 17 niveles de señal, que funciona en banda base, calcular el máximo ancho de banda si el ruido es despreciable y la tasa de transmisión es de 10 Mbits/s. ¿Qué tipo de medio guiado se podría utilizar para el sistema?
- Throughput = 2𝐻 𝑙𝑜𝑔2 (𝑉) [bits/s], 𝑉 niveles discretos de la señal, ancho de banda finito H
- H = Throughput/2log2(V) = 10 x 10^6/2log2(17) = 1.223.252,711 = **1,223 MHz**
- Se puede usar un **par trenzado de categoría 3**, ya que el ancho de banda es de 16 MHz

### 2. ¿Cuál es la tasa de transmisión máxima en un canal óptico con fibra de ancho de banda de 1 THz y conversores optoeléctricos de 100 Gbaudios, si la relación SNR es de 15 dB y la modulación utilizada en los conversores es de 4 símbolos en cuadratura?
- 𝑇ℎ𝑟𝑜𝑢𝑔ℎ𝑝𝑢𝑡 = 𝐻 𝑙𝑜𝑔2 (1 + 𝑆𝑁𝑅) [bits/s] = 10^12 log2 (1 + 10^(15/10)) = 5.02780767 x 10^12 = **5.03 Tbps**
- Tasa de transmisión en función de modulación = 100 Gbaudios x num de bits por símbolo = 100 x 10^9 x 2 = 200 x 10^9 = **200 Gbps**

### 3. Si en el sistema anterior se introduce un conector de fibra con un 20% de pérdidas, responder a las siguientes cuestiones:  
a) ¿Se verá afectada la tasa de transmisión máxima?  
b) ¿Qué velocidad máxima se tendrá en la salida?
- a) Como reduce la potencia del señal, la SNR es afectada, y **sí afecta la tasa de transmisión.**
- b) SNR nuevo = SNR viejo x 0,8 , Tasa Transmisión nueva = 10^12 log2 (1 + 10^(15/10) x 0,8) = **4,72 Tbps**

### 4. Indicar el tipo de modulación que se está utilizando y los problemas que plantea en los casos b y c.
- **16-QAM**
- b) Puntos crecen en tamaño por ruido. Ruidos mas bajos pueden causar errores con símbolos de bits mayores.
- c) Puntos cambian de distancia al centro y posición en rotación por distorsión de amplitud y distorsión de fase.

### 5. Sabiendo que se transmiten dos señales de forma simultánea y que se aplican dos modulaciones diferentes:
a) Indicar qué dos modulaciones se están aplicando.
b) Recuperar la información de ambas señales.
- FSK (Modulación por desplazamiento de frecuencia) y PSK (Modulación por desplazamiento de fase)
- FSK = 011001011010100110 y PSK = 110011110000001100

### 6. Indicar las longitudes de onda que se transmiten en cada uno de los puntos marcados en el esquema.
![Figura 1](/Diagramas/Figura1.png)
- a) l1 + ruido
- b) l2 + ruido
- c) l1
- d) l2
- e) l3 
- f) l4
- g) l3 + ruido
- h) l4 + ruido

### 7. Se considera una pila de protocolos de 4 capas. La capa 4 envía un bloque de 1 Kbyte. La capa 3 añade cabeceras de 256 bits y cada paquete es de 512 bytes. La capa 2 añade cabeceras de 512 bits y el campo de datos de las tramas son de 128 bytes. La capa 1 añade a cada 30 bytes de datos, 32 bits de comienzo, un byte de parada, y 16 bits de CRC. Dibujar todo el proceso de encapsulamiento del sistema transmisor y calcular la eficiencia del sistema.
![Figura 2](/Diagramas/Figura2.png)
- Eficiencia = Datos útiles / Datos transmitidos = 1024/1386 = 0,74

### 8. Un sistema satélite divide la información de la capa 3 en bloques de 1904 bits, a los que añade una cabecera de 64 bits. Si cada trama tarda en transmitirse 20 ms y la latencia del satélite es de 85 ms, ¿cuánto tiempo tardará en realizar la transmisión de 5 Mbytes de información?
- 426.345 ms

### 9. Calcular el resultado de un paquete de datos “1111011101010101” en un sistema de enlace de datos con las siguientes especificaciones:
1. Secuencia de inicio de trama “010101010”.
2. Protección frente a errores H(7,4).
3. Tamaño máximo por trama de 4 bytes.
- 1111 0111 0101 0101 + H74 = 1111111 0001111 0100101 0100101 Dividir dos tramas + 010101010 = 0101 0101 0111 1111 0001 1110 1001 01(00) y 0101 0101 0010 0101 (0000 0000 0000 0000)

### 10. Un fabricante indica que su sistema integra un CRC-8 con el siguiente polinomiogenerador: 𝐺(𝑥) = 𝑥8 + 𝑥7 + 𝑥2 + 1. Plantear los pasos que se deben realizar para calcular la trama resultante, considerando que el CRC se aplica al final de la trama 2 del ejercicio anterior

### 11. ¿Cuántos errores pueden llegar a corregir la codificación H(15,11) y el CRC-32?
- H(15,11) puede corregir un error en un bloque de 11 bits
- CRC-32 no puede corregir errores, pero los puede detectar

### 12. Se recibe la trama “1111111101011010101011” y se conoce que el protocolo está constituido por una cabecera “11111111” y que los datos están codificados con H(14,10), ¿cuáles son los datos útiles que se han transmitido?
- 0101101011

### 13. ¿A qué protocolo de la capa de enlace de datos corresponde el siguiente esquema temporal?
- TCP

### 14. ¿Se puede aplicar el protocolo del ejercicio anterior en el siguiente escenario?
- No

### 15. Dibujar un diagrama de ventana deslizante con un receptor con buffer para tres tramas y un transmisor que dispone de 5 tramas desordenadas que llegan en el orden 0, 3, 2, 4, 1.

### 16. Un canal coaxial con FDM con una tasa de transmisión de 500 Mbits/s con una longitud media de trama de 1/𝜇 = 12584 bits y una tasa de llegada de trama 𝜆 = 20000 trama/s:
1. ¿Qué retardo tendrá?
2. Si lo comparten entre 256 usuarios ¿cuántas portadoras serán necesarias?
3. ¿Cuánto tiempo tardará un nodo en detectar una colisión?
- 1\. Retardo de Transmisión = Longitud de trama / Tasa transmisión = 2.5168 x 10^-5 = **25,2 µs**
- 2\. 256 portadas
- 3\. Tiempo de propagación = Longitud de canal / Velocidad de propagación (Diré que 0,7 x velocidad de luz) = No se sabe / 0,7 x c

### 17. Representar la trama “1111111101011010101011” con codificación Manchester y Manchester diferencial. Indicar las unidades y magnitudes en los ejes.
