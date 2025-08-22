---
title: Início
nav_order: 1
permalink: /
---

<style>
:root { --qe-max: 1100px; }
.qe-hero { text-align:center; padding:2.5rem 1rem 2rem; margin:0 auto 1rem; max-width:var(--qe-max); }
.qe-logo { width:120px; height:auto; border-radius:8px; margin-bottom:.75rem; }
.qe-hero h1 { margin:.25rem 0 .5rem; font-weight:700; }
.qe-hero p { margin:.25rem 0 .75rem; }
.qe-cards { display:grid; gap:1rem; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); margin:0 auto 2rem; max-width:var(--qe-max); }
.qe-card { padding:1rem; border:1px solid var(--color-border,#ddd); border-radius:.5rem; background:var(--color-canvas-subtle,#fff); }
.qe-card h3 { margin-top:.25rem; }
.qe-card .btn { display:inline-block; margin-top:.25rem; }
.qe-footer { text-align:center; margin:2rem auto 0; max-width:var(--qe-max); opacity:.85; }
</style>

<div class="qe-hero">
  <img src="{{ '/assets/Paulo_C_Coimbra_Academy_logo.jpg' | relative_url }}" alt="Paulo C. Coimbra Academy" class="qe-logo">
  <h1>QuantEcon — Ciência de Dados e IA aplicados à Economia e Finanças</h1>
  <p>Projeto de extensão da UFJF coordenado pelo Prof. Paulo C. Coimbra</p>
  <p><a class="btn btn-primary" href="{{ '/docs/sobre' | relative_url }}">Conheça o projeto</a></p>
</div>

## Destaques

<div class="qe-cards">
  <div class="qe-card">
    <h3>📊 Boletim Econômico</h3>
    <p>Visualizações interativas e análises semanais</p>
    <p><a class="btn" href="{{ '/docs/boletins' | relative_url }}">Ver boletim</a></p>
  </div>
  <div class="qe-card">
    <h3>🎓 Minicurso Python</h3>
    <p>Trilha formativa com certificado</p>
    <p><a class="btn" href="{{ '/docs/minicursos' | relative_url }}">Acessar minicurso</a></p>
  </div>
  <div class="qe-card">
    <h3>🧪 Tutorial IA</h3>
    <p>Notebooks interativos com passo a passo</p>
    <p><a class="btn" href="{{ '/docs/tutoriais' | relative_url }}">Ver tutorial</a></p>
  </div>
</div>

---

<p class="qe-footer">
  Projeto de Extensão | Universidade Federal de Juiz de Fora — 
  Contato: <a href="mailto:paulo.coimbra@ufjf.br">paulo.coimbra@ufjf.br</a> — Licença MIT
</p>
