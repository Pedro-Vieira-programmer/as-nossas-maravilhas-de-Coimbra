# As Nossas Maravilhas de Coimbra - Screen 1

## Descrição
Esta é a versão web responsiva do ecrã 1 do design Figma da aplicação "As Nossas Maravilhas de Coimbra".

## Estrutura de Ficheiros

```
Code/
├── index.html          # HTML semântico com toda a estrutura
├── style.css           # CSS responsivo com media queries
└── README.md           # Este ficheiro
```

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

### Opção 1: Abrir Diretamente
1. Abra `index.html` num navegador web (Firefox, Chrome, Safari, Edge, etc.)
2. O design carrega automaticamente com todas as imagens

### Opção 2: Servidor Local (Recomendado)
```bash
# Usando Python 3
python -m http.server 8000

# Usando Node.js/npm
npx http-server

# Usando Live Server no VS Code
# Instale a extensão Live Server e clique "Go Live"
```
Acesse `http://localhost:8000` ou a porta indicada

## Imagens Utilizadas

As imagens são referenciadas a partir da pasta `Screens/screen1`:
- `polygon.png` - Hexágono decorativo (coral)
- `image1.png` - Mapa de Coimbra
- `maintext.png` - Título (não utilizada no HTML - texto renderizado)
- `result.png` - Foto da Torre/Igreja
- `button.png` - Botão (não utilizada no HTML - botão renderizado)
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
1. Verifique se os ficheiros estão em `Screens/screen1/`
2. Certifique-se que os caminhos dos ficheiros estão corretos
3. Teste num navegador moderno (Chrome, Firefox, Safari, Edge)

---

**Versão**: 1.0
**Data**: 2026-05-10
**Status**: ✅ Completo - Screen 1 responsivo
