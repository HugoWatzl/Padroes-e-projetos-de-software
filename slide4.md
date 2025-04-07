# 🏗️ RUP (Rational Unified Process) 

## 💡 O que é RUP para leigos? 
**RUP** é uma forma organizada de criar software. Ele ajuda equipes a **planejar, desenvolver e entregar** sistemas com qualidade e segurança. **Divide o trabalho em fases** como construção civil (projeto → fundação → paredes → acabamento).

### Versão Simplificada (Para Todos)
1. **É um método passo-a-passo** para criar sistemas digitais
2. **Permite ajustes contínuos** através de versões intermediárias
3. Suas características principais : **Interativo e incremental**

## 🔄 As 4 Fases Essenciais
| Fase          | Objetivo                     | Duração   | 📊 Artefatos Típicos       |
|---------------|------------------------------|-----------|---------------------------|
| **Concepção** | Definir escopo e viabilidade | 1-3 semanas | Documento de Visão, Protótipos |
| **Elaboração**| Criar arquitetura estável    | 2-6 semanas | Diagramas UML, Plano Detalhado |
| **Construção**| Desenvolver componentes      | 3-12 meses | Código-fonte, Testes Automatizados |
| **Transição** | Implantar e ajustar          | 1-3 meses  | Manuais, Relatórios de Performance |

## ⚙️ 9 Disciplinas Principais
1. **Modelagem de Negócios** (Fluxogramas AS-IS)
2. **Requisitos** (Casos de Uso)
3. **Análise & Projeto** (Diagramas UML)
4. **Implementação** (Código)
5. **Testes** (Plano de Testes)
6. **Implantação** (Scripts de Deploy)
7. **Gerenciamento** (Cronogramas)
8. **Configuração** (Controle de Versões)
9. **Ambiente** (Ferramentas DevOps)

## ✅ Vantagens do RUP

- Permite identificar erros mais cedo.
- Flexível para mudanças durante o projeto.
- Entregas parciais e frequentes.
- Melhor comunicação com o cliente.



## ❌ Desvantagens

- Processo mais complexo e detalhado.
- Pode ser demorado.
- Não recomendado para projetos muito pequenos.

---
## ✅ **Características-Chave**

    A[Iterativo] --> B[Reduz riscos]
    C[Baseado em Casos de Uso] --> D[Alinhamento com negócio]
    E[Arquitetura-Cêntrico] --> F[Estabilidade técnica]
    G[Gestão de Riscos] --> H[Previsibilidade]
    
## Kahoot estudo
<P> https://create.kahoot.it/share/aula-3-processo-unificado-rup/04f76d12-5c5c-4848-9d98-36e6ac6313f4</P>

## 🤔 Quando usar?

> Use o RUP quando o projeto for **grande, complexo ou crítico**, e exigir **qualidade e controle rigoroso**.

##  Como Funciona na Prática?
- **Iterações**: Cada fase tem mini-ciclos (ex: 2 semanas de programação → teste → ajuste)
- **Disciplinas Paralelas**:
  -  Documentar requisitos 📝
  -  Programar funcionalidades 💻
  -  Testar continuamente
  -  Preparar a implantação

## 🛠️ Ferramentas Visuais (UML)
O RUP usa diagramas como:
```mermaid
graph TD
    A[Casos de Uso] --> B[Diagrama de Classes]
    B --> C[Fluxo do Sistema]
    C --> D[Testes]

