Detecção de Tentativas de Brute Force (Threshold Baixo)

Descrição

Esta query tem como foco identificar possíveis tentativas iniciais de ataque de brute force em ambientes Windows, utilizando eventos de falha de autenticação.

Objetivo

Detectar múltiplas tentativas de login falhas para um mesmo usuário ou endereço IP, permitindo identificar comportamentos suspeitos em estágio inicial.

Lógica da Detecção

A query filtra eventos `EventCode=4625` no índice `wineventlog`, que representam falhas de autenticação no Windows, e realiza uma contagem por usuário e IP de origem.

Em seguida, aplica um threshold (`count > 5`) para destacar padrões anormais de tentativas de login.

Query

spl
index=wineventlog EventCode=4625
| stats count by user, src_ip
| where count > 5


Evidência

Este diretório contém prints da execução da query no Splunk, demonstrando a identificação de múltiplas tentativas de login falhas.

Observação

Atividade realizada em ambiente de laboratório controlado para fins educacionais.
