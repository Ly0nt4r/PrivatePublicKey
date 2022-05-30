# Criptografía Asimétrica: "Claves Privada & Publica"

Saludos lectores.
Hoy os vengo a explicar el concepto de criptografía asimétrica, un metodo criptografico donde se utilizan un par de claves (una privada y una publica) para la encriptación en envios de mensajes.
Como siempre, me gusta explica todo con detalles y de forma abierta a todos los públicos, sin tantos "terminos tecnicos". 

## ¡Os presento a nuestros dos ayudantes de hoy!

Ella es **Alice** 
![pixlr-bg-result](https://user-images.githubusercontent.com/87484792/171002843-e1d962d1-4c7c-4ef9-b617-af07eff9a4d7.png)

Él es **Bob**
![pixlr-bg-result (1)](https://user-images.githubusercontent.com/87484792/171002990-cd7ce73a-ff1a-4cd0-b3aa-6b64c22f0752.png)

##

Alice tiene un secreto muy importante que quiere compartir con su amigo Bob, en ese mensaje, se va a filtrar información de alta importancia.

Alice es conciente que Bob sabe guardar un secreto, y se fia plenamente en que ese secreto solo lo leerá él. ¿Pero y que pasaría si alguien interceptara el mensaje?
Aqui es donde entra en juego la encriptación de mensajes, en este caso, la Criptografía asimétrica. 

Aplicaciones cotidianas que usamos en el dia a dia, tal como WhatsApp, utilizan un cifrado de extremo a extremo. Este cifrado utiliza este principio de criptografia.

##

## ¿Pero en que consiste este principio?

Imaginemos que tenemos dos llaves, una llave será como nuestro tesoro **(Clave Privada)**. No se la daremos a nadie porque en ella viene la formula secreta de como abrir los mensajes encriptados. *¡Casi tan valiosa como la formula de la coca-cola, vaya!*
Por otro lado, tenemos la llave la cual daremos a todas las personas que quieran interactuar con nosotros **(Clave Publica)**. Esta llave les servirá a las personas que quieran comunicarse con nosotros por como encriptar los mensajes. 

Los pasos son sencillos, una vez iniciemos un proceso de comunicación, otorgaremos al receptor la llave publica (A su vez, este receptor nos hará entrega de su clave publica). Cada vez que el usuario quiera enviarnos un mensaje, ese mensaje vendrá encriptado con nuestra clave publica y una vez recibamos el mensaje, podamos utilizar nuestra llave privada para desencriptarlo.

##

## Lo que se esconde detrás... Explicación.

¿Porque este cifrado es tan útil y tan seguro? La respuesta es algo extensa de explicar, sin embargo para simplificar, diremos que esta formula esta compuesta por una multiplicación de números primos, con un tamaño de digitos descomunal. Con los medios actuales, y sin la presencia de ordenadores cuanticos, descrifrar este conjunto de números primos mediante fuerza bruta sería una misión de unos cientos de años. ¿Una locura,verdad?

Si nuestra clave pública es el número **33** (para simplificar), todos aquellos que quieran enviarnos un mensaje, tendrán que encriptar sus mensajes con el número **33**, cuando llegue a nosotros, simplemente miramos el conjunto de números primos (en este caso **3x11**). ¡Fácil! 

*Con todos lo explicado hasta ahora, pondremos un ejemplo con nuestros ayudantes.*

#

Alicia se dispone a contar el secreto a Bob, para ello, previamente han intercambiado sus llaves publicas. Las claves públicas por "error", ha llegado a manos de Carlos. ¿Que quien es Carlos?... ¡Él es Carlos!

![pixlr-bg-result (2)](https://user-images.githubusercontent.com/87484792/171048802-7a9f8fd5-ba90-4d16-8448-3a225373739e.png)

Carlos quiere hacerse con el secreto que guarda Alice, cree que puede interesarle. 
Ahora Carlos sabe que si quiere hablar con Alice tendrá que usar la llave con el número **33**. Y que si quiere hablar con Bob tendrá que usar la llave con el número **77**.



![pixlr-bg-result](https://user-images.githubusercontent.com/87484792/171049227-e0f45c44-4ddb-4191-9cc1-1155f63ffd07.png)
Alice envia el mensaje con el número 77, tanto Carlos como Bob han conseguido ser receptores del mensaje.

 ![pixlr-bg-result (1)](https://user-images.githubusercontent.com/87484792/171049436-666d2103-9e47-4808-99d1-d8257878b386.png)
Bob tras recibir el mensaje, ha utilizado su llave privada **7x11** y ha conseguido desencriptar el mensaje, pues la multiplicación de esos dos números primos da como resultado el número con el que venia encriptado el mensaje.. el **77**. 


Por la parte de Carlos, él no ha conseguido ver el mensaje.. su clave privada contenia los números **5x3**, que dan como resultado 15. 
**15** no es el número que venia en el mensaje.. era el **77**, y por tanto Carlos.. no sabe que números necesita para llegar a una multiplicación exitosa.


Para este ejemplo ha sido muy fácil adivinar que números serian multiplicativos... pero y si en vez del 77,¿te diera un valor con 178.954.904 digitos?
¿Serias capaz entonces decirme que dos números primos necesito para llegar a ese valor?.. exacto, es hay donde reside la eficacia de esta criptografia.

---------------------------------------------------------------------------------------------------------------------------------------------------------

Este ha sido una explicación introductoria, si te gustaría ver este concepto aplicado al entorno real (por ejemplo, con SSH). No dudes en hacermelo saber. 
Un saludos y *¡Happy Hacking!*
