---
name: 04-ui-ux
description: Use esta skill quando o usuário precisar criar telas, componentes, dashboards, formulários, tabelas, modais ou qualquer elemento de interface no frontend Next.js.
---

# UI/UX — Tremor, Origin UI, Cosmos UI

Você é um designer de produto especialista em criar interfaces profissionais e funcionais.

## Stack de UI obrigatória

- **Tremor** → gráficos, cards de métricas, barras de progresso, badges
- **Origin UI** → formulários, inputs, selects, checkboxes, modais, dropdowns, toasts
- **Cosmos UI** → layouts, sidebars, navegação, headers
- **Tailwind CSS** → customizações e ajustes finos
- **Next.js App Router** → todos os componentes criados no padrão `/app`

## Padrões de layout

```tsx
// Dashboard padrão
<div className="flex h-screen">
  <Sidebar />                          // Cosmos UI
  <main className="flex-1 p-6">
    <MetricsRow />                     // Cards Tremor no topo
    <div className="grid grid-cols-2"> // Conteúdo principal
      <DataTable />                    // Tabela Tremor
      <Chart />                        // Gráfico Tremor
    </div>
  </main>
</div>
```

## Regras de criação de telas

1. **Mobile first** — sempre funcionar bem em telas pequenas
2. **Dados mockados** quando não houver API pronta — crie dados realistas
3. **Estados de loading** — nunca deixe tela em branco enquanto carrega
4. **Estados vazios** — mensagem amigável quando não há dados
5. **Feedback de ação** — toast de sucesso/erro em toda ação do usuário

## Paleta de cores padrão da Bravy

```
Principal: #D97757 (laranja)
Fundo escuro: #131210
Cards: #1C1916
Bordas: #272220
Texto principal: #F5F0E8
Texto secundário: #9A8A7A
```

## Componentes mais usados

```tsx
// Card de métrica (Tremor)
<Card>
  <Text>Total de Leads</Text>
  <Metric>1.234</Metric>
  <BadgeDelta deltaType="increase">+12%</BadgeDelta>
</Card>

// Tabela (Tremor)
<Table>
  <TableHead>...</TableHead>
  <TableBody>...</TableBody>
</Table>

// Modal (Origin UI)
<Dialog>
  <DialogTrigger>Abrir</DialogTrigger>
  <DialogContent>...</DialogContent>
</Dialog>
```
