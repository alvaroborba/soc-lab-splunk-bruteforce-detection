Simulação de Atividades SMB

Descrição

Este diretório contém simulações de atividades no protocolo SMB com o objetivo de gerar logs para análise em ambiente SOC (Splunk).

Brute Force via SMB

Objetivo

Simular um ataque de brute force contra o serviço SMB para gerar eventos de autenticação no sistema Windows e validar mecanismos de detecção no SIEM.

Lógica da Atividade

O comando utiliza a ferramenta Hydra para realizar tentativas automatizadas de login no protocolo SMB.

Parâmetros utilizados:

 `-L users.txt` → lista de usuários
 `-P rockyou.txt` → lista de senhas
 `smb://192.168.x.x` → alvo
 `-t 4` → conexões paralelas

Gera múltiplas falhas de autenticação no sistema alvo.

bash
hydra -L users.txt -P rockyou.txt smb://192.168.x.x -t 4

Enumeração SMB

Objetivo
 
Enumerar compartilhamentos disponíveis no host via SMB utilizando credenciais válidas.

Lógica da Atividade

O comando utiliza a ferramenta smbclient para listar os compartilhamentos do host alvo.

Parâmetros utilizados:

 `-L` → lista compartilhamentos
 `//192.168.1.10` → alvo
 `-U administrador` → usuário

Pode gerar eventos de autenticação e acesso no sistema.

bash
smbclient -L //192.168.1.10 -U administrador

Evidência

Inclui print da execução do comando `smbclient`, demonstrando os compartilhamentos disponíveis.

Observação

Atividades realizadas em ambiente controlado para fins educacionais.

