# Projeto Conta Bancária - TypeScript

<br />

<div align="center">
   <img src="https://i.imgur.com/izFuHID.png" title="source: imgur.com" width="25%"/>
</div>

<br /><br />

## 1. Descrição


O **Projeto Conta Bancária** é um sistema de gestão projetado para simular e gerenciar operações financeiras relacionadas a contas bancárias. Ele oferece funcionalidades como criação, consulta, edição e exclusão de contas, além de transações como depósitos, saques e transferências.

O sistema organiza as informações dos clientes, incluindo nome, número da conta, saldo, entre outras, garantindo a realização de operações de forma segura e eficiente. Seu principal objetivo é automatizar e simplificar a administração de contas bancárias, categorizadas por tipo e finalidade, como Conta Corrente e Conta Poupança, promovendo eficiência e confiabilidade em ambientes financeiros.

Este projeto, desenvolvido em TypeScript, foca no estudo e aplicação de conceitos de **Programação Orientada a Objetos (POO)**, incluindo:

- Classes e Objetos;
- Atributos e Métodos;
- Modificadores de Acesso;
- Herança e Polimorfismo;
- Classes Abstratas;
- Interfaces.

Além de servir como um simulador funcional, o projeto oferece uma base prática para compreender princípios fundamentais da POO aplicados em um cenário realista.

<br />

## 2. Diagrama de Classes



Um **Diagrama de Classes** é um modelo visual usado na programação orientada a objetos para representar a estrutura de um sistema. Ele exibe classes, seus atributos, métodos e os relacionamentos entre elas, como associações, heranças e dependências. Esse diagrama ajuda a planejar e entender a arquitetura do sistema, mostrando como os componentes interagem e se conectam. É amplamente utilizado em fases de design e documentação de projetos. Abaixo, você confere o Diagrama de Classes contendo o modelo de dados do Projeto Conta Bancária:

```mermaid
classDiagram
class Conta {
  - _numero: number
  - _agencia: number
  - _tipo: number
  - _titular: string
  - _saldo: number
  + get numero() number
  + get agencia() number
  + get tipo() number
  + get titular() string
  + get saldo() number
  + set numero(numero: number) void
  + set agencia(agencia: number) void
  + set tipo(tipo: number) void
  + set titular(titular: string) void
  + set saldo(saldo: number) void
  + sacar(valor: number) boolean
  + depositar(valor: number) void
  + visualizar() void
}
class ContaCorrente {
  - _limite: number
  + get limite() number
  + set limite(limite: number) void
  + sacar(valor: number) boolean
  + visualizar() void
}
class ContaPoupanca {
  - _aniversario: number
  + get aniversario() number
  + set aniversario(aniversario: number) void
  + visualizar() void
}
ContaCorrente --> Conta
ContaPoupanca --> Conta
```

<br />

## 3. Tecnologias utilizadas

- Node.js v16+ ou superior
- TypeScript v5+ ou superior

<br />

## 4. Instalação
1. Clone este repositório:
   ```bash
   git clone https://github.com/rafaelq80/conta_bancaria_tjs06.git
   ```

2. Acesse a pasta do projeto:
   ```bash
   cd conta_bancaria_tjs06
   ```

3. Instale as dependências:
   ```bash
   npm install
   ```

<br />

## 5. Como Executar

1. Execute o projeto:
   ```bash
   ts-node Menu.ts
   ```
   

<br />

## 6. Funcionalidades

### 1. Criação de Conta
Permite criar uma nova conta bancária especificando nome do titular, número da agência, número da conta e saldo inicial, al´me das propriedades específicas de cada tipo de conta.

### 2. Listagem de Contas
Lista todas as contas cadastradas no sistema.

### 3. Consulta de Conta

- Por número: Encontra uma conta pelo número.
- Por nome: Encontra uma ou mais contas associadas a um titular.

### 4. Edição de Conta
Permite atualizar os dados de uma conta existente a partir do número da conta.

### 5. Exclusão de Conta
Remove uma conta especifica a partir do número da conta.

### 6. Saque
Realiza a retirada de um valor de uma conta, desde que o saldo seja suficiente.

### 7. Depósito
Adiciona um valor ao saldo de uma conta existente.

### 8. Transferência
Transfere um valor de uma conta para outra, respeitando os saldos e limites.

<br />

## 7. Tela Inicial do Sistema



<div align="center">
   <img src="https://i.imgur.com/MFK9yXB.png" title="source: imgur.com" width="90%"/>
</div>
