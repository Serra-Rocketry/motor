# Migração do Drive para Git

## Origem

- **Fonte:** Google Drive, pasta "3-Propulsão"
- **Data da exportação:** 24/06/2026
- **Formato:** 3 arquivos ZIP (`3-Propulsão-20260624T230916Z-3-001.zip`, `-002`, `-003`)
- **Total:** ~5.4 GB, 390 arquivos
- **Backup local:** pasta `drive/` (não versionada, mantida como referência)

## Regras de Normalização

Nomes de arquivos e pastas foram normalizados para compatibilidade com Git:

- Acentos removidos: `ã→a`, `ç→c`, `é→e`, `ó→o`, `í→i`, `ú→u`
- Espaços → `_`
- Parênteses removidos
- Maiúsculas/minúsculas mantidas
- Exemplo: `Restrição_motor.SLDPRT` → `Restricao_motor.SLDPRT`

---

## Batch 1 — Estrutura e CAD (24/06/2026)

### Copiado

| Origem no Drive | Destino no Repo | Qtd |
|---|---|---|
| `Dados Testes Estático/Dados SDcard/MotorGabriel.txt` | `docs/static-tests/motor-gabriel/data.txt` | 1 |
| `Dados Testes Estático/Dados SDcard/MotorCaramelo.txt` | `docs/static-tests/motor-caramelo/data.txt` | 1 |
| `Dados Testes Estático/Gráficos/Motor I (69-31...).jpg` | `docs/static-tests/motor-i/graph.jpg` | 1 |
| `Dados Testes Estático/Gráficos/Motor Caramelo (65-35).jpg` | `docs/static-tests/motor-caramelo/graph.jpg` | 1 |
| `Dados Testes Estático/Gráficos/*.sciprj` | `docs/static-tests/scilab/` | 2 |
| `Motor SR1500/Componentes/` | `docs/motors/sr1500/cad/` | 8 |
| `Motor SR1500/Openmotor e Desenhos Técnicos/` | `docs/motors/sr1500/drawings/` | 3 |
| `Motor SR1500/Openmotor e Desenhos Técnicos/Motor SR1500.ric` | `docs/motors/sr1500/openmotor/` | 1 |
| `Motor SR1500/Componentes/GUIAALMA10MM.STL` | `docs/motors/sr1500/stl/` | 1 |
| `Motor SR1500/Componentes/CE3E3V2_GUIAALMA10MM.gcode` | `docs/motors/sr1500/gcode/` | 1 |
| `Motor SR1500/O_Ring .jpeg` | `docs/imagens/sr1500/o_ring.jpg` | 1 |
| `SR21000/` (top-level CAD) | `docs/motors/sr21000/cad/` | 21 |
| `SR21000/Desenhos Tecnicos/` | `docs/motors/sr21000/drawings/` | 6 |
| `SR21000/*.ric` | `docs/motors/sr21000/openmotor/` | 3 |
| `SR21000/Inibidor/MoldeInibidor.STL` + `Fotos/Nozzle.STL` | `docs/motors/sr21000/stl/` | 2 |
| `SR21000/*.x_t` | `docs/motors/sr21000/parasolid/` | 3 |
| `SR21000/Inibidor/CE3E3V2_MoldeInibidor.gcode` | `docs/motors/sr21000/gcode/` | 1 |
| `SR21000/Molde Prensagem/` | `docs/motors/sr21000/cad/` | 2 |
| `SR21000/Fotos e Informações/*.jpg` | `docs/imagens/sr21000/` | 2 |
| `SR21000/Fotos e Informações/captura*.png` | `docs/imagens/sr21000/capturas/` | 4 |
| `SR21000/Teste Hidrostático/Gráfico_*.png` | `docs/imagens/sr21000/` | 1 |
| `Motor SR21000 Inicial/` CAD | `docs/motors/sr21000-initial/cad/` | 4 |
| `Motor SR21000 Inicial/*.ric` | `docs/motors/sr21000-initial/openmotor/` | 2 |
| `Motor SR21000 Inicial/Fotos/` | `docs/imagens/sr21000-initial/` | 6 |
| `Dados e Testes Antigos/Motor 300M/` CAD | `docs/motors/300m/cad/` | 6 |
| `Dados e Testes Antigos/Motor 300M/*.STL` | `docs/motors/300m/stl/` | 2 |
| `Dados e Testes Antigos/Motor 300M/*.gcode` | `docs/motors/300m/gcode/` | 1 |
| `Dados e Testes Antigos/Motor V1.0/` CAD | `docs/motors/v1/cad/` | 4 |
| `Dados e Testes Antigos/Motor Papelão/` | `docs/motors/cardboard/` | 9 |
| `2026/Foguete 500M/` | `docs/rockets/500m/` | 10 |
| `2026/Foguete 1000M/` | `docs/rockets/1000m/` | 17 |
| `2025/Foguete Comercial/` | `docs/rockets/commercial/` | 3 |
| `2026/Molde/` | `docs/molds/` | 3 |
| `2025/Ideias/Molde Nozzle Cimento/` | `docs/nozzle/` | 9 |
| `2025/Ferramentas/` | `docs/tools/` | 6 |
| `2025/Código Nozzle/Calculo_Nozzle.ipynb` | `docs/nozzle/notebook/` | 1 |
| `2025/Código Nozzle/Passos a Seguir.png` | `docs/nozzle/` | 1 |

### docx → md (conversões)

| docx original | Destino |
|---|---|
| `Dimensões 1° motor.docx` | `docs/motors/v1/dimensoes.md` |
| `Tampa Motor.docx` | `docs/motors/v1/tampa_motor.md` |
| `Relatório SR21000.docx` | `docs/motors/sr21000/report.md` |
| `Anotações Caio.docx` | `docs/motors/sr21000/notes.md` |
| `Passos a Seguir Projeto SR 21000.docx` | `docs/motors/sr21000/next_steps.md` |
| `Materiais a ser utilizado.docx` | `docs/motors/sr21000-initial/materials.md` |
| `Pino_ParafusoSim-Análise estática 1-1.docx` | `docs/motors/sr21000/pin_analysis.md` |
| `Tubo-Teste De Pressão Interna Tubo-1.docx` | `docs/motors/sr21000/tube_pressure_test.md` |
| `Tubo-Análise estática 2-1.docx` | `docs/motors/sr21000/tube_analysis.md` |
| `Descrição Das Tarefas.docx` | `docs/training/task_description.md` |

### Ignorados (para processar depois)

| Item | Tamanho | Motivo | Próximo passo |
|---|---|---|---|
| `Eletrônica/` CAD | ~49 MB | Pertence ao thrust-stand | Mover para Serra-Rocketry/thrust-stand |
| `testeestatico/` STEP | ~0.1 MB | Bancada de teste, não motor | Vai para thrust-stand |
| Vídeos (.MOV/.MP4/.avi) | ~4.5 GB | Muito grandes para git | Batch 3: converter selecionados em GIFs |
| `.CWR` simulações | ~216 MB | Regeneráveis no SolidWorks | Ignorar permanentemente |
| `openMotor.exe` | 69 MB | Binário de terceiros | Ignorar (linkar download no README) |
| `.dmp`, `.err`, `.LOG`, `.MFC`, `.BMC`, `.BD2`, `.BDF`, `.PGF` | ~0.5 MB | Lixo de IDE/simulação | Ignorar permanentemente |
| `Reuniões/` (docx + png) | ~0.01 MB | Notas de reunião | Batch 4: converter para md |
| `Fotos HEIC` (testes de queima, estufa) | ~44 MB | Formato Apple, precisa converter | Batch 3: converter para jpg |
| `Testes Propelente/` (docx + fotos + xlsx) | ~8.8 MB | Documentação de propelentes | Reorganizar depois |
| `Dados Testes Estático/Dados SDcard/Motor6535.txt` | 34 B | Conteúdo: "Não Conseguimos Obter Os Dados :(" | Ignorar |
| `Dados Testes Estático/Dados SDcard/MotorÓxidoDeFerroeMagnésio.txt` | 31 B | Conteúdo: "Não Conseguimos Pegar Dados :(" | Ignorar |
| `SR21000/Teste Hidrostático/Mídias/` (vídeos) | ~340 MB | Vídeos de teste hidrostático | Batch 3: converter selecionados |
| `Motor SR21000 Inicial/` docx (relatório, anotações, etc.) | ~5 MB | Duplicata do SR21000 | Já copiado via SR21000 |
| `Fotos e Informações/Mont1.avi` | ~5 MB | Vídeo de montagem | Batch 3 |
| `Desenhos Tecnicos/*.PNG` (renderings) | ~0.3 MB | Imagens de referência | Já copiado em imagens/ |
| `.sciprj` (SciLab projects) | ~0.7 MB | Projetos SciLab | Já copiado em scilab/ |

---

## Próximos Batches (planejados)

| Batch | Conteúdo | Status |
|---|---|---|
| 2 | docx restantes (reuniões, propelentes, treinamento) | Pendente |
| 3 | Mídia (GIFs de testes, fotos HEIC→jpg, vídeos selecionados) | Pendente |
| 4 | Finalização (READMEs por subdiretório, revisão geral) | Pendente |
