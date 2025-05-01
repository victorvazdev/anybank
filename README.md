# 🏦 AnyBank - Simulador de Contas Bancárias em Dart

**AnyBank** é um projeto em Dart que simula múltiplos tipos de contas bancárias com comportamentos distintos, utilizando conceitos de **programação orientada a objetos**, **herança**, **polimorfismo**, **mixins** e **encapsulamento**.

---

## 🚀 Funcionalidades

- 📌 **Conta Corrente**: permite envio com cheque especial (empréstimo).
- 💰 **Conta Poupança**: inclui cálculo de rendimento.
- 🏢 **Conta Salário**: permite depósitos com identificação do empregador.
- 🏭 **Conta Empresa**: aplica taxa sobre transações usando mixin `Imposto`.
- 📈 **Conta Investimento**: aplica taxa sobre recebimentos e envios.
- 📊 Exibe o saldo de forma formatada a cada operação.

---

## 🧱 Arquitetura
```
lib/
├── conta.dart                # Classe abstrata base
├── conta_corrente.dart       # Subclasse: Conta Corrente
├── conta_poupanca.dart       # Subclasse: Conta Poupança
├── conta_salario.dart        # Subclasse: Conta Salário
├── conta_empresa.dart        # Subclasse: Conta Empresa
├── conta_investimento.dart   # Subclasse: Conta Investimento
├── imposto.dart              # Mixin de taxa de imposto
bin/
└── main.dart                 # Ponto de entrada do app
```

---

## 📋 Exemplo de Uso

```dart
ContaCorrente contaChris = ContaCorrente('Chris', 4000);
contaChris.imprimeSaldo();
contaChris.enviar(4300); // Usa limite de empréstimo (300)

ContaPoupanca contaDenize = ContaPoupanca('Denize', 4000);
contaDenize.calculaRendimento(); // Aplica 5% de rendimento

ContaSalario contaCatarina = ContaSalario('Catarina', 5000, 'Empresa X', '101010101000110');
contaCatarina.depositar(15000); // Deposita com CNPJ do empregador

ContaEmpresa contaMatheus = ContaEmpresa('Matheus', 2000);
contaMatheus.enviar(1000); // Aplica taxa de 3%

ContaInvestimento contaRoberta = ContaInvestimento('Roberta', 2000);
contaRoberta.receber(1000); // Aplica taxa de 3%
```

---

## 🧠 Conceitos Utilizados
* **Classes abstratas** para padronizar contratos (Conta)
* **Herança** para reutilizar e estender comportamento
* **Mixins** (Imposto) para aplicar funcionalidades de forma modular
* **Encapsulamento** com atributos privados (_saldo)
* **Sobrescrita de métodos** (@override) para comportamento customizado

---

## Exemplo de Saída

<img width="719" alt="Exemplo de saída do Anybank" src="https://github.com/user-attachments/assets/5c47a137-ccf5-4a8d-8ae9-f5c43921063b" />
