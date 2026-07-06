 MISSÃO EVORTEX — Mission Control AI

Sistema inteligente de monitoramento ambiental de uma cápsula espacial experimental, desenvolvido com Arduino Uno e interface web interativa.

Sobre o Projeto

A Missão EVORTEX simula o monitoramento em tempo real das condições internas de uma cápsula espacial. O sistema lê dados de sensores físicos conectados a um Arduino Uno e os exibe em um painel de controle futurista com alertas automáticos, gráficos históricos e um chatbot de IA integrado.

Desenvolvido como projeto acadêmico na FIAP — Global Solution 2026.1.

Time: EVORTEX

Funcionalidades

Dashboard interativo — painel futurista com leitura em tempo real de 4 sensores ambientais Alertas críticos automáticos — popups com protocolo de resposta passo a passo ao detectar situações de risco Chatbot ARIA — IA conversacional com base de conhecimento completa sobre a missão, sensores e protocolos de emergência Painel de análise — exibe condicionais, repetição, vetores e funções em tempo real Web Serial API — conexão direta com o Arduino via navegador (Chrome/Edge) Modo simulação — permite explorar todas as funcionalidades sem hardware conectado

Hardware

Microcontrolador: Arduino Uno Comunicação: USB Serial — 9600 baud Interface: Web Serial API (Google Chrome / Microsoft Edge)

Sensores:

A0 — Sensor de Gás (MQ-2 ou similar) — detecta concentração de gás inflamável/tóxico A1 — Sensor de Fogo (Fotodiodo IR) — lógica invertida: valor baixo = fogo detectado A3 — Sensor de Luminosidade (LDR) — verifica falha de iluminação interna A4 — Sensor de Temperatura (Termistor NTC, β=3950, R₀=100kΩ) D6 — Buzzer de Emergência — sirene 600–1400 Hz, ativado automaticamente por falha de luz

Limites de Alerta

Gás (A0): normal < 140 raw · atenção 140–200 raw · crítico > 200 raw Fogo (A1): normal > 350 raw · atenção 300–350 raw · crítico < 300 raw Luz (A3): funcionando ≥ 50 raw · falha < 50 raw Temperatura (A4): normal 18–30 °C · atenção 31–40 °C · crítico > 40 °C

Estrutura do Notebook

Célula 1 — Configuração do ambiente: verifica Python e prepara dependências Célula 2 — Interface EVORTEX no notebook: renderiza o painel no Colab Célula 3 — Chatbot ARIA em Python: conversa com a IA diretamente no terminal Célula 4 — Exporta missao_evortex.html para uso com Arduino real no Chrome/Edge

Como Usar

Modo Simulação (sem Arduino)

Abra o notebook no Google Colab Execute Célula 1 — configura o ambiente Execute Célula 4 — gera o arquivo missao_evortex.html Abra o arquivo no Google Chrome ou Microsoft Edge Use o Modo Simulação no painel para explorar todas as funcionalidades

Modo Real (com Arduino)

Faça o upload do código .ino para o Arduino Uno Conecte o Arduino ao computador via USB Abra o arquivo missao_evortex.html no Google Chrome ou Microsoft Edge Clique em Conectar Arduino no painel Selecione a porta serial correspondente

Atenção: A Web Serial API funciona apenas no Google Chrome ou Microsoft Edge. Não é suportada no Firefox ou Safari.

Tecnologias

Python 3 Google Colab / Jupyter Notebook Arduino (C++) HTML / CSS / JavaScript Web Serial API IPython.display

Conceitos Demonstrados

Estruturas condicionais e repetição Vetores e funções Comunicação serial Arduino ↔ navegador Leitura e conversão de sinais analógicos (ADC) Equação de Steinhart-Hart (cálculo de temperatura via NTC) Desenvolvimento de chatbot com base de conhecimento estruturada

Equipe

EVORTEX — FIAP, Global Solution 2026.1
