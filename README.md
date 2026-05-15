# 🎓 A-Frame Demo — Projeto de Faculdade

> **Disciplina:** Computação Gráfica / Desenvolvimento Web  
> **Aluno:** Yuri Alves Bordin  
> **Objetivo:** Demonstrar o uso da biblioteca [A-Frame](https://aframe.io) para criação de cenas 3D interativas no navegador, sem necessidade de build ou configuração.

---

## 📌 O que é o A-Frame?

[A-Frame](https://aframe.io) é uma biblioteca web criada pela Mozilla que permite construir experiências 3D e de Realidade Virtual (WebVR/WebXR) usando **somente HTML**. Ela é construída sobre o Three.js e segue o padrão de **Entity-Component System (ECS)**.

```html
<!-- Isso já é uma cena 3D funcional! -->
<a-scene>
  <a-box color="red" position="0 1 -3"></a-box>
  <a-camera></a-camera>
</a-scene>
```

---

## 📁 Estrutura do Projeto

```
aframe-demo-faculdade/
│
├── index.html            # Página inicial com menu das demos
│
├── cenas/
│   ├── primitivos.html   # Demo 1 — Primitivos 3D
│   ├── materiais.html    # Demo 2 — Materiais e Texturas
│   └── animacoes.html    # Demo 3 — Sistema de Animação
│
└── docs/
    └── roteiro.md        # Roteiro/anotações para apresentação
```

---

## 🚀 Como rodar

Não precisa de instalação. Basta abrir os arquivos `.html` no navegador:

```bash
# Opção 1 — abrir direto
open index.html

# Opção 2 — servidor local simples (recomendado)
npx serve .
# ou
python -m http.server 8080
```

---

## 🎮 Controles das cenas

| Ação | Controle |
|------|----------|
| Girar câmera | Clicar e arrastar |
| Mover | `WASD` |
| Zoom | Scroll do mouse |
| VR (se disponível) | Botão no canto inferior direito |

---

## 📚 Demos incluídas

### Demo 1 — Primitivos 3D
Demonstra as geometrias nativas do A-Frame: `<a-box>`, `<a-sphere>`, `<a-cylinder>`, `<a-cone>`, `<a-torus>`, `<a-plane>`.

### Demo 2 — Materiais e Texturas
Explora o sistema de materiais PBR: `roughness`, `metalness`, `opacity`, `emissive`, `wireframe`.

### Demo 3 — Animações
Mostra o sistema declarativo de animação via atributo `animation`: posição, rotação, escala e cor.

---

## 🔗 Referências

- [Documentação oficial — aframe.io/docs](https://aframe.io/docs/)
- [Repositório no GitHub — github.com/aframevr/aframe](https://github.com/aframevr/aframe)
- [Three.js — threejs.org](https://threejs.org)
- [WebXR Device API — MDN](https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API)

---

<sub>Projeto acadêmico — uso educacional</sub>
