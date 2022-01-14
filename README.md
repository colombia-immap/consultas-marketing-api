# Consultas JSON para la API de mercadeo de Facebook
Scripts JSON de consultas configuradas para recolectar datos de la API de mercadeo de Facebook

## Requisitos
1. Python > 3.6
2. PySocialWatcher: https://github.com/joaopalotti/pySocialWatcher/
3. Configurar token e id de usuario en Facebook developers: shorturl.at/tGV03

## Ejecutar las consultas 
1. En un archivo python: 
    
    `/ejecutar_consulta.py`
    ```
    import csv
    import json

    from pysocialwatcher import watcherAPI

    if __name__ == '__main__':
      watcher = watcherAPI(api_version="12.0", sleep_time=8, outputname="nombre_archivo_salida.csv")
      watcher.load_credentials_file("cerdenciales.csv")
      df = watcher.run_data_collection("nombre_script_consulta", remove_tmp_files=True)
    ```
    
2. En consola: `python ejecutar_consulta.py`
