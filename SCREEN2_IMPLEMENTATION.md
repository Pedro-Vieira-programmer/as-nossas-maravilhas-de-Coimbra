# 📍 Screen 2 - A Nossa Rota (Implementação)

## 📋 Descrição

Screen 2 implementa uma **rota linear vertical** que apresenta 11 pontos turísticos de Coimbra em sequência:

1. Escola Martim de Freitas
2. Miradouro do Penedo da Saudade
3. Jardim Botânico da Universidade de Coimbra
4. Parque da Cidade Manuel Braga
5. Jardins da Quinta das Lágrimas
6. Baixa Citadina
7. Sé Velha de Coimbra
8. Universidade de Coimbra
9. Jardim da Sereia
10. Mosteiro de Celas
11. Escola Martim de Freitas (regresso)

## 🏗️ Arquitetura Técnica

### Estrutura HTML Padrão

```html
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <meta name="description" content="A Nossa Rota - As Nossas Maravilhas de Coimbra">
    <meta name="theme-color" content="#ffffff">
    <title>A Nossa Rota - As Nossas Maravilhas de Coimbra</title>
    
    <!-- Componentes globais + estilos específicos -->
    <link rel="stylesheet" href="components.css">
    <link rel="stylesheet" href="screen2.css">
</head>
<body>
    <div class="route-container">
        <!-- Header: Imagem de título -->
        <header class="app-header app-header--with-image">
            <img src="./Screens/screen2/A nossa rota.png" 
                 alt="A nossa rota" 
                 class="app-header__title-image">
        </header>

        <!-- Main: Conteúdo rolável com rota -->
        <main class="app-content app-content--scrollable">
            <div class="route-list">
                <!-- Item 1: ... -->
                <!-- Item + Divisor -->
                <!-- Item 2: ... -->
                <!-- ... etc -->
            </div>
        </main>

        <!-- Footer: Botões de ação -->
        <footer class="app-footer app-footer--accent">
            <div class="footer-content">
                <div class="button-group">
                    <div class="btn btn--secondary-non">FIM</div>
                    <button class="btn btn--primary" onclick="handleIniciarClick()">
                        Deseja iniciar?
                    </button>
                </div>
            </div>
        </footer>
    </div>

    <script>
        function handleIniciarClick() {
            console.log('Deseja iniciar clicado');
            // Future navigation logic
        }

        function handleFinClick() {
            console.log('FIM clicado');
            // Future navigation logic
        }
    </script>
</body>
</html>
```

## 🎯 Componentes Utilizados

### 1. Header com Imagem

```html
<header class="app-header app-header--with-image">
    <img src="./Screens/screen2/A nossa rota.png" 
         alt="A nossa rota" 
         class="app-header__title-image">
</header>
```

**Classes CSS utilizadas:**
- `.app-header` - Componente base do header
- `.app-header--with-image` - Modificador para headers com imagem
- `.app-header__title-image` - Elemento imagem do header

### 2. Conteúdo Rolável

```html
<main class="app-content app-content--scrollable">
    <div class="route-list">
        <!-- Items da rota -->
    </div>
</main>
```

**Classes CSS utilizadas:**
- `.app-content` - Componente base de conteúdo
- `.app-content--scrollable` - Modificador para scroll vertical
- `.route-list` - Container dos items

### 3. Item da Rota (Route Card)

```html
<article class="route-card">
    <img src="./Screens/screen2/Rectangle 7.png" 
         alt="Escola Martim de Freitas" 
         class="route-card__image">
    <h2 class="route-card__label">Escola Martim de Freitas</h2>
</article>
```

**Classes CSS utilizadas:**
- `.route-card` - Container do item
- `.route-card__image` - Imagem do ponto turístico
- `.route-card__label` - Título/nome do local

### 4. Divisor entre Items (Route Divider)

```html
<div class="route-divider">
    <img src="./Screens/screen2/Arrow 2.png" 
         alt="" 
         class="route-divider__icon">
</div>
```

**Classes CSS utilizadas:**
- `.route-divider` - Container do divisor
- `.route-divider__icon` - Seta do divisor

### 5. Footer com Botões

```html
<footer class="app-footer app-footer--accent">
    <div class="footer-content">
        <div class="button-group">
            <div class="btn btn--secondary-non">FIM</div>
            <button class="btn btn--primary" onclick="handleIniciarClick()">
                Deseja iniciar?
            </button>
        </div>
    </div>
</footer>
```

**Classes CSS utilizadas:**
- `.app-footer` - Componente base do footer
- `.app-footer--accent` - Modificador com cor bege (#d9a48b)
- `.footer-content` - Container interno
- `.button-group` - Grupo de botões
- `.btn` - Componente botão base
- `.btn--primary` - Botão primário (preto)
- `.btn--secondary-non` - Botão secundário sem interação (bege)

## 🎨 Estilos Específicos (screen2.css)

```css
/* ============================================
   SCREEN 2 - A NOSSA ROTA
   Route display with vertical scroll
   ============================================ */

/* Route specific adjustments */
.route-list {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.route-card {
    margin-bottom: var(--spacing-xs);
}

/* Mobile optimizations */
@media (max-width: 479px) {
    .route-card__image {
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    }
}

/* Tablet optimizations */
@media (min-width: 480px) and (max-width: 768px) {
    .route-card__label {
        padding: var(--spacing-sm) var(--spacing-sm);
    }
}

/* Desktop optimizations */
@media (min-width: 769px) {
    .route-card {
        transition: transform 0.2s ease;
    }
    
    .route-card:hover .route-card__image {
        box-shadow: 0 6px 16px rgba(0, 0, 0, 0.15);
    }
}
```

## 📐 Layout e Responsividade

### Estrutura de Grid

```
┌─────────────────────────────────┐
│         Header (Fixa)           │  - Imagem "A nossa rota"
│  [app-header--with-image]       │  - Altura: auto
├─────────────────────────────────┤
│                                 │
│    Main Content (Scroll)        │  - .app-content--scrollable
│    ├─ route-list               │  - flex-direction: column
│    │  ├─ route-card            │  - items: centered
│    │  ├─ route-divider         │
│    │  ├─ route-card            │
│    │  ├─ route-divider         │
│    │  └─ ...                   │
│                                 │
├─────────────────────────────────┤
│         Footer (Fixa)           │  - app-footer--accent
│  [button-group]                 │  - Altura: auto
│   FIM | Deseja iniciar?        │
└─────────────────────────────────┘
```

### Breakpoints

| Dispositivo | Largura | Ajustes |
|-----------|---------|---------|
| Mobile | < 480px | Sombras box nos cards |
| Tablet | 480-768px | Padding nos labels |
| Desktop | > 768px | Hover effects, transitions |

## 🎯 Padrão de Implementação

### Como Adicionar um Novo Ponto à Rota

```html
<!-- Adicionar antes de </div> de route-list -->
<article class="route-card">
    <img src="./Screens/screen2/Rectangle XX.png" 
         alt="Nome do Local" 
         class="route-card__image">
    <h2 class="route-card__label">Nome do Local</h2>
</article>

<div class="route-divider">
    <img src="./Screens/screen2/Arrow XX.png" 
         alt="" 
         class="route-divider__icon">
</div>
```

### Como Criar um Screen Semelhante

1. Copiar `screen2.html` → `screen3.html`
2. Atualizar `<title>` e `<meta description>`
3. Atualizar paths de imagens (`screen2/` → `screen3/`)
4. Mudar ID do `<header>` imagem
5. Adicionar items específicos ao conteúdo
6. Atualizar links CSS (`screen2.css` → `screen3.css`)
7. Criar `screen3.css` com estilos específicos (copiar screen2.css como base)

## 📦 Assets Necessários

Localização: `./Screens/screen2/`

```
screen2/
├── A nossa rota.png         # Header title image
├── Rectangle 7.png          # Item 1 image
├── Rectangle 9.png          # Item 2 image
├── Rectangle 10.png         # Item 3 image
├── Rectangle 11.png         # Item 4 image
├── Rectangle 15.png         # Item 5 image
├── Rectangle 16.png         # Item 6 image
├── Rectangle 12.png         # Item 7 image
├── Rectangle 13.png         # Item 8 image
├── Rectangle 18.png         # Item 9 image
├── Rectangle 17.png         # Item 10 image
├── Rectangle 19.png         # Item 11 image
├── Arrow 2.png              # Divisor 1
├── Arrow 3.png              # Divisor 2
├── ...
└── Arrow 12.png             # Divisor 11
```

## 🔄 Navegação

Atualmente, os botões não navegam entre screens. Para implementar navegação:

```javascript
function handleIniciarClick() {
    // Navegar para screen seguinte ou lista
    window.location.href = './index.html';  // Exemplo
}

function handleFinClick() {
    // Voltar ou fechar
    window.history.back();
}
```

## ✅ Checklist de Testes

- [ ] Header renderiza corretamente
- [ ] Items estão alinhados verticalmente
- [ ] Divisores (arrows) aparecem entre items
- [ ] Scroll funciona em mobile
- [ ] Botões responsivos no footer
- [ ] Cores mantêm fidelidade ao design
- [ ] Responsive em 3 breakpoints (mobile, tablet, desktop)
- [ ] Sem erros na console do navegador

## 📚 Componentes Relacionados

- `components.css` - Todos os componentes reutilizáveis
- `DESIGN_SYSTEM.md` - Documentação completa do sistema
- `README.md` - Overview do projeto
- `index.html` - Screen 1 (tela inicial)

---

**Versão**: 1.0  
**Data**: 2026-05-17  
**Status**: ✅ Implementado e documentado  
**Referência**: As Nossas Maravilhas de Coimbra
