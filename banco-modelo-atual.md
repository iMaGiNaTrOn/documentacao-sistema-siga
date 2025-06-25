# Banco de Dados — Modelo Atual

## 🧩 Informações Gerais

- Nome do banco: `SIGA_unioeste`
- Sistema de gerenciamento: SQL Server
- Ferramenta usada para acesso: (X) SSMS  (X) DBeaver  ( ) Outro: __________

---

## 📑 Tabelas Atuais

### 1. Área
- **Descrição**: 
- **Colunas**:
  - `idarea`: bigint, PK, auto increment
  - `atualizadoem`: datetime2, permite nulo
  - `criadoem`: datetime2, permite nulo
  - `nome`: varchar(255), permite nulo
  - `oculta`: bit, permite nulo
  - `idunidade`:bigint, FK, permite nulo
- **Relacionamentos**:
  - Tem chave estrangeira? Qual?
    - idunidade
  - Relaciona-se com quais outras tabela?
    - Tem chave estrangeira de `unidade`, e sua chave primária em `chamado`, `serviço`, `área_operador` e `area_coordenador`.

### 1. Área do Coordenador
- **Descrição**: 
- **Colunas**:
  - `idarea`: bigint, PK, auto increment
  - `atualizadoem`: datetime2, permite nulo
  - `criadoem`: datetime2, permite nulo
  - `nome`: varchar(255), permite nulo
  - `oculta`: bit, permite nulo
  - `idunidade`:bigint, FK, permite nulo
- **Relacionamentos**:
  - Tem chave estrangeira? Qual?
    - idunidade
  - Relaciona-se com quais outras tabela?
    - Tem chave estrangeira de `unidade`, e sua chave primária em `chamado`, `serviço`, `área_operador` e `area_coordenador`.

---

## 🧪 Observações

- Tabelas que parecem estar **em desuso**:  
- Tabelas que estão sendo **utilizadas pelo backend**:
- Tabelas que precisam de **ajuste ou recriação**:
