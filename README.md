# DAW Project Hub

Pequeña página web para practicar un flujo profesional de trabajo con Git y GitHub.

## Entorno de desarrollo
- **Versión de Git:** [Anota aquí el resultado del comando git --version]
- **Sistema operativo:** Windows 11 
- **Editor de código:** Visual Studio Code



## Investigación sobre SSH

1. **¿Qué es SSH?**
   Es un protocolo de red seguro que permite autenticarse y comunicarse con un servidor remoto de forma totalmente cifrada.

2. **¿Qué diferencia existe entre una clave pública y una clave privada?**
   La clave pública cifra los datos y verifica la identidad en el servidor remoto, mientras que la clave privada descifra la información y autentica al usuario en su máquina local.

3. **¿Qué clave puede compartirse?**
   La clave pública se puede compartir libremente con servicios como GitHub.

4. **¿Qué clave no debe compartirse nunca?**
   La clave privada nunca debe compartirse, enviarse ni exponerse públicamente.

5. **¿Qué ventaja presenta SSH frente a introducir continuamente usuario y contraseña?**
   Permite realizar operaciones de lectura y escritura en los repositorios remotos de forma segura y automatizada sin tener que autenticarse manualmente en cada acción.

6. **¿Qué función cumple el archivo `known_hosts`?**
   Almacena las huellas digitales (fingerprints) de los servidores remotos conocidos para verificar su autenticidad y prevenir ataques de suplantación (Man-in-the-middle).

7. **¿Qué podría ocurrir si una clave privada se publica en GitHub?**
   Un atacante podría comprometer la identidad del usuario, acceder a repositorios privados, modificar código o suplantarle en cualquier servicio donde dicha clave esté configurada.


   Conexión SSH con GitHub: comprobada correctamente