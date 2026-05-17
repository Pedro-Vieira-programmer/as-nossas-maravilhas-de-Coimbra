# Design System - As Nossas Maravilhas de Coimbra

## Visão Geral
Este é um sistema de design modular e reutilizável para a aplicação web responsiva "As Nossas Maravilhas de Coimbra". Todos os componentes foram estruturados para serem reutilizáveis em múltiplos screens.

## Arquitetura CSS

### 1. **components.css** - Sistema Base
Contém todos os componentes reutilizáveis e design tokens (variáveis CSS).

**Componentes Disponíveis:**
- `.app-header` - Cabeçalho com título
- `.app-title` - Título principal
- `.app-title--underline` - Modificador para underline
- `.app-content` - Área de conteúdo principal
- `.app-content--scrollable` - Área scrollável
- `.app-footer` - Rodapé
- `.app-footer--accent` - Rodapé com cor de destaque
- `.btn` - Botão base
- `.btn--primary` - Botão primário (preto)
- `.btn--secondary` - Botão secundário (bege)
- `.button-group` - Grupo de botões
- `.route-card` - Card de rota/item
- `.route-card__image` - Imagem do card
- `.route-card__label` - Label do card
- `.route-divider` - Divisor entre items
- `.footer-title` - Título do rodapé

### 2. **screenX.css** - Estilos Específicos de Cada Screen
Customizações e overrides específicos para cada screen.

**Exemplos implementados:**
- **style.css** - Estilos específicos do Screen 1
- **screen2.css** - Estilos específicos do Screen 2  
- **screen3.css** - Estilos específicos do Screen 3

## Design Tokens (CSS Variables)

### Cores
```css
--color-primary: #d9a48b;        /* Bege principal */
--color-primary-dark: #d19478;   /* Bege escuro */
--color-secondary: #2a2a2a;      /* Cinzento escuro */
--color-secondary-dark: #1a1a1a; /* Cinzento muito escuro */
--color-neutral: #ffffff;        /* Branco */
--color-text: #1a1a1a;           /* Texto escuro */
--color-text-inverse: #ffffff;   /* Texto claro */
--color-overlay: rgba(0, 0, 0, 0.65); /* Overlay semi-transparente */
```

### Espaçamento
```css
--spacing-xs: 0.5rem;   /* Extra pequeno */
--spacing-sm: 0.8rem;   /* Pequeno */
--spacing-md: 1.2rem;   /* Médio */
--spacing-lg: 1.5rem;   /* Grande */
--spacing-xl: 2rem;     /* Extra grande */
```

### Border Radius
```css
--radius-sm: 0.5rem;    /* Pequeno */
--radius-md: 0.9rem;    /* Médio */
--radius-lg: 1rem;      /* Grande */
--radius-xl: 2rem;      /* Extra grande */
```

### Typography
```css
--font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica Neue', Arial, sans-serif;
--font-size-sm: 0.85rem;
--font-size-base: 0.9rem;
--font-size-md: 1rem;
--font-size-lg: 1.2rem;
--font-size-xl: 1.3rem;
--font-weight-regular: 600;
--font-weight-bold: 700;
```

### Sombras
```css
--shadow-sm: 0 3px 10px rgba(0, 0, 0, 0.12);
--shadow-md: 0 4px 12px rgba(0, 0, 0, 0.15);
--shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.15);
```

## Responsive Breakpoints

- **Mobile**: < 480px
- **Tablet**: 480px - 768px
- **Desktop**: > 768px
- **Landscape**: Qualquer resolução em modo landscape

Cada breakpoint ajusta automaticamente as variáveis CSS e componentes.

## Padrão de Implementação

Cada screen segue a mesma estrutura modular:
- **screenX.html** - Estrutura HTML específica do screen
- **screenX.css** - Estilos específicos (reutiliza components.css)
- **components.css** - Design system compartilhado (obrigatório)

### Exemplo de Estrutura HTML

```html
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>[TÍTULO]</title>
    <!-- IMPORTANTE: Sempre incluir components.css ANTES de screenX.css -->
    <link rel="stylesheet" href="components.css">
    <link rel="stylesheet" href="screenX.css">
</head>
<body>
    <div class="route-container">
        <!-- Header (pode ter imagem ou texto) -->
        <header class="app-header app-header--with-image">
            <img src="./Screens/screenX/image.png" alt="..." class="app-header__title-image">
        </header>

        <!-- Conteúdo principal (scrollável se necessário) -->
        <main class="app-content app-content--scrollable">
            <!-- Componentes específicos do screen -->
        </main>

        <!-- Rodapé -->
        <footer class="app-footer app-footer--accent">
            <div class="footer-content">
                <div class="button-group">
                    <button class="btn btn--secondary">Botão</button>
                    <button class="btn btn--primary">Ação</button>
                </div>
            </div>
        </footer>
    </div>
</body>
</html>
```

## Exemplos de Screens Implementados

### Screen 1 - Tela Inicial
**Ficheiros:** `index.html`, `style.css`

Estrutura única com layout absoluto para apresentação visual personalizada.
- Usa: `components.css` para variáveis CSS + `style.css` para estilos específicos
- Classes: `.screen1-container`, `.screen1-title-text`, `.screen1-iniciar-btn`, etc.

```html
<main class="screen1-container">
    <!-- Elementos específicos de Screen 1 -->
</main>
```

### Screen 2 - A Nossa Rota
**Ficheiros:** `screen2.html`, `screen2.css`

Rota linear com 11 pontos turísticos em sequência vertical.
- Usa: `components.css` (componentes) + `screen2.css` (customizações)
- Estrutura: `.route-container` → `.app-header` → `.app-content--scrollable` → `.app-footer`

```html
<div class="route-container">
    <header class="app-header app-header--with-image">
        <img src="./Screens/screen2/A nossa rota.png" alt="A nossa rota" class="app-header__title-image">
    </header>
    
    <main class="app-content app-content--scrollable">
        <div class="route-list">
            <!-- Cards de rota -->
        </div>
    </main>
    
    <footer class="app-footer app-footer--accent">
        <!-- Botões -->
    </footer>
</div>
```

### Screen 3 - Guia de Direções
**Ficheiros:** `screen3.html`, `screen3.css`

Guia com direções e mapa para um ponto turístico.
- Usa: `components.css` (base) + `screen3.css` (customizações)
- Estrutura: `.route-container` com conteúdo scrollável

## BEM Naming Convention

Usamos BEM (Block Element Modifier) para naming:

- **Block**: `.route-card`
- **Element**: `.route-card__image`
- **Modifier**: `.btn--primary`

Exemplos:
```
.app-header          // Block
.app-header__title   // Element
.app-header--sticky  // Modifier

.route-card          // Block
.route-card__image   // Element
.route-card--active  // Modifier
```

**Para screens únicos (Screen 1, 3, etc.):**
```
.screen1-container      // Block específico de Screen 1
.screen1-title-text     // Elemento específico
.screen1-iniciar-btn    // Botão específico
```

## Exemplo de Card de Rota (Screen 2)

### Estrutura Implementada
O Screen 2 implementa uma rota linear com 11 pontos turísticos em sequência vertical. Cada ponto é composto por:

```html
<!-- Item da Rota -->
<article class="route-card">
    <img src="./Screens/screen2/Rectangle 7.png" alt="Escola Martim de Freitas" class="route-card__image">
    <h2 class="route-card__label">Escola Martim de Freitas</h2>
</article>

<!-- Divisor entre items -->
<div class="route-divider">
    <img src="./Screens/screen2/Arrow 2.png" alt="" class="route-divider__icon">
</div>
```

## Como Usar CSS Variables

### Bom ✅
```css
.meu-elemento {
    background-color: var(--color-primary);
    color: var(--color-text);
    padding: var(--spacing-lg);
    border-radius: var(--radius-md);
}
```

### Evitar ❌
```css
.meu-elemento {
    background-color: #d9a48b;
    color: #1a1a1a;
    padding: 1.5rem;
    border-radius: 0.9rem;
}
```

## Modificadores de Botão

```html
<!-- Botão Primário (Preto) -->
<button class="btn btn--primary">Deseja iniciar?</button>

<!-- Botão Secundário (Bege com borda) -->
<button class="btn btn--secondary">FIM</button>

<!-- Botão Secundário Sem Borda -->
<div class="btn btn--secondary-non">FIM</div>

<!-- Grupo de Botões -->
<div class="button-group">
    <button class="btn btn--secondary">Botão 1</button>
    <button class="btn btn--primary">Botão 2</button>
</div>

<!-- Grupo Horizontal -->
<div class="button-group button-group--horizontal">
    <button class="btn btn--secondary">Esquerda</button>
    <button class="btn btn--primary">Direita</button>
</div>
```

## Scrollbar Customizado

O scrollbar é automaticamente estilizado em áreas com `.app-content--scrollable`:
- **Track**: Cinzento claro (#f0f0f0)
- **Thumb**: Bege (#d9a48b)
- **Hover**: Bege escuro (#d19478)

## Cores Exatas

Mantidas do design original:
- **Bege Principal**: #d9a48b (RGB: 217, 164, 139)
- **Preto/Cinzento**: #1a1a1a (RGB: 26, 26, 26)
- **Branco**: #ffffff (RGB: 255, 255, 255)

## Princípios de Design

1. **Mobile-First**: Começar com mobile e escalar para desktop
2. **Responsivo**: Adapta-se a qualquer tamanho de tela
3. **Acessível**: Contraste suficiente, tamanhos de toque mínimos (44px)
4. **Performante**: Usa CSS Variables para mudanças dinâmicas
5. **Modular**: Componentes independentes e reutilizáveis

## Checklist para Novo Screen

- [ ] Criar arquivo `screenX.html`
- [ ] Adicionar links para `components.css` e `screenX.css` (nesta ordem!)
- [ ] Usar classes de componentes existentes
- [ ] Manter estrutura HTML semântica
- [ ] Usar CSS Variables em vez de valores hardcoded
- [ ] Prefixar classes específicas com `screenX-`
- [ ] Testar em mobile, tablet e desktop
- [ ] Testar em landscape e portrait
- [ ] Validar acessibilidade
- [ ] Verificar performance

## Suporte a Navegadores

- Chrome/Edge 88+
- Firefox 87+
- Safari 14+
- iOS Safari 14+

---

Desenvolvido para: As Nossas Maravilhas de Coimbra
Última atualização: 2026-05-17
**Status**: ✅ Documentado com exemplos reais (Screen 1, Screen 2 + Screen 3)
**Padrão**: Modular - components.css + screenX.css (padrão único para todos os 24 screens)
