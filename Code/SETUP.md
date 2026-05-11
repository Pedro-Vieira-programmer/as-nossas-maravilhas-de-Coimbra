# Guia de Implementação - Screen 1

## 📋 Resumo do Projeto

Conversão do design do Screen 1 do Figma em uma aplicação web responsiva que mantém 100% de fidelidade visual ao design original.

## 📁 Estrutura de Ficheiros Criada

```
Code/
├── index.html              # Ficheiro principal da aplicação
├── style.css               # Estilos responsivos
├── README.md               # Documentação completa
├── SETUP.md               # Este ficheiro
└── test-responsive.html    # Página de teste responsivo
```

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

## 🚀 Como Começar

### Opção 1: Abrir Ficheiro Diretamente
```bash
# Windows
start Code\index.html

# macOS
open Code/index.html

# Linux
xdg-open Code/index.html
```

### Opção 2: Servidor Local (Recomendado)

#### Usando Python (Recomendado)
```bash
cd Code
python -m http.server 8000
# Acesse http://localhost:8000
```

#### Usando Node.js
```bash
cd Code
npx http-server
```

#### Usando VS Code Live Server
1. Instale extensão "Live Server"
2. Abra index.html em VS Code
3. Clique direito > "Open with Live Server"

## 📱 Testar Responsividade

### Chrome DevTools (Melhor Opção)
1. Abra index.html no Chrome
2. Pressione `F12` para abrir DevTools
3. Clique no ícone de device toggle (`Ctrl+Shift+M` ou `Cmd+Shift+M`)
4. Teste diferentes dispositivos do dropdown
5. Verifique comportamento em diferentes tamanhos

### Teste Manual
1. Abra a página no navegador
2. Redimensione a janela
3. Observe como o layout se adapta
4. Teste em orientação paisagem (F11 para fullscreen)

### Página de Teste Dedicada
```bash
# Abra test-responsive.html para visualizar múltiplos dispositivos simultaneamente
start Code\test-responsive.html
```

## 🔧 Personalização Futura

### Adicionar Novos Ecrãs
Para converter os restantes 23 ecrãs:

1. **Prepare os assets:**
   ```bash
   cd Screens/screen2
   ls -la  # Confirme que tem todos os ficheiros .png necessários
   ```

2. **Crie novo ficheiro HTML:**
   - Copie o `index.html`
   - Renomeie para `screen2.html`
   - Atualize os paths das imagens para `../Screens/screen2/`
   - Ajuste o HTML conforme o novo design

3. **Adapte CSS se necessário:**
   - Adicione estilos específicos para o novo ecrã
   - Mantenha as mesmas convenções de media queries
   - Use as mesmas cores e fontes

### Modificar Cores
Se precisar ajustar cores mantendo o responsivo:

1. Abra `style.css`
2. Encontre as variáveis de cor (ex: `#d9a48b`)
3. Use CSS Custom Properties para facilitar:
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

## 📊 Breakpoints Explicados

| Tipo | Largura | Casos de Uso |
|------|---------|-------------|
| Extra Small | < 360px | Smartwatches, muito pequenos |
| Small | 360-480px | Maioria dos phones (iPhone SE, Galaxy A10) |
| Medium | 481-768px | Tablets pequenos, phones grandes |
| Large | 769px+ | Tablets grandes, Desktops |
| Landscape | Qualquer | Telefone em rotação |

## 🎨 Cores Utilizadas

```css
Coral/Peach (Button):  #d9a48b
Dark Text:             #1a1a1a
Gray Background:       #d3d3d3  (na imagem)
White:                 #ffffff
Light Gray (body):     #f5f5f5
```

## 🖼️ Imagens Utilizadas

- `polygon.png` - Hexágono decorativo (coral)
- `image1.png` - Mapa de Coimbra
- `result.png` - Torre/Igreja
- `rectange.png` - Retângulo cinzento
- `maintext.png` - Referência (não usado, texto renderizado)
- `button.png` - Referência (não usado, botão renderizado)

## 🐛 Troubleshooting

### Imagens não carregam
- Verifique que a pasta `Screens/screen1/` existe
- Confirme os paths: `../Screens/screen1/filename.png`
- Teste com servidor local em vez de ficheiro direto

### Layout não responsivo
- Confirme que tem `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Limpe cache do navegador (Ctrl+Shift+Delete)
- Teste em incógnito/private mode

### Botão não funciona
- Verifique que JavaScript está habilitado
- Abra console (F12) para ver mensagens
- Verifique função `handleStartClick()`

## 📝 Notas Importantes

1. **Caminhos de Ficheiros**: Os paths são relativos. Se mover os ficheiros, atualize os paths
2. **Servidor Local**: Recomendado para melhor compatibilidade e segurança
3. **Cache**: Se fizer alterações, limpe o cache ou use DevTools (Disable cache)
4. **Mobile Testing**: Sempre teste em dispositivos reais se possível

## 🔄 Próximos Passos

1. ✅ Teste o screen1 em vários dispositivos
2. ⬜ Adapte os restantes 23 ecrãs seguindo o mesmo padrão
3. ⬜ Implemente navegação entre ecrãs
4. ⬜ Otimize imagens se necessário
5. ⬜ Deploy em servidor web

## 📞 Suporte

Se encontrar problemas:

1. Verifique o console do navegador (F12 > Console)
2. Confirme os paths dos ficheiros
3. Teste com servidor local
4. Limpe cache e cookies
5. Use diferentes navegadores para teste

---

**Versão**: 1.0
**Data**: 2026-05-10
**Status**: ✅ Pronto para uso
