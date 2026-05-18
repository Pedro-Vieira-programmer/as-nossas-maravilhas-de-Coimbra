# 🚀 Deployment - GitHub Pages

Documentação para publicação e manutenção em GitHub Pages.

## 📋 Status Atual

| Item | Status | URL |
|------|--------|-----|
| GitHub Pages | ✅ Ativo | https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/ |
| Repositório | ✅ Público | https://github.com/Pedro-Vieira-programmer/as-nossas-maravilhas-de-coimbra |
| Certificado SSL | ✅ Automático | HTTPS certificado |
| Build | ✅ Automático | Sem build necessário (static files) |

---

## 🔧 Configuração GitHub Pages

### 1. Verificar Configuração

No repositório GitHub:
1. Ir a **Settings** → **Pages**
2. Verificar:
   - ✅ Source: `Deploy from a branch`
   - ✅ Branch: `main` (ou `master`)
   - ✅ Folder: `/ (root)`

### 2. Tempo de Deploy

Após `git push`:
- ⏱️ 30 segundos a 2 minutos para publicar
- Verifique: [Actions tab](https://github.com/Pedro-Vieira-programmer/as-nossas-maravilhas-de-coimbra/actions)

---

## 📝 Workflow de Atualização

### Para Programadores

```bash
# 1. Clonar repositório
git clone https://github.com/Pedro-Vieira-programmer/as-nossas-maravilhas-de-coimbra.git
cd as-nossas-maravilhas-de-coimbra

# 2. Criar branch de feature
git checkout -b feature/melhoria-xyz

# 3. Fazer alterações locais
# ... edite ficheiros ...

# 4. Testar localmente
python -m http.server 8000
# Aceda a http://localhost:8000

# 5. Commit e push
git add .
git commit -m "Descrição clara da mudança"
git push origin feature/melhoria-xyz

# 6. Criar Pull Request no GitHub
# → GitHub UI → Compare & pull request

# 7. Après merge no main
# → Deploy automático em 1-2 minutos
```

### Verificação de Publicação

```bash
# Refresque a página publicada
https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/

# Ou verifique o histórico de deploy
# GitHub → Settings → Pages → Deployment history
```

---

## ⚙️ Estrutura para Produção

### Ficheiros Críticos (não delete)

```
✅ index.html                   # Screen 1 - Landing
✅ screen2.html ... screen24.html # Todos os screens
✅ components.css               # Design system (CRÍTICO)
✅ style.css, screenX.css       # Estilos específicos
✅ Screens/                     # Pasta com todas as imagens
✅ icon.png                     # Favicon
✅ .gitignore                   # Configuração git
✅ README.md                    # Documentação principal
```

### Ficheiros Opcionais (pode limpar)

```
⚠️  test-responsive.html        # Apenas para testes (pode remover)
⚠️  reorganizar_novo.py         # Scripts internos (pode remover)
⚠️  orientation-files/          # Documentação auxiliar (pode mover)
⚠️  RESTRUCTURING_SUMMARY.md    # Histórico (pode arquivar)
```

---

## 🔍 Monitoramento

### Check-list Mensal

- [ ] Aceda ao link publicado
- [ ] Teste em diferentes navegadores (Chrome, Firefox, Safari)
- [ ] Teste em mobile (360px, 768px, 1920px)
- [ ] Teste modo landscape
- [ ] Verifique se imagens carregam
- [ ] Verifique navegação entre screens

### Troubleshooting

#### Problema: Página não atualiza após push

```
Solução:
1. Aguarde 2 minutos
2. Limpe cache: Ctrl+Shift+Delete
3. Abra em modo incógnito: Ctrl+Shift+N
4. Verifique GitHub Actions → Deploy status
```

#### Problema: Imagens não carregam

```
Solução:
1. Verifique: Screens/ folder existe
2. Verifique paths em HTML: ./Screens/screenX/...
3. Teste localmente: python -m http.server
4. Confirm ficheiros fazem git add
```

#### Problema: Layout quebrado no GitHub Pages

```
Solução:
1. Verifique viewport meta tag em HTML
2. Verifique CSS imports: components.css ANTES de screenX.css
3. Teste em navegador diferente
4. Abra console (F12) para ver erros
```

---

## 📊 Métricas e Performance

### Tamanho do Repositório
- Ficheiros HTML: ~25 ficheiros × ~3KB = 75KB
- CSS: ~3-4 ficheiros × ~10KB = 40KB
- Imagens: Screens/ folder = ~50-100MB (depende dos assets)
- **Total**: ~100-150MB (aceitável para GitHub)

### Performance GitHub Pages
- Load time: < 2 segundos (sem imagens grandes)
- Cache: Automático via CloudFlare
- CDN: Global (GitHub + CloudFlare)

---

## 🔐 Segurança

### Configurado

- ✅ HTTPS automático (certificado Let's Encrypt)
- ✅ Repositório privado ou público (defina a preferência)
- ✅ Sem dados sensíveis (projeto estático)
- ✅ Sem APIs externas (exceto Google Maps opcional)

### Recomendações

- ✅ Mantenha `.gitignore` atualizado
- ✅ Nunca commit chaves API (se adicionar depois)
- ✅ Revise pull requests antes de merge
- ✅ Use ramos para features em desenvolvimento

---

## 📱 Versões

### Versionamento Semântico

```
X.Y.Z

X = Major  (novo screen, alteração de arquitetura)
Y = Minor  (novo componente, melhoria)
Z = Patch  (bug fix, otimização)

Exemplo:
v3.0.0 - 24 Screens completos (major)
v3.1.0 - Novo componente UI (minor)
v3.1.1 - Bug fix responsivo (patch)
```

### Tag Releases

```bash
# Criar tag (após completar versão)
git tag -a v3.0.0 -m "24 Screens completos"
git push origin v3.0.0

# Ver no GitHub → Releases
```

---

## 📞 Suporte Técnico

### Recursos

| Tópico | Ficheiro |
|--------|----------|
| **Arquitectura** | [ARCHITECTURE.md](./ARCHITECTURE.md) |
| **Design System** | [DESIGN_SYSTEM.md](./DESIGN_SYSTEM.md) |
| **Início Rápido** | [GETTING_STARTED.md](./GETTING_STARTED.md) |
| **Contribuir** | [.github/CONTRIBUTING.md](./.github/CONTRIBUTING.md) |

### Checklist Pre-Deploy

- [ ] Todos os 24 screens testados
- [ ] CSS sem erros (console F12 limpo)
- [ ] Imagens carregam corretamente
- [ ] Navegação entre screens funciona
- [ ] Responsivo em mobile/tablet/desktop
- [ ] README atualizado
- [ ] Commits com mensagens descritivas
- [ ] Branch main pronta para deploy

---

## 🎉 Publicado com Sucesso

A aplicação está publicada e acessível em:

👉 **https://pedro-vieira-programmer.github.io/as-nossas-maravilhas-de-coimbra/**

**Versão**: 3.0  
**Data**: 2026-05-18  
**Status**: ✅ Em Produção  
**Desenvolvedor**: Pedro Vieira  
**Co-autoria**: Copilot
