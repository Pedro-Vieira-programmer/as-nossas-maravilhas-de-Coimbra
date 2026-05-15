# 🏛️ As Nossas Maravilhas de Coimbra

Uma aplicação web responsiva que transforma o design Figma em uma experiência digital imersiva dos pontos turísticos de Coimbra.

## 📱 Sobre o Projeto

Este projeto converte o design do Figma "As Nossas Maravilhas de Coimbra" numa aplicação web completamente responsiva, mantendo 100% de fidelidade visual ao design original em todas as plataformas (desktop, tablet, mobile).

**Status**: ✅ Screen 1 completo e responsivo | 📈 Escalável para 24 screens

## ✨ Características Principais

- ✅ **Totalmente Responsivo**: Desktop, Tablet, Mobile (360px - 1920px)
- ✅ **Mobile-First Design**: Otimizado para pequenos ecrãs com upgrade para grandes
- ✅ **Design Preservado**: Cores, textos, imagens e espaçamentos 100% fiéis
- ✅ **Cross-Browser**: Chrome, Firefox, Safari, Edge
- ✅ **Sem Dependências**: HTML5 + CSS3 puro (sem frameworks)
- ✅ **Performance**: Otimizado para carregamento rápido
- ✅ **Notch/Safe Area**: Suporte para dispositivos com notch (iPhones X+)

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
├── index.html                  # Ficheiro principal
├── style.css                   # Estilos responsivos
├── test-responsive.html        # Página de teste
│
├── Screens/
│   └── imagens/               # Assets do projeto
│       ├── polygon.png        # Decoração hexagonal
│       ├── image1.png         # Mapa de Coimbra
│       ├── university.png     # Foto da Universidade
│       └── rectange.png       # Fundo
│
├── orientation-files/          # Documentação
│   ├── README.md              # Docs técnicas
│   ├── SETUP.md               # Setup detalhado
│   ├── CHANGES.md             # Alterações
│   └── ...
│
├── .github/
│   └── CONTRIBUTING.md        # Diretrizes de contribuição
│
└── docs/                       # Documentação adicional
```

## 🎨 Cores Principais

```
Coral/Peach:        #d9a48b
Dark Text:          #1a1a1a
Light Gray:         #f5f5f5
White:              #ffffff
```

## 🔧 Tecnologias Utilizadas

- **HTML5**: Semântica e acessibilidade
- **CSS3**: Grid, Flexbox, Media Queries
- **Vanilla JavaScript**: Sem dependências
- **PNG**: Imagens otimizadas

## 📚 Documentação

- **[GETTING_STARTED.md](./GETTING_STARTED.md)** - Guia de início rápido
- **[orientation-files/README.md](./orientation-files/README.md)** - Documentação técnica
- **[orientation-files/SETUP.md](./orientation-files/SETUP.md)** - Setup e configuração
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

## 🔮 Roadmap

- [x] Screen 1 - Implementação inicial
- [ ] Screens 2-24 - Implementação em cadeia
- [ ] Navegação entre screens
- [ ] Animações e interações
- [ ] Backend (se necessário)

## 🤝 Como Contribuir

Consulte [CONTRIBUTING.md](./.github/CONTRIBUTING.md) para:
- Diretrizes de código
- Processo de pull requests
- Reporte de bugs
- Sugestões de melhorias

## 📞 Suporte

### Imagens não carregam?
- Verifique se `Screens/imagens/` existe
- Confirme paths: `./Screens/imagens/filename.png`
- Teste com servidor local

### Layout não responsivo?
- Limpe cache: `Ctrl+Shift+Delete`
- Abra em modo incógnito
- Teste em navegador moderno

### Mais ajuda?
- Verifique a console do navegador (`F12`)
- Leia [orientation-files/SETUP.md](./orientation-files/SETUP.md)

## 📄 Licença

Este projeto é parte do portfólio educacional da Universidade de Coimbra.

---

**Versão**: 2.0  
**Data**: 2026-05-13  
**Status**: ✅ Pronto para GitHub  
**Desenvolvedor**: Pedro Vieira

### 🔗 Links Rápidos
- 📖 [Documentação Completa](./orientation-files/README.md)
- ⚙️ [Setup e Configuração](./orientation-files/SETUP.md)
- 🐛 [Reporte um Bug](./orientation-files/README.md#troubleshooting)
- 🎯 [Roadmap do Projeto](./orientation-files/README.md)
