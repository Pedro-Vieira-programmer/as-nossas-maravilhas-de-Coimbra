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

### 2. **screen2.css** - Estilos Específicos do Screen 2
Customizações e overrides específicos para o Screen 2.

### 3. **screenX.css** - Padrão para Novos Screens
Criar um novo arquivo para cada screen seguindo o padrão `screenX.css`.

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

## Como Usar para Novos Screens

O projeto segue um padrão modular onde cada screen tem:
- **screenX.html** - Estrutura HTML específica do screen
- **screenX.css** - Estilos específicos (opcional, reutiliza components.css)
- **components.css** - Todos os componentes reutilizáveis

### Padrão de Implementação

Cada screen reutiliza a estrutura base:

```html
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <link rel="stylesheet" href="components.css">
    <link rel="stylesheet" href="screenX.css">  <!-- Específico do screen -->
</head>
<body>
    <div class="route-container">
        <!-- Header (pode ter imagem ou texto) -->
        <header class="app-header">
            <!-- Conteúdo específico -->
        </header>

        <!-- Conteúdo principal -->
        <main class="app-content app-content--scrollable">
            <!-- Usar componentes de components.css -->
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

### 1. Criar o HTML (screenX.html)

Usar a estrutura acima, adaptando conteúdo específico do screen.

### 2. Criar screenX.css (Opcional)

Se precisares de estilos específicos para o screen:

```css
/* ============================================
   SCREEN X - DESCRIÇÃO
   ============================================ */

/* Overrides específicos para este screen */
.seu-componente {
    /* estilos */
}

/* Responsive overrides */
@media (max-width: 479px) {
    .seu-componente {
        /* mobile */
    }
}
```

### 3. Reutilizar Componentes

Todos os componentes em `components.css` estão disponíveis:
- `.app-header` e `.app-header--with-image`
- `.app-content` e `.app-content--scrollable`
- `.app-footer` e `.app-footer--accent`
- `.route-card`, `.route-card__image`, `.route-card__label`
- `.route-divider`
- `.btn--primary`, `.btn--secondary`, `.btn--secondary-non`
- `.button-group`

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

### Screen 2 - Estrutura Completa
```html
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <meta name="description" content="A Nossa Rota - As Nossas Maravilhas de Coimbra">
    <title>A Nossa Rota - As Nossas Maravilhas de Coimbra</title>
    <link rel="stylesheet" href="components.css">
    <link rel="stylesheet" href="screen2.css">
</head>
<body>
    <div class="route-container">
        <!-- Header com imagem de título -->
        <header class="app-header app-header--with-image">
            <img src="./Screens/screen2/A nossa rota.png" alt="A nossa rota" class="app-header__title-image">
        </header>

        <!-- Conteúdo rolável -->
        <main class="app-content app-content--scrollable">
            <div class="route-list">
                <!-- Repetir para cada ponto da rota -->
                <article class="route-card">
                    <img src="./Screens/screen2/Rectangle X.png" alt="Local" class="route-card__image">
                    <h2 class="route-card__label">Nome do Local</h2>
                </article>
                <div class="route-divider">
                    <img src="./Screens/screen2/Arrow X.png" alt="" class="route-divider__icon">
                </div>
            </div>
        </main>

        <!-- Rodapé com botões -->
        <footer class="app-footer app-footer--accent">
            <div class="footer-content">
                <div class="button-group">
                    <div class="btn btn--secondary-non">FIM</div>
                    <button class="btn btn--primary" onclick="handleIniciarClick()">Deseja iniciar?</button>
                </div>
            </div>
        </footer>
    </div>
</body>
</html>
```

## Modificadores de Título

```html
<!-- Título com underline -->
<h1 class="app-title app-title--underline">A nossa rota</h1>

<!-- Título simples -->
<h1 class="app-title">Título Simples</h1>

<!-- Título no footer -->
<h3 class="footer-title footer-title--underline">FIM</h3>
```

## Modificadores de Botão

```html
<!-- Botão Primário (Preto) -->
<button class="btn btn--primary">Deseja iniciar?</button>

<!-- Botão Secundário (Bege) -->
<button class="btn btn--secondary">FIM</button>

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
- Track: Cinzento claro (#f0f0f0)
- Thumb: Bege (#d9a48b)
- Hover: Bege escuro (#d19478)

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
- [ ] Adicionar links para `components.css` e `screenX.css`
- [ ] Usar classes de componentes existentes
- [ ] Manter estrutura HTML semântica
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
**Status**: ✅ Documentado com exemplos reais (Screen 1 + Screen 2)
**Padrão**: Modular - cada screen reutiliza components.css com CSS específico opcional
