

Materiais do foguete:

Tampa: Aluminio 3 pol
Tubo 3Pol x 1/8: Aluminio 6063-T5
Nozzle: Inox 3 pol (Liga a definir)
Parafuso: inox M5 ( Espessura a definir a partir da simulação)
Oring: Viton
Alma : Teflon e Nylon





Oring

Dimensões:




Simulações:








Open Motor:
Utilizamos o software OpenMotor para prever o comportamento da pressão nos componentes do motor e o empuxo gerado.


Meteor:











## 2. Validação dos Elementos de Fixação (Parafusos M6)
Conversão de carga
A pressão interna de  usada como limite de segurança superior em cálculos é convertida para o  :

Área da Tampa ()

Força Total de Expulsão ()
Como a tampa tem uma área de aproximadamente , a pressão interna será:

Carga Cortante por Parafuso ()

Não usamos apenas a tensão média (), mas sim a Equação de Jourawski. Para o cálculo da tensão máxima via Equação de Jourawski, utiliza-se o raio efetivo () derivado da área resistente normativa do parafuso M6 ().
Raio Efetivo (): derivado da área resistente

Primeiro Momento de Área (): para uma seção semicircular

Momento de Inércia (): para a seção circular do parafuso

Largura da Seção na Linha Neutra (): diâmetro efetivo na linha neutra

Tensão de Cisalhamento Máxima (Equação de Jourawski)
Conforme desenvolvido anteriormente, a tensão máxima ocorre na linha neutra da seção transversal do parafuso explícita pela fórmula:


Isso é feito porque o cisalhamento em parafusos circulares não é uniforme; ele atinge o máximo na linha neutra. Com uma carga cortante de  por parafuso, a tensão máxima de  nos diz exatamente o estresse no ponto mais crítico da seção transversal do M6.

### Propriedades Mecânicas do Material dos Parafusos
Os elementos de fixação especificados para o projeto possuem as seguintes propriedades nominais de resistência, baseadas na padronização para fixadores métricos de alta resistência da classe 12.9:
Tensão Limite de Resistência à Tração:
Tensão de Escoamento à Tração:
### Tensão de Escoamento ao Cisalhamento () pelo Critério de Tresca
Para a determinação da capacidade de carga do parafuso sob condições de corte puro na linha neutra, adota-se o Critério de Tresca (também conhecido como Teoria da Tensão Cisalhante Máxima).
De acordo com este critério, o escoamento de um material dúctil inicia-se quando a tensão cisalhante máxima em qualquer ponto atinge a metade da tensão de escoamento obtida no ensaio de tração uniaxial simples. Matematicamente, a relação é expressa por:

Substituindo o valor de escoamento à tração do aço liga 12.9 ():


Como os valores de tensão atuante do sistema  já incorporam um fator de segurança de 2,5, a escolha de um limite de escoamento mais conservador pelo critério de Tresca (540 MPa) consolida uma abordagem de projeto robusta e de alta confiabilidade mecânica, garantindo que o componente opere significativamente abaixo de sua capacidade real de escoamento em regime puramente elástico.
## 3. Análise de Esmagamento do Tubo (Bearing Stress)
A análise de esmagamento avalia a compressão na parede do furo.
Tensão de Esmagamento Atuante ()
A força de cada parafuso sendo  é distribuída na área projetada do furo :

O Fator de Esmagamento ()
Diferente da tração simples, um material em torno de um furo possui restrição lateral, o que gera um estado de tensão triaxial que endurece o material localmente. Conforme normas aeroespaciais (MMPDS) e mecânicas (Eurocode), para ligas de alumínio, o limite de esmagamento é majorado pelo fator 1,6:

Limite de Esmagamento Real () do alumínio 6063-T5:


A , a tensão de esmagamento atingiria aproximadamente   em parafuso. Como este valor ainda é inferior ao limite real de esmagamento (), o metal permanece no regime elástico, evitando a ovalização do furo.

Fazer com 8 parafusos M6 Aço liga 12.9 , fator de esmagamento 1,6

Simulação De Pressão Tubo:



Pressão da Simulação =  (F.S 2,5)*519,31 Psi = 1298,275 Psi





Simulação Parafusos:

A área da tampa é 0,00361567M^2 , logo a Força que a pressão de 519,31 Psi com Fator de Segurança 2,5 realiza é igual a 0,00361567M^2 * 8951291,0246(Pa) = 32.364,91 N

Logo a força que cada parafuso tem que resistir é 32364,91N /Número de Parafusos

Para uma análise inicial foram selecionados 4 parafusos M5 de Aço Inox, logo a força sobre cada parafuso é de 32364,91/4 = 8091,23 N

Resultado da simulação:




A partir da simulação , verificou-se que os 4 parafusos M5 de Aço Inox x 20mm resistiram ao esforço de cisalhamento de 8091,23 N.

Simular efeito da pressão no acoplamento parafuso tubo


