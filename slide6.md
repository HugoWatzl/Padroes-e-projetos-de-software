# Casos de uso e Histórias de Usuário

## 🔷 O QUE SÃO?

| Conceito             | Explicação Rápida                                                                 |
|----------------------|-----------------------------------------------------------------------------------|
| **Caso de Uso**       | Descreve **como o sistema se comporta** em situações específicas, passo a passo. |
| **História de Usuário** | Descreve **o que o usuário deseja** e **por quê**, de forma curta e simples.       |

---

## 📦 CASO DE USO (Use Case - UC)

📌 **Formato Detalhado**  
Usado para **explicar passo a passo** como o sistema e o usuário interagem.

### 🧩 Componentes principais:
- **Ator**: Quem usa o sistema (ex: cliente, funcionário).
- **Fluxo Principal**: Caminho normal das ações.
- **Fluxo Alternativo**: O que acontece se der erro.
- **Pré-condição**: O que deve existir antes.
- **Pós-condição**: O que acontece depois.

### 📘 Exemplo – Sistema de Hotel
**UC: Reservar Quarto**  
**Ator:** Cliente  
**Fluxo Principal:**
1. Cliente seleciona datas  
2. Sistema verifica disponibilidade  
3. Cliente confirma reserva  

**Fluxo Alternativo:**  
3a. Quarto indisponível → sistema sugere outras datas

✅ **Bom para:** Projetos mais complexos ou documentações detalhadas.

<br>

## ✅ Relação «include»

### 📌 Definição:
Indica que um **caso de uso SEMPRE inclui o comportamento de outro**.  
Ou seja, o caso de uso principal **depende** do outro para funcionar.

### 💡 Quando usar:
Use «include» quando **vários casos de uso compartilham a mesma funcionalidade**.  
Ajuda a **evitar repetição** e a manter o sistema modular.

### 📍 Exemplo:
Em um sistema bancário:
- "Sacar Dinheiro" inclui "Autenticar Cliente"
- "Depositar Dinheiro" também inclui "Autenticar Cliente"

🔁 *Ou seja: a autenticação é necessária em ambos, e por isso é incluída.*

---

## ✅ Relação «extend»

### 📌 Definição:
Indica que um caso de uso pode **adicionar comportamento OPCIONAL a outro**, **sob certas condições**.

### 💡 Quando usar:
Use «extend» para funcionalidades **que só ocorrem às vezes**, dependendo de uma escolha ou situação.

### 📍 Exemplo:
Em um sistema bancário:
- "Visualizar Saldo" pode ser estendido por "Imprimir Extrato"
  - Apenas se o cliente quiser imprimir

📎 *Ou seja: "Imprimir Extrato" é um extra que não é sempre executado.*

---

## 📺 Vídeo recomendado:
**Título:** Include e Extend em Diagramas de Casos de Uso  
🎥 [Video explicando](https://www.youtube.com/watch?v=LGkzco2pfyc)

---

## Diagrama de Casos de Uso de um sistema de Loja Online (E-commerce)

```pgsql
 
                    <<include>>             <<include>>
[Cliente] ─────> (Finalizar Compra) ─────> (Confirmar Endereço)
                                │
                                └─────> (Selecionar Forma de Pagamento)
                                │
                  <<extend>>   │        <<extend>>
                      └──────> (Aplicar Cupom de Desconto)
                      └──────> (Escolher Presente)

[Cliente] ──> (Visualizar Produtos)
      │         │
      │         └──> (Adicionar ao Carrinho) ───> (Visualizar Carrinho)
      │
      └──> (Cadastrar-se)
      └──> (Fazer Login)
      └──> (Receber Confirmação de Pedido)

[Administrador] ──> (Login como Administrador)
        │
        ├──> (Cadastrar Produto)
        ├──> (Editar Produto)
        ├──> (Remover Produto)
        ├──> (Visualizar Pedidos)
        └──> (Atualizar Status do Pedido)

```
<br>
---

## 📌 HISTÓRIA DE USUÁRIO (User Story)

 **Formato Simples e Rápido**  
Foco na **necessidade e valor para o usuário**, usado em métodos ágeis como Scrum.

### 🧩 Estrutura:
> **Como** [tipo de usuário], **quero** [ação] **para** [objetivo].

###  Critérios de Aceitação:
- Regras que precisam ser atendidas para considerar a entrega pronta/testável.

### 📘 Exemplo – Sistema de Consultório
**História:**  
> Como dentista, quero visualizar minha agenda para gerenciar meu tempo.

**Critérios de Aceitação:**
1. Consultas listadas por horário  
2. Consultas urgentes destacadas em vermelho

✅ **Bom para:** Projetos ágeis, comunicação rápida e focada em valor.

---

## 📊 TABELA COMPARATIVA

| Critério              | Casos de Uso                           | Histórias de Usuário                       |
|-----------------------|----------------------------------------|--------------------------------------------|
| **Formato**           | Narrativa passo a passo (detalhado)    | Frase curta + critérios de aceitação       |
| **Foco**              | Comportamento do sistema               | Desejo/necessidade do usuário              |
| **Detalhamento**      | Alto (fluxos, exceções, condições)     | Baixo (ideia geral + validação simples)    |
| **Usado em**          | Engenharia tradicional (UML)           | Metodologias ágeis (Scrum, Kanban)         |
| **Exemplo**           | "Sistema verifica cartão e valida..."  | "Como usuário, quero fazer login..."       |

---

## 🧠 DICA DE MEMORIZAÇÃO

| Tipo              | Pense em...                                |
|-------------------|---------------------------------------------|
| **Caso de Uso**   | Roteiro de teatro com todos os passos       |
| **História de Usuário** | Anotação no post-it de um desejo          |

---
# Exercícios:

## 📝 Exercício – Caso de Uso


### Uma plataforma de streaming deseja permitir que usuários assistam a filmes online. Para isso, o usuário deve estar logado no sistema, escolher um filme disponível e clicar no botão "Assistir". Se o usuário não estiver logado, será redirecionado para a tela de login.

---

 *Gabarito* : 

### Caso de Uso: Assistir Filme/Série

- **👤 Ator Principal:** Usuário

---

### 📋 Fluxo Principal:

1. Usuário acessa a plataforma já logado.  
2. Usuário navega pelo catálogo e seleciona um filme ou série disponível.  
3. Usuário clica no botão “Assistir”.  
4. Sistema carrega o conteúdo.  
5. Filme/Série começa a ser exibido para o usuário.  

---

### ⚠️ Fluxos Alternativos:

- **Usuário não está logado:**  
  → Sistema redireciona para a tela de login.

- **Pagamento pendente:**  
  → Sistema exibe mensagem de bloqueio e redireciona o usuário para a tela de mensalidade.

- **Sem conexão com a internet:**  
  → Usuário não consegue realizar login e o sistema exibe mensagem de erro.



## 📚 História de Usuário – Assistir Filme

### 📖 História:
**Como** usuário da plataforma de streaming, **quero** assistir a filmes e séries online,  **para** aproveitar meu tempo livre com entretenimento.

---

### ✅ Critérios de Aceitação:

1. O sistema deve permitir assistir ao conteúdo apenas se o usuário estiver logado.
2. O conteúdo deve começar a ser exibido em até 5 segundos após clicar em "Assistir".
3. Caso o pagamento esteja pendente, o sistema deve bloquear o acesso e mostrar uma mensagem com opção de regularizar.
4. Se o usuário estiver sem conexão, uma mensagem de erro deve ser exibida impedindo o acesso.


## ✅ Relação «include»

### 📌 Definição:
Indica que um **caso de uso SEMPRE inclui o comportamento de outro**.  
Ou seja, o caso de uso principal **depende** do outro para funcionar.

### 💡 Quando usar:
Use «include» quando **vários casos de uso compartilham a mesma funcionalidade**.  
Ajuda a **evitar repetição** e a manter o sistema modular.

### 📍 Exemplo:
Em um sistema bancário:
- "Sacar Dinheiro" inclui "Autenticar Cliente"
- "Depositar Dinheiro" também inclui "Autenticar Cliente"

🔁 *Ou seja: a autenticação é necessária em ambos, e por isso é incluída.*


