Consultas de Monitoramento e Detecção (Splunk)

Descrição

Este diretório contém queries utilizadas no Splunk para monitoramento de eventos Windows e Sysmon, com foco na detecção de atividades suspeitas e análise de comportamento no ambiente.

Consultas

Falhas de Login (4625)**
  Identifica tentativas de autenticação mal sucedidas, podendo indicar erros de credenciais ou ataques de brute force.

Logins com Sucesso (4624)**
  Monitora acessos válidos e permite correlação com eventos de falha para identificar possíveis comprometimentos.

Detecção de Brute Force**
  Identifica múltiplas tentativas de login falhas acima de um threshold, indicando possível ataque de força bruta.

Volume de Eventos por Host**
  Mostra quais máquinas geram mais logs, auxiliando na criação de baseline e identificação de anomalias.

Criação de Processos (Sysmon)**
  Permite visualizar processos executados, incluindo usuário e linha de comando, auxiliando na detecção de atividades suspeitas.

Frequência de Execução de Processos**
  Apresenta os processos mais executados no ambiente, ajudando a identificar padrões e comportamentos incomuns.

Objetivo

Demonstrar na prática a análise de logs e a criação de detecções básicas em ambiente SOC, utilizando Splunk e Sysmon.

Observação

Atividades realizadas em ambiente de laboratório controlado para fins educacionais.

