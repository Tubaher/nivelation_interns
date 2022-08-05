# Abrir Jupyter Notebook desde una MV

1. Iniciar una sesión de screen
```
screen -S jupyter
```

2. Activar entorno de conda
```
conda activate
```

3. Ejecutar jupyter notebook en X puerto
```
jupyter-notebook -ip 0.0.0.0 --port 8888 --allow-root
```

4. Ingresar con la ip de la MV y el puerto en el explorador
```
http://xx.xxx.xxx.xx:8888
```