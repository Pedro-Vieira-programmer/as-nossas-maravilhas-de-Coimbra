# 🚀 Guia de Acesso - GitHub Pages

## ⚡ Acesso em 1 Clique (Utilizadores)

### 🌐 Aceder Diretamente Online
```
https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/
```

**É isto!** Nenhuma instalação, nenhum download. Apenas abra o link no navegador e desfrute! 🎉

---

## 💻 Para Programadores/Contribuidores

Se quiser **trabalhar no código** ou **contribuir**, siga este guia.

### ⚡ Setup em 30 Segundos (Desenvolvimento Local)

1. **Clonar o Repositório**
```bash
git clone https://github.com/Pedro-Vieira-programmer/as-nossas-maravilhas-de-coimbra.git
cd as-nossas-maravilhas-de-coimbra
```

2. **Iniciar Servidor Local**
```bash
# Opção 1: Python (recomendado)
python -m http.server 8000

# Opção 2: Node.js
npx http-server

# Opção 3: VS Code Live Server
# Clique direito em index.html → "Open with Live Server"
```

3. **Abrir Navegador**
Aceda a `http://localhost:8000`

---

## 📋 Requisitos (Apenas para Desenvolvimento)

- **Navegador moderno** (Chrome, Firefox, Safari, Edge)
- **Git** (para clonar repositório)
- **Python 3** OU **Node.js** (para servidor local)

### Verificar Versões Instaladas
```bash
# Python
python --version

# Node.js
node --version

# Git
git --version
```

---

## 🎯 Próximos Passos

### Para Utilizadores Finais ✅
Pronto! Aceda a: https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/

**Screens disponíveis:**
- **Screen 1**: Tela inicial "As Nossas Maravilhas de Coimbra"
- **Screen 2**: Rota linear com 11 pontos turísticos

### Para Desenvolvedores 🔧
1. Clone o repositório (ver Setup acima)
2. Inicie servidor local
3. Aceda a `http://localhost:8000`
4. **Teste os screens disponíveis:**
   - `http://localhost:8000/index.html` - Screen 1
   - `http://localhost:8000/screen2.html` - Screen 2 (Rota)
5. Leia [SCREEN2_IMPLEMENTATION.md](./SCREEN2_IMPLEMENTATION.md) para entender o padrão implementado
6. Leia [DESIGN_SYSTEM.md](./DESIGN_SYSTEM.md) para documentação do sistema de componentes
7. Consulte [.github/CONTRIBUTING.md](./.github/CONTRIBUTING.md) para contribuir

---

## 🧪 Testar Responsividade

### Método 1: GitHub Pages (Recomendado para Utilizadores)
1. Abra no telemóvel o link: https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/
2. Rode o telemóvel para testar landscape
3. Teste em tablets também

### Método 2: Chrome DevTools (Para Programadores)
```
1. Abra http://localhost:8000 no Chrome
2. Pressione F12 (ou Cmd+Option+I no Mac)
3. Clique no ícone de device (Ctrl+Shift+M)
4. Seleccione diferentes dispositivos
5. Teste orientação
```

### Método 3: Redimensionar Janela
```
1. Abra http://localhost:8000
2. Redimensione manualmente a janela
3. Observe como o layout se adapta
```

### Método 4: Página de Teste Responsiva
```bash
# Abra test-responsive.html para múltiplos tamanhos
open test-responsive.html
```

---

## 🐛 Troubleshooting

### "Não consigo aceder ao link do GitHub Pages"
```
→ Certifique-se que GitHub Pages está ativado
→ Verifique: Settings → Pages → Source
→ A branch deve estar configurada (main)
→ Aguarde 1-2 minutos para deploy
```

### "Imagens não carregam no GitHub Pages"
```
→ Verifique paths: ./Screens/imagens/
→ Certifique-se que ficheiros existem
→ Teste localmente primeiro: python -m http.server 8000
```

### "Servidor local não inicia"
```bash
# Tente outra porta
python -m http.server 8001

# Verifique se 8000 está ocupada
netstat -an | grep 8000  # Linux/Mac
netstat -an | findstr 8000  # Windows
```

### "Layout não responsivo localmente"
```
1. Limpe cache: Ctrl+Shift+Delete
2. Abra em modo incógnito: Ctrl+Shift+N
3. Teste em navegador diferente
4. Verifique viewport meta tag em index.html
```

---

## 💡 Dicas Úteis

### Sincronizar com GitHub
```bash
# Depois de editar localmente
git add .
git commit -m "Descrição da mudança"
git push origin main

# GitHub Pages fará deploy automaticamente (1-2 min)
```

### Ver Mudanças no GitHub Pages
```
1. Editado localmente
2. Faz git push
3. Aceda a Settings → Pages para ver status
4. Aguarde 1-2 minutos
5. Refresque: https://pedro-vieira-programmer.github.io/...
```

### Testar em Dispositivos Reais
```bash
# Descobrir IP local
ipconfig  # Windows
ifconfig  # Mac/Linux

# No dispositivo móvel, aceda a:
http://[SEU_IP]:8000
```

### Recarregar Cache
```
No navegador:
- Ctrl+Shift+R (Windows/Linux)
- Cmd+Shift+R (Mac)

Em DevTools:
- F12 → Settings → Disable cache (enquanto DevTools aberto)
```

---

## 📚 Documentação

| Tópico | Ficheiro |
|--------|----------|
| **Docs Técnicas** | [DESIGN_SYSTEM.md](./DESIGN_SYSTEM.md) |
| **Screen 2** | [SCREEN2_IMPLEMENTATION.md](./SCREEN2_IMPLEMENTATION.md) |
| **Setup Detalhado** | [orientation-files/SETUP.md](./orientation-files/SETUP.md) |
| **Como Contribuir** | [.github/CONTRIBUTING.md](./.github/CONTRIBUTING.md) |
| **Histórico** | [orientation-files/CHANGES.md](./orientation-files/CHANGES.md) |

---

## ✅ Próximas Ações

### Utilizadores Finais
- [ ] Aceder ao link: https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/
- [ ] Testar em diferentes dispositivos
- [ ] Desfrutar do projeto!

### Programadores
- [ ] Clonar repositório
- [ ] Iniciar servidor local
- [ ] Fazer alterações
- [ ] Fazer commit e push
- [ ] Ver atualizado no GitHub Pages

---

## 🆘 Precisa de Ajuda?

1. **Verifique FAQs** acima (Troubleshooting)
2. **Leia documentação** em [orientation-files/](./orientation-files/)
3. **Abra uma issue** no GitHub
4. **Consulte** [.github/CONTRIBUTING.md](./.github/CONTRIBUTING.md)

---

**Versão**: 2.1
**Atualizado**: 17 de Maio de 2026
**Status**: ✅ Pronto para GitHub Pages - Screen 1 + Screen 2

🎉 Bem-vindo! Divirta-se explorando "As Nossas Maravilhas de Coimbra"!
