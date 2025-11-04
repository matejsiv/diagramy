# R markdown page
<!--
This Markdown document contains **only** the HTML/CSS needed to display responsive buttons.
Open this file in a Markdown renderer that supports raw HTML (GitHub, VS Code, most static site generators).
-->

<style>
  /* Reset minimal */
  :root{
    --gap: 0.75rem;
    --min-button-width: 160px;
  }
  html,body{height:100%;margin:0;padding:0}
  .btn-grid{
    box-sizing:border-box;
    min-height:100vh; /* full-screen vertical center */
    display:grid;
    /* auto-fit creates as many columns as fit, each at least minmax */
    grid-template-columns: repeat(auto-fit, minmax(var(--min-button-width), 1fr));
    gap:var(--gap);
    padding:calc(var(--gap) * 1.5);
    align-content:center;
    justify-items:center;
    background:transparent;
  }
  .btn{
    appearance:none;
    -webkit-appearance:none;
    border:0;
    cursor:pointer;
    width:100%; /* let grid column define width */
    max-width:720px;
    padding:clamp(0.6rem, 1.8vw, 1.2rem);
    font-size:clamp(1rem, 2.6vw, 1.25rem);
    line-height:1.1;
    border-radius:12px;
    background:linear-gradient(135deg,#0ea5a8,#06b6d4);
    color:white;
    font-weight:600;
    box-shadow:0 6px 18px rgba(3,7,18,0.12), inset 0 -2px 0 rgba(0,0,0,0.06);
    transition:transform .12s ease, box-shadow .12s ease, filter .12s ease;
    text-align:center;
  }
  .btn:active{transform:translateY(1px) scale(.998)}
  .btn:focus{outline:3px solid rgba(6,182,212,0.18);outline-offset:3px}
  .btn:hover{filter:brightness(1.02);transform:translateY(-2px)}

  /* Small screens: make gap smaller and min width smaller */
  @media (max-width:420px){
    :root{--min-button-width:120px}
    .btn{border-radius:10px}
  }

  /* Extra large screens: increase min width so buttons don't stretch too thin */
  @media (min-width:1400px){
    :root{--min-button-width:220px}
  }
</style>

<div class="btn-grid">
  <button class="btn" role="button" aria-label="Lesson 1">Lesson 1</button>
  <button class="btn" role="button" aria-label="Lesson 2">Lesson 2</button>
  <button class="btn" role="button" aria-label="Quiz">Quiz</button>
  <button class="btn" role="button" aria-label="Resources">Resources</button>
  <button class="btn" role="button" aria-label="Submit homework">Submit homework</button>
  <button class="btn" role="button" aria-label="Contact">Contact</button>
</div> 
