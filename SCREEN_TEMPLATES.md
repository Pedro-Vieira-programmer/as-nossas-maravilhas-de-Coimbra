# Screen Templates - Guia de Implementação Rápida

## 📋 Estrutura Base

Todos os screens seguem a mesma estrutura de layout:

```html
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[TÍTULO DO SCREEN]</title>
    <link rel="stylesheet" href="components.css">    <!-- Design System -->
    <link rel="stylesheet" href="screen[N].css">     <!-- Estilos Específicos -->
</head>
<body>
    <div class="route-container">
        <!-- Header -->
        <header class="app-header app-header--with-image">
            <!-- Conteúdo do header -->
        </header>

        <!-- Main Content -->
        <main class="app-content app-content--scrollable">
            <!-- Conteúdo específico do screen -->
        </main>

        <!-- Footer -->
        <footer class="app-footer">
            <!-- Botões e elementos finais -->
        </footer>
    </div>
</body>
</html>
```

## 🎨 Sistema de Cores (CSS Variables)

Definidas em `components.css`:

| Variável | Valor | Uso |
|----------|-------|-----|
| `--color-primary` | #d9a48b | Botões, acentos, backgrounds |
| `--color-primary-dark` | #d19478 | Hover states |
| `--color-secondary` | #2a2a2a | Textos escuros |
| `--color-secondary-dark` | #1a1a1a | Textos muito escuros |
| `--color-neutral` | #ffffff | Backgrounds brancos |
| `--color-text-inverse` | #ffffff | Texto inverso |

**Como usar:**
```css
.meu-elemento {
    background-color: var(--color-primary);
    color: var(--color-text);
}
```

## 📏 Espaçamento (CSS Variables)

| Variável | Valor | Uso |
|----------|-------|-----|
| `--spacing-xs` | 0.5rem | Gaps pequenos |
| `--spacing-sm` | 0.8rem | Espaçamento pequeno |
| `--spacing-md` | 1.2rem | Espaçamento médio |
| `--spacing-lg` | 1.5rem | Espaçamento grande |
| `--spacing-xl` | 2rem | Espaçamento extra grande |

## 🔲 Border Radius (CSS Variables)

| Variável | Valor | Uso |
|----------|-------|-----|
| `--radius-sm` | 0.5rem | Cantos pequenos |
| `--radius-md` | 0.9rem | Cantos médios |
| `--radius-lg` | 1rem | Cantos grandes |
| `--radius-xl` | 2rem | Cantos muito grandes |

## 🧩 Componentes Reutilizáveis

### Header com Imagem
```html
<header class="app-header app-header--with-image">
    <img src="Screens/screen[N]/[imagem].png" alt="[descrição]" class="app-header__title-image">
</header>
```

### Conteúdo Principal (com scroll)
```html
<main class="app-content app-content--scrollable">
    <!-- Seus elementos aqui -->
</main>
```

### Footer com Botão
```html
<footer class="app-footer">
    <button class="screen[N]-button">
        <img src="Screens/screen[N]/[imagem].png" alt="[descrição]">
    </button>
</footer>
```

### Cartão de Rota
```html
<div class="route-card">
    <img src="..." class="route-card__image" alt="...">
    <p class="route-card__label">Label texto</p>
</div>
```

### Botão
```html
<button class="btn btn--primary">Texto do botão</button>
<button class="btn btn--secondary">Texto do botão</button>
```

## 📱 Breakpoints Responsivos

O design system já inclui breakpoints. No seu `screen[N].css`, use:

```css
/* Mobile */
@media (max-width: 479px) {
    /* Estilos para mobile */
}

/* Tablet */
@media (min-width: 480px) and (max-width: 768px) {
    /* Estilos para tablet */
}

/* Desktop */
@media (min-width: 769px) {
    /* Estilos para desktop */
}

/* Landscape */
@media (orientation: landscape) {
    /* Estilos para landscape */
}
```

## 🚀 Processo Rápido para Novo Screen

### Passo 1: Criar Pasta de Assets
```
Screens/screen[N]/
├── imagem1.png
├── imagem2.png
├── icone.png
└── ...
```

### Passo 2: Criar HTML
- Copiar estrutura base acima
- Substituir [N] pelo número do screen
- Usar componentes do `components.css`

### Passo 3: Criar CSS Específico
- Nome: `screen[N].css`
- Apenas customizações para aquele screen
- Herdar variáveis do `components.css`

### Exemplo Prático (Screen 5):

**screen5.html:**
```html
<!DOCTYPE html>
<html lang="pt-PT">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Informações - As nossas maravilhas de Coimbra</title>
    <link rel="stylesheet" href="components.css">
    <link rel="stylesheet" href="screen5.css">
</head>
<body>
    <div class="route-container">
        <header class="app-header app-header--with-image">
            <img src="Screens/screen5/titulo.png" alt="Título" class="app-header__title-image">
        </header>

        <main class="app-content app-content--scrollable">
            <h1 class="screen5-titulo">
                <img src="Screens/screen5/info-title.png" alt="Informações">
            </h1>
            <!-- Mais conteúdo aqui -->
        </main>

        <footer class="app-footer">
            <button class="screen5-button">
                <img src="Screens/screen5/botao.png" alt="Próximo">
            </button>
        </footer>
    </div>
</body>
</html>
```

**screen5.css:**
```css
/* Apenas customizações específicas */
.app-header {
    background-color: var(--color-primary);
}

.screen5-titulo {
    margin-bottom: var(--spacing-lg);
}

/* Responsivos apenas se necessário */
@media (max-width: 479px) {
    .screen5-titulo {
        margin-bottom: var(--spacing-md);
    }
}
```

## ✅ Checklist para Novo Screen

- [ ] Pasta `Screens/screen[N]` criada com todos os assets
- [ ] Arquivo `screen[N].html` criado com estrutura base
- [ ] Arquivo `screen[N].css` criado (apenas customizações)
- [ ] Links CSS corretos no HTML (`components.css` e `screen[N].css`)
- [ ] Imagens com caminhos corretos (`Screens/screen[N]/...`)
- [ ] Cores usando `var(--color-*)` do design system
- [ ] Espaçamento usando `var(--spacing-*)` do design system
- [ ] Breakpoints responsivos definidos
- [ ] Testado em mobile, tablet e desktop

## 🎯 Resumo

1. **Reutilizar componentes** - Use classes do `components.css`
2. **Usar CSS Variables** - Cores e espaçamento consistentes
3. **Minimal CSS** - Apenas o específico de cada screen em `screen[N].css`
4. **Responsivo por padrão** - Design system cobre breakpoints
5. **Velocidade** - Novos screens em minutos!

---

**Última atualização:** 17 de Maio de 2026
