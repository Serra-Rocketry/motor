# Motor — Serra Rocketry

Desenhos CAD, especificações e dados de testes estáticos de motores de foguetes.

## Sobre

Este repositório contém a documentação técnica dos motores desenvolvidos pela equipe Serra Rocketry (IPRJ/UERJ). Aqui ficam os desenhos de peça, montagens, simulações OpenMotor e dados brutos de testes estáticos.

> **Nota:** O sistema de aquisição de dados (firmware, hardware, calibração) fica no repositório [thrust-stand](https://github.com/Serra-Rocketry/thrust-stand). Este repo armazena apenas os dados coletados e a documentação dos motores.

## Fronteira de Responsabilidade

Este repositório (`motor`) contém a **documentação da propulsão** e é a **fonte de verdade para geometria e dados brutos de motores**.

**Este repo contém:**
- Geometria do motor (CAD: .SLDPRT, .SLDASM, .SLDDRW, .STL, .STEP)
- Dados brutos de teste estático (.txt do SD card)
- Simulações OpenMotor (.ric)
- Gráficos simples de validação (thrust/pressão x tempo)
- Imagens e GIFs de testes
- Documentação técnica dos motores (.md)

**Este repo NÃO contém:**
- Análises sofisticadas de voo → [analysis](https://github.com/Serra-Rocketry/analysis)
- Biblioteca de motores (app web) → [analysis](https://github.com/Serra-Rocketry/analysis)
- Computador de bordo → [flight-computer](https://github.com/Serra-Rocketry/flight-computer)
- Simulações de trajetória → [analysis](https://github.com/Serra-Rocketry/analysis)

**Diagrama:**
```
[motor] ──dados brutos──→ [analysis] ──→ app web, biblioteca
   │                           │
   │ Propulsão                 │ Telemetria
   │ - Geometria               │ - Análise de testes
   │ - Dados SD card           │ - Simulações de voo
   │ - CAD                     │ - Visualização
   │ - OpenMotor (.ric)        │ - Biblioteca de motores
```

## Estrutura

```
docs/
├── static-tests/          # Dados de testes estáticos
│   ├── motor-gabriel/     # Dados SD + gráfico
│   ├── motor-caramelo/
│   ├── motor-i/
│   └── scilab/            # Projetos SciLab para análise
├── motors/                # Documentação por motor
│   ├── sr21000/           # Motor principal (2025)
│   ├── sr1500/            # Motor SR1500
│   ├── 300m/              # Motor 300M
│   ├── v1/                # Motor V1.0
│   └── cardboard/         # Motor de papelão
├── rockets/               # Foguetes (não apenas motores)
│   ├── 500m/              # Foguete de 500m
│   ├── 1000m/             # Foguete de 1km
│   └── commercial/        # Foguete comercial
├── molds/                 # Moldes para propelentes
├── nozzle/                # Nozzle de cimento + cálculos
├── tools/                 # Ferramentas e gabaritos
├── imagens/               # Fotos, renderings, gráficos
└── training/              # Documentação de treinamento
```

## Motores

| Motor | Status | Descrição |
|---|---|---|
| SR21000 | Em desenvolvimento | Motor principal, KNSB, 21000 Ns |
| SR1500 | Concluído | Motor de teste, 1500 Ns |
| 300M | Concluído | Motor 300M com guiamento |
| V1.0 | Concluído | Primeiro motor da equipe |
| Cardboard | Concluído | Motor de papelão (teste) |

## Como Usar

### Abrir arquivos CAD

Os arquivos `.SLDPRT` e `.SLDASM` são do SolidWorks. Se não tiver SolidWorks:

- Use o [eDrawings Viewer](https://www.solidworks.com/product/edrawings-viewer) (gratuito)
- Arquivos `.STEP` abrem em qualquer CAD (FreeCAD, Fusion 360, etc.)
- Arquivos `.STL` são para impressão 3D (slicer)

### Simulações OpenMotor

Arquivos `.ric` são do [OpenMotor](https://github.com/reilleya/openMotor), software livre de simulação de motores de foguete. Para abrir:

1. Instale o OpenMotor: `pip install openmotor` ou baixe o executável
2. Abra o arquivo `.ric` correspondente ao motor
3. Execute a simulação

### Dados de Teste

Os arquivos `.txt` em `static-tests/` contêm dados brutos do SD card no formato:

```
HH:MM:SS ; empuxo(kN) ; tempo(ms)
```

## Contribuindo

Este projeto segue as [Boas Práticas da Serra Rocketry](https://github.com/Serra-Rocketry/best-practices). Para contribuir:

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/nome`)
3. Commit suas mudanças
4. Abra um Pull Request

### Regras para Arquivos CAD

- Normalizar nomes: sem acentos, espaços → `_`
- SolidWorks 2024+ (compatível com versões anteriores)
- Incluir desenhos técnicos (`.SLDDRW`) quando disponível
- Exportar `.STEP` para interoperabilidade

## Links

- [Thrust Stand](https://github.com/Serra-Rocketry/thrust-stand) — Sistema de aquisição de dados
- [Ignitor](https://github.com/Serra-Rocketry/ignitor) — Sistema de ignição remota
- [Best Practices](https://github.com/Serra-Rocketry/best-practices) — Boas práticas da equipe
- [MIGRATION.md](./MIGRATION.md) — Histórico de migração do Drive

---

**Mantido por:** Equipe Serra Rocketry — IPRJ/UERJ
