# Testes Estáticos

Dados brutos e gráficos de testes estáticos de motores de foguete.

## Testes Disponíveis

| Motor | Dados | Gráfico | SciLab |
|---|---|---|---|
| [Motor Gabriel](./motor-gabriel/) | [data.txt](./motor-gabriel/data.txt) | — | — |
| [Motor Caramelo](./motor-caramelo/) | [data.txt](./motor-caramelo/data.txt) | [graph.jpg](./motor-caramelo/graph.jpg) | [motor_caramelo.sciprj](./scilab/motor_caramelo.sciprj) |
| Motor I (69-31 Grãos torrados) | — | [graph.jpg](./motor-i/graph.jpg) | [motor_i.sciprj](./scilab/motor_i.sciprj) |

## Formato dos Dados

Os dados brutos do SD card seguem o formato:

```
HH:MM:SS ; empuxo(kN) ; tempo(ms)
```

Exemplo (Motor Gabriel):
```
12:17:22 ; 0.007 ; 114500
12:17:22 ; 0.007 ; 114600
12:17:23 ; 0.006 ; 114700
```

## Análise

Os projetos SciLab (`.sciprj`) em [scilab/](./scilab/) podem ser abertos com [Scilab](https://www.scilab.org/) para análise e geração de gráficos.

## Sistema de Aquisição

O sistema de aquisição de dados (thrust stand) fica no repositório [Serra-Rocketry/thrust-stand](https://github.com/Serra-Rocketry/thrust-stand). Este diretório contém apenas os dados coletados.
