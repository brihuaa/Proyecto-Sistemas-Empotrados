# Proyecto-Sistemas-Empotrados

# Proyecto Final - Monitor de Movimiento con Wi-Fi

Este proyecto utiliza un microcontrolador (ESP32) junto con sensores de movimiento y un LED NeoPixel para detectar actividad y mostrar su estado a través de una página web en tiempo real.

## Descripción
- **Detección de movimiento**: Usa dos sensores conectados a los pines 4 y 5.
- **Indicador visual (LED NeoPixel)**: 
  - **Rojo**: Error de conexión Wi-Fi.
  - **Verde**: Conexión Wi-Fi exitosa.
  - **Azul**: Movimiento detectado en alguno de los sensores.
- **Servidor web**: Muestra el estado de los sensores en una página que se actualiza automáticamente cada 2 segundos.

## Componentes Requeridos
- Placa ESP32.
- 2 sensores de movimiento (ej.: PIR).
- LED NeoPixel (1 unidad).
- Conexiones eléctricas y protoboard.

## Configuración
1. **Conexiones**:
   - Sensor 1 ➔ Pin 4.
   - Sensor 2 ➔ Pin 5.
   - LED NeoPixel ➔ Pin 48.
2. **Wi-Fi**:
   - Modifica `ssid` y `password` en el código con los datos de tu red.
3. **Bibliotecas**:
   - Instala `WiFi.h` (incluida en ESP32) y `Adafruit_NeoPixel` (via Arduino Library Manager).

## Instalación
1. Carga el código `ProyectoFinal.ino` en la placa ESP32 usando Arduino IDE.
2. Asegúrate de que las bibliotecas estén correctamente instaladas.
3. Conecta los componentes según la configuración de pines.

## Uso
1. Enciende el dispositivo. El LED se pondrá verde al conectarse a Wi-Fi.
2. Accede a la URL mostrada en el Monitor Serie (ej.: `http://192.168.x.x`).
3. La página web mostrará:
   - "No hay movimiento detectado en: Sensor X" si hay movimiento.
   - "En todos hay movimiento" si no hay detección.

## Errores Conocidos
- La página web invierte el mensaje cuando hay movimiento (indica "No hay movimiento" en los sensores activos). Esto requiere ajustes en el código.

## Licencia
Libre para uso educativo y personal. Se requiere atribución si se redistribuye.

---

**Nota**: Para mayor claridad, verifica las conexiones de los sensores y asegúrate de que la red Wi-Fi tenga señal adecuada.****
