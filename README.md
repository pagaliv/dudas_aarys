# Dudas Aarys

## EJERCICIOS

### Demostración del Límite y cual es la formula de aloha con particiones porque no la he encontrado, en la diaopostiva 34 de AARYS_Servicios_Avan...ados_Red_Capa_Enlace.pdf esta Emax(p=1/(2N-1))= [1-1/(2N-1)]2(N-1) = 0.5e pero no estoy seguro de que sea esa


#### Concepto a analizar: 
Demostrar que el siguiente límite converge a $e^{-1}$:

$$\lim_{n \to \infty} \left(1 - \frac{1}{n}\right)^{n-1} = e^{-1}$$

---

#### Desarrollo de la demostración:

**Paso 1: Reescribir la expresión**

Comenzamos separando el exponente $(n-1)$ como $n \cdot \frac{n-1}{n} = n \cdot (1 - \frac{1}{n})$:

$$\left(1 - \frac{1}{n}\right)^{n-1} = \frac{\left(1 - \frac{1}{n}\right)^{n}}{\left(1 - \frac{1}{n}\right)}$$

---

**Paso 2: Aplicar logaritmo natural a ambos lados**

Para facilitar el análisis del límite, aplicamos $\ln$ a ambos lados:

$$\ln \left[\lim_{n \to \infty} \frac{\left(1 - \frac{1}{n}\right)^{n}}{\left(1 - \frac{1}{n}\right)}\right] = \ln(e^{-1}) = -1$$

Por propiedades del logaritmo:

$$\lim_{n \to \infty} \ln \left[\frac{\left(1 - \frac{1}{n}\right)^{n}}{\left(1 - \frac{1}{n}\right)}\right] = -1$$

---

**Paso 3: Simplificar el denominador**

**Nota sobre por qué podemos evaluar solo el denominador:**

El denominador $\left(1 - \frac{1}{n}\right)$ tiende a $1$ cuando $n \to \infty$, ya que $\frac{1}{n} \to 0$. 

**¿Por qué no podemos hacer lo mismo con el numerador?**

El numerador $\left(1 - \frac{1}{n}\right)^{n}$ es una **forma indeterminada** del tipo $1^{\infty}$. Aunque la base tiende a $1$, el exponente $n$ tiende a infinito, y estas dos tendencias "compiten" entre sí. Por eso necesitamos usar técnicas más sofisticadas (L'Hôpital) para evaluarlo.

En cambio, el denominador es simplemente $\left(1 - \frac{1}{n}\right)$ sin exponente creciente, por lo que su límite es directo: $1 - 0 = 1$.

Evaluando el límite en el denominador:

$$\lim_{n \to \infty} \left(1 - \frac{1}{n}\right) = 1$$

Por lo tanto:

$$\lim_{n \to \infty} \ln\left(1 - \frac{1}{n}\right)^{n} = -1$$

---

**Paso 4: Aplicar propiedades de logaritmos**

Usando la propiedad $\ln(a^b) = b \ln(a)$:

$$\lim_{n \to \infty} n \cdot \ln\left(1 - \frac{1}{n}\right) = -1$$

---

**Paso 5: Aplicar la Regla de L'Hôpital**

Este límite tiene la forma indeterminada $\infty \cdot 0$. Para resolverlo, reescribimos:

$$\lim_{n \to \infty} n \cdot \ln\left(1 - \frac{1}{n}\right) = \lim_{n \to \infty} \frac{\ln\left(1 - \frac{1}{n}\right)}{\frac{1}{n}}$$

Ahora tenemos la forma $\frac{0}{0}$, por lo que podemos aplicar L'Hôpital:

**Derivada del numerador:**
$$\frac{d}{dn}\left[\ln\left(1 - \frac{1}{n}\right)\right] = \frac{1}{1 - \frac{1}{n}} \cdot \frac{1}{n^2} = \frac{1}{n^2\left(1 - \frac{1}{n}\right)}$$

**Derivada del denominador:**
$$\frac{d}{dn}\left[\frac{1}{n}\right] = -\frac{1}{n^2}$$

**Aplicando L'Hôpital:**

$$\lim_{n \to \infty} \frac{\frac{1}{n^2\left(1 - \frac{1}{n}\right)}}{-\frac{1}{n^2}} = \lim_{n \to \infty} \frac{1}{n^2\left(1 - \frac{1}{n}\right)} \cdot \frac{n^2}{-1}$$

$$= \lim_{n \to \infty} \frac{-1}{1 - \frac{1}{n}} = \frac{-1}{1 - 0} = -1$$

---

**Paso 6: Revertir el logaritmo**

Hemos demostrado que:

$$\lim_{n \to \infty} \ln\left(1 - \frac{1}{n}\right)^{n} = -1$$

Aplicando la función exponencial a ambos lados:

$$\lim_{n \to \infty} \left(1 - \frac{1}{n}\right)^{n} = e^{-1}$$

Y dado que el denominador $\left(1 - \frac{1}{n}\right) \to 1$:

$$\lim_{n \to \infty} \left(1 - \frac{1}{n}\right)^{n-1} = \lim_{n \to \infty} \frac{\left(1 - \frac{1}{n}\right)^{n}}{\left(1 - \frac{1}{n}\right)} = \frac{e^{-1}}{1} = e^{-1}$$

**∴ Queda demostrado** ✓

---

## TEMA: Red - Capa de Enlace

### Primera Duda: Características de protocolo de acceso múltiple broadcast de R bps

#### Concepto a analizar: 
> **Será descentralizado**: no habrá un único nodo maestro encargado del control (no supeditar al fallo del nodo maestro). Sin sincronización.

#### Duda:
¿A qué se refiere exactamente con "descentralizado" y "sin sincronización" en este contexto?

#### Mi interpretación (por si no me acuerdo el día que pregunte):
Lo que entiendo es que el protocolo no dependerá de un nodo/dispositivo que se encargue de repartir el ancho de banda entre los nodos que quieren transmitir información.

**Interpretación adicional:**
- **Descentralizado**: Ningún nodo tiene autoridad especial; todos los nodos son iguales y toman decisiones de forma autónoma sobre cuándo transmitir.
- **Sin sincronización**: No requiere un reloj común ni coordinación temporal entre nodos. Cada nodo decide independientemente cuándo intentar transmitir.

#### Referencia:
> Diapositiva 12 de "AARYS_Servicios_Avan...ados_Red_Capa_Enlace.pdf"

---
### Duda:
¿Como funciona exactamente CDMA?

#### Mi interpretación (por si no me acuerdo el día que pregunte):
Lo que no entiendo es como los nodos receptores son capaz de diferenciar los nodos que envian si estan mezclados ya que varios pueden transmitir de froma simultanea.


#### Referencia:
> Diapositiva 28 de "AARYS_Servicios_Avan...ados_Red_Capa_Enlace.pdf"
---
### Duda:
¿En aloha sin particiones todas las tramas tienen también una longitud fija?

#### Referencia:
> Diapositiva 34 de "AARYS_Servicios_Avan...ados_Red_Capa_Enlace.pdf"

---
### Duda:
¿Hay que saberse todas las siglas e los protocolos  como CDMA , CSMA, CSMA/CD ...? POrque el profesor dijo que no habia que aprenderse de memoria las cosas pero no estoy seguro de si esto entra dentro de las cosas que no hay que saberse de memoria. 

---
### Duda:
¿Hay que saberse datos historiocos del estilo de Origenes de las tecnologias ? Espero que no

#### Referencia:
> Diapositiva 55 de "AARYS_Servicios_Avan...ados_Red_Capa_Enlace.pdf"
---
### Duda:
¿Hay que saberse las tecnologias de ethernet de la diapo 69?
#### Referencia:
> Diapositiva 69 de "AARYS_Servicios_Avan...ados_Red_Capa_Enlace.pdf"
---
### Duda:
¿Puede entrar codificación Manchester?, lo digo porque ya lo hemos dado en otras asignaturas pero debería refrescarlo.

#### Referencia:
> Diapositiva 70 de "AARYS_Servicios_Avan...ados_Red_Capa_Enlace.pdf"
---
### Duda:
¿Nos tenemos que saber todos los formatos de paquetes de por ejemplo OSPF (todos su varientes como hello o LSU), RIP y demás de memoria? Porque en el examen preguntaba el Ethernet que entiendo que es sencillo y que es basico, pero no se si se deben aprender de memoria todos y en tal caso cuales son los que nos debemos aprender de memoria basicos. 

#### Referencia:
> Diapositiva 70 de "AARYS_Servicios_Avan...ados_Red_Capa_Enlace.pdf"
---
## OSPF
### Distancia administrativa
- Debemos aprendernos que la distancia adminsitrativa de OSPF es 110, la de RIP 120 y la ruta estatica 1, si este es el caso nos debemos saber alguna más? 
---
## EXAMEN TEORICO 2024
### Duda:
En el examen se pregunta en profundidad Ethernet, en los apuntes se habla tambien de PPP y de WIFI pero no se estudian en profundidar como Ethernet, en el examen podría entrar tambén en la misma profundidad PPP y Wifi y en tal caso PPP en las diapositivas se desarolla pero wifi no lo he encontrado, así que donde esta el temario sobre wifi. 


