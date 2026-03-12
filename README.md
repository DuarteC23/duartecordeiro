# Duarte Cordeiro — Portfolio

Site de portfolio pessoal com feed estilo Instagram. Fácil de gerir e publicar no GitHub Pages.

---

## 🚀 Como publicar no GitHub Pages

1. Cria um repositório no GitHub (ex: `duarte-cordeiro-portfolio`)
2. Faz upload de todos estes ficheiros para o repositório
3. Vai a **Settings → Pages**
4. Em **Source**, seleciona `Deploy from a branch` → `main` → `/ (root)`
5. Clica **Save** — o site fica online em `https://teu-username.github.io/duarte-cordeiro-portfolio/`

---

## 📁 Estrutura de ficheiros

```
portfolio/
├── index.html              ← página principal (não precisas editar)
├── css/
│   └── style.css           ← estilos (não precisas editar)
├── js/
│   ├── media-config.js     ← ✏️ EDITA AQUI para adicionar/remover conteúdo
│   └── main.js             ← lógica do site (não precisas editar)
└── media/
    ├── logo.png            ← ✏️ coloca aqui o teu logo
    ├── foto1.jpg           ← as tuas fotos
    ├── video1.mp4          ← os teus vídeos
    └── ...
```

---

## ➕ Como adicionar uma foto ou vídeo

1. **Coloca o ficheiro** na pasta `media/`
2. **Abre** `js/media-config.js`
3. **Adiciona uma linha** dentro do array `MEDIA`:

```js
// FOTO:
{ src: "nome-do-ficheiro.jpg", type: "photo", ratio: "portrait", label: "Título opcional" },

// VÍDEO:
{ src: "nome-do-video.mp4", type: "video", ratio: "landscape", wide: true, label: "Título opcional" },
```

### Opções de `ratio`:
| Valor | Proporção | Uso recomendado |
|-------|-----------|-----------------|
| `"portrait"` | 4:5 | Fotos verticais |
| `"square"` | 1:1 | Fotos quadradas |
| `"landscape"` | 16:9 | Fotos/vídeos horizontais |

### `wide: true`
Adiciona `wide: true` para o item ocupar **2 colunas** (bom para paisagens e vídeos).

---

## ➖ Como remover conteúdo

No ficheiro `js/media-config.js`, **apaga ou comenta** a linha do item:

```js
// { src: "foto-antiga.jpg", type: "photo", ratio: "portrait" },
```

---

## 🖼️ Logo

Substitui o ficheiro `media/logo.png` pelo teu logo (PNG com fundo transparente, versão branca).

---

## 📐 Ordem do conteúdo

Os itens aparecem no feed **pela mesma ordem** que estão no ficheiro `media-config.js`. Para reordenar, basta mover as linhas.

---

## 💡 Dicas

- Para vídeos mais leves no site, usa ficheiros `.mp4` comprimidos (H.264)
- As fotos devem ter no máximo 2–3 MB cada para carregarem rápido
- Podes misturar fotos e vídeos à vontade — o feed adapta-se automaticamente
