---
title: Início
nav_order: 1
permalink: /
---

<!-- ==================  CSS inline: sidebar 200px + FULL-WIDTH  ================== -->
<style>
  :root { --sidebar-w: 200px; }

  /* Sidebar com 200px e conteúdo deslocado (desktop) */
  @media (min-width: 66rem){
    .side-bar{ width: var(--sidebar-w); }
    .main, .main-content-wrap{ margin-left: var(--sidebar-w); }
  }

  /* Conteúdo SEM limite de largura SEMPRE (full-width),
     mas você pode trocar por 1200px se preferir limitar:
     .main-content{ max-width: 1200px !important; } */
  .main-content{ max-width: none !important; }
  .main-content, .main-content-wrap, .main{ width: auto; }

  /* Transições suaves */
  .side-bar, .main, .main-content-wrap{ transition: margin-left .2s ease, transform .2s ease; }

  /* Estado recolhido: sidebar sai e o conteúdo ocupa TUDO (sem recuo) */
  body.jtd-collapsed .side-bar{ transform: translateX(-100%); }
  body.jtd-collapsed .main, 
  body.jtd-collapsed .main-content-wrap{ margin-left: 0 !important; }

  /* Botão ☰ fixo e discreto (mostrado só em telas largas) */
  #jtd-toggle{
    position: fixed; top: .75rem; left: .75rem; z-index: 9999;
    width: 2.1rem; height: 2.1rem; padding: 0;
    display: none; align-items: center; justify-content: center;
    border: 1px solid var(--color-border, #3a3a3a);
    background: var(--color-canvas, #111);
    color: var(--color-fg-default, #fff);
    border-radius: .375rem; cursor: pointer; line-height: 1;
  }
  @media (min-width: 66rem){ #jtd-toggle{ display: inline-flex; } }
  /* Quando a sidebar está aberta, empurra o botão para a direita da sidebar */
  @media (min-width: 66rem){
    body:not(.jtd-collapsed) #jtd-toggle{ left: calc(var(--sidebar-w) + .75rem); }
  }
</style>

<!-- ==================  Botão ☰ no DOM  ================== -->
<button id="jtd-toggle" aria-label="Alternar barra lateral">☰</button>

{% include topnav.html %}

<div class="qe-hero">
  <h1>QuantEcon — Ciência de Dados e IA aplicados à Economia e Finanças</h1>
  <p>Projeto de extensão da UFJF coordenado pelo Prof. Paulo C. Coimbra</p>
  <p><a class="btn btn-primary" href="{{ '/sobre/' | relative_url }}">Conheça o projeto</a></p>
</div>

## Destaques

<div class="qe-cards">
  <div class="qe-card">
    <h3>📊 Boletim Econômico</h3>
    <p>Visualizações interativas e análises semanais</p>
    <p><a class="btn" href="{{ '/boletim/' | relative_url }}">Ver boletim</a></p>
  </div>
  <div class="qe-card">
    <h3>🎓 Minicurso Python</h3>
    <p>Trilha formativa com certificado</p>
    <p><a class="btn" href="{{ '/minicurso/' | relative_url }}">Acessar minicurso</a></p>
  </div>
  <div class="qe-card">
    <h3>🧪 Tutorial IA</h3>
    <p>Notebooks interativos com passo a passo</p>
    <p><a class="btn" href="{{ '/tutorial/' | relative_url }}">Ver tutorial</a></p>
  </div>
</div>

---

<p class="qe-footer">
  Projeto de Extensão | Universidade Federal de Juiz de Fora — 
  Contato: <a href="mailto:paulo.coimbra@ufjf.br">paulo.coimbra@ufjf.br</a> — Licença MIT
</p>

<!-- ==================  JS inline: toggle e preferência  ================== -->
<script>
(function(){
  var KEY = 'jtd-collapsed::{{ site.baseurl }}';

  // Restaura preferência
  if (localStorage.getItem(KEY) === 'true') {
    document.body.classList.add('jtd-collapsed');
  }

  var btn = document.getElementById('jtd-toggle');
  if (!btn) return;

  btn.addEventListener('click', function(){
    document.body.classList.toggle('jtd-collapsed');
    localStorage.setItem(KEY, document.body.classList.contains('jtd-collapsed'));
  });
})();
</script>
