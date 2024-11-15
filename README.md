# VHDL Project

Dit project bevat een implementatie van digitale ontwerpen en simulaties geschreven in **VHDL**. Het doel van dit project is om [kort projectdoel beschrijven, bv. een digitale klok, een ALU, etc.] te ontwikkelen en te testen.

## Inhoud

- `src/`: Bevat de VHDL-bronbestanden.
- `testbench/`: Bevat de testbench-bestanden voor simulatie.
- `docs/`: Optioneel, documentatie en diagrammen die het ontwerp ondersteunen.
- `build/`: Optioneel, gegenereerde bestanden en syntheseresultaten.

## Vereisten

Zorg ervoor dat de volgende tools zijn geïnstalleerd:

- **VHDL-compiler** (bijv. ModelSim, GHDL, Vivado)
- **Simulator** (optioneel geïntegreerd in de VHDL-compiler)
- Optioneel: FPGA-tools als het ontwerp wordt gesynthetiseerd (bijv. Quartus, Vivado)

### Installatie van GHDL

1. Download en installeer GHDL volgens de [officiële documentatie](https://ghdl.github.io/).
2. Controleer of GHDL correct is geïnstalleerd:
   ```bash
   ghdl --version
   ```

## Gebruik

### Simulatie

1. Compileer de VHDL-bronbestanden:
   ```bash
   ghdl -a src/<bestand1>.vhd src/<bestand2>.vhd
   ```
2. Compileer de testbench:
   ```bash
   ghdl -a testbench/<testbench_bestand>.vhd
   ```
3. Link het ontwerp:
   ```bash
   ghdl -e <top_entity>
   ```
4. Voer de simulatie uit:
   ```bash
   ghdl -r <top_entity> --vcd=output.vcd
   ```
5. Analyseer het `.vcd`-bestand met een waveform-viewer (bijv. GTKWave):
   ```bash
   gtkwave output.vcd
   ```

### Synthese

Als je het ontwerp wilt implementeren op een FPGA, exporteer dan de netlist en gebruik tools zoals Vivado of Quartus. Raadpleeg de specifieke documentatie voor je FPGA-tool.

## Projectstructuur

```
project/
├── src/
│   ├── module1.vhd
│   ├── module2.vhd
│   └── top.vhd
├── testbench/
│   ├── testbench_module1.vhd
│   └── testbench_top.vhd
├── docs/
│   └── diagram.png
└── build/
    └── output_files/
```

## Contributies

Contributies zijn welkom! Volg de richtlijnen in `CONTRIBUTING.md` (indien beschikbaar).

## Licentie

Dit project is gelicentieerd onder de [jouw licentie hier]. Zie `LICENSE` voor meer details.

---
