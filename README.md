# ENSAino-100A

## 🇧🇷 PT-BR

### Visão Geral

O **ENSAino-100A** reúne os arquivos de hardware da placa ENSAino 100A, incluindo esquemático, PCB, BOM, documentação de fabricação e arquivos Gerber.

O objetivo do repositório é manter a base técnica da placa organizada para fabricação, revisão elétrica e manutenção do hardware.

### Funcionalidades

- Documentação de esquemático e layout de PCB.
- Arquivos Gerber para fabricação.
- Lista de materiais e documentação de apoio.
- Referência para montagem, revisão e rastreabilidade da placa.

### Estrutura

- `ENSAino100APCB/`: arquivos de projeto eletrônico, fabricação e documentação.
- `LICENSE`: licença do repositório.

### Validação

1. Revise o esquemático antes de solicitar fabricação.
2. Confira a BOM contra os componentes disponíveis.
3. Valide os arquivos Gerber no visualizador da fabricante.
4. Registre versão de placa e lote de fabricação.

### Pontos de Atenção

- Conferir nomes e versões dos arquivos de fabricação antes de enviar para produção.
- Manter histórico de revisão da placa junto à documentação.
- Criar firmware de bring-up quando uma nova revisão de hardware for fabricada.

### Licença

Consulte o arquivo `LICENSE` deste repositório.

---

## 🇺🇸 English

### Overview

**ENSAino-100A** contains the hardware files for the ENSAino 100A board, including schematic, PCB, BOM, manufacturing documentation, and Gerber files.

The repository keeps the board technical base organized for manufacturing, electrical review, and hardware maintenance.

### Features

- Schematic and PCB layout documentation.
- Gerber files for manufacturing.
- Bill of materials and support documentation.
- Reference material for assembly, review, and board traceability.

### Structure

- `ENSAino100APCB/`: electronic project, manufacturing, and documentation files.
- `LICENSE`: repository license.

### Validation

1. Review the schematic before requesting manufacturing.
2. Check the BOM against available components.
3. Validate Gerber files with the manufacturer viewer.
4. Record board revision and manufacturing batch.

### Notes

- Check manufacturing file names and versions before production.
- Keep board revision history with the documentation.
- Create bring-up firmware when a new hardware revision is manufactured.

### License

See the `LICENSE` file in this repository.

### Auditoria / Audit
#### PT-BR
- O maior ganho ainda vem de reduzir String e alocacao dinamica nos caminhos mais frequentes.
- Vale centralizar contrato de protocolo, limites de buffer e configuracao persistida.
- Revisar estados paralelos e variantes legadas para evitar manutencao duplicada.
- Prioridade pratica: manter o caminho critico simples, previsivel e com menos heap.
#### EN
- The biggest remaining win is to reduce String and dynamic allocation in the hottest paths.
- Keep the protocol contract, buffer limits and persisted configuration centralized.
- Review parallel states and legacy variants to avoid duplicate maintenance.
- Practical priority: keep the critical path simple, predictable and with less heap pressure.

