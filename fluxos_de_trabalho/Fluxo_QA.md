# ⚙️ **Automação de Fluxos E2E – Playwright**

---

## 📖 **Introdução**

Automatizar fluxos E2E (end-to-end) é essencial para garantir a qualidade e escalabilidade do sistema.
Este documento define o **padrão visual, técnico e de organização** para gravação, documentação e acompanhamento de testes E2E usando o Playwright.

---

## 🗂️ **Sumário**

1. [Visão Geral – Macrofluxo do Processo](#1-visão-geral--macrofluxo-do-processo)
2. [Checklist de Preparação](#2-checklist-de-preparação)
3. [Passo a Passo – Gravação de Fluxos (Playwright)](#3-passo-a-passo--gravação-de-fluxos-playwright)
4. [Template de Documentação dos Fluxos](#4-template-de-documentação-dos-fluxos)
5. [Exemplo de Preenchimento – Documentação Completa](#5-exemplo-de-preenchimento--documentação-completa)
6. [Dashboard de Status dos Fluxos](#6-dashboard-de-status-dos-fluxos)
7. [Dúvidas Frequentes – FAQ](#7-dúvidas-frequentes--faq)
8. [Considerações Finais](#8-considerações-finais)

---

## 1️⃣ **Visão Geral – Macrofluxo do Processo**

```ascii
╔════════════════════════════╗
║      Fluxo Global         ║
╚════════════════════════════╝
     ⬇️
[ 1. Gravação do Fluxo 🖱️ ]
     ⬇️
[ 2. Salvamento e Nomeação 💾 ]
     ⬇️
[ 3. Preenchimento do Template 📝 ]
     ⬇️
[ 4. Entrega para Revisão Técnica 🔍 ]
     ⬇️
[ 5. Transformação em Teste Automatizado 🤖 ]
     ⬇️
[ 6. Validação & Atualização do Dashboard ✅ ]
```

* Cada etapa é obrigatória para garantir rastreabilidade, clareza e padronização.

---

## 2️⃣ **Checklist de Preparação**

> 📋 **Antes de iniciar a gravação, confirme:**

* [ ] Acesso ao terminal (Windows, Mac ou Linux)
* [ ] Caminho da pasta onde os scripts serão salvos
* [ ] URL do sistema a ser testado
* [ ] Template de documentação disponível
* [ ] Local para salvar scripts e documentação
* [ ] Agenda e prioridades dos fluxos que serão gravados

---

## 3️⃣ **Passo a Passo – Gravação de Fluxos (Playwright)**

### 3.1. **Abertura do Terminal**

```ascii
╔════════════════════════════╗
║  Fluxo: Abrir o Terminal  ║
╚════════════════════════════╝
        ⬇️
[ Escolher Sistema Operacional ]
        ⬇️
┌─────────────┬──────────────┬────────────┐
│   Windows   │     Mac      │   Linux    │
├─────────────┼──────────────┼────────────┤
│ Win+R, cmd  │ Cmd+Space,   │ Menu Apps, │
│ ENTER       │ digite       │ procure    │
│             │ "Terminal"   │ "Terminal" │
└─────────────┴──────────────┴────────────┘
```

* **Dica:** É importante trabalhar sempre na mesma pasta, para centralizar todos os scripts gravados.

---

### 3.2. **Navegação pelo Terminal**

```ascii
╔══════════════════════════════════════╗
║  Fluxo: Navegar entre Pastas (cd)   ║
╚══════════════════════════════════════╝
        ⬇️
[ cd caminho/da/pasta ]
        ⬇️
[ cd .. ]   ← Volta um diretório
        ⬇️
[ dir ]     ← Lista arquivos (Windows)
[ ls ]      ← Lista arquivos (Mac/Linux)
```

* **Exemplo Windows:**
  `cd C:\Users\QA\Projetos\playwright-tests`
* **Exemplo Mac/Linux:**
  `cd /home/qa/playwright-tests`

---

### 3.3. **Início da Gravação**

```ascii
╔═════════════════════════════╗
║  Fluxo: Iniciar Gravação   ║
╚═════════════════════════════╝
        ⬇️
[ Confirmar pasta correta ]
        ⬇️
[ Executar comando Playwright ]
        ⬇️
npx playwright codegen https://enderecodomeusistema.com
        ⬇️
[ Abrir navegador automaticamente ]
```

* O comando deve ser executado sempre na pasta de scripts.

---

### 3.4. **Execução do Fluxo no Navegador**

```ascii
╔════════════════════════════════╗
║  Fluxo: Executar o Processo   ║
╚════════════════════════════════╝
        ⬇️
[ Navegador aberto pelo Playwright ]
        ⬇️
[ Realizar UM fluxo completo (ex: login) ]
        ⬇️
[ Não misturar fluxos na mesma gravação ]
```

* Manter o processo objetivo e direto.
* Se houver qualquer erro, reiniciar a gravação do fluxo.

---

### 3.5. **Finalização e Salvamento**

```ascii
╔═════════════════════════════════════╗
║  Fluxo: Exportar e Nomear Script   ║
╚═════════════════════════════════════╝
        ⬇️
[ Finalizar fluxo no navegador ]
        ⬇️
[ Exportar/Salvar script gerado ]
        ⬇️
[ Nomear como: login-basico.spec.ts ]
        ⬇️
[ Salvar na pasta padrão ]
```

* O nome do arquivo deve ser objetivo e refletir o fluxo gravado.

---

### 3.6. **Documentação do Fluxo**

```ascii
╔══════════════════════════════╗
║  Fluxo: Documentar o Script ║
╚══════════════════════════════╝
        ⬇️
[ Preencher template padrão ]
        ⬇️
[ Nome do Fluxo | Objetivo | Passos | Observações ]
        ⬇️
[ Salvar junto ao script ]
```

* Todo fluxo deve estar acompanhado do template preenchido (próxima seção).

---

### 3.7. **Entrega e Revisão**

```ascii
╔═════════════════════════════╗
║  Fluxo: Envio para Revisão ║
╚═════════════════════════════╝
        ⬇️
[ Enviar script + template ]
        ⬇️
[ Aguardar revisão técnica ]
        ⬇️
[ Só iniciar novo fluxo após retorno ]
```

---

## 4️⃣ **Template de Documentação dos Fluxos**

> 📝 **Template Padrão**
>
> Preencher todas as informações abaixo e anexar junto ao arquivo de script.

```markdown
---
Nome do Fluxo:
[Exemplo: Login Básico]

Objetivo do Fluxo:
[Descrever o objetivo principal do fluxo.]

Passos Executados:
1. [Listar cada etapa realizada.]
2. ...

Observações:
[Indicar erros, alertas, mensagens, comportamentos inesperados, etc.]
---
```

---

## 5️⃣ **Exemplo de Preenchimento – Documentação Completa**

```markdown
---
Nome do Fluxo:
Login Básico

Objetivo do Fluxo:
Verificar que o usuário consegue acessar o sistema utilizando credenciais válidas.

Passos Executados:
1. Acessar página de login (/login)
2. Preencher campo de usuário
3. Preencher campo de senha
4. Clicar em “Entrar”
5. Verificar acesso ao dashboard

Observações:
Fluxo executado conforme esperado. Não foram observados erros.
---
```

---

## 6️⃣ **Dashboard de Status dos Fluxos**

> 📊 **Controle e Visão Global**
>
> Utilize a tabela abaixo para acompanhar fluxos gravados, revisados e automatizados.

| Nome do Fluxo          | Objetivo                | Status  | Script                    | Última Revisão | Observações        |
| ---------------------- | ----------------------- | ------- | ------------------------- | -------------- | ------------------ |
| Login Básico           | Login no sistema        | Gravado | login-basico.spec.ts      | 2024-07-10     | OK                 |
| Criação de Ticket      | Abrir novo chamado      | Gravado | criar-ticket.spec.ts      | 2024-07-10     | OK                 |
| Visualização de Ticket | Ver detalhes do chamado | Gravado | visualizar-ticket.spec.ts | 2024-07-10     | Aguardando revisão |

---

## 7️⃣ **Dúvidas Frequentes – FAQ**

### ❓ Perguntas Comuns

* **É necessário saber programar?**
  Não. Basta seguir o passo a passo, preencher o template e realizar o fluxo como no uso normal do sistema.

* **Posso gravar vários fluxos juntos?**
  Não. O ideal é sempre um fluxo por gravação para garantir organização, clareza e facilidade de manutenção.

* **O que fazer se errar durante a gravação?**
  Recomenda-se reiniciar o processo do fluxo. Isso evita registros confusos ou etapas misturadas.

* **Como proceder em caso de dúvidas técnicas ou dificuldades?**
  Consultar o responsável técnico do projeto ou a equipe de suporte, conforme procedimentos internos.

---

## 8️⃣ **Considerações Finais**

> 💡 A automação estruturada de fluxos com Playwright traz benefícios diretos para qualidade, agilidade e segurança dos testes do sistema.
>
> * Documentar e organizar os fluxos facilita a evolução do projeto.
> * A rastreabilidade é ampliada, evitando retrabalho manual.
> * O alinhamento de toda a equipe reduz falhas e agiliza entregas.

**Este material deve ser revisado e atualizado sempre que houver mudanças no processo, para garantir as melhores práticas do time.**

---

## 🎨 **Resumo Visual – Jornada Completa**

```ascii
╔════════════════════════════════════════════════════════════════════════╗
║               JORNADA DE AUTOMAÇÃO DE FLUXOS E2E                    ║
╠═════════════════════╦════════════════╦════════════════╦══════════════╣
║  Gravação do Fluxo  ║  Documentação  ║  Revisão       ║  Automação   ║
╠═════════════════════╬════════════════╬════════════════╬══════════════╣
║ Playwright Codegen  ║ Template Padrão║ Técnico/Dev    ║ Teste E2E    ║
╠═════════════════════╬════════════════╬════════════════╬══════════════╣
║      🖱️             ║      📝         ║      🔍         ║     🤖       ║
╚═════════════════════╩════════════════╩════════════════╩══════════════╝
```

---

**FIM DO DOCUMENTO**

> Para sugestões, dúvidas ou atualização de etapas, entrar em contato com o responsável técnico do projeto.

---
