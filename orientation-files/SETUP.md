# Guia de Implementação e Desenvolvimento

## 📋 Resumo do Projeto

Conversão do design do Screen 1 do Figma em uma aplicação web responsiva hospedada em **GitHub Pages**.

## 🌐 Aceso Online (Utilizadores)

Link direto (sem instalação):
```
https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/
```

---

## 💻 Setup para Programadores/Desenvolvedores

### ⚡ Início Rápido (30 segundos)

#### 1. Clonar o Repositório
```bash
git clone https://github.com/Pedro-Vieira-programmer/as-nossas-maravilhas-de-coimbra.git
cd as-nossas-maravilhas-de-coimbra
```

#### 2. Iniciar Servidor Local

**Python (Recomendado):**
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
2. Abra index.html em VS Code
3. Clique direito > "Open with Live Server"

#### 3. Editar e Testar
- Modifique os ficheiros localmente
- Servidor recarrega automaticamente
- Teste responsividade (F12 → Device Toggle)

#### 4. Fazer Commit e Push
```bash
git add .
git commit -m "Descrição da mudança"
git push origin main
```

#### 5. GitHub Pages Deploy Automático
- GitHub Pages fará deploy em 1-2 minutos
- Verifique em: https://pedro-vieira-programmer.github.io/...

---

## 🎯 O Que Foi Implementado

### ✅ HTML Semântico
- Estrutura limpa e organizada
- Comentários explicativos
- Meta tags corretas (viewport, charset, etc.)
- Semântica apropriada (`<main>`, `<h1>`, `<button>`)

### ✅ CSS Responsivo
- Media queries para 5 breakpoints diferentes
- Suporte para orientação paisagem
- Suporte para notches/safe areas
- Flexbox e CSS Grid
- Transições suaves

### ✅ Design Preservado
- Cores exatamente iguais
- Textos exatamente iguais
- Todas as imagens originais referenciadas
- Ícones inalterados
- Tamanhos, margens e espaçamentos mantidos
- Sombras, bordas e cantos arredondados

### ✅ Compatibilidade
- Chrome, Firefox, Safari, Edge
- Desktop, Tablet, Mobile
- Todos os tamanhos de tela
- Orientações Portrait e Landscape

---

## 📁 Estrutura de Ficheiros

```
.
├── index.html              # Ficheiro principal da aplicação
├── style.css               # Estilos responsivos
├── test-responsive.html    # Página de teste responsivo
│
├── Screens/
│   ├── imagens/           # Assets dos ecrãs (Screen 1)
│   └── screen1/           # (Original, mantido)
│
└── orientation-files/      # Documentação
    ├── README.md
    ├── SETUP.md
    └── ...
```

---

## 📱 Testar Responsividade

### Localmente (Chrome DevTools)
1. Abra `http://localhost:8000` no Chrome
2. Pressione `F12` para abrir DevTools
3. Clique no ícone de device (`Ctrl+Shift+M`)
4. Teste diferentes dispositivos do dropdown
5. Verifique comportamento em diferentes tamanhos

### Teste Manual
1. Abra a página no navegador
2. Redimensione a janela
3. Observe como o layout se adapta
4. Teste em orientação paisagem

### Página de Teste Dedicada
```bash
# Abra test-responsive.html para visualizar múltiplos dispositivos simultaneamente
start test-responsive.html
```

### Telemóvel Real
1. Descobra seu IP local: `ipconfig` (Windows) ou `ifconfig` (Mac/Linux)
2. No telemóvel, aceda a: `http://[SEU_IP]:8000`
3. Rode o telemóvel para testar landscape

---

## 🔄 Editar e Atualizar Ficheiros

### Ficheiros Principais (Não criar novos)

**Editar em vez de criar:**
- `index.html` - Estrutura
- `style.css` - Estilos
- `GETTING_STARTED.md` - Guia de acesso
- `README.md` - Overview

**Localização:**
- HTML/CSS: Raiz do projeto
- Docs: `orientation-files/`

### Workflow de Edição

```bash
# 1. Fazer mudança
# Edite index.html ou style.css

# 2. Testar localmente
# http://localhost:8000 (auto-reload)

# 3. Verificar responsividade
# F12 → Device Toggle

# 4. Commit
git add .
git commit -m "Descrição clara da mudança"

# 5. Push
git push origin main

# 6. GitHub Pages atualiza automaticamente
# Aguarde 1-2 minutos
# Verifique em: https://pedro-vieira-programmer.github.io/...
```

---

## 🔧 Personalização Futura

### Adicionar Novos Ecrãs
Para converter os restantes 23 ecrãs:

1. **Prepare os assets:**
   ```bash
   ls Screens/imagens/  # Confirme assets existem
   ```

2. **Crie novo ficheiro HTML:**
   - Copie o `index.html`
   - Renomeie para `screen2.html`
   - Atualize os paths das imagens para `./Screens/imagens/`
   - Ajuste o HTML conforme o novo design

3. **Adapte CSS:**
   - Adicione estilos específicos para o novo ecrã
   - Mantenha convenções de media queries
   - Use as mesmas cores e fontes

### Modificar Cores
Se precisar ajustar cores:

1. Abra `style.css`
2. Encontre as variáveis de cor (ex: `#d9a48b`)
3. Considere usar CSS Custom Properties:
   ```css
   :root {
       --coral-button: #d9a48b;
       --dark-text: #1a1a1a;
       --gray-bg: #d3d3d3;
   }
   ```

### Adicionar Funcionalidades JavaScript
O ficheiro `index.html` já tem um espaço para JavaScript:
```javascript
function handleStartClick() {
    console.log('Iniciar clicado');
    // Adicione aqui a lógica de navegação
}
```

---

## 📊 Breakpoints Explicados

| Tipo | Largura | Casos de Uso |
|------|---------|-------------|
| Extra Small | < 360px | Smartwatches, muito pequenos |
| Small | 360-480px | Maioria dos phones (iPhone SE, Galaxy A10) |
| Medium | 481-768px | Tablets pequenos, phones grandes |
| Large | 769px+ | Tablets grandes, Desktops |
| Landscape | Qualquer | Telefone em rotação |

---

## 🎨 Cores Utilizadas

```css
Coral/Peach (Button):  #d9a48b
Dark Text:             #1a1a1a
Gray Background:       #d3d3d3  (na imagem)
White:                 #ffffff
Light Gray (body):     #f5f5f5
```

---

## 🖼️ Imagens Utilizadas

Localizadas em `Screens/imagens/`:
- `polygon.png` - Hexágono decorativo (coral)
- `image1.png` - Mapa de Coimbra
- `university.png` - Universidade de Coimbra
- `rectange.png` - Retângulo cinzento

---

## 🐛 Troubleshooting

### Imagens não carregam (Local)
- Verifique que a pasta `Screens/imagens/` existe
- Confirme os paths: `./Screens/imagens/filename.png`
- Teste com servidor local em vez de ficheiro direto

### Imagens não carregam (GitHub Pages)
- Verifique GitHub Pages está ativado em Settings
- Confirme paths no código
- Aguarde 1-2 minutos após push
- Limpe cache do navegador

### Layout não responsivo
- Confirme que tem `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Limpe cache do navegador (Ctrl+Shift+Delete)
- Teste em incógnito/private mode

### Botão não funciona
- Verifique que JavaScript está habilitado
- Abra console (F12) para ver mensagens
- Verifique função `handleStartClick()`

### Servidor local não inicia
```bash
# Tente outra porta
python -m http.server 8001

# Verifique se 8000 está ocupada
netstat -an | grep 8000  # Linux/Mac
netstat -an | findstr 8000  # Windows
```

---

## 📝 Notas Importantes

1. **Caminhos de Ficheiros**: Os paths são relativos. Se mover os ficheiros, atualize os paths
2. **GitHub Pages**: Recarrega automaticamente após push (1-2 min)
3. **Cache**: Se fizer alterações, limpe o cache ou use DevTools (Disable cache)
4. **Mobile Testing**: Sempre teste em dispositivos reais se possível
5. **Editar, não Criar**: Atualize ficheiros existentes em vez de criar novos

---

## 🔄 Próximos Passos

1. ✅ Screen 1 implementado
2. ⬜ Screens 2-24 em desenvolvimento
3. ⬜ Navegação entre screens
4. ⬜ Animações e interações
5. ⬜ Backend (se necessário)

---

## 📞 Suporte

Se encontrar problemas:

1. Verifique o console do navegador (F12 > Console)
2. Confirme os paths dos ficheiros
3. Teste com servidor local
4. Limpe cache e cookies
5. Use diferentes navegadores para teste

---

**Versão**: 2.0
**Data**: 2026-05-13
**Status**: ✅ Pronto para uso
**Hospedagem**: ✅ GitHub Pages
**Método de Acesso**: 🌐 Link online (sem instalação)
