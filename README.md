# 🏛️ As Nossas Maravilhas de Coimbra

Uma aplicação web responsiva que transforma o design Figma em uma experiência digital imersiva dos pontos turísticos de Coimbra.

## 📱 Sobre o Projeto

Este projeto converte o design do Figma "As Nossas Maravilhas de Coimbra" numa aplicação web completamente responsiva, mantendo 100% de fidelidade visual ao design original em todas as plataformas (desktop, tablet, mobile).

**Status**: ✅ Screen 1 (Tela Inicial) | ✅ Screen 2 (Rota) | ✅ Screen 3 (Guia) | 📈 Escalável para 24 screens

## ✨ Características Principais

- ✅ **Arquitetura Modular**: Design system centralizado + estilos específicos por screen
- ✅ **Totalmente Responsivo**: Desktop, Tablet, Mobile (360px - 1920px)
- ✅ **Mobile-First Design**: Otimizado para pequenos ecrãs com upgrade para grandes
- ✅ **Design Preservado**: Cores, textos, imagens e espaçamentos 100% fiéis
- ✅ **Cross-Browser**: Chrome, Firefox, Safari, Edge
- ✅ **Sem Dependências**: HTML5 + CSS3 puro (sem frameworks)
- ✅ **Performance**: Otimizado para carregamento rápido
- ✅ **Notch/Safe Area**: Suporte para dispositivos com notch (iPhones X+)
- ✅ **CSS Variables**: Sistema de cores e tokens centralizado

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
├── components.css               # DESIGN SYSTEM (CSS Variables + componentes reutilizáveis)
│
├── index.html                   # Screen 1 - Tela Inicial
├── style.css                    # Estilos específicos Screen 1
│
├── screen2.html                 # Screen 2 - Rota (11 pontos)
├── screen2.css                  # Estilos específicos Screen 2
│
├── screen3.html                 # Screen 3 - Guia de Direções
├── screen3.css                  # Estilos específicos Screen 3
│
├── test-responsive.html         # Página de teste responsivo
│
├── Screens/                     # Assets e recursos visuais
│   ├── screen1/                 # Imagens do Screen 1
│   ├── screen2/                 # Imagens do Screen 2 (rota)
│   ├── screen3/                 # Imagens do Screen 3 (guia)
│   └── screen4 até screen24/    # Pastas preparadas para futuros screens
│
├── orientation-files/           # Documentação auxiliar
│
└── .github/
    └── CONTRIBUTING.md          # Diretrizes de contribuição
```

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

- **[ARCHITECTURE.md](./ARCHITECTURE.md)** - Estrutura modular e como escalar para 24 screens
- **[DESIGN_SYSTEM.md](./DESIGN_SYSTEM.md)** - Sistema de design, componentes e CSS Variables
- **[SCREEN_TEMPLATES.md](./SCREEN_TEMPLATES.md)** - Template rápido para novos screens
- **[GETTING_STARTED.md](./GETTING_STARTED.md)** - Guia de início rápido
- **[orientation-files/README.md](./orientation-files/README.md)** - Documentação técnica
- **[.github/CONTRIBUTING.md](./.github/CONTRIBUTING.md)** - Como contribuir

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
| 3 | Guia de Direções | ✅ Completo | Guia com mapa e direções |
| 4-24 | Futuros | ⏳ Preparado | Pronto para implementação |

## 🔮 Roadmap

- [x] Screen 1 - Tela inicial (Completo)
- [x] Screen 2 - Rota linear (Completo)
- [x] Screen 3 - Guia de Direções (Completo)
- [ ] Screens 4-24 - Implementação em cadeia
- [ ] Navegação entre screens
- [ ] Animações e interações
- [ ] Backend (se necessário)

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

**Versão**: 2.2  
**Data**: 2026-05-17  
**Status**: ✅ Screens 1-3 implementados com padrão modular | 📈 Pronto para GitHub  
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
