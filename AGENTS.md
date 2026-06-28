# AGENTS.md — Motor

## Visão do Projeto

Repositório de documentação técnica da equipe Serra Rocketry para motores de foguetes: desenhos CAD, especificações, dados de testes estáticos e simulações OpenMotor. Contém apenas documentação — nenhum código executável.

## Fronteira de Responsabilidade

Este repositório é a **fonte de verdade para geometria e dados brutos de motores**.

**Este repo contém:**
- CAD (.SLDPRT, .SLDASM, .SLDDRW, .STL, .STEP)
- Dados brutos de teste estático (.txt do SD card)
- Simulações OpenMotor (.ric)
- Gráficos simples de validação (thrust/pressão x tempo)
- Imagens e GIFs de testes
- Documentação técnica dos motores (.md)

**Este repo NÃO contém (vai para analysis/flight-computer/etc):**
- Análises processadas de voo
- Biblioteca de motores (app web)
- Simulações de trajetória
- Computador de bordo
- Análises estatísticas avançadas

**Se o usuário pedir para adicionar dados de análise sofisticada**, guiar para o repositório [analysis](https://github.com/Serra-Rocketry/analysis).

**Referências:**
- [analysis](https://github.com/Serra-Rocketry/analysis) — app Flask de análise e biblioteca de motores
- [flight-computer](https://github.com/Serra-Rocketry/flight-computer) — computador de bordo
- [thrust-stand](https://github.com/Serra-Rocketry/thrust-stand) — sistema de aquisição de dados

## Estrutura do Repositório

```
docs/
├── static-tests/      # Dados brutos e gráficos de testes estáticos
├── motors/            # CAD e documentação por motor
│   ├── sr21000/       # Motor principal (final)
│   ├── sr1500/
│   ├── 300m/
│   ├── v1/
│   └── cardboard/
├── rockets/           # CAD dos foguetes (não apenas motores)
│   ├── 500m/
│   ├── 1000m/
│   └── commercial/
├── molds/             # Moldes (STEP)
├── nozzle/            # Nozzle de cimento + cálculos
├── tools/             # Ferramentas e gabaritos
└── training/          # Documentação de treinamento
```

## Convenções de Nomes de Arquivos

- **Sem acentos:** `ã→a`, `ç→c`, `é→e`, `ó→o`, `í→i`, `ú→u`
- **Sem espaços:** usar `_` como separador
- **Sem parênteses:** remover
- **Manter maiúsculas/minúsculas** originais
- Exemplo: `Restrição_motor.SLDPRT` → `Restricao_motor.SLDPRT`

## Organização por Motor

Cada motor tem subpastas conforme aplicável:

| Subpasta | Conteúdo |
|---|---|
| `cad/` | `.SLDPRT` (peças), `.SLDASM` (montagens) |
| `drawings/` | `.SLDDRW` (desenhos técnicos), `.pdf` |
| `openmotor/` | `.ric` (arquivos de simulação OpenMotor) |
| `stl/` | `.STL` para impressão 3D |
| `parasolid/` | `.x_t` (formato Parasolid para interop) |
| `gcode/` | `.gcode` para impressão 3D |
| `images/` | Fotos, renderings e gráficos do motor |

## Convenções de Imagens

- Imagens ficam em `docs/motors/{motor}/images/`
- Renderings SolidWorks: nome descritivo, ex: `render_sr21000.jpg`
- Capturas de tela: em subpasta `capturas/`
- **Tamanho máximo: 500 KB por imagem** (regra das Boas Práticas)
- Comprimir antes de commitar: `convert input.jpg -resize 1200x -quality 80 -strip output.jpg`
- Embed no markdown: `![Descrição](./images/render.jpg)`
- Layout em docs: HTML tables para imagens lado a lado (3 por linha, 300px width), imagens isoladas em 300px

## Dados de Teste Estático

- Dados brutos do SD card: `docs/static-tests/{motor}/data.txt`
- Gráficos: `docs/static-tests/{motor}/empuxo_pressao.jpg`
- Projetos SciLab: `docs/static-tests/scilab/`
- Os dados do thrust-stand (sistema de aquisição) ficam no repo [Serra-Rocketry/thrust-stand](https://github.com/Serra-Rocketry/thrust-stand)

## O que NÃO versionar

- Pasta `drive/` (backup local do Google Drive)
- Vídeos grandes (`.MOV`, `.MP4`, `.avi`) — usar Git LFS ou hosting externo
- Binários de terceiros (`.exe`)
- Arquivos regeneráveis do SolidWorks (`.CWR`, `.dmp`, `.err`, `.LOG`, `.MFC`)
- Ver `.gitignore` completo

## Workflow

1. **Branching:** feature branches a partir de main (`feature/nome`)
2. **Commits:** mensagens em português, descritivas
3. **Arquivos CAD:** SolidWorks 2024+ (compatível com versões anteriores)
4. **Simulações OpenMotor:** arquivos `.ric` versionados diretamente
5. **Documentação:** Markdown em português

## Referências

- [Boas Práticas — Serra Rocketry](https://github.com/Serra-Rocketry/best-practices)
- [Thrust Stand — Sistema de Aquisição](https://github.com/Serra-Rocketry/thrust-stand)
- [OpenMotor — Software de Simulação](https://github.com/reilleya/openMotor)
- [MIGRATION.md](./MIGRATION.md) — histórico de migração do Drive
