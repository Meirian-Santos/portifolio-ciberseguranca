# Relatório de Incidentes de Segurança Cibernética

## Cenário:

## ![cenario redes](https://github.com/user-attachments/assets/0547199a-aa31-41aa-834f-432851aab2cd)

 ## **1. Resumo do Problema**

Durante a análise de tráfego de rede utilizando `tcpdump`, identificamos problemas na resolução de DNS para o domínio **yummyrecipesforme.com**. O protocolo UDP foi utilizado para enviar solicitações ao servidor DNS, mas recebeu como resposta mensagens de erro ICMP indicando que a **porta UDP 53 estava inacessível**. 

Cada evento de log contém:
- **Duas primeiras linhas**: Solicitação UDP enviada do navegador para o servidor DNS.
- **Terceira e quarta linhas**: Resposta ICMP indicando erro (**"udp port 53 unreachable"**).

A porta **53** é essencial para a comunicação DNS, e os erros identificados indicam que o servidor DNS não está respondendo adequadamente. O uso do símbolo **"A?"** na requisição DNS e a presença de flags na resposta UDP reforçam a existência de falhas na resolução do domínio.

---

## **2. Análise e Causa do Incidente**

O incidente ocorreu **às 13h24**, quando clientes da organização relataram que receberam a mensagem **"destination port unreachable"** ao tentar acessar o site **yummyrecipesforme.com**. A equipe de cibersegurança foi acionada para investigar e restaurar o acesso ao serviço.

Utilizando a ferramenta **tcpdump**, confirmamos que a porta **53 estava inacessível**. As possíveis causas incluem:
- O **servidor DNS pode estar fora do ar**.
- O **tráfego DNS pode estar sendo bloqueado por um firewall**.
- Um **ataque de negação de serviço (DoS) pode ter sobrecarregado o servidor DNS**.

### **Plano de Ação**

Para solucionar o problema, as próximas etapas incluem:
1. **Verificar a disponibilidade do servidor DNS**.
2. **Analisar regras de firewall para identificar bloqueios na porta 53**.
3. **Investigar logs do servidor para verificar sinais de ataque DoS**.
4. **Redirecionar temporariamente o tráfego DNS para um servidor alternativo**.
5. **Implementar medidas de mitigação contra futuros ataques DoS**.

A investigação segue em andamento para restaurar a operação normal do serviço o mais rápido possível.

---
