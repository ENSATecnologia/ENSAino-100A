# ENSAino-100A

The **ENSAino-100A** is an open-source development board based on the **ATmega2561** microcontroller.
It includes:

- Isolated power supplies
- Digital input ports (Wiegand, magnetic sensors, push buttons)
- Analog ports (NTC and touchpad)
- Digital output ports (2x relays)
- Serial ports (RS-232 and isolated RS-485)
- 433 MHz RF module
- 10BASE-T Ethernet (ENC28J60)
- RTC (DS1307)
- 16x2 LCD display
- LEDs and expansion ports

This project is based on the excellent [MCUdude/MegaCore](https://github.com/MCUdude/MegaCore) project.

---

## Repository contents

The current repository mainly contains hardware design files for PCB fabrication and documentation:

- Schematic (`.sch`)
- PCB layout (`.pcb`)
- Interface and subsystem PDFs
- Bill of Materials (`.xlsx`)
- Gerber package (`.zip`)

---

## MegaCore setup

### 1) Install MegaCore using Arduino Boards Manager

This method requires **Arduino IDE 1.6.4 or newer**.

1. Open the Arduino IDE.
2. Go to **File > Preferences**.
3. Add the following URL in **Additional Boards Manager URLs**:

   ```text
   https://mcudude.github.io/MegaCore/package_MCUdude_MegaCore_index.json
   ```

4. Go to **Tools > Board > Boards Manager...**.
5. Wait for package indexes to finish downloading.
6. Find **MegaCore** and click **Install**.
7. Close the Boards Manager window after installation.

### 2) First-time board configuration

1. Wire your microcontroller according to the [pinout](#pinout).
2. In **Tools > Board**, select **MegaCore** and your target MCU.
3. Select your preferred clock frequency (**16 MHz** is common).
4. Select your programmer in **Tools > Programmer**.
5. Click **Burn Bootloader** to set fuses and bootloader.

### 3) Upload firmware

You can upload in two ways:

1. **Via USB-to-serial adapter**
   - Disconnect ISP programmer.
   - Connect USB-to-serial interface.
   - Select the correct serial port and click **Upload**.
   - If upload times out, check RX/TX wiring and auto-reset circuit.

2. **Via ISP programmer**
   - Keep programmer connected.
   - Hold `Shift` while clicking **Upload**.
   - This uploads directly with the programmer (bootloader is not used).

---

## Pinout

### ATmega2561 (64-pin)

There is no universal Arduino pinout standard for this chip family. MegaCore defines a practical mapping. The default LED pin is Arduino **D13 (PB5)**.

> On ENSAino-100A, this behavior maps to **LED LD5**, which blinks when reset/bootloader activity occurs.

<p align="center">
  <img src="https://i.imgur.com/sweRJs3.jpg" width="350" alt="ATmega2561 pinout from MegaCore" />
</p>

---

## Programmer notes

- Always ensure the selected MCU, clock, and programmer match your hardware setup.
- For time-critical applications, prefer a stable external oscillator.
- After changing fuse-related options, run **Burn Bootloader** again to apply settings.

---

## Credits

- [MCUdude/MegaCore](https://github.com/MCUdude/MegaCore)

<!-- ENSA-AUDIT-README:START -->

---

## 🔍 Visao Geral Tecnica

Projeto de hardware/documentacao com esquematico P-CAD, PCB, BOM, PDFs e pacote Gerber.

## 🛠 Status da Auditoria

- ✅ Artefatos de hardware analisados.
- ⚠️ Nenhuma alteracao aplicada, pois mudancas em PCB/BOM exigem ferramenta EDA e validacao fisica.
- 📦 O pacote Gerber usa nomes `PCU-IOT-100A`, diferentes do nome do projeto.

## ⚠️ Pontos de Atencao

- Conferir se BOM, PDF, PCB e Gerber representam exatamente a mesma revisao.
- Revisar metadados de fonte `3V3` herdados de simbolo antigo.
- Conferir componente de memoria com valor `24LC512` e referencia original `AT25FS010`.
- Adicionar documentacao de fabricacao com stackup, cobre, acabamento e tolerancias.

## 🚀 Proximos Passos

1. Regenerar Gerbers com nome/revisao `ENSAino-100A`.
2. Criar `MANUFACTURING.md` com checklist de fabricacao.
3. Adicionar firmware minimo de bring-up para validar placa.

<!-- ENSA-AUDIT-README:END -->
