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
    - `idunidade`
  - Relaciona-se com quais outras tabela?
    - Tem chave estrangeira de `unidade`, e sua chave primária em `chamado`, `serviço`, `área_operador` e `area_coordenador`.

### 2. Coordenador de Área

- **Descrição**: Descreve qual usuário é considerado coordenador de qual área, e quando sua designação começa e termina, ou começou e terminará.
- **Colunas**:
  - `idarea`: bigint, FK, não nulo
  - `idusuario`: bigint, FK, não nulo
  - `datainiciodesignacao`: datetime2, permite nulo
  - `datafimdesignacao`: datetime2, permite nulo
- **Relacionamentos**:
  - Tem chave estrangeira? Qual?
    - `idarea` e `idusuario`
  - Relaciona-se com quais outras tabela?
    - Tem chave estrangeira de `idarea` e `idusuario`

### 3. Atualização de Sistema

- **Descrição**: Descreve sobre as atualizações do sistema, com suas datas de lançamento, descrição e versão. Tabela independente, agindo em função da manutenabilidade.
- **Colunas**:
  - `idatualizacaosistema`: bigint, PK, não nulo
  - `atualizadoem`: datetime2, permite nulo
  - `criadoem`: datetime2, permite nulo
  - `data`: datetime2, permite nulo
  - `descricao`: nvarchar(MAX), permite nulo
  - `versao`: varchar(255), permite nulo
- **Relacionamentos**:
  - Tem chave estrangeira? Qual?
    - Não.
  - Relaciona-se com quais outras tabela?
    - Não se relaciona com outras tabelas.
  
---

## 🧪 Observações

- Tabelas que parecem estar **em desuso**:  
- Tabelas que estão sendo **utilizadas pelo backend**:
- Tabelas que precisam de **ajuste ou recriação**:
