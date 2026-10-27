# favero-laboratorio
# Clínica Favero — Laboratório de Agentes

Ambiente de desenvolvimento e testes do atendimento virtual da Clínica Favero.

**Status:** planejamento e documentação inicial. As integrações e o funcionamento do agente ainda precisam ser implementados ou verificados e testados antes do atendimento real.

## Objetivo

Construir uma consultora virtual que acolha interessados, entenda seus objetivos, esclareça dúvidas com informações aprovadas pela clínica e facilite o agendamento de avaliações.

O agente de atendimento será o primeiro componente deste laboratório. A expansão para outras funções será definida em etapas posteriores.

## Funções previstas

- Atender em português brasileiro, com linguagem acolhedora, natural e objetiva.
- Entender o interesse do paciente com perguntas abertas, uma de cada vez.
- Explicar os serviços com base no material aprovado pela clínica.
- Ajudar a avançar para uma avaliação, respeitando a decisão do paciente.
- Consultar a agenda e oferecer duas ou três opções realmente disponíveis.
- Confirmar agendamentos somente após o retorno de sucesso da ferramenta.
- Encaminhar a conversa para a equipe humana quando necessário ou solicitado.
- Enviar lembretes e retornos conforme autorização do paciente e regras do canal.

## Fluxo de atendimento

1. Apresentar-se como assistente virtual da Clínica Favero.
2. Acolher e entender o objetivo da pessoa.
3. Responder às dúvidas usando a base aprovada.
4. Explicar o próximo passo e as condições comerciais aplicáveis.
5. Consultar horários, confirmar a escolha e registrar o agendamento.
6. Entregar confirmação ou encaminhar ao humano com um resumo.

Se uma informação ou ferramenta estiver indisponível, explicar a limitação e oferecer um próximo passo possível.

## Regras de conversa

- Personalizar o atendimento sem transformar a conversa em um interrogatório.
- Explicar o valor da avaliação e a necessidade de análise individual.
- Usar apenas preços, taxas, descontos e condições aprovados e atualizados.
- Não inventar informações, resultados, depoimentos ou horários.
- Não prometer resultados estéticos nem garantir indicação de procedimentos.
- Não diagnosticar, prescrever, indicar medicamentos ou definir condutas clínicas.
- Encaminhar dúvidas clínicas, intercorrências e situações de urgência à assistência apropriada, sem tentar resolvê-las comercialmente.
- Solicitar somente os dados necessários ao atendimento.
- Não insistir após recusa ou pedido para interromper contatos.

## Base de conhecimento própria — RAG

O agente deverá consultar uma base exclusiva da Clínica Favero.

Essa base reunirá materiais sobre serviços, avaliação, dúvidas frequentes, políticas comerciais e regras operacionais.

Requisitos:

- Revisar e aprovar cada conteúdo antes de liberá-lo para respostas.
- Registrar fonte, versão, responsável pela aprovação e data de revisão.
- Separar documentos originais, rascunhos e respostas aprovadas.
- Retirar da consulta conteúdos desatualizados ou substituídos.
- Não tratar sugestões geradas por IA como orientação clínica aprovada.
- Na ausência de uma resposta confiável, reconhecer a dúvida e encaminhar ao humano.
- Não misturar informações de pacientes ou de outros projetos.

## Componentes previstos

- **Canal:** WhatsApp oficial, com integração a configurar e validar.
- **Agente de atendimento:** conversa, esclarece dúvidas e conduz o fluxo.
- **Base RAG:** fornece informações aprovadas da clínica.
- **Agenda:** consulta disponibilidade e registra agendamentos autorizados.
- **Equipe humana:** assume exceções, decisões clínicas e solicitações do paciente.
- **Infraestrutura em nuvem:** sustenta a operação contínua após implantação e testes.

OpenClaw, Hermes, modelo de IA, banco de dados e hospedagem permanecem sujeitos à definição técnica e à validação das integrações. Este README não confirma a escolha ou o funcionamento dessas ferramentas.

## Repasse para a equipe humana

O resumo deverá conter apenas o necessário:

- Identificação e contato, quando fornecidos.
- Objetivo e serviço de interesse.
- Dúvidas e objeções mencionadas.
- Informações já transmitidas.
- Preferência de horário e situação do agendamento.
- Motivo do encaminhamento e próximo passo combinado.

## Proteção de dados e acessos

- Usar dados fictícios nos testes iniciais.
- Guardar senhas, tokens e chaves fora do repositório.
- Não incluir conversas, fotos, prontuários ou dados reais de pacientes nos arquivos ou no histórico do GitHub.
- Limitar o acesso aos sistemas conforme a função de cada componente.
- Definir armazenamento, retenção, exclusão e registro de acesso antes do uso com dados reais.

## Etapas de implantação

1. Aprovar o escopo e as regras de atendimento.
2. Organizar e revisar a base de conhecimento.
3. Construir o protótipo com dados fictícios.
4. Conectar e testar WhatsApp, agenda e repasse humano.
5. Simular dúvidas, objeções, indisponibilidade de ferramentas e pedidos de atendimento humano.
6. Realizar um piloto supervisionado e corrigir falhas antes de ampliar a operação.

## Indicadores de validação

Acompanhar tempo de primeira resposta, avaliações agendadas, comparecimento, necessidade de intervenção humana, erros de informação e falhas de agendamento.

Operação 24 horas e primeira resposta em menos de um minuto são metas a validar, não resultados já demonstrados.

## Execução

O projeto está na etapa inicial de documentação. As instruções de instalação, configuração e execução serão incluídas quando houver uma implementação testada.
