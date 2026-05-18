# ⚡ Quick Reference - Guia Rápido

Referência rápida para informações principais sobre o projeto.

---

## 🚀 Acesso Rápido

### 📱 Utilizadores
```
Abra: https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/
```

### 💻 Programadores
```bash
git clone https://github.com/Pedro-Vieira-programmer/as-nossas-maravilhas-de-coimbra.git
python -m http.server 8000
# Aceda a http://localhost:8000
```

---

## 📋 Documentação Essencial (7 ficheiros)

| Ficheiro | O Quê? | Quando? |
|----------|--------|---------|
| **README.md** | Overview | Primeiro |
| **PROJECT.md** | Técnico | Entender |
| **STRUCTURE.md** | Ficheiros | Navegar |
| **ARCHITECTURE.md** | Como funciona | Modificar |
| **DESIGN_SYSTEM.md** | Componentes | Codificar |
| **DEPLOYMENT.md** | GitHub Pages | Publicar |
| **CHANGELOG.md** | Histórico | Atualizar |

👉 Veja [DOCUMENTATION.md](./DOCUMENTATION.md) para índice completo

---

## 🎨 Cores & Espaçamento

### Cores
```css
Primário:     #d9a48b  (var(--color-primary))
Primário+:    #d19478  (var(--color-primary-dark))
Texto:        #2a2a2a  (var(--color-secondary))
Branco:       #ffffff  (var(--color-neutral))
```

### Espaçamento
```css
xs: 0.5rem   sm: 0.8rem   md: 1.2rem
lg: 1.5rem   xl: 2rem
```

---

## 📱 Breakpoints

```
< 480px     Mobile
480-768px   Tablet
> 768px     Desktop
landscape   Qualquer (horizontal)
```

---

## 📂 Estrutura Crítica

```
✅ components.css       # CORE - não apague!
✅ screenX.html         # 24 ficheiros
✅ screenX.css          # Estilos
✅ Screens/screenX/     # Imagens
```

---

## 🔧 Tarefas Comuns

### Alterar Cor Principal
```css
/* components.css */
--color-primary: #NOVACOR;
/* Afeta TODOS os 24 screens automaticamente! */
```

### Adicionar Novo Screen
```bash
# 1. Copiar ficheiros
cp screen2.html screenN.html
touch screenN.css
mkdir -p Screens/screenN

# 2. Editar conteúdo
# ... modificar HTML e CSS ...

# 3. Commit
git add .
git commit -m "Adicionar Screen N"
git push origin main
```

### Testar Responsividade
```bash
# Local
open http://localhost:8000
# F12 → Ctrl+Shift+M → testar dispositivos

# GitHub Pages
https://github.io/...
# Abrir em telemóvel
```

### Deploy para GitHub Pages
```bash
git push origin main
# Automático em 1-2 minutos
```

---

## 💡 Padrões Importantes

### ✅ Fazer
```html
<!-- Usar CSS Variables -->
<link rel="stylesheet" href="components.css">  <!-- PRIMEIRO -->
<link rel="stylesheet" href="screenX.css">     <!-- Depois -->

<!-- Usar componentes existentes -->
<button class="btn btn--primary">Ação</button>

<!-- Prefixar classes -->
.screen5-title { }
```

### ❌ Evitar
```html
<!-- Hardcode cores -->
color: #d9a48b;  ❌ Usar var(--color-primary)

<!-- Criar duplicatas -->
.custom-button { }  ❌ Usar .btn

<!-- Sem prefixo -->
.title { }  ❌ Usar .screen5-title
```

---

## 📊 Stats

| Item | Quantidade |
|------|-----------|
| Screens | 24 |
| Ficheiros HTML | 24 |
| Ficheiros CSS | 7 |
| Documentação | 8 |
| Imagens | ~300 |
| **Status** | **✅ 100% Completo** |

---

## 🐛 Troubleshooting

| Problema | Solução |
|----------|---------|
| Imagens não carregam | `./Screens/screenX/...` correto? |
| Layout quebrado | CSS import order? components.css ANTES |
| Não responsivo | Viewport meta tag? Testar F12 |
| GitHub Pages 404 | Aguarde 2 min, refresque página |
| Cor não muda | Usar var(--color-*) não hardcode |

---

## 🔗 Links Importantes

- 📱 **App**: https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/
- 📚 **GitHub**: https://github.com/Pedro-Vieira-programmer/as-nossas-maravilhas-de-coimbra
- 🐛 **Issues**: https://github.com/Pedro-Vieira-programmer/as-nossas-maravilhas-de-coimbra/issues
- 📖 **Docs Completas**: [DOCUMENTATION.md](./DOCUMENTATION.md)

---

## ✅ Checklist Antes de Commit

- [ ] HTML válido (sem erros F12)
- [ ] CSS imports corretos
- [ ] Imagens têm alt text
- [ ] Responsivo testado
- [ ] Usa CSS Variables
- [ ] Commit com mensagem clara
- [ ] Git push origin main

---

## 👥 Contacto

| Tipo | Info |
|------|------|
| **Desenvolvedor** | Pedro Vieira |
| **Co-autoria** | Copilot |
| **GitHub** | [Perfil](https://github.com/Pedro-Vieira-programmer) |
| **Versão** | 3.0 |
| **Data** | 2026-05-18 |

---

**Status**: ✅ Pronto para Produção  
**Deploy**: ✅ GitHub Pages Ativo  
**Documentação**: ✅ Completa
