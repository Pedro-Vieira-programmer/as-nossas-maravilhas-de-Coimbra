# 🏗️ Arquitetura - Padrão Modular

Documento explicando a arquitetura modular do projeto e como escalar para 24 screens.

## 📋 Visão Geral

Este projeto implementa um **sistema modular centralizado** onde:

1. **`components.css`** - Design system único com CSS Variables (cores, espaçamento, tipografia)
2. **`screenX.html`** - HTML específico de cada screen
3. **`screenX.css`** - Estilos customizados para cada screen

**Benefício**: Alterar uma cor em `components.css` afeta **todos os 24 screens** automaticamente.

---

## 🎯 Estrutura Base

### Ficheiro 1: components.css (Design System - Obrigatório)

Define todas as **variáveis CSS e componentes reutilizáveis**:

```css
:root {
    /* Cores */
    --color-primary: #d9a48b;
    --color-secondary: #2a2a2a;
    /* ... mais variáveis ... */
}

/* Componentes reutilizáveis */
.route-container { }
.app-header { }
.app-content { }
.app-footer { }
.btn { }
/* ... etc */
```

### Ficheiro 2: screenX.html (Estrutura Específica)

Cada screen tem seu próprio HTML com a mesma **estrutura base**:

```html
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>[TÍTULO DO SCREEN]</title>
    
    <!-- IMPORTANTE: Sempre incluir components.css PRIMEIRO -->
    <link rel="stylesheet" href="components.css">
    <link rel="stylesheet" href="screenX.css">
</head>
<body>
    <!-- Para layouts tipo Screen 2 (com header/content/footer) -->
    <div class="route-container">
        <header class="app-header app-header--with-image">
            <!-- ... conteúdo ... -->
        </header>
        <main class="app-content app-content--scrollable">
            <!-- ... conteúdo ... -->
        </main>
        <footer class="app-footer">
            <!-- ... conteúdo ... -->
        </footer>
    </div>
    
    <!-- OU para layouts custom (tipo Screen 1) -->
    <main class="screen1-container">
        <!-- ... conteúdo customizado ... -->
    </main>
</body>
</html>
```

### Ficheiro 3: screenX.css (Customizações)

Contém **apenas os estilos específicos** do screen. Reutiliza componentes de `components.css`:

```css
/* ============================================
   SCREEN X - [DESCRIÇÃO]
   ============================================ */

/* Customizações específicas deste screen */
.screenX-title {
    color: var(--color-primary);
    font-size: var(--font-size-lg);
}

/* Responsive overrides */
@media (max-width: 479px) {
    .screenX-title {
        font-size: var(--font-size-md);
    }
}
```

---

## 📱 Padrões de Layout Implementados

### Padrão 1: Screen 2, 3 (Com Header/Content/Footer)

Ideal para screens com estrutura vertical clara:

```
┌─────────────────────┐
│  APP HEADER         │ (components.css)
├─────────────────────┤
│                     │
│  APP CONTENT        │ (scrollável, components.css)
│  (scrollable)       │
│                     │
├─────────────────────┤
│  APP FOOTER         │ (components.css)
└─────────────────────┘
```

**Ficheiros necessários:**
- `screenX.html` (estrutura simples)
- `screenX.css` (customizações mínimas)
- `components.css` (obrigatório)

### Padrão 2: Screen 1 (Layout Custom)

Para screens com layouts únicos e complexos:

```
┌─────────────────────┐
│  Hexagon    Map     │
│  (custom layout)    │
│      Title          │
│    University       │
│    Button           │
└─────────────────────┘
```

**Ficheiros necessários:**
- `index.html` (com estrutura própria: `.screen1-container`)
- `style.css` (estilos customizados)
- `components.css` (para CSS Variables)

---

## 📂 Estrutura de Ficheiros

```
as-nossas-maravilhas-de-coimbra/
├── components.css                    # ⭐ CORE - Design System
│
├── index.html  + style.css           # Screen 1 (Layout custom)
├── screen2.html + screen2.css        # Screen 2 (Padrão)
├── screen3.html + screen3.css        # Screen 3 (Padrão)
├── screen4.html + screen4.css        # Screen 4 (Padrão)
│   ... (até screen24)
│
├── Screens/
│   ├── screen1/
│   ├── screen2/
│   ├── screen3/
│   └── ... (screen4 até screen24)
│
└── Documentação/
    ├── ARCHITECTURE.md   (este ficheiro)
    ├── DESIGN_SYSTEM.md
    ├── SCREEN_TEMPLATES.md
    └── ...
```

---

## 🎨 CSS Variables (Design Tokens)

### Como Funcionam

Todas as cores, tamanhos e espaçamentos são **variáveis CSS** definidas em `components.css`:

```css
:root {
    /* Cores */
    --color-primary: #d9a48b;
    --color-text: #1a1a1a;
    
    /* Espaçamento */
    --spacing-lg: 1.5rem;
    
    /* Tipografia */
    --font-size-lg: 1.2rem;
}
```

### Vantagem: Alteração Global

**Antes** (Sem sistema):
- Alterar cor em Screen 1 ✅
- Alterar cor em Screen 2 ✅
- Alterar cor em Screen 3 ✅
- ... (repetir 24 vezes) ❌ **Ineficiente!**

**Depois** (Com CSS Variables):
```css
/* Alterar EM UM ÚNICO LUGAR */
--color-primary: #ff0000;

/* Afeta TODOS OS 24 SCREENS automaticamente! */
```

---

## 📝 Checklist para Novo Screen

### 1️⃣ Criar Ficheiro HTML

```bash
# Copiar template
cp screen2.html screenN.html

# Ajustar:
# - <title> 
# - Links CSS (screenN.css)
# - Classes (screenN-something)
# - Conteúdo específico
```

### 2️⃣ Criar Ficheiro CSS

```bash
touch screenN.css
```

Conteúdo mínimo:
```css
/* ============================================
   SCREEN N - [DESCRIÇÃO]
   ============================================ */

/* Customizações específicas */
.screenN-title {
    /* ... */
}

/* Responsive */
@media (max-width: 479px) {
    /* ... */
}
```

### 3️⃣ Adicionar Assets

```bash
mkdir -p Screens/screenN
# Copiar imagens para Screens/screenN/
```

### 4️⃣ Verificação

- [ ] HTML valida (sem erros no console F12)
- [ ] CSS importa `components.css` ANTES de `screenN.css`
- [ ] Classes reutilizam nomenclatura existente
- [ ] Responsivo em mobile/tablet/desktop
- [ ] Landscape testado

---

## 🔄 Fluxo de Desenvolvimento

```
1. Entender objetivo do Screen
   ↓
2. Escolher padrão (Header/Content/Footer ou Custom)
   ↓
3. Criar screenX.html com estrutura base
   ↓
4. Criar screenX.css com customizações
   ↓
5. Testar responsividade
   ↓
6. Usar CSS Variables (nunca hardcode cores)
   ↓
7. Pronto! ✅
```

---

## 🌳 Exemplo: Criar Screen 4

### Passo 1: Preparar ficheiros

```bash
cp screen2.html screen4.html
touch screen4.css
mkdir -p Screens/screen4
```

### Passo 2: Editar screen4.html

```html
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Screen 4 - As nossas maravilhas de Coimbra</title>
    <link rel="stylesheet" href="components.css">
    <link rel="stylesheet" href="screen4.css">
</head>
<body>
    <div class="route-container">
        <header class="app-header app-header--with-image">
            <img src="./Screens/screen4/title.png" alt="Screen 4" class="app-header__title-image">
        </header>
        
        <main class="app-content app-content--scrollable">
            <!-- Conteúdo específico Screen 4 -->
        </main>
        
        <footer class="app-footer app-footer--accent">
            <!-- Botões -->
        </footer>
    </div>
</body>
</html>
```

### Passo 3: Editar screen4.css

```css
/* ============================================
   SCREEN 4 - [NOME DO SCREEN]
   ============================================ */

.screen4-custom-element {
    background-color: var(--color-primary);
    color: var(--color-text);
    padding: var(--spacing-lg);
}

@media (max-width: 479px) {
    .screen4-custom-element {
        padding: var(--spacing-md);
    }
}
```

### Passo 4: Testar
- Abrir `http://localhost:8000/screen4.html`
- Pressionar F12
- `Ctrl+Shift+M` para testar responsividade

✅ **Pronto!**

---

## 🔗 Conectar Screens (Futura Navegação)

Quando adicionar navegação:

```javascript
// Navegar entre screens
document.querySelector('.btn-proximo').addEventListener('click', () => {
    window.location.href = 'screen3.html';
});
```

Ou com SPA (Single Page App):
```javascript
history.pushState(null, '', 'screen3.html');
```

---

## 📊 Escalabilidade

### Atual (3 Screens)
- ✅ `index.html` + `style.css`
- ✅ `screen2.html` + `screen2.css`
- ✅ `screen3.html` + `screen3.css`

### Pronto para 24 Screens
- ⏳ `screen4.html` + `screen4.css`
- ⏳ `screen5.html` + `screen5.css`
- ⏳ ... (até `screen24.html` + `screen24.css`)

**Cada novo screen:** ~2 minutos com o padrão estabelecido!

---

## ⚠️ Boas Práticas

### ✅ Fazer

```css
/* Usar CSS Variables */
.screenX-element {
    color: var(--color-primary);
    padding: var(--spacing-lg);
    font-size: var(--font-size-md);
}

/* Reutilizar componentes de components.css */
<button class="btn btn--primary">Ação</button>

/* Prefixar classes específicas */
.screen4-title { }
.screen4-subtitle { }
```

### ❌ Evitar

```css
/* Hardcoding cores */
.screenX-element {
    color: #d9a48b;
    padding: 1.5rem;
}

/* Criar novos componentes duplicados */
.my-custom-button { } /* Usar .btn em vez */

/* Não prefixar classes */
.title { } /* Usar .screen4-title */
```

---

## 📞 Suporte

- Dúvidas sobre CSS Variables? → Veja [DESIGN_SYSTEM.md](./DESIGN_SYSTEM.md)
- Precisa de template? → Veja [SCREEN_TEMPLATES.md](./SCREEN_TEMPLATES.md)
- Exemplos reais? → Veja `screen2.html` e `screen3.html`

---

**Versão**: 1.0  
**Data**: 2026-05-17  
**Status**: ✅ Arquitetura modular pronta para 24 screens
