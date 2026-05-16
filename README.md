# aframe-demo-faculdade

Demonstração interativa da biblioteca [A-Frame](https://aframe.io) para criação de cenas 3D no navegador via WebXR. Desenvolvido como projeto acadêmico para a disciplina de Computação Gráfica.

**Autor:** Yuri Alves Bordin

---

## Sobre o A-Frame

A-Frame é uma biblioteca web de código aberto desenvolvida pela Mozilla que permite construir experiências 3D e de Realidade Virtual (WebVR/WebXR) usando HTML declarativo. Internamente é construída sobre o [Three.js](https://threejs.org) e segue o padrão arquitetural **Entity-Component System (ECS)**, onde cada elemento da cena é uma entidade que recebe comportamentos por meio de componentes.

O diferencial é permitir que cenas 3D completas sejam descritas em HTML puro, sem pipeline de build, bundler ou configuração de ambiente:

```html
<a-scene>
  <a-box color="#4CC3D9" position="0 1 -3"></a-box>
  <a-camera></a-camera>
</a-scene>
```

---

## Estrutura do Projeto

```
aframe-demo-faculdade/
|
+-- index.html              # Pagina inicial com navegacao entre as demos
|
+-- cenas/
|   +-- primitivos.html     # Demo 1 — Primitivos geometricos com morphing
|   +-- materiais.html      # Demo 2 — Modelo atomico com iluminacao dinamica
|   +-- animacoes.html      # Demo 3 — Importacao de modelos 3D externos
|
+-- docs/
|   +-- roteiro.md          # Roteiro para apresentacao oral
|
+-- .gitignore
```

---

## Como Executar

Nao ha dependencias ou etapas de build. Sirva os arquivos localmente:

```bash
# Python
python -m http.server 8080

# Node.js
npx serve .
```

Acesse `http://localhost:8080` no navegador.

> **Nota:** abrir via `file://` pode causar erros de CORS em alguns navegadores. Recomenda-se usar um servidor local.

---

## Demos

### Demo 1 — Primitivos em Morphing

Exibe os primitivos geometricos nativos do A-Frame (`<a-box>`, `<a-sphere>`, `<a-cylinder>`, `<a-cone>`, `<a-torus>`, `<a-torus-knot>`, `<a-icosahedron>`, entre outros) com transicoes automaticas entre formas a cada 2,8 segundos. Cada troca aplica um material PBR aleatorio, variando `roughness`, `metalness`, `opacity`, `emissive` e `wireframe`.

### Demo 2 — Modelo Atomico

Simulacao de um atomo com nucleo central e eletrons orbitando em planos distribuidos tridimensionalmente. A quantidade de eletrons e configuravel em tempo real via slider (1 a 10). Cada eletron emite luz pontual colorida e transiciona continuamente entre cores via interpolacao HSL, iluminando o nucleo e os eletrons vizinhos.

### Demo 3 — Importacao de Modelo 3D

Permite carregar um arquivo `.glb`, `.gltf` ou `.obj` do sistema de arquivos local via drag-and-drop ou seletor de arquivo. O modelo e centralizado e escalonado automaticamente. A cena oferece controles de orbita estilo Blender: arrastar para orbitar, scroll para zoom e botao direito para pan. Suporte completo a toque em dispositivos moveis.

---

## Controles

| Acao | Mouse | Touch |
|---|---|---|
| Orbitar a camera | Clicar e arrastar | Um dedo |
| Zoom | Scroll | Pinch (dois dedos) |
| Pan | Botao direito + arrastar | — |

As demos 1 e 2 utilizam os controles nativos de look do A-Frame (`look-controls` + `wasd-controls`).

---

## Compatibilidade

Testado nos navegadores modernos com suporte a WebGL 2.0:

- Google Chrome 120+
- Mozilla Firefox 120+
- Microsoft Edge 120+
- Safari 17+ (suporte parcial a WebXR)

---

<sub>Projeto academico — uso educacional.</sub>
