simple WiFi-based setup this probably best way for ESP-12E + ESP32-CAM
How it works

ESP-12E sends:

http://<ESP32-CAM-IP>/capture

ESP32-CAM responds by capturing an image.

PART 1 — ESP32-CAM CODE (Camera Server)

Use the standard camera example (modified slightly).

In Arduino IDE:
Board: AI Thinker ESP32-CAM
Include: esp_camera.h, WiFi.h
What you’ll see
ESP32-CAM prints its IP in Serial Monitor
ESP-12E sends request every 10 sec
ESP32-CAM captures image and returns it
Common issues
Wrong IP → won’t work
Weak power → ESP32-CAM crashes (needs solid 5V!)
GPIO0 LOW when uploading → required for flashing
