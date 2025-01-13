# Sistema Bancário Simples

## 📋 Descrição

Este projeto é um sistema bancário simples desenvolvido em Python. Ele permite gerenciar clientes, contas bancárias e realizar transações básicas, como depósitos, saques e exibição de extratos. Foi implementado com conceitos de Programação Orientada a Objetos (POO) e boas práticas de design, incluindo abstração, herança e polimorfismo.

---

## 🚀 Funcionalidades

- **Gerenciamento de Clientes**:
  - Cadastro de novos clientes.
  - Associação de contas bancárias a clientes existentes.

- **Gerenciamento de Contas**:
  - Criação de contas bancárias do tipo **Conta Corrente**.
  - Limite de saque diário configurável.
  - Histórico de transações.

- **Operações Bancárias**:
  - Depósitos.
  - Saques (com validação de saldo e limite).
  - Visualização do extrato com histórico de transações.

- **Outras Funções**:
  - Listagem de todas as contas registradas no sistema.

---

## 🛠️ Estrutura do Código

### **Principais Classes**

1. **`Cliente`**:
   - Classe base para representar um cliente genérico.
   - Atributos: `endereco` e `contas`.
   - Métodos:
     - `realizar_transacao`: Registra transações na conta associada.
     - `adicionar_conta`: Associa contas ao cliente.

2. **`PessoaFisica`**:
   - Subclasse de `Cliente` para representar pessoas físicas.
   - Atributos adicionais: `nome`, `data_nascimento`, `cpf`.

3. **`Conta`**:
   - Classe base para contas bancárias.
   - Atributos: `saldo`, `numero`, `agencia`, `cliente`, `historico`.
   - Métodos:
     - `sacar`: Realiza saques (valida saldo e valor).
     - `depositar`: Realiza depósitos.
   - Método de classe:
     - `nova_conta`: Cria uma nova conta.

4. **`ContaCorrente`**:
   - Subclasse de `Conta` para contas correntes.
   - Atributos adicionais: `limite`, `limite_saques`.
   - Sobrescreve o método `sacar` para incluir validações extras.

5. **`Historico`**:
   - Armazena o histórico de transações realizadas em uma conta.

6. **`Transacao`** (abstrata):
   - Define a interface para operações de transação.
   - Subclasses:
     - **`Saque`**: Representa operações de saque.
     - **`Deposito`**: Representa operações de depósito.

---

## 📋 Menu de Operações

O sistema oferece as seguintes opções por meio de um menu interativo:

- `[d]` Depositar
- `[s]` Sacar
- `[e]` Exibir Extrato
- `[nu]` Novo Usuário
- `[nc]` Nova Conta
- `[lc]` Listar Contas
- `[sair]` Sair do programa

---

## 📚 Exemplo de Uso

### **Fluxo de Cadastro e Transações**

1. **Cadastrar um novo cliente**:
   - Selecionar a opção `[nu]` no menu.
   - Informar CPF, nome, data de nascimento e endereço.

2. **Criar uma conta para o cliente**:
   - Selecionar a opção `[nc]`.
   - Informar o CPF do cliente previamente cadastrado.

3. **Realizar um depósito**:
   - Selecionar a opção `[d]`.
   - Informar o CPF do cliente e o valor do depósito.

4. **Realizar um saque**:
   - Selecionar a opção `[s]`.
   - Informar o CPF do cliente e o valor do saque (respeitando o saldo e limites).

5. **Exibir o extrato**:
   - Selecionar a opção `[e]`.
   - Informar o CPF do cliente para visualizar o histórico de transações e saldo.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem**: Python 3
- **Conceitos**:
  - Programação Orientada a Objetos (POO)
  - Abstração
  - Herança
  - Polimorfismo

---

## 📦 Como Executar

1. Certifique-se de ter o **Python 3** instalado em sua máquina.
2. Baixe ou clone este repositório.
3. Execute o arquivo `main.py` em um terminal ou IDE Python:
   ```bash
   python main.py
