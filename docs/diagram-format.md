{
  "version": 1,
  "author": "Gemini",
  "editor": "wokwi",
  "parts": [
    { "type": "wokwi-esp32-devkit-v1", "id": "esp", "top": -9.5, "left": -110.1, "attrs": {} },
    { "type": "wokwi-led", "id": "led1", "top": -67.6, "left": 134, "attrs": { "color": "red" } },
    { "type": "wokwi-resistor", "id": "r1", "top": -4.75, "left": 105.1, "attrs": { "value": "220" } },
    { "type": "wokwi-piezo-buzzer", "id": "bz1", "top": 47.6, "left": 124.4, "attrs": {} },
    { "type": "wokwi-potentiometer", "id": "pot1", "top": 59.5, "left": -235.3, "attrs": {} }
  ],
  "connections": [
    [ "esp:TX0", "$serialMonitor:RX", "", [] ],
    [ "esp:RX0", "$serialMonitor:TX", "", [] ],
    [ "led1:A", "r1:1", "green", [ "h0" ] ],
    [ "r1:2", "esp:D12", "green", [ "v0" ] ],
    [ "led1:C", "esp:GND.2", "black", [ "h0", "v-67.2", "h-220.8", "v230.4" ] ],
    [ "bz1:1", "esp:GND.2", "black", [ "h-153.6", "v230.4" ] ],
    [ "bz1:2", "esp:D14", "green", [ "h-144", "v124.8" ] ],
    [ "pot1:GND", "esp:GND.1", "black", [ "h0" ] ],
    [ "pot1:VCC", "esp:3V3", "red", [ "h0" ] ],
    [ "pot1:SIG", "esp:D34", "green", [ "v0" ] ]
  ],
  "dependencies": {}
}
