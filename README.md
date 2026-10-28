# TP2-ISI
Osca Nahuel Jose

Justificación del diseño UML

1. Abstraccion de autoria y Factory Method

Para representar a los autores de las respuestas, cree una clase abstracta llamada "Autor", de la cual heredan "Usuario" y "AgenteAI". Esto permite que una respuesta pueda ser realizada tanto por un usuario registrado como por un agente de inteligencia artificial, sin tener que crear una relacion diferente para cada caso.
La clase "Respuesta" se relaciona directamente con "Autor", por lo que no necesita saber que tipo de autor esta generando la respuesta. De esta forma, se utiliza el polimorfismo y se evita repetir código o depender de clases especificas.
Tambien incorpore una fábrica llamada "FabricaAutor", junto con "FabricaUsuario" y "FabricaAgenteAI". Cada fabrica se encarga de crear un tipo de autor diferente. Si en el futuro se necesita agregar otro tipo de autor, se puede hacer sin tener que modificar las clases que ya utilizan la abstracción "Autor".

2. Patron Strategy

Para la generacion de respuestas mediante inteligencia artificial, utilice el patron Strategy. Defini la interfaz "EstrategiaAI", que contiene el método "generarRespuesta()", y las clases "EstrategiaOpenAI", "EstrategiaGemin"` y "EstrategiaLocal", que implementan ese método de distintas maneras.
La clase "AgenteAI" tiene una referencia a "EstrategiaAI", que puede cambiar mediante el metodo "setEstrategia()". Esto permite elegir que estrategia utilizar sin tener que modificar la clase "AgenteAI" cada vez que se quiera cambiar de proveedor.
Se pueden agregar nuevos proveedores de inteligencia artificial o cambiar entre los existentes sin afectar el resto del sistema.

el diagrama UML esta en archivo .astah lo cual es nesesario abrirlo con ese programa, de todas formas le dejo fotos.
