https://github.com/LValdes2003/Ejercicios-1a3-Redes/tree/main  
Leonardo Valdés Esparza

# Ejercicios-1a3-Redes

## Introducción a las Redes de Ordenadores
### 1. Diferencias entre el modelo OSI y el modelo TCP/IP
| OSI | TCP/IP |
| ---  |  --- |
| 7 capas | 4 capas |
| Centrado en conexiones (TCP) | No centrado en conexiones (TCP o UDP) |
| Modelo no práctico | Modelo práctico |
| Ruteo de paquetes en capa Red | Ruteo de paquetes en capa Internet |
| Se pueden definir protocolos en cada capa | Enfocado en protocolos estandarizados |

### 2. Uso de cada de Transporte
| OSI | TCP/IP |
| ---  |  --- |
| Mandar datos (TCP) | Mandar datos (TCP o UDP) |

### 3. Diferencia entre TCP y UDP
| TCP | UDP |
| ---  |  --- |
| Verificación de entrega de paquetes | Ninguna verificación |
| Mas lento | Mas rápido |
| Usos: bajar archivos, correos, etc. | Usos: transmisión de video, videojuegos online, etc. |

### 4. ¿Qué protocolo de la capa de aplicación se utiliza para la transferencia de archivos?
FTP = File Transfer Protocol
Alternativas: SFTP = Secure FTP (Transmisión segura), TFTP = Trivial FTP (Versión simple sin autentificación) 

### 5. Describe el proceso de resolución de nombres en DNS.
1. El cliente busca la página en el navegador
2. Se busca el IP que corresponde en el cache DNS de la máquina, si no se encuentra:
3. El servidor DNS en la red intenta encontrar que IP corresponde con el nombre: si no se encuentra:
4. Busca en servidores raíz, que dan la dirección de los servidores que saben donde está la página
5. El navegador va a a la página
Ejemplo: Quiero ir a google.com. No sé donde está. Pregunto al servidor en mi red. No sabe. Pregunta a un servidor raíz. Nos dirige al servidor que tiene direcciones de páginas .com. El servidor nos dice donde está google. Navegamos a la página.

## Capa Física
### 1. Tasa de transmición máxima
a) A hacer las calculaciones, me han salido diferentes los números que en la solución dada. Convirtiendo 15dB a SNR lineal, me sale ~31.62, y usando la fórmula de Shannon me sale:
- 5,028 * 10^9 para Coaxial (5,028 Gbps)
- 3,017 * 10^9 para Par Trenzado (3,017 Gbps) 
- 5,028 * 10^11 para Fibra Óptica (502,8 Gbps)

b)  
<img src="https://github.com/user-attachments/assets/0c65a177-aafc-4817-b19c-3e39d752a136" alt="Tasa Transmision Grafica" width="400" height="250">  
A incrementar el SNR (10 a 15 dB) Se aumenta la tasa de transmisión máxima. La fibra óptica es la mejor opción, ya que el ancho de banda es mayor.
