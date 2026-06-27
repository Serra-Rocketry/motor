# Motores

Documentação CAD e especificações dos motores desenvolvidos pela Serra Rocketry.

## Motores

| Motor | Status | Propulsante | Empuxo | Arquivos |
|---|---|---|---|---|
| [SR21000](./sr21000/) | Em desenvolvimento | KNSB | 21000 Ns | CAD, desenhos, OpenMotor, STL, Parasolid |
| [SR1500](./sr1500/) | Concluído | KNSU | 1500 Ns | CAD, desenhos, OpenMotor, STL, gcode |
| [300M](./300m/) | Concluído | KNSU | — | CAD, STL, gcode |
| [V1](./v1/) | Concluído | KNSU | — | CAD |
| [Cardboard](./cardboard/) | Concluído | KNSU | — | CAD, STL (moldes) |

## Estrutura por motor

Cada motor pode ter as seguintes subpastas:

| Subpasta | Conteúdo | Software |
|---|---|---|
| `cad/` | Peças (`.SLDPRT`) e montagens (`.SLDASM`) | SolidWorks |
| `drawings/` | Desenhos técnicos (`.SLDDRW`, `.pdf`) | SolidWorks |
| `openmotor/` | Simulações (`.ric`) | [OpenMotor](https://github.com/reilleya/openMotor) |
| `stl/` | Modelos para impressão 3D (`.STL`) | Slicer |
| `parasolid/` | Modelos Parasolid (`.x_t`) | Interop CAD |
| `gcode/` | Instruções de impressão 3D (`.gcode`) | Slicer |

## Como abrir os arquivos

- **SolidWorks** (`.SLDPRT`, `.SLDASM`, `.SLDDRW`): SolidWorks 2024+ ou [eDrawings Viewer](https://www.solidworks.com/product/edrawings-viewer) (gratuito)
- **STEP** (`.step`, `.STEP`): qualquer CAD (FreeCAD, Fusion 360, SolidWorks)
- **STL** (`.STL`): qualquer slicer de impressão 3D
- **OpenMotor** (`.ric`): [OpenMotor](https://github.com/reilleya/openMotor) — software livre de simulação
- **Parasolid** (`.x_t`): SolidWorks, Fusion 360, ou qualquer CAD que suporte o formato
