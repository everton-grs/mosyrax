# Mosyrax: Simulador Interativo de Transistor MOS (NMOS-PMOS)

Mosyrax é uma aplicação educacional interativa composta por dois módulos autônomos - Simulador Interativo de Transistor NMOS e Simulador Interativo de Transistor PMOS - implementados como arquivos HTML independentes e executados diretamente em navegador web, sem necessidade de instalação ou compilação. Cada módulo integra, em uma única estrutura, a interface gráfica, a representação visual do dispositivo e as rotinas computacionais responsáveis pela simulação.

O sistema permite a visualização didática, em tempo real, do comportamento físico e elétrico de transistores MOS, incluindo a formação do canal de inversão, a região de depleção, o fenômeno de pinch-off, a corrente de dreno e os regimes de operação do transistor (corte, triodo e saturação), a partir da manipulação interativa de parâmetros elétricos e geométricos.

A aplicação combina modelagem matemática, atualização dinâmica de variáveis e representação gráfica simultânea, possibilitando ao usuário observar, de forma integrada, a relação entre as equações do dispositivo, sua resposta elétrica e sua interpretação física.

---

## Interface Gráfica (PMOS)
<img width="1022" height="907" alt="capa" src="https://github.com/user-attachments/assets/27e4e049-578f-45d4-99ee-8aebed1fa667" />

## 📌 Visão Geral

A aplicação foi projetada para facilitar a compreensão dos principais fenômenos em transistores MOS, incluindo:

- formação do canal de inversão  
- região de depleção  
- efeito de *pinch-off*  
- corrente de dreno  
- regimes de operação: corte, triodo e saturação  

Tudo isso é controlado por meio da manipulação interativa de parâmetros elétricos e geométricos.

---

## ⚙️ Funcionamento

O funcionamento do sistema ocorre da seguinte forma:

1. O usuário abre o arquivo HTML correspondente ao transistor desejado (aguarde 30 s)
2. A interface carrega:
   - diagrama do transistor  
   - controles interativos  
   - gráfico da curva característica  
3. Alterações nos parâmetros disparam a atualização da simulação
4. O sistema recalcula:
   - corrente  
   - resistências  
   - modo de operação  
5. A interface é atualizada em tempo real com:
   - gráficos  
   - animações  
   - representação física do dispositivo  
6. As equações são destacadas conforme o regime de operação

---

## 🎯 Finalidade e Aplicações

O Mosyrax foi desenvolvido para apoiar:

- ensino de eletrônica e microeletrônica  
- disciplinas de semicondutores  
- circuitos analógicos e digitais  
- demonstrações didáticas em laboratório  
- estudo autônomo  

---

## 🏗️ Arquitetura

- aplicação **front-end autocontida**
- execução local no navegador
- sem backend

### Estrutura

- `NMOS.html` → simulador NMOS  
- `PMOS.html` → simulador PMOS  

Cada arquivo contém:

- HTML (estrutura)
- CSS (estilização)
- JavaScript (lógica e simulação)
- SVG (visualização do dispositivo)

---

## 🧰 Tecnologias Utilizadas

- HTML5  
- CSS3  
- JavaScript  
- SVG  
- Tailwind CSS  
- Chart.js  
- KaTeX  
- fontes: Inter e Fira Code  

---

## 🚀 Funcionalidades

### 🔹 Simulador NMOS

- controle de VGS, VDS, k'n, λ', W e L  
- cálculo automático de W/L e λ  
- identificação do modo de operação  
- cálculo de ID, ro e Ron  
- curva ID × VDS em tempo real  
- ponto de operação destacado  
- animação de elétrons  
- visualização do canal e do efeito de *pinch-off*  

### 🔹 Simulador PMOS

- funcionalidade equivalente ao simulador NMOS  
- uso de valores absolutos para facilitar a análise didática  
- cálculo de |ID|, ro e Ron  
- curva |ID| × |VDS|  
- representação física do PMOS  
- animação do fluxo de cargas  

---

## 📐 Modelagem Matemática

O modelo implementa equações clássicas de transistores MOS.

### NMOS

- condição de corte:  
  `VGS < Vth → ID = 0`

- regiões de triodo e saturação com modulação do comprimento de canal:  
  `(1 + λVDS)`

- resistências aproximadas:
  - `ro ≈ 1 / (λ ID)`
  - `Ron = 1 / [μn Cox (W/L)(VGS − Vth)]`

### PMOS

- condição de corte:  
  `|VGS| < |VTH| → |ID| = 0`

- equações em módulo (valores absolutos)

- resistências aproximadas:
  - `ro ≈ 1 / (λ |ID|)`
  - `Ron = 1 / [μp Cox (W/L)(|VGS| − |VTH|)]`

---

## 🖥️ Interface

A interface integra, em uma única página:

- diagrama físico do transistor  
- controles interativos  
- gráfico da curva característica  
- painel de status  
- explicações conceituais  
- equações matemáticas renderizadas  
- animações didáticas  

---

## 🔌 Entradas e Saídas

### Entradas

- VGS e VDS  
- k'n ou k'p  
- λ'  
- W e L  

### Saídas

- corrente de dreno (ID)  
- resistências (ro e Ron)  
- modo de operação  
- curva característica  
- representação visual dinâmica  

---

## 💻 Requisitos

- navegador moderno (Chrome, Edge, Firefox etc.)  
- suporte a HTML5, CSS3 e JavaScript  

---

## 📎 Observações

- não requer instalação  
- não utiliza backend  
- execução totalmente local  
