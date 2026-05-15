# 🤝 Contribuindo para o Projeto

Obrigado por considerar contribuir para "As Nossas Maravilhas de Coimbra"! 

**Utilizadores**: Basta aceder a: https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/

**Contribuidores**: Siga o guia abaixo.

---

## 📋 Código de Conduta

Este projeto segue um código de conduta para garantir um ambiente inclusivo e respeitoso para todos.

### Compromissos
- Ser respeitoso com diferentes pontos de vista
- Aceitar críticas construtivas com dignidade
- Focar no que é melhor para a comunidade
- Mostrar empatia com outros membros

---

## 🚀 Como Começar (Para Contribuidores)

### 1. Fork do Repositório
```bash
# Clique no botão "Fork" no GitHub
# Depois clone seu fork:
git clone https://github.com/seu-usuario/as-nossas-maravilhas-de-coimbra.git
cd as-nossas-maravilhas-de-coimbra
```

### 2. Criar Branch para Sua Feature
```bash
git checkout -b feature/nome-da-feature
# Ou para bug fixes:
git checkout -b bugfix/descricao-do-bug
```

### 3. Iniciar Servidor Local
```bash
# Teste suas mudanças localmente antes de submeter
python -m http.server 8000
# Aceda a http://localhost:8000
```

### 4. Fazer Alterações
- Edite ficheiros existentes (não crie novos)
- Respeite a estrutura existente do código
- Teste suas mudanças localmente

### 5. Fazer Commit
```bash
git add .
git commit -m "Descrição clara da mudança"
# Exemplo: "Melhorar responsividade em tablets"
```

### 6. Push para seu Fork
```bash
git push origin feature/nome-da-feature
```

### 7. Abrir Pull Request
- Vá para o repositório original no GitHub
- Clique em "New Pull Request"
- Seleccione seu branch e adicione descrição
- Aguarde revisão

### 8. GitHub Pages Deploy Automático
- Após merge, GitHub Pages fará deploy automaticamente (1-2 min)
- Verifique em: https://pedro-vieira-programmer.github.io/...

---

## 📝 Tipos de Contribuições

### 🐛 Reportar Bugs
**Antes de criar issue:**
1. Verifique issues existentes
2. Teste em múltiplos navegadores
3. Teste no GitHub Pages (online)

**Ao criar issue, inclua:**
```markdown
## Descrição do Bug
[Descrição clara]

## Onde Reproduzir
[GitHub Pages ou local]

## Comportamento Esperado
[O que deveria acontecer]

## Comportamento Atual
[O que está acontecendo]

## Screenshots
[Se aplicável]

## Ambiente
- Browser: Chrome 120
- OS: Windows 11
- Resolução: 1920x1080
```

### ✨ Sugerir Features
**Descreva:**
- O problema que resolve
- Solução proposta
- Exemplos/screenshots
- Possíveis alternativas

### 📚 Melhorar Documentação
- Fixes typos
- Clarificar instruções
- Adicionar exemplos
- Melhorar guias

### 🎨 Melhorar Design/UX
- Layout responsivo
- Acessibilidade
- Performance
- Visual

---

## 🛠️ Padrões de Código

### HTML
```html
<!-- Use semântica apropriada -->
<main>
  <h1>Título Principal</h1>
  <button type="button">Ação</button>
</main>

<!-- Indente com 2 espaços -->
<!-- Use aspas duplas em atributos -->
```

### CSS
```css
/* Use classes descritivas */
.hero-section {
  display: grid;
  gap: 1rem;
}

/* Mobile-first approach */
@media (min-width: 768px) {
  .hero-section {
    gap: 2rem;
  }
}

/* Organize por breakpoints */
```

### JavaScript
```javascript
// Use arrow functions modernas
const handleClick = () => {
  console.log('Clicado');
};

// Nomes descritivos
const isResponsive = window.innerWidth < 768;

// Evite variáveis globais
```

---

## 📐 Estrutura do Projeto

```
├── index.html              # Principal (editar, não criar novo)
├── style.css               # Estilos (editar, não criar novo)
├── test-responsive.html    # Teste
│
├── Screens/imagens/        # Assets
├── orientation-files/      # Docs técnicas
│   ├── README.md
│   ├── SETUP.md
│   └── ...
│
└── .github/                # Config GitHub
```

**Importante**: Atualize ficheiros existentes em vez de criar novos!

---

## 🔄 Workflow de Edição

```bash
# 1. Clone e crie branch
git clone https://github.com/seu-usuario/...
git checkout -b feature/melhoria

# 2. Edite ficheiros localmente
# Atualize: index.html, style.css, docs...

# 3. Teste localmente
python -m http.server 8000
# Abra http://localhost:8000

# 4. Verifique responsividade
# F12 → Device Toggle
# Teste em múltiplos tamanhos

# 5. Commit e Push
git add .
git commit -m "Descrição clara"
git push origin feature/melhoria

# 6. Abra Pull Request no GitHub
# Aguarde revisão e merge

# 7. GitHub Pages atualiza (1-2 min)
```

---

## ✅ Checklist para Pull Request

- [ ] Testei em Chrome, Firefox, Safari
- [ ] Testei responsividade (F12 ou telemóvel real)
- [ ] Testei localmente: http://localhost:8000
- [ ] Limpei console (sem erros/warnings)
- [ ] Paths estão corretos (`./Screens/imagens/`, etc)
- [ ] Não adicionei dependências externas
- [ ] Documentei mudanças (se aplicável)
- [ ] Meu código segue os padrões do projeto
- [ ] Sem quebra de funcionalidades existentes
- [ ] Editar ficheiros existentes (não criar novos)

---

## 🧪 Testes

### Localmente
```bash
# Inicie servidor
python -m http.server 8000

# Abra http://localhost:8000
# F12 para abrir DevTools
# Ctrl+Shift+M para mobile view
```

### Verificar Responsividade
| Dispositivo | Largura | Testar |
|------------|---------|--------|
| Smartwatch | 320px | ✓ |
| Phone | 375px | ✓ |
| Tablet | 768px | ✓ |
| Desktop | 1920px | ✓ |
| Landscape | Qualquer | ✓ |

### No GitHub Pages
1. Após merge, aguarde 1-2 minutos
2. Aceda a: https://pedro-vieira-programmer.github.io/...
3. Verifique que mudanças aparecem
4. Teste responsividade no telemóvel real

---

## 📚 Recursos Úteis

- [MDN Web Docs](https://developer.mozilla.org/) - Referência HTML/CSS/JS
- [CSS Tricks](https://css-tricks.com/) - Guias CSS
- [Can I Use](https://caniuse.com/) - Compatibilidade Browser
- [orientation-files/README.md](../orientation-files/README.md) - Docs técnicas
- [orientation-files/SETUP.md](../orientation-files/SETUP.md) - Setup detalhado

---

## 🎯 Prioridades de Contribuição

### Baixa Prioridade
- Typos em documentação
- Comentários de código
- Pequenas melhorias CSS

### Média Prioridade
- Novos screens (2-24)
- Melhorias responsividade
- Documentação expandida

### Alta Prioridade
- Bugs críticos
- Acessibilidade
- Performance

---

## 📞 Dúvidas?

1. Verifique [GETTING_STARTED.md](../GETTING_STARTED.md)
2. Consulte [orientation-files/SETUP.md](../orientation-files/SETUP.md)
3. Abra uma issue no GitHub
4. Contacte via discussions

---

## 🎓 Aprender Mais

- **Setup**: [orientation-files/SETUP.md](../orientation-files/SETUP.md)
- **Docs Técnicas**: [orientation-files/README.md](../orientation-files/README.md)
- **Início Rápido**: [GETTING_STARTED.md](../GETTING_STARTED.md)
- **Main README**: [README.md](../README.md)

---

**Obrigado por contribuir!** 🎉

Cada contribuição, não importa o tamanho, ajuda a tornar este projeto melhor para todos.

---

**Última atualização**: 2026-05-13
**Versão**: 2.0
**Hospedagem**: GitHub Pages
