# Relatório Técnico de Propulsão: Dimensionamento e Testes Computacionais do Motor Sólido (Classe 500m)

## 1. Simulação de propelente (OpenMotor)
Utilizamos o software OpenMotor para prever o comportamento da pressão nos componentes do motor e o empuxo gerado.

Imagem 1 - Simulação de comportamento dos grãos.
Diâmetro Interno Câmara De Combustão - 40 mm
Comprimento Total Propelente - 250 mm
Número de Segmentos - 2
Diâmetro da Alma - 15 mm
Máxima Pressão De Operação - 350 Psi
Tempo de Queima - 1,59 s
Impulso Total - 559,71 Ns
Empuxo Máximo - ~ 550N
Empuxo Médio - ~ 380 N
Massa Propelente - 0,47 Kg
2. Materiais


Tubo (3” x ⅛”): Alumínio 6063-T5;
Tampa (3 Pol): Alumínio 6061;
Nozzle (3 Pol): Aço Inox AISI 304;
Parafuso (M5): Aço Inox AISI 304;
O’ring: Viton;
Alma: a definir.


## 3. Estudo de Pressão Radial e Resistência Mecânica do Tubo

A Pressão máxima de operação do motor é de 350 PSi , Para esse projeto utilizaremos um fator de segurança de 2.5 , sendo assim , todas os cálculos de esforços e simulações serão feitas considerando a pressão máxima com o fator de segurança aplicado, Sendo 875 PSi a pressão de simulação.


Imagem 2 - Simulação de pressão em tubo
A Partir da simulação de esforços pela pressão interna no tubo, temos como resultado todos os esforços dentro do limite elástico do material.











## 4. Validação dos Elementos de Fixação (Parafusos M5)
Conversão de carga
A pressão interna de  usada como limite de segurança superior em cálculos é convertida para o  :

Área da Tampa ()

Força Total de Expulsão ()
Como a tampa tem uma área de aproximadamente , a pressão interna será:

Carga Cortante por Parafuso ()

Não usamos apenas a tensão média (), mas sim a Equação de Jourawski. Para o cálculo da tensão máxima via Equação de Jourawski, utiliza-se o raio efetivo () derivado da área resistente normativa do parafuso M5 ().
Raio Efetivo (): derivado da área resistente

Primeiro Momento de Área (): para uma seção semicircular

Momento de Inércia (): para a seção circular do parafuso

Largura da Seção na Linha Neutra (): diâmetro efetivo na linha neutra

Tensão de Cisalhamento Máxima (Equação de Jourawski)
Conforme desenvolvido anteriormente, a tensão máxima ocorre na linha neutra da seção transversal do parafuso explícita pela fórmula:


Isso é feito porque o cisalhamento em parafusos circulares não é uniforme; ele atinge o máximo na linha neutra. Com uma carga cortante de  por parafuso, a tensão máxima de  nos diz exatamente o estresse no ponto mais crítico da seção transversal do M5.
Propriedades Mecânicas do Material dos Parafusos
Os elementos de fixação especificados para o projeto possuem as seguintes propriedades nominais de resistência, baseadas na padronização para fixadores métricos de alta resistência da classe A2-70:
Tensão Limite de Resistência à Tração:
Tensão de Escoamento à Tração:
### Tensão de Escoamento ao Cisalhamento () pelo Critério de Tresca
Para a determinação da capacidade de carga do parafuso sob condições de corte puro na linha neutra, adota-se o Critério de Tresca (também conhecido como Teoria da Tensão Cisalhante Máxima).
De acordo com este critério, o escoamento de um material dúctil inicia-se quando a tensão cisalhante máxima em qualquer ponto atinge a metade da tensão de escoamento obtida no ensaio de tração uniaxial simples. Matematicamente, a relação é expressa por:

Substituindo o valor de escoamento à tração do aço inox A2-70 ():


Como os valores de tensão atuante do sistema  já incorporam um fator de segurança de 2,5, a escolha de um limite de escoamento mais conservador pelo critério de Tresca (225 MPa) consolida uma abordagem de projeto robusta.
Embora a tensão atuante majorada esteja próxima do limite de Tresca, isso garante que, mesmo no pior cenário estatístico e com as cargas de segurança aplicadas, o componente ainda se manterá dentro do regime elástico de forma confiável.

## 5. Análise de Esmagamento do Tubo (Bearing Stress)
A análise de esmagamento avalia a compressão na parede do furo.
Tensão de Esmagamento Atuante ()
A força de cada parafuso sendo  é distribuída na área projetada do furo :

O Fator de Esmagamento ()
Diferente da tração simples, um material em torno de um furo possui restrição lateral, o que gera um estado de tensão triaxial que endurece o material localmente. Conforme normas aeroespaciais (MMPDS) e mecânicas (Eurocode), para ligas de alumínio, o limite de esmagamento é majorado pelo fator 1,5:
Limite de Esmagamento Real ():
A , a tensão de esmagamento atingiria aproximadamente . Como este valor ainda é inferior ao limite real de esmagamento (), o metal permanece no regime elástico, evitando a ovalização do furo.


