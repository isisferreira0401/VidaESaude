# 🏥 Sistema de Gestão Hospitalar "Vida & Saúde"

Este repositório contém a modelagem e implementação do Banco de Dados Relacional para o **Hospital Geral Vida & Saúde**, desenvolvido como solução para a centralização, organização e análise dos dados operacionais da instituição.

---

## 📌 Sobre o Projeto

O Hospital Geral Vida & Saúde operava anteriormente utilizando registros manuais e planilhas isoladas, gerando problemas operacionais graves. Para sanar esses gargalos, este banco de dados foi projetado em conformidade com as regras de integridade referencial e normalização até a **3ª Forma Normal (3FN)**.

### 🎯 Principais Objetivos Alcançados:
- **Modelagem Relacional:** Estruturação de entidades para gerenciar pacientes, médicos, quartos, internações, consultas e prescrições.
- **Integridade Referencial:** Prevenção contra exclusões acidentais de históricos clínicos.
- **Relatórios de Negócio:** Desenvolvimento de 15 consultas SQL estratégicas (DQL) para suporte a tomada de decisões da diretoria, finanças, recepção e auditoria.

---

## 🗂️ Estrutura do Banco de Dados

O esquema do banco de dados `hospital_db` é composto por 6 tabelas interligadas:

1. **`pacientes`**: Cadastro dos pacientes (CPF único, dados pessoais e convênio).
2. **`medicos`**: Registro dos profissionais de saúde (CRM único e especialidade).
3. **`quartos`**: Controle dos leitos, andares e tipos de acomodação.
4. **`internacoes`**: Registro de entrada/saída de pacientes nos quartos e valores de diária.
5. **`consultas`**: Agendamento e realização de consultas médicas.
6. **`prescricoes`**: Receituário de medicamentos associado às consultas realizadas.

---

## 📁 Estrutura do Repositório

```text
.
├── 01_ddl_criar_banco.sql       # Script DDL (Criação do Schema e Tabelas)
├── 02_dml_popular_banco.sql     # Script DML (Inserção dos dados de teste)
├── 03_dql_consultas.sql         # Script DQL (As 15 consultas estratégicas)
└── README.md                    # Documentação do projeto
```

---

## 🚀 Como Executar o Projeto

### Pré-requisitos:
- [MySQL Server 8.0+](https://dev.mysql.com/downloads/mysql/) ou compatível.
- [MySQL Workbench](https://dev.mysql.com/downloads/workbench/) ou outro cliente SQL de sua preferência.

### Passo a Passo:

1. **Clonar o Repositório:**
   ```bash
   git clone https://github.com/SEU-USUARIO/sistema-gestao-hospitalar.git
   cd sistema-gestao-hospitalar
   ```

2. **Executar a Criação do Banco (DDL):**
   Abra e execute o arquivo `01_ddl_criar_banco.sql` no seu cliente MySQL.

3. **Inserir os Dados de Teste (DML):**
   Execute o arquivo `02_dml_popular_banco.sql` para povoar as tabelas.

4. **Executar as Consultas de Negócio (DQL):**
   Execute as queries contidas em `03_dql_consultas.sql` para gerar os relatórios estratégicos.

---

## 📊 Consultas Estratégicas (DQL)

O projeto inclui respostas SQL para 15 perguntas cruciais do negócio:

1. **Relatório de Farmácia:** Mapeamento de paciente, médico, data e medicação prescrita.
2. **Auditoria de Internações:** Histórico de acomodações, andares e valores de diárias.
3. **Atendimentos na Recepção:** Relação de convênios x médicos atendentes.
4. **Coordenação Médica:** Controle geral de prescrições emitidas por especialidade.
5. **Cruzamento de Dados:** Pacientes com histórico duplo (internação e consulta).
6. **Histórico Geral de Consultas:** Ordenação cronológica dos atendimentos mais recentes.
7. **Análise Financeira de Diárias:** Listagem ordenada do menor para o maior valor.
8. **Média de Consultas:** Indicador do ticket médio das consultas.
9. **Faturamento de Consultas:** Receita total obtida com consultas médicas.
10. **Filtro de Pacientes:** Busca específica para famílias selecionadas (ex: "Silva").
11. **Filtro por Especialidade:** Mapeamento de atendimentos em Cardiologia.
12. **Relatório do 1º Semestre de 2026:** Internações ocorridas entre 01/01/2026 e 30/06/2026.
13. **Faturamento por Convênio:** Total gasto por pacientes Unimed (ordenado por valor).
14. **Custo por Andar:** Levantamento agrupado de diárias por andar para famílias selecionadas (ex: "Oliveira").
15. **Faturamento Cirúrgico:** Receita agrupada de especialidades da área de Cirurgia.

---

## ✒️ Licença e Autoria

Projeto desenvolvido para validação técnica e ambiente de homologação do **Hospital Geral Vida & Saúde**.