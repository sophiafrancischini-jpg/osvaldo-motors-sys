# Osvaldo

Objetivo do Sistema: Automatizar a gestão da oficina mecânica por meio do cadastro simplificado de
veículos e emissão de Ordens de Serviço (OS) com separação de custos de peças e mão de obra. O
sistema realiza o cálculo automático com acréscimo de 20% na mão de obra para veículos importados,
restringe opções de pagamento ao modelo à vista (bloqueando fiado/crédito pendente) e apresenta uma
interface ultra-simplificada para uso em balcão.

# Osvaldo - Sistema de Gestão da Oficina Mecânica

## MER - Modelo Entidade-Relacionamento

### Entidades e Atributos

#### CLIENTE

- **id_cliente** (PK)
- nome

#### VEÍCULO

- **id_veiculo** (PK)
- placa
- modelo
- importado
- **id_cliente** (FK)

#### ORDEM DE SERVIÇO

- **id_os** (PK)
- valor_mao_obra
- valor_pecas
- acrescimo_importado
- valor_total
- **id_veiculo** (FK)

#### SERVIÇO

- **id_servico** (PK)
- descricao
- valor
- **id_os** (FK)

#### PEÇA

- **id_peca** (PK)
- descricao
- valor
- **id_os** (FK)

#### PAGAMENTO

- **id_pagamento** (PK)
- forma_pagamento
- valor_pago
- **id_os** (FK)
