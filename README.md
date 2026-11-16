# rfid-vehicle-access

parking gate for a 3-spot lot. embedded systems class project, 2022.

- **entry**: pic16f877a reads an rfid card (mfrc522). valid card + free spot → servo opens the gate, 16x2 lcd shows the card id and spots left.
- **exit**: arduino + ultrasonic sensor. car closer than 7 cm → gate opens.
- **monitoring**: esp32 runs its own wifi access point and serves a small page showing which spots are free, read from 3 ir sensors.

## layout

```
RFID Acceso/        pic firmware (ccs c project)
Secuencia_Salida/   arduino exit sequence
dashboardhtml/      esp32 web server, page lives in SuperMon.h
M6_07-...pdf        slides
```

wifi credentials in `dashboardhtml.ino` are placeholders. set your own before flashing.
