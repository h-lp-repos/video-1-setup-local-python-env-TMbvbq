# Video 1: Preparar el Entorno Local de Python

## Objetivo
Crear un entorno de Python reproducible e instalar exactamente las dependencias utilizadas en el laboratorio
(Sentence-Transformers, faiss-cpu, psutil, numpy).

## Pasos

1. Abrí una terminal en este directorio y verificá los archivos:
   ```bash
   ls
   ```

2. Creá y activá un entorno virtual:

   * **venv** (Linux/macOS/Windows PowerShell):

     ```bash
     python3 -m venv .venv
     source .venv/bin/activate    # Unix/macOS
     .\.venv\Scripts\activate    # Windows PowerShell
     ```
   * **conda**:

     ```bash
     conda create -n lesson4 python=3.8
     conda activate lesson4
     ```
3. Instalá las dependencias:

   ```bash
   pip install -r requirements.txt
   ```
4. Verificá las importaciones:

   ```bash
   python run_local_embeddings.py
   ```

   Deberías ver el mensaje `Environment OK`.

## Solución de problemas

* **Errores al construir wheels**: instalá el wheel precompilado de `faiss-cpu` o usá
  `conda install -c conda-forge faiss-cpu`.
* **Versión incorrecta de Python**: asegurate de estar usando Python 3.8 o superior.
