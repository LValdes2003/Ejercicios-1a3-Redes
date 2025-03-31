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

