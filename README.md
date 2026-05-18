# 🏛️ As Nossas Maravilhas de Coimbra

> Uma aplicação web responsiva e interativa que celebra o patrimônio turístico de Coimbra.

## 📱 Sobre o Projeto

**Contexto:** 
_[Adicione aqui uma breve descrição do motivo e contexto da criação desta aplicação]_

---

Este projeto implementa uma aplicação web completamente responsiva com 24 ecrãs, mantendo 100% de fidelidade visual ao design original em todas as plataformas (desktop, tablet, mobile, landscape).

**Status**: ✅ 24 Screens Completos | ✅ Publicado em GitHub Pages | ✅ Pronto para Produção

## ✨ Características Principais

- ✅ **24 Screens Completos** - Toda a aplicação implementada
- ✅ **Arquitetura Modular** - Design system centralizado + estilos específicos por screen
- ✅ **Totalmente Responsivo** - Desktop, Tablet, Mobile (360px - 1920px), Landscape
- ✅ **Design Preservado** - Cores, textos, imagens e espaçamentos 100% fiéis ao design original
- ✅ **Cross-Browser** - Chrome, Firefox, Safari, Edge
- ✅ **Sem Dependências** - HTML5 + CSS3 puro (sem frameworks ou build tools)
- ✅ **Performance** - Otimizado para carregamento rápido
- ✅ **Notch/Safe Area** - Suporte para dispositivos com notch (iPhones X+)
- ✅ **CSS Variables** - Sistema de cores e tokens centralizado para manutenção fácil
- ✅ **Navegação Completa** - Fluxo entre todos os 24 ecrãs
- ✅ **GitHub Pages** - Hospedagem automática e gratuita

## 📊 Compatibilidade

| Dispositivo | Largura | Status |
|------------|---------|--------|
| Smartwatches | < 360px | ✅ Suportado |
| Phones | 360-480px | ✅ Otimizado |
| Tablets | 481-768px | ✅ Otimizado |
| Desktops | 769px+ | ✅ Otimizado |
| Landscape | Qualquer | ✅ Suportado |

## 🚀 Aceder à Aplicação

### 🌐 GitHub Pages (Recomendado - Online)
Aceda diretamente ao link do GitHub Pages:
```
https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/
```
**Nenhuma instalação necessária!** Apenas abra no navegador.

### 💻 Desenvolvimento Local (Para Editores)
Se quiser trabalhar no código ou contribuir:

**Python 3:**
```bash
python -m http.server 8000
# Aceda a http://localhost:8000
```

**Node.js:**
```bash
npx http-server
```

**VS Code Live Server:**
1. Instale extensão "Live Server"
2. Clique direito em index.html → "Open with Live Server"

👉 **[Ver Instruções Detalhadas](./GETTING_STARTED.md)**

## 📁 Estrutura do Projeto

```
as-nossas-maravilhas-de-coimbra/
├── 🎬 Ficheiros HTML (24 screens)
│   ├── index.html                   # Screen 1 - Landing
│   ├── screen2.html - screen24.html # Screens 2-24
│
├── 🎨 Design System
│   ├── components.css               # CORE - CSS Variables + Componentes
│   ├── style.css, screenX.css       # Estilos específicos
│
├── 🖼️ Assets
│   ├── Screens/screen1...screen24/  # Imagens de cada screen
│   └── icon.png                     # Favicon
│
└── 📚 Documentação
    ├── README.md                    # Documentação principal
    ├── PROJECT.md                   # Overview técnico
    ├── ARCHITECTURE.md              # Estrutura modular
    ├── STRUCTURE.md                 # Organização de ficheiros
    ├── DESIGN_SYSTEM.md             # Sistema de design
    ├── DEPLOYMENT.md                # GitHub Pages
    └── ...
```

👉 **[Ver estrutura completa](./STRUCTURE.md)**

## 🎨 Cores Principais

```
Coral/Peach (Primário):  #d9a48b
Coral/Peach (Escuro):    #d19478
Preto (Secundário):      #2a2a2a
Preto (Muito Escuro):    #1a1a1a
Branco (Neutral):        #ffffff
```

## 🔧 Tecnologias Utilizadas

- **HTML5**: Semântica e acessibilidade
- **CSS3**: Grid, Flexbox, Media Queries, CSS Variables
- **Vanilla JavaScript**: Sem dependências
- **PNG**: Imagens otimizadas

## 📚 Documentação

- **[PROJECT.md](./PROJECT.md)** - Overview do projeto (comece aqui!)
- **[STRUCTURE.md](./STRUCTURE.md)** - Organização de ficheiros
- **[ARCHITECTURE.md](./ARCHITECTURE.md)** - Estrutura modular
- **[DESIGN_SYSTEM.md](./DESIGN_SYSTEM.md)** - Sistema de design e componentes
- **[DEPLOYMENT.md](./DEPLOYMENT.md)** - GitHub Pages
- **[CHANGELOG.md](./CHANGELOG.md)** - Histórico de versões
- **[GETTING_STARTED.md](./GETTING_STARTED.md)** - Início rápido
- **[SCREEN_TEMPLATES.md](./SCREEN_TEMPLATES.md)** - Templates
- **[.github/CONTRIBUTING.md](./.github/CONTRIBUTING.md)** - Contribuições

## 🧪 Testes

### Chrome DevTools (Recomendado)
1. Abra index.html no Chrome
2. Pressione `F12` para DevTools
3. `Ctrl+Shift+M` para device emulation
4. Teste diferentes dispositivos

### Página de Teste Responsiva
```bash
# Abra test-responsive.html para visualizar múltiplos tamanhos
open test-responsive.html
```

## 📊 Screens Implementados

| Screen | Nome | Estado | Descrição |
|--------|------|--------|-----------|
| 1 | Tela Inicial | ✅ Completo | "As Nossas Maravilhas de Coimbra" - Landing page |
| 2 | A Nossa Rota | ✅ Completo | 11 pontos turísticos em rota linear |
| 3-24 | Guias Detalhados | ✅ Completo | Guias adicionais dos POIs |

**Total: 24 Screens | Status: ✅ 100% Implementado**

## 🔮 Roadmap

- [x] Screen 1 - Tela inicial (Completo)
- [x] Screen 2 - Rota linear (Completo)
- [x] Screens 3-24 - Guias e direções (Completo)
- [x] Navegação entre screens (Completo)
- [ ] Futuras melhorias (animações, interações)

## 🤝 Como Contribuir

Consulte [CONTRIBUTING.md](./.github/CONTRIBUTING.md) para:
- Diretrizes de código
- Padrão modular (components.css + screenX.css)
- Processo de pull requests
- Reporte de bugs
- Sugestões de melhorias

## 📞 Suporte

### Imagens não carregam?
- Verifique se `Screens/` existe
- Confirme paths: `./Screens/screenX/filename.png`
- Teste com servidor local

### Layout não responsivo?
- Limpe cache: `Ctrl+Shift+Delete`
- Abra em modo incógnito
- Teste em navegador moderno

### Mais ajuda?
- Verifique a console do navegador (`F12`)
- Leia [ARCHITECTURE.md](./ARCHITECTURE.md)
- Leia [DESIGN_SYSTEM.md](./DESIGN_SYSTEM.md)

## 📄 Licença

Este projeto é parte do portfólio educacional da Universidade de Coimbra.

---

**Versão**: 3.0  
**Data**: 2026-05-18  
**Status**: ✅ 24 Screens 100% Implementados | ✅ GitHub Pages Ativo | ✅ Produção  
**Desenvolvedor**: Pedro Vieira  
**Co-autoria**: Copilot

### 🔗 Links Rápidos
- 📖 [Arquitetura](./ARCHITECTURE.md)
- 🎨 [Design System](./DESIGN_SYSTEM.md)
- 🏗️ [Screen Templates](./SCREEN_TEMPLATES.md)
- 🚀 [Getting Started](./GETTING_STARTED.md)
- 🔧 [Documentação Técnica](./orientation-files/README.md)
- 🐛 [Reporte um Bug](./orientation-files/README.md#troubleshooting)
- 🎯 [Roadmap do Projeto](./README.md#-roadmap)
