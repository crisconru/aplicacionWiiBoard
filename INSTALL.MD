# Instalación

Para poder trabajar con la WiiBoard se ha optado por usar una Raspberry Pi 3B (viene con Bluetooth incorporado).

## Parear CPU-WiiBoard

Para parear abrimos una terminal y hacemos

```bash
sudo bluetoothctl
# Se abre un prompt nuevo donde se introducen los comandos siguientes
agent on
default-agent
# Ahora le damos al boton sync donde estan las pilas de la WiiBoard
scan on
# Apuntamos la MAC -> XX:XX:XX:XX:XX:XX
# Nos emparejamos con la WiiBoard
pair <mac>
# Por último nos conectamos
connect <mac>
```

## Dependencias

En la terminal hacemos

```bash
sudo apt install libcwiid1 libcwiid-dev python-cwiid
```

Si todo sale bien, se abrá instalado todo para trabajar con el Python 2 del sistema.
