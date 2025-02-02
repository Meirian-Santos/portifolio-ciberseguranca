# Auditoria de Segurança da Botium Toys

![Cenário para a auditoria](https://github.com/user-attachments/assets/67deac59-bcad-419e-a5c2-2229a9143eb9)

## Escopo da Auditoria
O escopo da auditoria abrange toda a infraestrutura de segurança da Botium Toys, incluindo:
- Equipamentos internos de negócios no escritório.
- Equipamentos de funcionários (dispositivos de usuário final como desktops, laptops, smartphones, etc.).
- Rede interna e acesso à internet.
- Sistemas de gerenciamento como contabilidade, telecomunicações, banco de dados, segurança, e-commerce e gerenciamento de inventário.
- Dados retidos e armazenados.
- Manutenção de sistemas legados.
- Produtos da loja disponíveis para venda.

## Objetivos da Auditoria
- Avaliar os ativos atualmente gerenciados pelo departamento de TI da Botium Toys.

- Avaliar os controles e práticas de conformidade da empresa.
- Completar a lista de verificação de controles e conformidade para identificar áreas que precisam ser melhoradas, a fim de melhorar a postura de segurança cibernética da empresa.

---

## Análise do Relatório de Avaliação de Risco

### 1. Gestão inadequada de ativos
- **Descrição**: A empresa não possui um gerenciamento adequado de ativos e, como resultado, não sabe quais ativos estão sob risco. Isso aumenta o potencial de perdas e falhas de conformidade.
- **Risco**: Alto. A falta de visibilidade sobre os ativos compromete a gestão eficiente da segurança.

### 2. Falta de controles adequados e conformidade com regulamentos
- **Descrição**: A empresa não está em total conformidade com os regulamentos locais e internacionais, especialmente relacionados ao tratamento de dados confidenciais, como dados de cartões de crédito e dados pessoais de clientes.
- **Risco**: Alto. A falta de conformidade pode resultar em multas severas e em danos à reputação.

### 3. Controle de Acesso e Privacidade
- **Descrição**: Todos os funcionários têm acesso irrestrito aos dados armazenados internamente e podem acessar dados de cartões de crédito e informações pessoais dos clientes.
- **Risco**: Alto. O controle de acesso inadequado pode resultar em vazamento ou uso indevido de dados sensíveis.

### 4. Criptografia e Proteção de Dados
- **Descrição**: A empresa não está utilizando criptografia para garantir a confidencialidade de informações sensíveis, como cartões de crédito, em seus sistemas.
- **Risco**: Alto. A ausência de criptografia compromete a proteção de dados sensíveis durante o armazenamento e transmissão.

---

## Controles Administrativos

### 1. Least Privilege (Privilégio Mínimo)
- **Status**: Não implementado.
- **Recomendação**: Implementar controles de privilégio mínimo, onde os usuários só terão acesso aos recursos necessários para suas funções específicas.

### 2. Plano de Recuperação de Desastres
- **Status**: Não implementado.
- **Recomendação**: Desenvolver e implementar um plano de recuperação de desastres que cubra todos os cenários de falhas críticas nos sistemas e dados.

### 3. Política de Senhas
- **Status**: Parcialmente implementado.
- **Recomendação**: Atualizar a política de senhas para incluir requisitos de complexidade (mínimo de 8 caracteres, combinação de letras, números e caracteres especiais).

### 4. Política de Controle de Acesso
- **Status**: Não implementado.
- **Recomendação**: Criar políticas claras de controle de acesso, implementando autenticação forte e validação contínua para usuários e dispositivos.

### 5. Separação de Funções
- **Status**: Não implementado.
- **Recomendação**: Implementar separação de funções para garantir que uma única pessoa não tenha controle total sobre processos críticos.

---

## Controles Técnicos

### 1. Firewall
- **Status**: Implementado.
- **Recomendação**: Continuar monitorando e atualizando as regras do firewall para garantir a proteção contra tráfego malicioso.

### 2. IDS/IPS (Sistema de Detecção/Prevenção de Intrusões)
- **Status**: Não implementado.
- **Recomendação**: Implementar um sistema de IDS/IPS para monitorar e responder a tráfego anômalo em tempo real.

### 3. Criptografia
- **Status**: Não implementado.
- **Recomendação**: Implementar criptografia para proteger dados sensíveis, especialmente informações de cartões de crédito e dados pessoais dos clientes.

### 4. Backups
- **Status**: Não implementado.
- **Recomendação**: Estabelecer um programa de backup regular para garantir a recuperação de dados críticos após um incidente.

### 5. Antivirus
- **Status**: Implementado.
- **Recomendação**: Manter o antivírus atualizado e realizar verificações regulares em todos os dispositivos e servidores.

### 6. Gestão de Senhas
- **Status**: Não implementado.
- **Recomendação**: Adotar um sistema de gerenciamento de senhas centralizado e garantir que as senhas atendam aos requisitos de complexidade.

---

## Controles Físicos

### 1. Cofre com Controle de Tempo
- **Status**: Não implementado.
- **Recomendação**: Considerar a implementação de cofres para proteger fisicamente dados e dispositivos críticos.

### 2. Iluminação Adequada
- **Status**: Implementado.
- **Recomendação**: Manter a iluminação adequada nas instalações para desmotivar ataques físicos.

---

## Conclusões da Auditoria
A auditoria revelou falhas críticas em vários controles administrativos, técnicos e físicos, o que representa um risco significativo para a segurança e a conformidade da Botium Toys. A implementação de controles como criptografia, recuperação de desastres, IDS/IPS e um plano de gerenciamento de senhas deve ser uma prioridade. Além disso, a empresa precisa melhorar suas políticas de controle de acesso, privilégio mínimo e separação de funções para reduzir o risco de ameaças internas e externas.

---

## Recomendações Finais
1. **Implementar controles de privilégio mínimo e separação de funções**.
2. **Desenvolver e implementar um plano de recuperação de desastres**.
3. **Adotar criptografia e implementar IDS/IPS** para melhorar a proteção de dados.
4. **Estabelecer uma política de senhas mais robusta e adotar um sistema de gerenciamento de senhas**.
5. **Realizar backups regulares** para garantir a continuidade dos negócios em caso de desastre.

Essas ações são essenciais para fortalecer a postura de segurança da Botium Toys e garantir a conformidade com regulamentações de segurança, especialmente ao lidar com dados sensíveis e privados.
