# Relatório de Incidentes de Segurança Cibernética

## Parte 1: Resumo do Problema Encontrado no DNS e no ICMP

### Registro de Tráfego

O protocolo **UDP** revela que:

Isso se baseia nos resultados da análise de rede, que mostram que a resposta de **eco ICMP** retornou a mensagem de erro:

> `udp port 53 unreachable` (porta UDP 53 inacessível)

A porta indicada na mensagem de erro é usada para:

- O serviço **DNS** (Domain Name System).

O problema mais provável é:

- O **servidor DNS** de destino **não está acessível**, impossibilitando a resolução do domínio `www.yummyrecipesforme.com`.

## Parte 2: Análise dos Dados e Causa do Incidente

### Hora do Incidente

- **Horário:** 13h24, 32,192571 segundos.

### Como a Equipe de TI Tomou Conhecimento do Incidente

- Clientes relataram que **não conseguiram acessar o site** `www.yummyrecipesforme.com`.
- O erro retornado foi **"porta de destino inalcançável"**.
- O analista tentou acessar o site e **recebeu o mesmo erro**.
- Para investigar, utilizou a ferramenta **tcpdump** para capturar pacotes de rede.

### Ações Tomadas pelo Departamento de TI

1. **Captura de Pacotes** usando `tcpdump` enquanto tentava acessar o site.
2. **Análise do Tráfego de Rede**, observando pacotes **UDP e ICMP**.
3. **Identificação do Problema**:
   - O navegador enviou uma **consulta DNS via UDP** para obter o endereço IP do domínio.
   - O servidor DNS **respondeu com um erro ICMP**, informando que **a porta 53 estava inacessível**.
4. **Reportou o problema** aos engenheiros de segurança para análise mais aprofundada.

### Descobertas Principais

- **Endereço IP de Origem:** `192.51.100.15` (computador do analista).
- **Endereço IP de Destino:** `203.0.113.2` (servidor DNS).
- **Mensagem de erro capturada:** `ICMP 203.0.113.2 - udp port 53 unreachable`.
- **Conclusão:** O **servidor DNS não está acessível**, impedindo a resolução do domínio.

### Causa Provável do Incidente

- **Falha no servidor DNS**: O serviço DNS pode estar **desligado, mal configurado ou bloqueado**.
- **Problema de conectividade na rede**: O tráfego UDP pode estar **sendo filtrado ou bloqueado por um firewall**.

---

📌 *Este relatório foi gerado como parte de um estudo sobre análise de tráfego de rede e incidentes de segurança cibernética.*
