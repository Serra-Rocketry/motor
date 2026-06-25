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
| `Reuniões/` (docx + png) | ~0.01 MB | Notas de reunião | ✅ Batch 2: convertido para md |
| `Fotos HEIC` (testes de queima, estufa) | ~44 MB | Formato Apple, precisa converter | Batch 3: converter para jpg |
| `Testes Propelente/` (docx + fotos + xlsx) | ~8.8 MB | Documentação de propelentes | ✅ Batch 2: copiado para propellants/ |
| `Dados Testes Estático/Dados SDcard/Motor6535.txt` | 34 B | Conteúdo: "Não Conseguimos Obter Os Dados :(" | Ignorar |
| `Dados Testes Estático/Dados SDcard/MotorÓxidoDeFerroeMagnésio.txt` | 31 B | Conteúdo: "Não Conseguimos Pegar Dados :(" | Ignorar |
| `SR21000/Teste Hidrostático/Mídias/` (vídeos) | ~340 MB | Vídeos de teste hidrostático | Batch 3: converter selecionados |
| `Motor SR21000 Inicial/` docx (relatório, anotações, etc.) | ~5 MB | Duplicata do SR21000 | Já copiado via SR21000 |
| `Fotos e Informações/Mont1.avi` | ~5 MB | Vídeo de montagem | Batch 3 |
| `Desenhos Tecnicos/*.PNG` (renderings) | ~0.3 MB | Imagens de referência | Já copiado em imagens/ |
| `.sciprj` (SciLab projects) | ~0.7 MB | Projetos SciLab | Já copiado em scilab/ |

---

## Batch 2 — Documentação restante (24/06/2026)

### docx → md

| docx original | Destino |
|---|---|
| `SR21000/Teste Hidrostático/Descrição do Teste.docx` | `docs/motors/sr21000/hydrostatic_test_description.md` |
| `Motor SR21000 Inicial/Simulações/Case do motor/Tubo-Teste De Pressão Interna Tubo-1.docx` | `docs/motors/sr21000-initial/tube_pressure_simulation.md` |
| `Testes Propelente/Teste Granulometria.../Descrição Do Teste.docx` | `docs/propellants/granulometry_test_description.md` |
| `Reuniões/Reunião Dia 09_08_2024.docx` | `docs/meetings/2024-08-09.md` |
| `Reuniões/Reunião 06_02_2026 (Caio e Italo).docx` | `docs/meetings/2026-02-06.md` |
| `2026/Foguete 1000M/Documentação.docx` | `docs/rockets/1000m/documentation.md` |
| `2026/Foguete 500M/Documentação do motor de 500m.docx` | `docs/rockets/500m/documentation.md` |
| `2026/Eletrônica/Ignitor/Funcionamento.docx` | `docs/ignitor/funcionamento.md` |
| `Teste De Queima 09-06-2023/Propelentes.docx` | `docs/propellants/teste_queima_2023-06-09.md` |
| `2026/Ideias.docx` | `docs/ideas.md` |

### Arquivos copiados

| Arquivo | Destino |
|---|---|
| `SR21000/Teste Hidrostático/*.xlsx` | `docs/motors/sr21000/TESTE_HIDROSTATICO_SR21000_88bar.xlsx` |
| `SR21000/Bulkhead_Sensor_Pressão.pdf` | `docs/motors/sr21000/drawings/Bulkhead_Sensor_Pressao.pdf` |
| `Foguete 500M/Teste Hidrostático/*.xls` | `docs/rockets/500m/TESTE_HIDROSTATICO_500m_62bar.xls` |
| `Teste De Queima/Dados Propelentes.xlsx` | `docs/propellants/dados_propelentes.xlsx` |
| `Teste Reprodutibilidade/*.xlsx` | `docs/propellants/teste_reprodutibilidade.xlsx` |
| `Teste estufa/planilha_teste_estufa.xlsx` | `docs/propellants/planilha_teste_estufa.xlsx` |
| `Ignitor/*.pdf` (fluxogramas) | `docs/ignitor/` |
| `Ignitor/README.md` | `docs/ignitor/README.md` |
| `Reunião Dia 16-05-2025/*.png` | `docs/meetings/images/` |
| `Reunião Dia 16-05-2025/*.ric` | `docs/meetings/` |
| `SR21000/Teste Hidrostático/Mídias/` (fotos) | `docs/imagens/sr21000/hydrostatic/` |
| `Propelentes.jpeg` (foto) | `docs/propellants/photos/` |

### Novas pastas criadas

- `docs/propellants/` — documentação e dados de propelentes
- `docs/meetings/` — notas de reunião
- `docs/ignitor/` — documentação do ignitor (pertence ao thrust-stand)
- `docs/imagens/sr21000/hydrostatic/` — fotos do teste hidrostático

---

## Batch 3 — GIFs de testes de queima (25/06/2026)

### Vídeos convertidos para GIF (320px, 8fps)

10 vídeos do teste de queima 09/06/2023 convertidos para GIF. Vídeos originais (~2.1 GB) mantidos apenas no `drive/`.

| Vídeo original | GIF | Tamanho |
|---|---|---|
| `Propelente 1 - 65% Nitrato 35% Açúcar.MOV` | `prop_1_knsu_padrao.gif` | 25 MB |
| `Propelente 2 - 65% Nitrato 35% Açúcar.MOV` | `prop_2_knsu_coroa.gif` | 13 MB |
| `Propelente 3 - 70% Nitrato 30% Açúcar.MOV` | `prop_3_knsu_70_30.gif` | 13 MB |
| `Propelente 4 - 50% Nitrato 50% Açúcar.MOV` | `prop_4_50_50.gif` | 32 MB |
| `Propelente 5 - 65% Nitrato 35% Dextrose.MOV` | `prop_5_knd.gif` | 13 MB |
| `Dextrose part 2.MOV` | `prop_5b_dextrose_part2.gif` | 4,5 MB |
| `Propelente 7 - ...CuFe2O4.MOV` | `prop_7_cufe2o4.gif` | 9,8 MB |
| `Propelente 8 - ...CoFe2O4.MOV` | `prop_8_cofe2o4.gif` | 20 MB |
| `Propelente 9 - ...NiFe2O4.MOV` | `prop_9_nife2o4.gif` | 14 MB |
| `Propelente 10 - ...ZnFe2O4.MOV` | `prop_10_znfe2o4.gif` | 14 MB |

**Total GIFs:** 155 MB (vs ~2.1 GB originais)

### Documentação atualizada

- `docs/propellants/teste_queima_2023-06-09.md` — reescrito com tabela, GIFs embutidos e links para dados
- Issue #1 criada: esclarecer diferença do Propelente 2 ("jeito do coroa")

### Vídeos ignorados (mantidos no drive/)

| Grupo | Tamanho | Motivo |
|---|---|---|
| Teste De Queima 10-07-2023 (5 vídeos) | ~560 MB | Sem nomes, sem documentação |
| Teste estufa (~35 vídeos) | ~1.9 GB | Sem nomes descritivos |
| Reunião OpenMotor.mp4 | 145 MB | Gravação de reunião |

## Batch 4 — Finalização (25/06/2026)

### READMEs criados

| Arquivo | Descrição |
|---|---|
| `docs/motors/README.md` | Visão geral dos motores e estrutura por motor |
| `docs/rockets/README.md` | Visão geral dos foguetes |
| `docs/propellants/README.md` | Documentação de propelentes e testes |
| `docs/static-tests/README.md` | Dados de testes estáticos e formato dos dados |
| `docs/nozzle/README.md` | Projeto do nozzle de cimento |
| `docs/tools/README.md` | Ferramentas e gabaritos |

### Revisão geral

- Estrutura verificada: 208 arquivos em 65 diretórios
- 27 arquivos Markdown (docs + READMEs)
- 11 simulações OpenMotor (.ric)
- Todos os nomes de arquivos normalizados
- `.gitignore` funcionando (drive/ não versionado)

---

## Status Final

| Batch | Commit | Arquivos | Conteúdo | Data |
|---|---|---|---|---|
| 1 | `b455cda` | 152 | Estrutura + CAD + test data | 24/06/2026 |
| 2 | `6f28990` | 46 | docx→md + planilhas + fotos | 24/06/2026 |
| 3 | `5bce81e` | 12 | GIFs de testes de queima | 25/06/2026 |
| 4 | — | 7 | READMEs + revisão | 25/06/2026 |
| **Total** | | **217** | | |

### Itens restantes no drive/ (não versionados)

| Item | Tamanho | Ação futura |
|---|---|---|
| Teste De Queima 10-07-2023 (5 vídeos) | ~560 MB | Ignorar (sem documentação) |
| Teste estufa (~35 vídeos) | ~1.9 GB | Ignorar (sem nomes) |
| Reunião OpenMotor.mp4 | 145 MB | Ignorar |
| Eletrônica/ CAD | ~49 MB | Mover para thrust-stand |
| testeestatico/ STEP | ~0.1 MB | Mover para thrust-stand |

### Próximos passos (opcional)

- Converter fotos HEIC → JPG (batch futuro, se necessário)
- Adicionar dados dos testes de queima 10-07-2023 quando documentação estiver disponível
- Mover arquivos de Eletrônica para o repositório thrust-stand
