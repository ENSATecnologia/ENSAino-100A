# ENSAino-100A

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
