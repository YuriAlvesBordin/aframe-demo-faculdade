# 📋 Roteiro de Apresentação

## Introdução (~2 min)

- O que é o A-Frame?
- Por que usar? (sem build, só HTML, suporte a WebXR)
- Quem criou? (Mozilla, 2015)

---

## Demo 01 — Primitivos (~3 min)

Abrir `cenas/primitivos.html`

- Mostrar o HTML fonte — cada objeto é uma tag
- Destacar atributos: `position`, `color`, `rotation`
- Explicar o sistema de coordenadas (X, Y, Z)

```html
<!-- Cubo na posição x=-4, y=1, z=-5 -->
<a-box position="-4 1 -5" color="#64ffda"></a-box>
```

---

## Demo 02 — Materiais (~3 min)

Abrir `cenas/materiais.html`

- Mostrar diferença visual entre roughness e metalness
- Explicar PBR (Physically Based Rendering)
- Mostrar emissive e wireframe

```html
<!-- Material metálico espelhado -->
<a-sphere material="roughness:0; metalness:1"></a-sphere>
```

---

## Demo 03 — Animações (~3 min)

Abrir `cenas/animacoes.html`

- Mostrar animações declarativas (sem JS!)
- Explicar os parâmetros: `property`, `from/to`, `dur`, `dir`, `easing`
- Mostrar múltiplas animações em paralelo (`animation__1`, `animation__2`...)

```html
<a-box animation="property:rotation; to:0 360 0; loop:true; dur:3000">
</a-box>
```

---

## Conclusão (~1 min)

- A-Frame = WebXR acessível a qualquer dev web
- Funciona em desktop, mobile e headsets VR
- Ecossistema de componentes da comunidade (aframe-extras, etc.)

---

## Links úteis

- https://aframe.io/docs/
- https://github.com/aframevr/aframe
- https://aframe.io/aframe-school/ (tutorial interativo)
