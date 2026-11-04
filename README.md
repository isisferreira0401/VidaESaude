 # Sistema de Gestão Hospitalar Vida & Saúde

Este repositório contém a modelagem e implementação do Banco de Dados Relacional para o Hospital Geral Vida & Saúde, desenvolvido como solução para a centralização, organização e análise dos dados operacionais da instituição.

📌 Sobre o Projeto

O Hospital Geral Vida & Saúde operava anteriormente utilizando registros manuais e planilhas isoladas, gerando problemas operacionais graves. Para sanar esses gargalos, este banco de dados foi projetado em conformidade com as regras de integridade referencial e normalização até a 3ª Forma Normal (3FN).

🎯 Principais Objetivos Alcançados:

Modelagem Relacional: Estruturação de entidades para gerenciar pacientes, médicos, quartos, internações, consultas e prescrições.

Integridade Referencial: Prevenção contra exclusões acidentais de históricos clínicos.

Relatórios de Negócio: Desenvolvimento de 15 consultas SQL estratégicas (DQL) para suporte a tomada de decisões da diretoria, finanças, recepção e auditoria.

🗂️ Estrutura do Banco de Dados

O esquema do banco de dados hospital_db é composto por 6 tabelas interligadas:

pacientes: Cadastro dos pacientes (CPF único, dados pessoais e convênio).

medicos: Registro dos profissionais de saúde (CRM único e especialidade).

quartos: Controle dos leitos, andares e tipos de acomodação.

internacoes: Registro de entrada/saída de pacientes nos quartos e valores de diária.

consultas: Agendamento e realização de consultas médicas.

prescricoes: Receituário de medicamentos associado às consultas realizadas.

📁 Estrutura do Repositório

.
├── 01_ddl_criar_banco.sql       # Script DDL (Criação do Schema e Tabelas)
├── 02_dml_popular_banco.sql     # Script DML (Inserção dos dados de teste)
├── 03_dql_consultas.sql         # Script DQL (As 15 consultas estratégicas)
└── README.md                    # Documentação do projeto



📊 Consultas Estratégicas (DQL)

O projeto inclui respostas SQL para 15 perguntas cruciais do negócio:

Relatório de Farmácia: Mapeamento de paciente, médico, data e medicação prescrita.

Auditoria de Internações: Histórico de acomodações, andares e valores de diárias.

Atendimentos na Recepção: Relação de convênios x médicos atendentes.

Coordenação Médica: Controle geral de prescrições emitidas por especialidade.

Cruzamento de Dados: Pacientes com histórico duplo (internação e consulta).

Histórico Geral de Consultas: Ordenação cronológica dos atendimentos mais recentes.

Análise Financeira de Diárias: Listagem ordenada do menor para o maior valor.

Média de Consultas: Indicador do ticket médio das consultas.

Faturamento de Consultas: Receita total obtida com consultas médicas.

Filtro de Pacientes: Busca específica para famílias selecionadas (ex: "Silva").

Filtro por Especialidade: Mapeamento de atendimentos em Cardiologia.

Relatório do 1º Semestre de 2026: Internações ocorridas entre 01/01/2026 e 30/06/2026.

Faturamento por Convênio: Total gasto por pacientes Unimed (ordenado por valor).

Custo por Andar: Levantamento agrupado de diárias por andar para famílias selecionadas (ex: "Oliveira").

Faturamento Cirúrgico: Receita agrupada de especialidades da área de Cirurgia.
