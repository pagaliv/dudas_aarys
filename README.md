#  Dudas Aarys

## EJERCICIOS

### Demostración del Límite

#### Concepto a analizar: 
Demostrar que el siguiente límite converge a $e^{-1}$:

$$\lim_{n \to \infty} \left(1 - \frac{1}{n}\right)^{n-1} = e^{-1}$$

#### Duda: 
¿Cómo se demuestrael limite con aloha con particiones, no he encontrado la igualdad que hay que hacer ?

#### Lo que tengo apuntado:
(copilot, borra esto y ponlo en bonito)
#### Paso 1, pasar abajo, lo entiendo
(1-1/N)^(N-1)= ((1-1/N)^N)/((1-1/N) 
#### Paso 2 añadir un ln en ambos lados
 ln Lim(((1-1/N)^N)/((1-1/N)) = ln (e^{-1})
 #### Paso 3 aplicar el limite en la part de abajo, duda en esta parte, porque no se puede repetir este proceso n veces y eliminar la n? me refiero, ¿si se puede hacer una vez porque nose puede hacer n veces?
 en el limite 1-(1/N)= 1 porque 1/N=0 lo que lleva a 
 ln Lim(((1-1/N)^N) = ln (e^{-1})
 #### Paso 4 aplicando la logica de los logaritmos
 ln Lim(((1-1/N)^N) = ln (e^{-1})
   Lim(n*ln(1-1/N) = ln (e^{-1})
 #### Paso 5, se aplica lopial
 desarolla aqui lopial sobre la formula y ve explicando

 quedando -(1)/(1-1/N) = -1
 #### Paso 6, revertir cambios
 ln Lim(((1-1/N)^N)/((1-1/N)) = -1 
 esta parte todo el ratoes con el limite pero se me pasa ponerlo
 (((1-(1/N))^N)/(1-(1/N) = ((1 - (1/N))^N = (1 + (1/-N)^-N = (((1+1/(-N))^N)^-1= e⁻¹ 
---

##  TEMA: Red - Capa de Enlace

###  Primera Duda: Características de protocolo de acceso múltiple broadcast de R bps

####  Concepto a analizar: 
> **Será descentralizado**:  no habrá un único nodo maestro encargado del control (no supeditar al fallo del nodo maestro). Sin sincronización.

####  Duda:
¿A qué se refiere exactamente con "descentralizado" y "sin sincronización" en este contexto?

#### Mi interpretación (por si no me acuerdo el día que pregunte)
Lo que entiendo es que el protocolo no dependerá de un nodo/dispositivo que se encargue de repartir el ancho de banda entre los nodos que quieren transmitir información. 

#### Referencia
> Diapositiva 12 de "AARYS_Servicios_Avan...ados_Red_Capa_Enlace.pdf" .
---
