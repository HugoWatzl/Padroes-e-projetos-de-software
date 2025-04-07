# Engenharia de requisitos 

## 📌 Requisitos Funcionais (RF)

### Definição:
Descrevem **O QUE** o sistema deve fazer – as funcionalidades e interações com usuários ou outros sistemas.

### Como identificar?
Usam **verbos de ação**:  
> "O sistema deve [calcular, enviar, cadastrar, gerar]..."

Referem-se a **tarefas específicas**.

### Exemplos:
- "O sistema deve permitir login com e-mail e senha."
- "O usuário pode filtrar produtos por categoria."
- "O sistema deve emitir relatório financeiro mensal em PDF."

### Características:
✔️ São testáveis (ex.: "O login funciona?")  
✔️ Podem ser mapeados em casos de uso.

---

## 📌 Requisitos Não-Funcionais (RNF)

### Definição:
Definem **COMO** o sistema deve se comportar – restrições, qualidade e desempenho.

### Como identificar?
Usam **adjetivos ou métricas**:  
> "O sistema deve ser [rápido, seguro, compatível, disponível]..."

Referem-se a **atributos do sistema**.

### Exemplos:
- "O tempo de resposta deve ser ≤ 2 segundos para 1.000 usuários simultâneos."
- "Dados sensíveis devem ser criptografados com AES-256."
- "O sistema deve ter disponibilidade de 99,9% (24/7)."

### Categorias comuns (ISO 25010):
- Desempenho (velocidade, escalabilidade)  
- Segurança (criptografia, autenticação)  
- Usabilidade (acessibilidade, intuitividade)  
- Compatibilidade (integração com outros sistemas)

---

## 📊 Tabela Comparativa

| Critério          | Requisitos Funcionais         | Requisitos Não-Funcionais                 |
|-------------------|-------------------------------|-------------------------------------------|
| **Foco**          | Funcionalidades               | Qualidade / Restrições                    |
| **Exemplo**       | "Cadastrar usuário"           | "Cadastro em ≤ 3 segundos"                |
| **Base**          | Regras de negócio             | Normas técnicas (ex.: GDPR)               |
| **Mensuração**    | Teste funcional (passa/falha) | Métricas (ex.: tempo, % uptime)           |

---

## 🔍 Dicas Para Não Errar

### Pergunte "**O quê?**" vs "**Como?**"

- **"O sistema deve fazer X?"** → RF  
- **"O sistema deve ser Y?"** → RNF

### Use a fórmula:

**RF:**  
> "Como [ator], eu quero [ação] para [objetivo]."  
> _Exemplo: "Como cliente, eu quero filtrar produtos por preço para encontrar opções acessíveis."_

**RNF:**  
> "O sistema deve [atributo] sob [condição]."  
> _Exemplo: "O sistema deve responder em ≤ 1 segundo com 500 usuários online."_

### Cuidado com ambiguidades:

- ❌ "O sistema deve ser fácil de usar." (vago)  
- ✅ "Usuários completam cadastro em ≤ 2 minutos sem treinamento." (mensurável)

---
## 💡 Exemplo   (Sistema de E-commerce)

### RF:
- "Carrinho deve calcular total incluindo frete."
- "Usuário pode aplicar cupom de desconto."

### RNF:
- "Checkout seguro (SSL/TLS)."
- "Página carrega em ≤ 1.5s no mobile."

---

## ⚠️ Por Que São Importantes?

- **RF**: Garantem que o sistema faz o que os usuários precisam.  
- **RNF**: Determinam se o sistema será útil, rápido e confiável.

## 🔀 Qual a diferença entre requisitos funcionais e não-funcionais?


### *Funcionais*: descrevem o que o sistema deve fazer.

### *Não-funcionais*: descrevem como o sistema deve se comportar (desempenho, segurança, etc).

<br>

# 📝 Exercicio pratico!

## Sobre o sistema do mercadolivre identifique 10 requisitos funcionais presentes e 5 requisitos não-funcionais:

### Requisitos funcionais

1. O usuário pode acessar o site sem estar logado ;   
2. O usuário deve se cadastrar antes de efetuar uma compra ; 
3. O usuário pode adicionar produtos ao carrinho ;  
4. O usuário pode favoritar produtos ;  
5. O usuário pode aplicar cupons de desconto;   
6. O usuário pode pesquisar produtos na barra de pesquisa ;   
7. O sistema deve exibir na página inicial os itens mais vendidos ; 
8. O sistema deve recomendar itens baseados no histórico de interesse do usuário ;
9. O sistema deve exibir propagandas segmentadas ;  
10. O usuário pode filtrar produtos por categoriadurante a pesquisa.

### Requisitos não funcionais

1. O sistema deve garantir um meio de pagamento seguro, utilizando criptografia de dados (ex.: SSL/TLS) e autenticação ;
2.  O sistema deve realizar logout automático da conta do usuário após 48 horas de inatividade, visando segurança em ambiente na nuvem ;
3. O processo de compra deve ser intuitivo e ter tempo médio de resposta inferior a 2 segundos por etapa em 95% das interações dos usuários ;
4. O sistema deve apresentar tempo de resposta ≤ 2 segundos para 95% das buscas realizadas pelos usuários ;
5. O sistema de carregar os produtos em um tempo resposta ≤ 1.5 segundospara 95% das buscas realizadas pelos usuários .
