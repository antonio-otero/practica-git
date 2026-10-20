# practica-git

Repositorio de prácticas del módulo **MP0614 — Despregamento de Aplicacións Web** (2º DAW,
IES San Clemente).

Aquí se practica el flujo de trabajo que se usa para contribuir a un proyecto del que **no
eres propietario**: bifurcas el repositorio a tu cuenta, trabajas en tu copia y propones tus
cambios mediante una solicitud de incorporación entre repositorios distintos.

El contenido es lo de menos. Lo que se evalúa es el camino.

## Qué tienes que hacer

Añadir un fichero con tus datos dentro de `participantes/`, llamado como tu cuenta de GitHub.
Si tu cuenta es `anagh`, el fichero es `participantes/anagh.md`.

### 1. Bifurca este repositorio

Botón **Fork**, arriba a la derecha. Te deja una copia en tu cuenta sobre la que sí tienes
permisos de escritura.

### 2. Clónate tu copia

Ojo a la dirección: es la de **tu** cuenta, no la del original.

```
git clone git@github.com:TUUSUARIO/practica-git.git
cd practica-git
git remote -v
```

### 3. Crea una rama

```
git switch -c alta/TUUSUARIO
```

### 4. Añade tu fichero

Copia `participantes/_plantilla.md`, renómbralo con tu cuenta y rellénalo.

```
cp participantes/_plantilla.md participantes/TUUSUARIO.md
```

### 5. Confirma y sube la rama

```
git add participantes/TUUSUARIO.md
git commit -m "Añade a TUUSUARIO a la lista de participantes"
git push -u origin alta/TUUSUARIO
```

### 6. Abre la solicitud

Al terminar el `push`, GitHub devuelve un enlace para abrirla. Antes de crearla,
**comprueba la cabecera**: a la izquierda tiene que estar `antonio-otero/practica-git` como
destino, y a la derecha tu copia con tu rama. Es el error más común: dejarla apuntando a tu
propio repositorio, con lo que la solicitud no le llega a nadie.

En la descripción, una línea diciendo qué añades.

## Reglas del fichero

- Un fichero por persona, dentro de `participantes/`, con el nombre exacto de la cuenta.
- Nada de tocar los ficheros de otras personas ni el `README.md`.
- Nada de datos personales más allá de lo que pide la plantilla: ni teléfono, ni dirección,
  ni correo personal.

Un fichero por persona no es un capricho: si todos escribiéramos en la misma lista, cada
solicitud entraría en conflicto con la anterior y pasaríais más tiempo resolviendo conflictos
que aprendiendo a proponer cambios. Separar los ficheros es, precisamente, una de las formas
de evitar conflictos en un proyecto con mucha gente.

## Después de que te la integren

Si vas a seguir trabajando sobre tu copia, conviene añadir el original como segundo remoto
para poder traerte lo que vaya entrando:

```
git remote add upstream git@github.com:antonio-otero/practica-git.git
git fetch upstream
git switch main
git merge upstream/main
```

Por convenio, `origin` es siempre tu copia y `upstream` el proyecto original.

## Qué se corrige

| Se mira | Qué se espera |
| --- | --- |
| La bifurcación | Existe en tu cuenta y de ella sale la rama |
| La rama | Nombre descriptivo, no `main` |
| La confirmación | Mensaje en imperativo, que diga qué hace |
| La solicitud | Cruza de tu repositorio al original, con descripción |
| El fichero | En `participantes/`, con el nombre de tu cuenta y la plantilla completa |
