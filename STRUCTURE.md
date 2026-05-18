# 📁 Estrutura de Ficheiros

Guia rápido da organização do repositório.

---

## 🗂️ Diretório Principal

```
as-nossas-maravilhas-de-coimbra/
├── 📄 DOCUMENTAÇÃO GERAL
│   ├── README.md                    # Documentação principal
│   ├── PROJECT.md                   # Overview técnico
│   ├── ARCHITECTURE.md              # Estrutura modular
│   ├── DESIGN_SYSTEM.md             # Sistema de design
│   ├── DEPLOYMENT.md                # GitHub Pages
│   ├── GETTING_STARTED.md           # Início rápido
│   ├── SCREEN_TEMPLATES.md          # Templates
│   └── STRUCTURE.md                 # Este ficheiro
│
├── 🎬 FICHEIROS HTML (24 Screens)
│   ├── index.html                   # Screen 1: Landing
│   ├── screen2.html                 # Screen 2: Rota
│   ├── screen3.html                 # Screen 3: Guia - Escola Martim
│   ├── screen4.html                 # Screen 4: Guia - Penedo Saudade
│   ├── screen5.html                 # Screen 5: Guia - Jardim Botânico
│   └── ... (screen6 até screen24)   # Screens 6-24
│
├── 🎨 CSS - DESIGN SYSTEM
│   ├── components.css               # ⭐ CORE - CSS Variables + Componentes
│   ├── style.css                    # Estilos específicos Screen 1
│   ├── screen2.css                  # Estilos específicos Screen 2
│   ├── screen3.css                  # Estilos específicos Screen 3
│   ├── directions.css               # Estilos compartilhados (guias)
│   ├── info.css                     # Estilos compartilhados (info)
│   └── screenX.css                  # Estilos específicos (cada screen)
│
├── 🖼️ ASSETS
│   ├── Screens/
│   │   ├── screen1/                 # Imagens Screen 1
│   │   │   ├── polygon.png
│   │   │   ├── image1.png
│   │   │   ├── university.png
│   │   │   └── rectangle.png
│   │   ├── screen2/                 # Imagens Screen 2
│   │   │   ├── A nossa rota.png
│   │   │   ├── Rectangle 7.png ... Rectangle 19.png
│   │   │   └── Arrow 2.png ... Arrow 12.png
│   │   ├── screen3/                 # Imagens Screen 3
│   │   └── ... (screen4 até screen24)
│   │
│   └── icon.png                     # Favicon da app
│
├── 🔧 CONFIGURAÇÃO
│   ├── .github/
│   │   ├── CONTRIBUTING.md          # Diretrizes de contribuição
│   │   └── workflows/               # GitHub Actions (se houver)
│   │
│   ├── .gitignore                   # Ficheiros ignorados pelo Git
│   ├── README.md                    # README do .github
│   └── [config files]
│
├── 📚 DOCUMENTAÇÃO AUXILIAR
│   ├── orientation-files/
│   │   ├── README.md                # Documentação técnica
│   │   ├── SETUP.md                 # Setup detalhado
│   │   ├── COMPLETION.md            # Status do projeto
│   │   └── [histórico de versões]
│   │
│   ├── RESTRUCTURING_SUMMARY.md     # Histórico de refactoring
│   ├── SCREEN2_IMPLEMENTATION.md    # Exemplo Screen 2
│   ├── REORGANIZACAO_RESUMO.txt     # Histórico (texto)
│   └── ATUALIZACAO_GUIAS_GITHUB_PAGES.md
│
└── 🧪 TESTES
    └── test-responsive.html         # Página de teste responsivo
```

---

## 📊 Quantidade de Ficheiros

| Tipo | Quantidade | Total |
|------|-----------|-------|
| HTML Screens | 24 | 24 |
| CSS Principais | 1 (components.css) | 1 |
| CSS Específicos | ~6 | ~6 |
| Imagens | ~300+ | 300+ |
| Documentação | 7 | 7 |
| **TOTAL** | | **~350+** |

---

## 🔑 Ficheiros Críticos

### ⭐ CORE (não apague!)

```
✅ components.css           # Design system - OBRIGATÓRIO
✅ index.html               # Screen 1 - Landing
✅ screen2.html             # Screen 2 - Rota
✅ Screens/                 # Pasta com todas as imagens
✅ .gitignore              # Configuração Git
```

### ⚠️ Importante (não mude paths!)

```
✅ screenX.html            # Todos os screens (1-24)
✅ screenX.css             # Estilos específicos
✅ Screens/screenX/        # Imagens de cada screen
```

### 📚 Documentação (referência)

```
📖 README.md               # Sempre manter atualizado
📖 PROJECT.md              # Overview técnico
📖 ARCHITECTURE.md         # Para novos contributors
📖 DEPLOYMENT.md           # Para publish em GitHub Pages
```

### 🧹 Pode Limpar (opcional)

```
🗑️ test-responsive.html    # Apenas para testes
🗑️ orientation-files/      # Documentação interna
🗑️ RESTRUCTURING_SUMMARY.md # Histórico antigo
🗑️ reorganizar_novo.py     # Scripts internos
```

---

## 📏 Tamanho Típico

```
HTML files:        ~80KB    (24 ficheiros × ~3KB)
CSS files:         ~50KB    (7 ficheiros × ~7KB)
Imagens:          ~80MB    (300+ PNG files)
Documentação:     ~150KB    (8 ficheiros .md)
Configuração:     ~10KB     (.gitignore, etc)
─────────────────────────
TOTAL:            ~80MB
```

---

## 🔗 Relações entre Ficheiros

```
📱 SCREEN TÍPICA
  │
  ├─ screenX.html
  │  ├─ <link> components.css     ← Design system
  │  ├─ <link> screenX.css        ← Customizações
  │  ├─ <link> icon.png           ← Favicon
  │  └─ <img> Screens/screenX/    ← Imagens
  │
  └─ screenX.css
     └─ usa variáveis de components.css
        (--color-primary, --spacing-lg, etc)
```

---

## 📋 Checklist Antes de Commit

```
☑️ Ficheiros HTML válidos
   □ <title> presente e relevante
   □ <meta name="viewport"> correto
   □ Links CSS em ordem: components.css ANTES de screenX.css
   □ Imagens com alt text
   □ Paths relativos corretos: ./Screens/screenX/

☑️ Ficheiros CSS
   □ Usa CSS Variables (não hardcoded)
   □ Breakpoints responsivos definidos
   □ Sem erros de sintaxe

☑️ Imagens
   □ Estão em Screens/screenX/
   □ Nomes sem caracteres especiais
   □ Formato PNG (idealmente)
   □ Otimizadas (< 500KB cada)

☑️ Documentação
   □ README.md atualizado
   □ Comentários em código crítico
   □ Sem ficheiros .txt ou temporários
```

---

## 🚀 Deploy em GitHub Pages

### Ficheiros que precisam estar no repositório:

```
✅ Todos os .html files
✅ Todos os .css files
✅ Pasta Screens/ completa
✅ icon.png
✅ .gitignore
✅ README.md
✅ (Documentação .md)
```

### Ficheiros que NÃO precisam (para repo limpo):

```
❌ node_modules/
❌ .DS_Store (Mac)
❌ Thumbs.db (Windows)
❌ *.log files
❌ Ficheiros temporários
```

Estes ficam automaticamente ignorados pelo `.gitignore`.

---

## 📝 Adicionar Novo Screen

### Passo 1: Criar ficheiro HTML

```
1. Copiar screen2.html → screenN.html
2. Editar:
   - <title>
   - Links CSS (screenN.css)
   - Classes (screenN-*)
   - Conteúdo específico
```

### Passo 2: Criar pasta de assets

```
mkdir Screens/screenN
(copiar imagens para esta pasta)
```

### Passo 3: Criar ficheiro CSS

```
touch screenN.css
(adicionar customizações)
```

### Passo 4: Commit e push

```
git add .
git commit -m "Adicionar Screen N"
git push origin main
```

---

## 🔍 Encontrar Ficheiros Rapidamente

```bash
# Todos os HTML screens
ls *.html

# Todos os CSS files
ls *.css

# Todos os assets de um screen
ls Screens/screen2/

# Ficheiros modificados recentemente
git log --oneline -10

# Histórico de um ficheiro específico
git log --follow components.css
```

---

## 📞 Questões Comuns

### "Aonde estão as imagens?"
→ Pasta: `Screens/screenX/`

### "Qual é o ficheiro CSS principal?"
→ `components.css` (Design system)

### "Como adicionar novo screen?"
→ Ver secção "Adicionar Novo Screen" acima

### "Posso eliminar orientation-files?"
→ Sim, é documentação auxiliar (backup primeiro)

### "Por que 24 screens?"
→ 1 Landing + 1 Rota + 11 POIs × 2 = 24

---

**Versão**: 1.0  
**Data**: 2026-05-18  
**Status**: ✅ Documentação Estrutural Completa
