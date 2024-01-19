---
title: "Creando un Entorno Virtual en Python para un Desarrollo Aislado"
date: 2024-01-19
image: "/path/to/image.png"
type: "post"
tags:
  [
    "blog",
    "Python",
    "Software Development",
    "Virtual Environment",
    "Virtualenv",
    "Programming",
    "Web Development",
    "Technology",
    "Python Programming",
    "Dependency Management",
    "Programming Tutorials",
    "Environment Configuration",
    "Technological Solutions",
    "Isolated Development",
    "Pip",
    "Development Tools",
  ]
---

Bienvenido a Ctrl+Fix Tech, donde desentrañamos misterios tecnológicos y proporcionamos soluciones efectivas. En esta primera entrada, aprenderemos paso a paso cómo crear un entorno virtual en Python, una práctica esencial para mantener tus proyectos organizados y aislar las dependencias. ¡Vamos allá!

[Descubre cómo funciona un entorno virtual](/posts/entorno_virtual/)

### Paso 1: Instalar `virtualenv`

Primero, asegúrate de tener `virtualenv` instalado. Si aún no lo tienes, puedes hacerlo ejecutando el siguiente comando en tu terminal:

```bash
pip install virtualenv
```

### Paso 2: Crear un Entorno Virtual

1. Abre tu terminal y navega al directorio de tu proyecto:

```bash
cd ruta/a/tu/proyecto
```

2. Crea un entorno virtual con el siguiente comando:

```bash
virtualenv nombre_del_entorno
```

### Paso 3: Activar el Entorno Virtual

En sistemas basados en **`Unix (Linux/Mac)`**, activa el entorno virtual con:

```bash
source nombre_del_entorno/bin/activate
```

En **`Windows`**, usa:

```bash
nombre_del_entorno\Scripts\activate
```

Verás que el prompt de tu terminal cambia, indicando que estás dentro del entorno virtual.

### Paso 4: Instalar Dependencias

Dentro del entorno virtual, puedes instalar las bibliotecas y paquetes que necesites usando `pip` sin afectar tu sistema global. Por ejemplo:

```python
pip install nombre_del_paquete
```

### Paso 5: Desactivar el Entorno Virtual

Cuando hayas terminado de trabajar en tu proyecto, desactiva el entorno virtual con:

```bash
deactivate
```

### Conclusión

¡Felicidades! Ahora tienes un entorno virtual de Python configurado y listo para ser utilizado. Esta práctica te permitirá gestionar de manera eficiente las dependencias de tus proyectos y evitar conflictos entre versiones. En futuras entradas, exploraremos más trucos y consejos para potenciar tu desarrollo. ¡Hasta la próxima solución en Ctrl+Fix Tech!

### Ejemplo de ejecucion

```
PS C:\Users\CTRLFIX> cd .\Desktop\ # Cambia al directorio Desktop
PS C:\Users\CTRLFIX\Desktop> cd .\pruebasenv\ # Cambia al directorio pruebasenv dentro de Desktop
PS C:\Users\CTRLFIX\Desktop\pruebasenv> virtualenv testing # Crea un entorno virtual llamado 'testing'
PS C:\Users\CTRLFIX\Desktop\pruebasenv> .\testing\Scripts\activate # Activa el entorno virtual 'testing'
# nota como el promt cambia a tener el nombre de el entorno virtual (testing en este caso por que asi se nombro al momento de su creacion)
(testing) PS C:\Users\CTRLFIX\Desktop\pruebasenv> pip install paramiko # Instala la biblioteca 'paramiko' en el entorno virtual
Collecting paramiko
Using cached paramiko-3.4.0-py3-none-any.whl.metadata (4.4 kB)
Collecting bcrypt>=3.2 (from paramiko)
Using cached bcrypt-4.1.2-cp39-abi3-win_amd64.whl.metadata (9.8 kB)
Collecting cryptography>=3.3 (from paramiko)
Downloading cryptography-41.0.7-cp37-abi3-win_amd64.whl.metadata (5.3 kB)
Collecting pynacl>=1.5 (from paramiko)
Downloading PyNaCL-1.5.0-cp36-abi3-win_amd64.whl (212 kB)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 212.1/212.1 kB 323.0 kB/s eta 0:00:00
Collecting cffi>=1.12 (from cryptography>=3.3->paramiko)
Downloading cffi-1.16.0-cp310-cp310-win_amd64.whl.metadata (1.5 kB)
Collecting pycparser (from cffi>=1.12->cryptography>=3.3->paramiko)
Downloading pycparser-2.21-py2.py3-none-any.whl (118 kB)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 118.7/118.7 kB 45.7 kB/s eta 0:00:00
Using cached paramiko-3.4.0-py3-none-any.whl (225 kB)
Using cached bcrypt-4.1.2-cp39-abi3-win_amd64.whl (158 kB)
Downloading cryptography-41.0.7-cp37-abi3-win_amd64.whl (2.7 MB)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.7/2.7 MB 64.3 kB/s eta 0:00:00
Downloading cffi-1.16.0-cp310-cp310-win_amd64.whl (181 kB)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 181.6/181.6 kB 49.6 kB/s eta 0:00:00
Installing collected packages: pycparser, bcrypt, cffi, pynacl, cryptography, paramiko
Successfully installed bcrypt-4.1.2 cffi-1.16.0 cryptography-41.0.7 paramiko-3.4.0 pycparser-2.21
(testing) PS C:\Users\CTRLFIX\Desktop\pruebasenv> deactivate # Desactiva el entorno virtual 'testing'
# Aqui el promt vuelve a su estado normal y se sabe por que le nombre del entorno virtual desaparecio
PS C:\Users\CTRLFIX\Desktop\pruebasenv>
```
