---
id: introducao-eletronica-digital
title: Introdução à Eletrônica Digital
---
# Introdução à Eletrônica Digital

A eletrônica digital é a base fundamental de toda a computação moderna. Ela estuda como representar, processar e armazenar informações usando sinais elétricos discretos, em contraste com a eletrônica analógica, que lida com grandezas contínuas.

## Sinais Analógicos vs. Sinais Digitais

Na natureza, a maioria dos fenômenos físicos ocorre de forma contínua no tempo: a temperatura de uma sala, a pressão do ar ou a intensidade da luz. Em termos elétricos, um **sinal analógico** pode assumir infinitos valores de tensão dentro de um intervalo.

A grande limitação dos sinais analógicos é a vulnerabilidade ao ruído: qualquer pequena interferência elétrica altera o sinal original de forma irreversível.

Em contrapartida, um **sinal digital** é discretizado. Em um sistema binário, abstraímos a variação de tensão para apenas dois estados bem definidos: **$0$** e **$1$** (ou *BAIXO* e *ALTO*).

![Comparação entre Sinal Analógico e Sinal Digital](../../../../assets/analog-vs-digital-signals.svg)

## Por que usar o Sistema Digital ?

A principal vantagem da eletrônica digital é a sua **alta tolerância ao ruído**.

Como o sistema só precisa distinguir entre dois estados ($0$ ou $1$), ele consegue suportar pequenas variações e interferências na linha de transmissão. Desde que o ruído não ultrapasse os limites de tolerância do circuito, a informação é interpretada e restaurada corretamente.

Isso possibilita:
* **Confiabilidade:** Transmissão e processamento de dados sem perda de informação.
* **Reprodutibilidade:** Facilidade para armazenar e copiar dados com precisão absoluta.
* **Abstração:** Construção de sistemas complexos (como processadores) a partir de blocos lógicos simples.
