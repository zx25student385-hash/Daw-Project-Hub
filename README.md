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
   ## Historial del proyecto

Es preferible realizar varios commits pequeños y coherentes en lugar de un único commit con toda la página porque facilita la trazabilidad de los cambios, permite aislar y corregir errores rápidamente sin perder otro trabajo, simplifica las revisiones de código y permite que cada funcionalidad se registre de forma independiente y clara.

## Seguridad y archivos ignorados

1. **¿Por qué `.env.example` puede publicarse?**
   Porque sirve como plantilla para que otros desarrolladores sepan qué variables de entorno necesita el proyecto para funcionar, sin exponer valores reales ni credenciales secretas.

2. **¿Por qué `.env` debe ignorarse?**
   Porque almacena información confidencial del entorno local (como claves de API, contraseñas o tokens privados) que jamás deben estar visibles públicamente.

3. **¿Qué habría que hacer si una contraseña o un token reales se hubieran publicado en GitHub?**
   Se debe revocar e invalidar la clave o token expuesto inmediatamente en el servicio correspondiente, generar uno nuevo y dar por comprometido el dato anterior.

4. **¿Bastaría con eliminar el archivo en un commit posterior?**
   No, porque Git guarda la historia completa del repositorio. Aunque se borre el archivo en un commit nuevo, el dato sensible seguiría siendo accesible consultando el historial de commits anteriores.

   ## Conflicto resuelto

- **Causa del conflicto:** Se modificó la misma línea del párrafo dentro del `<header>` en `index.html` con textos distintos en las ramas `main` y `feature/nuevo-eslogan`.
- **Archivo afectado:** `index.html`.
- **Decisión tomada:** Se revisaron ambas versiones y se optó por unificar la redacción manteniendo el eslogan más claro e integrador.
- **Proceso de resolución:** Se eliminaron manualmente los marcadores de conflicto (`<<<<<<<`, `=======`, `>>>>>>>`), se guardó el archivo limpio, se añadió al staging mediante `git add` y se completó la fusión creando el commit correspondiente.


## Sincronización remota

1. **¿Qué función cumple la opción `-u` en `git push -u origin main`?**
   Establece la relación de rastreo (*upstream*) entre la rama local `main` y la rama remota `origin/main`, permitiendo usar posteriormente comandos simplificados como `git push` o `git pull` sin especificar el remoto ni la rama.

2. **¿Qué diferencia existe entre `git fetch` y `git pull`?**
   `git fetch` descarga las novedades e información del repositorio remoto sin modificar ni alterar el código del directorio de trabajo local, mientras que `git pull` descarga los cambios y los fusiona (*merge*) automáticamente en la rama local activa.

   ## Enlaces de entrega

- **Repositorio remoto en GitHub:** `https://zx25student385-hash.github.io/daw-project-hub/`
- **Página publicada en GitHub Pages:** `https://zx25student385-hash.github.io/daw-project-hub/`

## Forks y colaboración

1. **¿Qué es un fork en GitHub?**
   Es una copia completa e independiente de un repositorio de GitHub alojada directamente en tu propia cuenta de usuario.

2. **¿En qué se diferencia un fork de una rama?**
   Una rama se crea dentro del propio repositorio original para aislar cambios, mientras que un fork es un repositorio completamente independiente ubicado en otra cuenta de GitHub.

3. **¿En qué cuenta se almacena un fork?**
   Se almacena en la cuenta personal de GitHub del usuario que realiza la copia (fork).

4. **¿Cuándo resulta útil trabajar mediante un fork?**
   Resulta útil cuando deseas contribuir a proyectos de código abierto o repositorios de terceros sobre los cuales no tienes permisos directos de escritura.

5. **¿Qué relación existe entre el repositorio original y el fork?**
   El fork mantiene un vínculo de origen que le permite rastrear los cambios del repositorio original y proponerle mejoras a través de Pull Requests.

6. **¿Qué es el repositorio upstream?**
   Es el nombre convencional que se le da al remoto que apunta directamente al repositorio original del cual creaste el fork.

7. **¿Qué diferencia existe entre origin y upstream?**
   - `origin`: Apunta a tu copia del proyecto (tu fork) en GitHub.
   - `upstream`: Apunta al repositorio original del propietario o proyecto principal.

8. **¿Cómo se propone que un cambio del fork llegue al repositorio original?**
   Publicando los cambios en una rama de tu fork en GitHub y abriendo desde allí una **Pull Request** hacia la rama principal del repositorio original.

9. **¿Quién decide si se acepta la propuesta?**
   El propietario, mantenedor o administrador del repositorio original.

10. **¿Puede seguir evolucionando el repositorio original mientras existe el fork?**
    Sí. Para actualizar tu fork con los nuevos cambios que ocurran en el original, basta con sincronizar tu rama local desde el remoto `upstream` y subirlos a tu `origin`.