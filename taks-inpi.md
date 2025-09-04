# 🧠 SPRINT - Interface de Busca Inteligente de Processos

> Stack: Angular + Tailwind CSS  
> Status inicial: Projeto já configurado.

---

## 🗂️ Epics

- **E1. Tela de seleção de processos**
- **E2. Tela de critérios de busca e execução**
- **E3. Tela de exibição de resultados**
- **E4. Integrações e lógica de fluxo**

---

## ✅ TO DO

### 📦 E1: Seleção de processos (modal)

- [ ] Criar componente `ProcessoSelectorModalComponent`
- [ ] Implementar tabela com colunas: Processo, Marca, Titular, Último Evento, Situação
- [ ] Implementar checkbox por linha e “Selecionar todos”
- [ ] Implementar botão **"Carregar dados dos processos (0)"** com contador dinâmico
- [ ] Implementar botão **Cancelar** (fecha modal)
- [ ] Criar serviço mockado para simular o carregamento dos dados dos processos selecionados

---

### 📦 E2: Tela principal de busca inteligente

- [ ] Criar layout com abas “Nominativa” e “Figurativa”
- [ ] Implementar seletor de processo no topo (estilo tab com botão “Adicionar processo”)
- [ ] Criar seção "Dados do processo" com dados do titular, marca, classe etc.
- [ ] Criar formulário lateral com critérios de busca:
  - Classe de Nice
  - Edição
  - Elementos Nominativos (1° e 2°)
- [ ] Criar componentes reutilizáveis:
  - Campo com Select
  - Campo de texto com autocomplete
- [ ] Implementar botão **Executar busca**

---

### 📦 E3: Tela de resultados de busca

- [ ] Criar tabela de resultados com colunas:
  - Processo
  - Similaridade (com cor por nível)
  - Depósito
  - Marca
  - Classe
  - Proprietário
  - Situação
- [ ] Implementar paginação no rodapé (com navegação por páginas)
- [ ] Adicionar botão **Enviar selecionados para Anterioridades**
- [ ] Adicionar checkbox “Selecionar tudo” para os resultados
- [ ] Implementar filtro dropdown “Todas as situações”

---

### 📦 E4: Integração e lógica de fluxo

- [ ] Implementar serviço para simular busca de processos com base nos critérios (mock JSON)
- [ ] Vincular fluxo:
  - Selecionar processos → abrir aba de busca → preencher dados
- [ ] Garantir persistência de dados ao trocar entre abas Nominativa/Figurativa
- [ ] Implementar estados de loading e “nenhum resultado encontrado”
- [ ] Criar feedback visual para similaridade:
  - Muito semelhante (>70%)
  - Parcialmente semelhante (~69%)
  - Pouco semelhante (<20%)

---

## 🚧 IN PROGRESS

*(Atualizar conforme andamento do time.)*

---

## 🏁 DONE

*(Mover as tasks finalizadas para esta seção.)*

---

## 🎨 Sugestões de Estilo com Tailwind

### 🎯 Badges de Similaridade

| Faixa             | Texto                | Classe Tailwind                |
|------------------|----------------------|--------------------------------|
| > 70%            | Muito semelhante     | `text-red-600 bg-red-100`     |
| 21% ~ 69%        | Parcialmente Semelhante     | `text-yellow-600 bg-yellow-100`|
| < 20%            | Pouco semelhante    | `text-green-600 bg-green-100` |

---

### 🎯 Layout e Componentes

- Grid principal: `grid-cols-[auto_1fr_auto]`
- Modal: `fixed inset-0 flex items-center justify-center bg-black/50`
- Tabelas: `divide-y divide-gray-200 text-sm text-gray-800`
- Abas: `flex border-b font-medium text-blue-700`

