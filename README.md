# DESAFIO ONLINE DA VEXPENSES

## 1. Descrição Técnica do Arquivo Original

O arquivo `main.tf` cria uma infraestrutura básica na AWS contendo os seguintes componentes:

- VPC, Subnet, Internet Gateway, Tabela de Rotas e Associação.
- Key Pair para acesso SSH a uma instância EC2.
- Security Group permitindo SSH de qualquer lugar e tráfego de saída irrestrito.
- Uma instância EC2 rodando Debian 12 com script de `user_data` para atualizar e melhorar o sistema.

## 2. Melhorias Implementadas

### Segurança:
- **Acesso SSH Restrito**: O acesso SSH foi restrito a um endereço IP específico para melhorar a segurança.
- **Regras de IPv6 Removidas**: Caso o ambiente não utilize IPv6, as regras de IPv6 irrestritas foram removidas para reduzir a superfície de ataque.

### Automação:
- **Instalação do Nginx**: A instância EC2 agora instala e inicia automaticamente o servidor Nginx logo após ser criada.

### Outras Melhorias:
- **Adição de Tags**: Foram adicionadas mais tags para facilitar a identificação dos recursos.
- **Modularidade**: O código foi ajustado para uma estrutura mais legível e fácil de manter.
