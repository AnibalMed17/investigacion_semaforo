___
## <center> Compositores: </center>
**<center>Neifi Anibal Medina Hernandez 2021-0959</center>**

**<center>Carlos Alberto Reynoso Cruz 2021-1188</center>**

**<center>Eddy Leonardo Mena Reyes  2021-0942</center>**
___

## Investigación: Problema de la concurrencia: semáforos.
- > 1. Concepto básico de semáforo en los sistemas operativos
- > 2. ¿En qué consisten los semáforos binarios y enteros?
- > 3. Relacion entre los semáforos y la sincronización
___

### 1. Concepto basico de semaforo en los sistemas operativos
En sistemas operativos, un semáforo es una herramienta de sincronización que se utiliza para administrar el acceso a recursos compartidos, como variables o archivos, entre diferentes procesos o hilos. Los semáforos actúan como banderas que indican el estado de un recurso compartido, permitiendo que los procesos o hilos accedan a él en un orden específico y evitando la competencia por los recursos.

Los semáforos pueden ser binarios o contadores. Los semáforos binarios tienen dos estados: ocupado o libre. Los semáforos contadores tienen un valor entero que se incrementa o decrementa según el acceso a un recurso compartido.

Cuando un proceso o hilo necesita acceder a un recurso compartido, primero comprueba el estado del semáforo. Si el semáforo está en un estado libre, el proceso o hilo lo establece en ocupado y accede al recurso. Si el semáforo ya está ocupado, el proceso o hilo se bloquea y espera hasta que el semáforo se libere.

Los semáforos se utilizan comúnmente en sistemas operativos para evitar problemas de concurrencia, como las condiciones de carrera, donde dos o más procesos o hilos intentan acceder al mismo recurso al mismo tiempo y producen resultados impredecibles. Con el uso adecuado de semáforos, los procesos y los hilos pueden compartir recursos de manera segura y eficiente.

##### _1.1 El problema de la concurrencia de los semáforos en los sistemas_

En los sistemas operativos, los semáforos son una herramienta esencial para la sincronización y la exclusión mutua de recursos compartidos entre procesos o hilos. Sin embargo, también pueden surgir problemas de concurrencia cuando se utilizan incorrectamente.

##### _1.2 ¿Qué es el problema de la concurrencia?_

El problema de la concurrencia se refiere a la situación en la que varios procesos o hilos intentan acceder a un recurso compartido al mismo tiempo y compiten por el acceso al mismo. Si no se maneja correctamente, esto puede dar lugar a errores y condiciones de carrera.

Por ejemplo, si dos procesos intentan escribir en un archivo al mismo tiempo, podrían producirse errores de escritura y la información del archivo podría corromperse. O si varios hilos intentan acceder a una variable compartida sin sincronización adecuada, podrían ocurrir inconsistencias y errores en los datos.
___

### 2. ¿En qué consisten los semáforos binarios y enteros?

Los semáforos binarios son aquellos que sólo tienen dos valores posibles: 0 y 1. Un semáforo binario se utiliza para asegurar la exclusión mutua entre procesos o hilos que compiten por un recurso compartido. Por lo tanto, un semáforo binario puede estar en dos estados posibles: ocupado (1) o libre (0). Cuando un proceso o hilo quiere acceder a un recurso compartido, primero comprueba el estado del semáforo. Si está libre (0), establece el semáforo en ocupado (1) y accede al recurso. Si el semáforo ya está ocupado (1), el proceso o hilo se bloquea hasta que el semáforo se libere.

Los semáforos enteros, por otro lado, tienen un valor numérico entero. Los semáforos enteros se utilizan para controlar el acceso a múltiples instancias de un recurso compartido, como un conjunto de recursos o una cola. Un semáforo entero se inicializa con un valor que representa el número de recursos disponibles. Cuando un proceso o hilo necesita acceder a uno de los recursos, primero comprueba el valor del semáforo. Si el valor es mayor que cero, disminuye el valor del semáforo en una unidad y accede al recurso. Si el valor del semáforo es cero, el proceso o hilo se bloquea y espera hasta que uno de los recursos se libere.

En resumen, los semáforos binarios se utilizan para controlar el acceso a un recurso compartido único, mientras que los semáforos enteros se utilizan para controlar el acceso a múltiples instancias de un recurso compartido. Ambos tipos de semáforos son esenciales para garantizar la sincronización y la exclusión mutua entre procesos o hilos en sistemas operativos.
___

### 3. Relacion entre los semáforos y la sincronización

Los semáforos son una herramienta fundamental para la sincronización en sistemas operativos. La sincronización se refiere al proceso de coordinación entre procesos o hilos que acceden a recursos compartidos. La falta de sincronización puede dar lugar a problemas como las condiciones de carrera, la inanición o el bloqueo.

Los semáforos permiten a los procesos o hilos coordinar el acceso a los recursos compartidos mediante el uso de banderas que indican el estado de los recursos. Los semáforos se utilizan para evitar que dos o más procesos o hilos intenten acceder al mismo recurso al mismo tiempo y produzcan resultados impredecibles.

Por ejemplo, imagine dos procesos que comparten una impresora. Si ambos procesos intentan imprimir al mismo tiempo, pueden producirse errores de impresión o el documento podría imprimirse incorrectamente. Si utilizamos un semáforo para controlar el acceso a la impresora, cada proceso espera a que el semáforo esté libre antes de intentar imprimir. Si el semáforo está ocupado, el proceso se bloquea hasta que el semáforo se libere, asegurando que sólo un proceso acceda a la impresora a la vez.

Además, los semáforos también se utilizan para sincronizar la ejecución de diferentes procesos o hilos. Por ejemplo, si un proceso depende de los resultados de otro proceso, el primer proceso debe esperar a que el segundo proceso termine antes de continuar. Los semáforos se utilizan para coordinar la finalización de los procesos y asegurar que se ejecuten en el orden correcto.
