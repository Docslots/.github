# DocSlot

Somos uma equipe de alunos do curso de Sistemas e Mídias Digitais (SMD) da Universidade Federal do Ceará (UFC). Estamos dedicados à produção de um trabalho acadêmico para a disciplina de **Teste de Software Aplicado**, sob orientação da Professora Marília S. Mendes.

## O Projeto

O **DocSlot** é um sistema de agendamento de consultas médicas, desenvolvido como projeto de teste para a disciplina. O sistema permite o cadastro de médicos e pacientes, a definição de horários (slots) disponíveis por médico e o agendamento e cancelamento de consultas nesses horários. Não há autenticação de usuários — o foco do projeto está na aplicação de testes sobre a lógica de negócio do sistema, e não em features de produção.

### Tecnologias Utilizadas

- **Backend**: NestJS (Node.js / TypeScript)
- **Frontend**: Next.js
- **Banco de Dados**: SQLite (via TypeORM)
- **Framework de Testes**: Jest

### Requisitos do Projeto

#### Requisitos Funcionais

| ID | Descrição |
|----|-----------|
| RF-01 | O sistema deve permitir o cadastro de um médico, informando nome e especialidade. |
| RF-02 | O sistema deve permitir o cadastro de um paciente, informando nome e telefone de contato. |
| RF-03 | O sistema deve permitir que um médico cadastre horários (slots) disponíveis para atendimento, informando data e hora. |
| RF-04 | O sistema deve permitir que um paciente agende uma consulta em um horário disponível de um médico específico. |
| RF-05 | O sistema deve permitir o cancelamento de uma consulta previamente agendada. |
| RF-06 | O sistema deve permitir a listagem de todos os horários disponíveis de um médico. |
| RF-07 | O sistema deve permitir a listagem de todas as consultas agendadas por um paciente. |

#### Requisitos Não Funcionais

| ID | Descrição |
|----|-----------|
| RNF-01 | O sistema deve responder a requisições de agendamento em até 2 segundos. |
| RNF-02 | O sistema deve ser implementado utilizando o framework NestJS, em Node.js. |
| RNF-03 | Os dados devem ser persistidos em um banco de dados SQLite. |
| RNF-04 | O sistema deve estar disponível via API RESTful, permitindo integração com a interface web (Next.js). |
| RNF-05 | O sistema deve retornar mensagens de erro claras e específicas em caso de falha de validação. |

#### Regras de Negócio

| ID | Descrição |
|----|-----------|
| RN-01 | Um horário (slot) só pode ser agendado por um paciente por vez; não é permitido agendamento duplicado no mesmo slot. |
| RN-02 | Um médico não pode cadastrar dois horários idênticos (mesma data e hora) para si mesmo. |
| RN-03 | Não é permitido agendar consulta em horário no passado. |
| RN-04 | Um slot com consulta cancelada volta a ficar disponível para novo agendamento. |
| RN-05 | O nome do médico e do paciente deve ter no mínimo 3 e no máximo 100 caracteres. |
| RN-06 | Uma consulta só pode ser cancelada se ainda não tiver ocorrido. |

### Testes

Neste repositório, você encontrará os materiais e o código desenvolvidos para a validação do DocSlot, totalizando **6 casos de teste** (3 manuais e 3 automáticos), elaborados a partir dos requisitos e regras de negócio listados acima. Os detalhes de cada caso de teste — descrição, pré-condições, passos, resultado esperado e status — estão documentados no relatório do projeto.

## Equipe

Guilherme Bessa e Samir Feitosa
