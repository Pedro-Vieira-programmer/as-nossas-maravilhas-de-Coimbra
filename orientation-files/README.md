# As Nossas Maravilhas de Coimbra - Documentação Técnica

## 🌐 Aceso Online
```
https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/
```
Hospedado em **GitHub Pages** - Sem necessidade de instalação!

## Descrição
Esta é a versão web responsiva do ecrã 1 do design Figma da aplicação "As Nossas Maravilhas de Coimbra".

## Funcionamento

### Compatibilidade
- ✅ Desktop (1920px até 1366px)
- ✅ Tablet (768px até 1024px)
- ✅ Mobile (360px até 768px)
- ✅ Orientação Paisagem (Landscape)
- ✅ Dispositivos com Notch/Safe Area

### Características Responsivas
- **Mobile-First**: Design otimizado para mobile
- **Media Queries**: 5 breakpoints diferentes
- **Viewport Meta Tag**: Suporte para todos os devices
- **Aspect Ratio**: Mantém proporções do design
- **Flexible Layout**: Layout adapta-se sem perder fidelidade visual

### Design Preservado
✅ Todas as cores exatamente iguais
✅ Todos os textos exatamente iguais
✅ Todas as imagens originais (sem alteração)
✅ Ícones inalterados (seta ↑)
✅ Tamanhos, margens e espaçamentos mantidos
✅ Sombras, bordas e cantos arredondados preservados
✅ Sem elementos adicionados ou removidos
✅ Máxima fidelidade visual

## Como Usar

### Opção 1: Aceder Online (Recomendado para Utilizadores)
Basta abrir no navegador:
```
https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/
```

### Opção 2: Desenvolvimento Local (Para Programadores)

**Clone o repositório:**
```bash
git clone https://github.com/Pedro-Vieira-programmer/as-nossas-maravilhas-de-coimbra.git
cd as-nossas-maravilhas-de-coimbra
```

**Inicie servidor local:**
```bash
# Python (recomendado)
python -m http.server 8000

# Node.js
npx http-server

# VS Code Live Server
# Clique direito em index.html → "Open with Live Server"
```

**Aceda a:**
```
http://localhost:8000
```

## Imagens Utilizadas

As imagens estão localizadas em `Screens/imagens/`:
- `polygon.png` - Hexágono decorativo (coral)
- `image1.png` - Mapa de Coimbra
- `university.png` - Universidade de Coimbra
- `rectange.png` - Retângulo cinzento do fundo

## Breakpoints de Responsive Design

| Dispositivo | Largura | Aplicação |
|------------|---------|-----------|
| Extra Small | < 360px | Smartwatches, pequenos phones |
| Small | 360-480px | Phones (iPhone SE, iPhone 11, etc) |
| Medium | 481-768px | Tablets pequenos |
| Large | 769px+ | Tablets grandes, Desktops |
| Landscape | Qualquer | Orientação paisagem |

## Cores

- **Coral/Peach Button**: `#d9a48b`
- **Dark Text**: `#1a1a1a`
- **Light Gray Background**: `#d3d3d3` (na imagem rectange.png)
- **White**: `#ffffff`

## Desenvolvimento Futuro

Para adicionar os restantes 23 ecrãs:
1. Prepare os assets na pasta `Screens/screenX`
2. Crie `screenX.html` baseado neste template
3. Adapte o CSS conforme necessário
4. Mantenha a mesma estrutura e convenções

## Notas Técnicas

- Uso de CSS Grid e Flexbox para layout responsivo
- Media queries para diferentes tamanhos de viewport
- Suporte para safe areas (notches em iPhones)
- Transições suaves no botão
- Sem dependências externas (CSS puro e HTML semântico)
- Otimizado para performance

## Suporte

Se encontrar problemas com imagens:
1. Verifique se os ficheiros estão em `Screens/imagens/`
2. Certifique-se que os caminhos dos ficheiros estão corretos
3. Teste num navegador moderno (Chrome, Firefox, Safari, Edge)

---

**Versão**: 2.0
**Data**: 2026-05-13
**Status**: ✅ Completo - Screen 1 responsivo
**Hospedagem**: ✅ GitHub Pages (Online)
