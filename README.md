# 🍽️ RestERP - Sistema de Gestão para Restaurantes

> **MVP Operacional** - Salão, Atendimento e Caixa

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Status](https://img.shields.io/badge/Status-MVP%20v136-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Mobile%20First-blue)

---

## 📱 O que é RestERP?

RestERP é um sistema ERP modularizado e configurável especialmente desenvolvido para **restaurantes e lanchonetes**. 

Nosso MVP v136 está **100% operacional** e pronto para uso em produção com foco em:
- ✅ **Salão** - Abrir comandas, lançar itens
- ✅ **Atendimento** - Gerenciamento de marmitas com "Preparo Já"
- ✅ **Caixa** - Checkout e pagamento

---

## 🚀 Começar Agora

### Acesso Rápido (Teste Online)
```
URL: https://brunohenrike86-creator.github.io/resto-erp/
Login: bruno
Senha: 1986
```

### Usar Localmente
1. Clone o repositório:
```bash
git clone https://github.com/brunohenrike86-creator/resto-erp.git
cd resto-erp
```

2. Abra `index.html` no navegador:
```bash
# Com Python 3
python -m http.server 8000

# Ou abra direto: double-click em index.html
```

3. Acesse: `http://localhost:8000`

---

## ✨ Features MVP v136

### 👥 Gestão de Usuários
- ✅ Login com permissões (Admin/Atendente)
- ✅ Cadastro/Edição de usuários
- ✅ Reset de senha
- ✅ Usuário protegido: bruno/1986

### 🍛 Cardápio Completo
- ✅ 27 itens cadastrados (Buffet, Marmitex, Bebidas, Sobremesas)
- ✅ Filtros por categoria
- ✅ Edição de preços em tempo real

### 📋 Operações de Salão
- ✅ Abrir comanda
- ✅ Lançar itens (busca por código ou nome)
- ✅ Observações por item (carnes + notas especiais)
- ✅ Cálculo automático de totais
- ✅ Edição de itens lançados

### 🍛 Marmitas Inteligentes
- ✅ Modal de seleção de carnes
- ✅ Observações adicionais (opcional)
- ✅ **PREPARO JÁ** - Marmita em preparo antes do pagamento
- ✅ Carnes do dia (configuráveis por dia da semana)

### 👨‍🍳 Tela de Preparo
- ✅ Fila visual de marmitas
- ✅ Estados: Aguardando → Em Preparo → Concluído (piscando)
- ✅ Grid responsivo sem scroll
- ✅ True fullscreen
- ✅ Cards desaparecem após 1:30min automaticamente
- ✅ Exibe observações de carnes e notas especiais

### 💳 Checkout
- ✅ Listagem de comandas abertas
- ✅ Seleção de comanda
- ✅ Visualização de itens
- ✅ Processamento de pagamento
- ✅ Atalho rápido para checkout

### 📊 Dashboard
- ✅ Resumo do dia (Abertas, Em Preparo, Pagas)
- ✅ Ticket médio
- ✅ Total de vendas
- ✅ Contador de comandas com Preparo Já

### ⚙️ Administração
- ✅ Gerenciamento de itens do cardápio
- ✅ Gerenciamento de usuários
- ✅ Configuração de carnes do dia
- ✅ Filtros dinâmicos

---

## 🎮 Como Usar - Fluxo Completo

### Cenário: Cliente Come no Salão + Leva Marmita

```
1. ABRIR COMANDA
   - Ir em "Lançar"
   - Digitar número da comanda (ex: 1)
   - Sistema cria comanda nova

2. LANÇAR ITENS
   - Digite código do item (001 = Buffet Livre)
   - Quantidade automática = 1
   - Aparece na lista com preço

3. LANÇAR MARMITA
   - Digite: 004 (Marmitex P)
   - Abre modal "Escolha as Carnes"
   - Selecione: Frango e Carne
   - (Opcional) Adicione observação: "Sem molho"
   - (Opcional) Ative ⚡ PREPARO JÁ
   - Confirma → Comanda vai para "Em Preparo" ANTES de pagar!

4. VISUALIZAR PREPARAÇÃO
   - Ir em "Preparo"
   - Vê card da marmita: Marmitex P (Frango e Carne | Sem molho)
   - Clicar "👨‍🍳 INICIAR" → fica laranja
   - Clicar "✓ CONCLUÍDO" → fica verde piscando

5. CHECKOUT
   - Ir em "Checkout"
   - Vê comanda com badge "⚡ PREPARO JÁ" (border laranja)
   - Clica na comanda
   - Visualiza itens + observações
   - Clica "💳 PAGAR"
   - Sistema fecha comanda

6. PRONTO!
   - Comanda saiu de "Abertas"
   - Entrou em "Pagas"
   - Dashboard atualizado
```

---

## 📱 Tecnologia

### Stack
- **Frontend:** HTML5 + CSS3 + JavaScript Vanilla
- **Persistência:** localStorage (v136) → Google Sheets (v2.0)
- **Responsivo:** Mobile-first, compatível com tablet e desktop
- **Sem dependências:** Zero npm, zero build tools

### Navegadores Suportados
- ✅ Chrome/Edge (88+)
- ✅ Firefox (87+)
- ✅ Safari (14+)
- ✅ Mobile (iOS Safari, Chrome Android)

---

## 🗂️ Estrutura do Projeto

```
resto-erp/
├── index.html              # Aplicação completa (v136)
├── README.md              # Este arquivo
├── LICENSE                # Licença MIT
└── docs/
    ├── FEATURES.md        # Detalhes de cada feature
    ├── ROADMAP.md         # Plano de desenvolvimento
    └── INSTALACAO.md      # Guia de instalação
```

---

## 🎯 Roadmap v2.0+

### Próximas Fases
- 📦 **Fase 2:** Backend Google Sheets + Sincronização
- 🧩 **Fase 3:** Modularização + Sistema de configuração
- 🖥️ **Fase 4:** Responsividade desktop aprimorada
- 👨‍🍳 **Modulo Cozinha:** Fila avançada com tempos
- 📊 **Modulo Estoque:** Controle de ingredientes
- 🚚 **Modulo Delivery:** Integração com plataformas

---

## 🐛 Feedback & Testes

### Teste de Usabilidade
Este MVP está sendo testado com usuários reais. Se você encontrar bugs ou tiver sugestões:

1. **Abra uma Issue:** https://github.com/brunohenrike86-creator/resto-erp/issues
2. **Descreva o problema** com print/vídeo se possível
3. **Sugestões de melhoria** são bem-vindas!

### Dados de Teste
- Login: `bruno` / Senha: `1986`
- Comandas criadas são salvas localmente (reset ao limpar cache)
- Cardápio pré-carregado com 27 itens

---

## 📄 Licença

Este projeto está licenciado sob a **Licença MIT** - veja [LICENSE](LICENSE) para detalhes.

Você é livre para:
- ✅ Usar comercialmente
- ✅ Modificar
- ✅ Distribuir
- ✅ Usar privadamente

Apenas mantenha a menção de licença.

---

## 🤝 Contribuições

Contribuições são bem-vindas! Veja [CONTRIBUTING.md](CONTRIBUTING.md) para detalhes.

### Como Contribuir
1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/melhoria`)
3. Commit suas mudanças (`git commit -m 'Add: nova feature'`)
4. Push para a branch (`git push origin feature/melhoria`)
5. Abra um Pull Request

---

## 📞 Suporte

- 📧 **Issues:** https://github.com/brunohenrike86-creator/resto-erp/issues
- 💬 **Discussões:** https://github.com/brunohenrike86-creator/resto-erp/discussions
- 📱 **Compatibilidade:** Testado em Chrome, Firefox, Safari, Edge

---

## 🙏 Créditos

**Desenvolvido com ❤️ para restaurantes**

MVP v136 - Maio 2026

---

**[⬆ Voltar ao topo](#restenerp---sistema-de-gestão-para-restaurantes)**
