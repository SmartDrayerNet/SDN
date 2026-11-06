# Hardware

All boards are designed in KiCad as one family. Shared blocks:

- **Power 12–24 V DC** — PTC fuse, reverse-polarity diode, TVS, LM2596 5 V buck, AMS1117 3.3 V, separate PTC-protected sensor supply, IN / 5V / 3V3 LEDs and test points
- **ESP32 DevKit (30-pin)** in sockets, with 15 + 15 breakout contacts (pin headers or 2.54 mm screw terminals) next to the sockets
- **RS485 / Modbus** — SP3485, SM712 protection, bias resistors, 120 Ω termination jumper
- **Opto-isolated digital inputs** — LTV-814 AC-input optocouplers, so both PNP and NPN 12–24 V sensors work (one jumper)
- **Analog inputs** — 0–10 V divider or 4–20 mA shunt (jumper), ADS1115 16-bit ADC
- A labelled section, icon and status LED for every input group

> Renders below are generated from the board files. The V2 boards have not been manufactured yet.

## SDN Sensor Hub V2 — 210 × 160 mm

![Hub](images/pcb_hub_v2_noesp.jpg)

3D preview in the manufacturer's viewer:

![Hub 3D](images/pcb_hub_v2_3d.jpg)

Order preview:

![Hub green](images/pcb_hub_v2_green.jpg)

## Elevator Node 3 and 5 — 176 × 120 mm

![Elevator 3](images/pcb_elevator3.jpg)
![Elevator 5](images/pcb_elevator5.jpg)

## Tower Node — 176 × 120 mm

![Tower](images/pcb_tower.jpg)

## Petkus Node — 176 × 168 mm

![Petkus](images/pcb_petkus.jpg)

## Flow Node — 176 × 168 mm

![Flow](images/pcb_flow.jpg)

## Tower Node 20 and Tower Node 20 JSN — 230 × 184 mm

![Tower 20](images/pcb_tower20.jpg)
![Tower 20 JSN](images/pcb_tower20jsn.jpg)

## Elevator RPM perfboard — working

![RPM board working](images/noria_rpm_working.jpg)

MT3608 boost 5 V → 12 V for the sensors, one PC817 per channel (2.2 kΩ LED resistor, 10 kΩ pull-up to 3.3 V).
Signal is 3.3 V without metal and 0 V with metal at the sensor. ▶ [Video](images/noria_rpm_demo.mp4)

## Prototypes

| | |
|---|---|
| ![Breadboard](images/proto_breadboard.jpg) | ![Node in box](images/proto_enclosure.jpg) |
| Breadboard stage | First node in an IP65 box |
| ![RPM board](images/proto_noria_board.jpg) | ![Panel](images/panel_hmi.jpg) |
| Elevator RPM perfboard | Pi 5 panel with the plant map |
