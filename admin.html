<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>TEMPLE — Auditorías Redes (Admin)</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Poppins:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet" />
<style>
  :root {
    --bg: #1c1a1b; --surface: #262324; --surface-2: #302c2d; --line: #423d3e;
    --text: #f8f7f7; --muted: #a89fa0;
    --teal: #209895; --teal-dim: #156b69;
    --pink: #d40967; --yellow: #ffdd00;
    --pass: var(--teal); --pass-bg: rgba(32,152,149,0.14);
    --fail: var(--pink); --fail-bg: rgba(212,9,103,0.14);
    --radius: 10px;
  }
  * { box-sizing: border-box; }
  body { margin: 0; background: var(--bg); color: var(--text); font-family: 'Poppins', sans-serif; min-height: 100vh; }
  .mono { font-family: 'IBM Plex Mono', monospace; }

  header.top { display: flex; align-items: center; justify-content: space-between; gap: 16px; flex-wrap: wrap; padding: 26px 32px 0; border-bottom: 1px solid var(--line); }
  .brand .mark { color: var(--teal); font-size: 13px; letter-spacing: 0.3em; font-weight: 600; }
  .brand h1 { font-size: 32px; margin: 6px 0 2px; font-weight: 400; }
  .brand .sub { color: var(--muted); font-size: 12.5px; margin-bottom: 16px; }

  .tabs { display: flex; gap: 4px; padding: 0 32px; border-bottom: 1px solid var(--line); }
  .tab-btn { background: transparent; border: none; color: var(--muted); font-family: 'Poppins', sans-serif; font-weight: 600; font-size: 13.5px; padding: 12px 4px; margin-right: 22px; cursor: pointer; border-bottom: 2px solid transparent; }
  .tab-btn.active { color: var(--text); border-bottom-color: var(--teal); }

  select, input[type="month"], input[type="text"], input[type="password"], input[type="number"], textarea {
    background: var(--surface); border: 1px solid var(--line); color: var(--text);
    border-radius: 8px; padding: 10px 12px; font-family: 'Poppins', sans-serif; font-size: 14px;
  }
  select:focus, input:focus, textarea:focus { outline: 2px solid var(--teal); outline-offset: 1px; }

  button { font-family: 'Poppins', sans-serif; font-weight: 600; font-size: 14px; border-radius: 8px; padding: 10px 16px; border: 1px solid var(--teal); background: var(--teal); color: #052423; cursor: pointer; }
  button:hover { background: #26aca9; }
  button.ghost { background: transparent; color: var(--text); border-color: var(--line); }
  button.ghost:hover { border-color: var(--teal); color: var(--teal); }
  button:focus-visible { outline: 2px solid var(--teal); outline-offset: 2px; }
  button:disabled { opacity: 0.5; cursor: not-allowed; }

  main { padding: 24px 32px 60px; max-width: 1100px; margin: 0 auto; }
  .view { display: none; }
  .view.active { display: block; }

  .controls { display: flex; align-items: center; gap: 10px; flex-wrap: wrap; margin-bottom: 14px; }
  .summary-bar { display: flex; gap: 28px; align-items: baseline; margin-bottom: 20px; color: var(--muted); font-size: 13px; flex-wrap: wrap; }
  .summary-bar b { color: var(--text); font-size: 15px; }

  /* Ranking */
  .ranking { display: flex; flex-direction: column; gap: 8px; }
  .rank-row { display: grid; grid-template-columns: 36px 1fr auto auto 90px; align-items: center; gap: 14px; background: var(--surface); border: 1px solid var(--line); border-radius: var(--radius); padding: 12px 16px; }
  .rank-row.empty { opacity: 0.5; }
  .rank-pos { font-family: 'Anton', sans-serif; font-size: 20px; color: var(--muted); text-align: center; }
  .rank-row:nth-child(1) .rank-pos { color: var(--yellow); }
  .rank-bar { font-weight: 700; }
  .rank-bar::before { content: "@"; color: var(--muted); font-weight: 500; }
  .rank-bars { display: flex; flex-direction: column; gap: 4px; min-width: 160px; }
  .mini-bar-row { display: grid; grid-template-columns: 70px 1fr; gap: 6px; align-items: center; font-size: 10px; color: var(--muted); }
  .mini-track { height: 4px; background: var(--surface-2); border-radius: 999px; overflow: hidden; }
  .mini-fill { height: 100%; background: var(--teal); }
  .rank-score { font-family: 'Anton', sans-serif; font-size: 26px; color: var(--teal); text-align: right; }
  .rank-score.fail { color: var(--pink); }
  .seal { font-size: 10px; font-weight: 700; letter-spacing: 0.1em; padding: 4px 9px; border-radius: 999px; text-transform: uppercase; white-space: nowrap; text-align: center; }
  .seal.pass { color: var(--teal); background: var(--pass-bg); border: 1px solid var(--teal); }
  .seal.fail { color: var(--pink); background: var(--fail-bg); border: 1px solid var(--pink); }
  .seal.none { color: var(--muted); background: rgba(255,255,255,0.03); border: 1px solid var(--line); }
  .rank-detail { grid-column: 1 / -1; display: none; border-top: 1px solid var(--line); margin-top: 10px; padding-top: 10px; font-size: 12.5px; color: var(--muted); line-height: 1.5; }
  .rank-detail.open { display: block; }
  .rank-detail b { color: var(--text); }
  .rank-detail .plan { padding-left: 18px; margin: 6px 0 0; }
  .rank-toggle { grid-column: 1/-1; text-align: right; }
  .rank-toggle button { padding: 4px 0; font-size: 11.5px; background: none; border: none; color: var(--muted); text-decoration: underline; }
  .rank-toggle button:hover { color: var(--teal); }
  .edit-toggle { font-size: 11.5px; color: var(--muted); background: none; border: none; padding: 0; text-decoration: underline; cursor: pointer; margin-top: 8px; }
  .edit-toggle:hover { color: var(--teal); }

  /* Por bar */
  .hist-controls { display: flex; gap: 10px; align-items: center; margin-bottom: 20px; }
  .hist-table { width: 100%; border-collapse: collapse; font-size: 13px; margin-top: 18px; }
  .hist-table th { text-align: left; color: var(--muted); font-size: 11.5px; text-transform: uppercase; letter-spacing: 0.05em; padding: 8px 10px; border-bottom: 1px solid var(--line); }
  .hist-table td { padding: 10px; border-bottom: 1px solid var(--line); vertical-align: top; }
  .hist-chart { display: flex; align-items: flex-end; gap: 10px; height: 160px; padding: 10px 0 0; }
  .hist-chart .col { display: flex; flex-direction: column; align-items: center; gap: 6px; flex: 1; height: 100%; justify-content: flex-end; }
  .hist-chart .bar { width: 100%; max-width: 42px; border-radius: 4px 4px 0 0; background: var(--teal); }
  .hist-chart .bar.fail { background: var(--pink); }
  .hist-chart .lbl { font-size: 10.5px; color: var(--muted); }
  .hist-chart .val { font-size: 11px; color: var(--text); font-weight: 600; }
  .plan-inline { margin: 0; padding-left: 16px; }

  .empty-msg { color: var(--muted); font-size: 13px; }

  /* Modal */
  .modal-backdrop { position: fixed; inset: 0; background: rgba(10,9,9,0.72); display: none; align-items: center; justify-content: center; padding: 20px; z-index: 50; overflow-y: auto; }
  .modal-backdrop.open { display: flex; }
  .modal { background: var(--surface); border: 1px solid var(--line); border-radius: 14px; padding: 26px; width: 100%; max-width: 620px; max-height: 88vh; overflow-y: auto; margin: auto; }
  .modal h2 { font-family: 'Anton', sans-serif; text-transform: uppercase; font-weight: 400; font-size: 24px; margin: 0 0 4px; letter-spacing: 0.02em; }
  .modal .hint { color: var(--muted); font-size: 12.5px; margin-bottom: 18px; }
  .modal .hint.warn { color: var(--yellow); }
  .field { display: flex; flex-direction: column; gap: 6px; margin-bottom: 14px; }
  .field label { font-size: 12.5px; color: var(--muted); font-weight: 600; }
  textarea { min-height: 70px; resize: vertical; font-family: 'Poppins', sans-serif; }
  .modal-actions { display: flex; justify-content: flex-end; gap: 10px; margin-top: 8px; }
  .status-msg { font-size: 12.5px; margin-top: 10px; }
  .status-msg.ok { color: var(--teal); }
  .status-msg.err { color: var(--pink); }

  .crit-block { border: 1px solid var(--line); border-radius: 8px; padding: 12px; margin-bottom: 10px; }
  .crit-block-head { display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px; font-size: 12.5px; font-weight: 600; }
  .crit-block input[type="number"] { width: 64px; }
  .crit-block textarea { min-height: 44px; font-size: 12.5px; width: 100%; margin-top: 6px; }

  .live-total { display: flex; align-items: baseline; gap: 12px; padding: 12px; background: var(--surface-2); border-radius: 8px; margin: 6px 0 16px; }
  .live-total .num { font-family: 'Anton', sans-serif; font-size: 30px; color: var(--teal); }
  .live-total .num.fail { color: var(--pink); }

  .plan-box { background: var(--surface-2); border: 1px dashed var(--line); border-radius: 8px; padding: 12px; margin-top: 4px; }
  .plan-box pre { white-space: pre-wrap; font-size: 12px; font-family: 'IBM Plex Mono', monospace; margin: 8px 0 0; color: var(--muted); }

  footer { text-align: center; color: var(--muted); font-size: 11.5px; padding: 20px; }
</style>
</head>
<body>

<header class="top">
  <div class="brand">
    <div class="mark">TEMPLE</div>
    <h1>Auditorías Redes — Panel</h1>
    <div class="sub">Vos puntuás · el sistema calcula aprobado/no aprobado · Claude arma el plan de acción</div>
  </div>
</header>

<div class="tabs">
  <button class="tab-btn active" data-view="ranking">Ranking mensual</button>
  <button class="tab-btn" data-view="porBar">Por bar</button>
</div>

<main>
  <div class="view active" id="viewRanking">
    <div class="controls">
      <select id="mesSelect"></select>
      <button class="ghost" id="btnConfig" title="Configurar repo y token">⚙ Config</button>
      <button id="btnNueva">＋ Cargar auditoría</button>
    </div>
    <div class="summary-bar" id="summaryBar"></div>
    <div class="ranking" id="ranking"></div>
  </div>

  <div class="view" id="viewPorBar">
    <div class="hist-controls">
      <select id="histBarSelect"></select>
    </div>
    <div id="histContent"></div>
  </div>
</main>

<footer>Datos leídos directamente desde <span class="mono" id="repoLabel">este repositorio</span> · umbral de aprobación 80/100</footer>

<!-- Modal: nueva/editar auditoría -->
<div class="modal-backdrop" id="modalAuditoria">
  <div class="modal">
    <h2 id="modalTitulo">Cargar auditoría</h2>
    <div class="hint">Puntuá cada criterio. El total y el aprobado/no aprobado se calculan solos. Para el plan de acción, copiá el prompt, pegalo en una pestaña de Claude, y traé la respuesta acá abajo.</div>
    <div class="field">
      <label for="inpBar">Bar</label>
      <select id="inpBar"></select>
    </div>
    <div class="field">
      <label for="inpMes">Mes auditado</label>
      <input type="month" id="inpMes" />
    </div>

    <div id="critFields"></div>

    <div class="live-total" id="liveTotal"></div>

    <div class="field">
      <label>Plan de acción</label>
      <button class="ghost" id="btnCopiarPrompt" type="button" style="margin-bottom:8px;">📋 Copiar prompt para Claude</button>
      <textarea id="inpPlanRaw" placeholder='Pegá acá la respuesta de Claude: un array JSON tipo ["Punto 1", "Punto 2"] o una lista, una por línea.'></textarea>
    </div>

    <div class="modal-actions">
      <button class="ghost" id="btnCancelarAuditoria">Cancelar</button>
      <button id="btnGuardarAuditoria">Guardar auditoría</button>
    </div>
    <div class="status-msg" id="auditoriaStatus"></div>
  </div>
</div>

<!-- Modal: config -->
<div class="modal-backdrop" id="modalConfig">
  <div class="modal">
    <h2>Configuración</h2>
    <div class="hint" id="configHint">El token queda guardado solo en tu navegador (localStorage), nunca se sube al repo. Necesita permiso "Contents: Read and write" sobre este repositorio.</div>
    <div class="field">
      <label for="cfgOwner">Owner (usuario u organización de GitHub)</label>
      <input type="text" id="cfgOwner" placeholder="ej: gonzalezmatiasn1" />
    </div>
    <div class="field">
      <label for="cfgRepo">Repositorio</label>
      <input type="text" id="cfgRepo" placeholder="ej: auditoriaredes" />
    </div>
    <div class="field">
      <label for="cfgToken">GitHub Token (personal access token, fine-grained)</label>
      <input type="password" id="cfgToken" placeholder="github_pat_..." />
    </div>
    <div class="modal-actions">
      <button class="ghost" id="btnCancelarConfig">Cancelar</button>
      <button id="btnGuardarConfig">Guardar</button>
    </div>
  </div>
</div>

<script>
  const BARES = [
    "casatemple","templebarriochino","templehollywood","templepuertomadero",
    "clubtemple","templecaminito","templemaschwitz",
    "templecatedral","templecordoba","templesalta","templetucuman",
    "templecomodoro","templeriogallegos","templerosario","templesgo"
  ];

  const CRITERIOS = [
    { key: "frecuencia", label: "Frecuencia (8 posteos/mes)", max: 25 },
    { key: "tono_contenido", label: "Tono según KV", max: 40 },
    { key: "estetica_visual", label: "Estética según KV", max: 25 },
    { key: "historias_destacadas", label: "Destacadas obligatorias (Menú, Horarios, Reservas)", max: 10 }
  ];
  const CRIT_LABELS = Object.fromEntries(CRITERIOS.map(c => [c.key, c.label]));

  function detectRepoFromLocation() {
    const host = location.hostname;
    const owner = host.endsWith(".github.io") ? host.split(".")[0] : null;
    const parts = location.pathname.split("/").filter(Boolean);
    const repo = parts.length ? parts[0] : null;
    return { owner, repo };
  }
  function loadConfig() {
    const stored = JSON.parse(localStorage.getItem("temple_audit_config") || "{}");
    const detected = detectRepoFromLocation();
    return { owner: stored.owner || detected.owner || "", repo: stored.repo || detected.repo || "", token: stored.token || "" };
  }
  function saveConfig(cfg) { localStorage.setItem("temple_audit_config", JSON.stringify(cfg)); }

  let config = loadConfig();
  let allData = [];
  let editingRecord = null; // record being edited, null = creating new

  document.getElementById("repoLabel").textContent = config.owner && config.repo ? `${config.owner}/${config.repo}` : "(configurá el repo en ⚙ Config)";

  document.querySelectorAll(".tab-btn").forEach(btn => {
    btn.addEventListener("click", () => {
      document.querySelectorAll(".tab-btn").forEach(b => b.classList.remove("active"));
      document.querySelectorAll(".view").forEach(v => v.classList.remove("active"));
      btn.classList.add("active");
      document.getElementById(btn.dataset.view === "ranking" ? "viewRanking" : "viewPorBar").classList.add("active");
      if (btn.dataset.view === "porBar") renderPorBar();
    });
  });

  async function fetchData() {
    if (!config.owner || !config.repo) return;
    try {
      const res = await fetch(`https://api.github.com/repos/${config.owner}/${config.repo}/contents/data`);
      if (!res.ok) { allData = []; renderRanking(); return; }
      const files = await res.json();
      const jsonFiles = files.filter(f => f.name.endsWith(".json"));
      const results = await Promise.all(jsonFiles.map(async f => {
        try {
          const r = await fetch(f.download_url);
          const json = await r.json();
          json.__sha = f.sha; json.__path = f.path;
          return json;
        } catch { return null; }
      }));
      allData = results.filter(Boolean);
      populateMesSelect();
      populateHistBarSelect();
      renderRanking();
    } catch (e) { console.error("Error cargando datos:", e); }
  }

  function populateMesSelect() {
    const meses = [...new Set(allData.map(d => d.mes))].sort().reverse();
    const sel = document.getElementById("mesSelect");
    const current = sel.value;
    sel.innerHTML = "";
    const now = new Date().toISOString().slice(0,7);
    const allMeses = [...new Set([now, ...meses])].sort().reverse();
    allMeses.forEach(m => {
      const opt = document.createElement("option");
      opt.value = m; opt.textContent = m;
      sel.appendChild(opt);
    });
    sel.value = allMeses.includes(current) ? current : allMeses[0];
  }
  function populateHistBarSelect() {
    const sel = document.getElementById("histBarSelect");
    if (sel.options.length) return;
    BARES.forEach(b => {
      const opt = document.createElement("option");
      opt.value = b; opt.textContent = "@" + b;
      sel.appendChild(opt);
    });
  }

  // ---------- Ranking mensual ----------
  function renderRanking() {
    const mes = document.getElementById("mesSelect").value;
    const wrap = document.getElementById("ranking");
    wrap.innerHTML = "";

    const enMes = allData.filter(d => d.mes === mes);
    const conDatos = BARES.map(bar => enMes.find(x => x.bar === bar)).filter(Boolean)
      .sort((a, b) => b.puntaje_total - a.puntaje_total);
    const sinDatos = BARES.filter(bar => !enMes.find(x => x.bar === bar));

    let pos = 1;
    conDatos.forEach(d => {
      wrap.appendChild(buildRankRow(d, pos));
      pos++;
    });
    sinDatos.forEach(bar => {
      const row = document.createElement("div");
      row.className = "rank-row empty";
      row.innerHTML = `
        <span class="rank-pos">—</span>
        <span class="rank-bar">${bar}</span>
        <span></span>
        <span class="seal none">Sin auditar</span>
        <span></span>
      `;
      wrap.appendChild(row);
    });

    const aprobadas = conDatos.filter(d => d.aprobado).length;
    const promedio = conDatos.length ? Math.round(conDatos.reduce((s, d) => s + d.puntaje_total, 0) / conDatos.length) : 0;
    document.getElementById("summaryBar").innerHTML = `
      <span><b>${conDatos.length}</b> / ${BARES.length} cuentas auditadas</span>
      <span><b>${aprobadas}</b> aprobadas</span>
      <span>promedio <b>${promedio}</b>/100</span>
    `;
  }

  function buildRankRow(d, pos) {
    const row = document.createElement("div");
    row.className = "rank-row";

    const miniBars = CRITERIOS.map(c => {
      const val = d.criterios?.[c.key]?.puntaje ?? 0;
      const max = d.criterios?.[c.key]?.max ?? c.max;
      return `<div class="mini-bar-row"><span>${c.label.split(" ")[0]}</span><div class="mini-track"><div class="mini-fill" style="width:${Math.round((val/max)*100)}%"></div></div></div>`;
    }).join("");

    row.innerHTML = `
      <span class="rank-pos">${pos}</span>
      <span class="rank-bar">${d.bar}</span>
      <div class="rank-bars">${miniBars}</div>
      <span class="seal ${d.aprobado ? "pass" : "fail"}">${d.aprobado ? "Aprobado" : "No aprobado"}</span>
      <span class="rank-score ${d.aprobado ? "" : "fail"}">${d.puntaje_total}</span>
      <div class="rank-toggle"><button type="button">ver detalle y plan de acción</button></div>
      <div class="rank-detail"></div>
    `;

    const toggleBtn = row.querySelector(".rank-toggle button");
    const detail = row.querySelector(".rank-detail");
    toggleBtn.addEventListener("click", () => {
      const open = detail.classList.toggle("open");
      toggleBtn.textContent = open ? "cerrar" : "ver detalle y plan de acción";
      if (open && !detail.dataset.built) {
        detail.dataset.built = "1";
        const critHtml = CRITERIOS.map(c => {
          const cd = d.criterios?.[c.key];
          if (!cd) return "";
          return `<div><b>${c.label} (${cd.puntaje}/${cd.max}):</b> ${cd.comentario || ""}</div>`;
        }).join("");
        const plan = (d.plan_de_accion || []).map(p => `<li>${p}</li>`).join("");
        detail.innerHTML = critHtml + (plan ? `<div style="margin-top:8px;"><b>Plan de acción</b><ul class="plan">${plan}</ul></div>` : "");
        const editBtn = document.createElement("button");
        editBtn.className = "edit-toggle";
        editBtn.textContent = "✎ editar esta auditoría";
        editBtn.addEventListener("click", () => openAuditModal(d));
        detail.appendChild(editBtn);
      }
    });

    return row;
  }

  document.getElementById("mesSelect").addEventListener("change", renderRanking);

  // ---------- Por bar ----------
  document.getElementById("histBarSelect").addEventListener("change", renderPorBar);

  function renderPorBar() {
    const bar = document.getElementById("histBarSelect").value;
    const content = document.getElementById("histContent");
    if (!bar) { content.innerHTML = `<div class="empty-msg">Configurá el repo primero.</div>`; return; }

    const registros = allData.filter(d => d.bar === bar).sort((a, b) => a.mes.localeCompare(b.mes));
    if (registros.length === 0) {
      content.innerHTML = `<div class="empty-msg">Todavía no hay auditorías cargadas para @${bar}.</div>`;
      return;
    }

    const chartCols = registros.map(r => `
      <div class="col">
        <span class="val">${r.puntaje_total}</span>
        <div class="bar ${r.aprobado ? "" : "fail"}" style="height:${(r.puntaje_total/100)*100}%"></div>
        <span class="lbl">${r.mes}</span>
      </div>
    `).join("");

    const promedio = Math.round(registros.reduce((s, r) => s + r.puntaje_total, 0) / registros.length);
    const aprobadas = registros.filter(r => r.aprobado).length;

    const rows = registros.map(r => `
      <tr>
        <td>${r.mes}</td>
        <td class="mono">${r.puntaje_total}/100</td>
        <td><span class="seal ${r.aprobado ? "pass" : "fail"}">${r.aprobado ? "Aprobado" : "No aprobado"}</span></td>
        <td>${(r.plan_de_accion || []).length ? `<ul class="plan-inline">${r.plan_de_accion.map(p => `<li>${p}</li>`).join("")}</ul>` : "—"}</td>
      </tr>
    `).join("");

    content.innerHTML = `
      <div class="summary-bar">
        <span><b>${registros.length}</b> meses auditados</span>
        <span><b>${aprobadas}</b> aprobados</span>
        <span>promedio <b>${promedio}</b>/100</span>
      </div>
      <div class="hist-chart">${chartCols}</div>
      <table class="hist-table">
        <thead><tr><th>Mes</th><th>Puntaje</th><th>Estado</th><th>Plan de acción</th></tr></thead>
        <tbody>${rows}</tbody>
      </table>
    `;
  }

  // ---------- Modal auditoría (crear/editar) ----------
  const modalAuditoria = document.getElementById("modalAuditoria");
  const inpBar = document.getElementById("inpBar");
  BARES.forEach(b => {
    const opt = document.createElement("option");
    opt.value = b; opt.textContent = "@" + b;
    inpBar.appendChild(opt);
  });

  function buildCritFields(existing) {
    const wrap = document.getElementById("critFields");
    wrap.innerHTML = "";
    CRITERIOS.forEach(c => {
      const cd = existing?.criterios?.[c.key];
      const block = document.createElement("div");
      block.className = "crit-block";
      block.innerHTML = `
        <div class="crit-block-head">
          <span>${c.label}</span>
          <input type="number" min="0" max="${c.max}" value="${cd ? cd.puntaje : 0}" data-key="${c.key}" data-field="puntaje" />
        </div>
        <textarea placeholder="Comentario (opcional)" data-key="${c.key}" data-field="comentario">${cd ? (cd.comentario || "") : ""}</textarea>
      `;
      wrap.appendChild(block);
    });
    wrap.querySelectorAll("input[type=number]").forEach(inp => inp.addEventListener("input", updateLiveTotal));
    updateLiveTotal();
  }

  function readCritFromForm() {
    const criterios = {};
    CRITERIOS.forEach(c => {
      const puntajeInp = document.querySelector(`#critFields input[data-key="${c.key}"]`);
      const comentarioTa = document.querySelector(`#critFields textarea[data-key="${c.key}"]`);
      let val = Number(puntajeInp.value);
      if (isNaN(val)) val = 0;
      val = Math.max(0, Math.min(c.max, val));
      criterios[c.key] = { puntaje: val, max: c.max, comentario: comentarioTa.value.trim() };
    });
    return criterios;
  }

  function updateLiveTotal() {
    const criterios = readCritFromForm();
    const total = Object.values(criterios).reduce((s, c) => s + c.puntaje, 0);
    const aprobado = total >= 80;
    document.getElementById("liveTotal").innerHTML = `
      <span class="num ${aprobado ? "" : "fail"}">${total}</span>
      <span>/ 100</span>
      <span class="seal ${aprobado ? "pass" : "fail"}">${aprobado ? "Aprobado" : "No aprobado"}</span>
    `;
  }

  function openAuditModal(existing) {
    editingRecord = existing || null;
    document.getElementById("modalTitulo").textContent = existing ? `Editar auditoría — @${existing.bar}` : "Cargar auditoría";
    document.getElementById("auditoriaStatus").textContent = "";
    inpBar.value = existing ? existing.bar : inpBar.value;
    inpBar.disabled = !!existing;
    document.getElementById("inpMes").value = existing ? existing.mes : document.getElementById("mesSelect").value || new Date().toISOString().slice(0,7);
    document.getElementById("inpMes").disabled = !!existing;
    buildCritFields(existing);
    document.getElementById("inpPlanRaw").value = existing?.plan_de_accion ? JSON.stringify(existing.plan_de_accion) : "";
    modalAuditoria.classList.add("open");
  }

  document.getElementById("btnNueva").addEventListener("click", () => {
    config = loadConfig();
    if (!config.owner || !config.repo || !config.token) {
      openConfigModal("Completá owner, repo y token para poder cargar o editar auditorías.");
      return;
    }
    openAuditModal(null);
  });
  document.getElementById("btnCancelarAuditoria").addEventListener("click", () => modalAuditoria.classList.remove("open"));

  document.getElementById("btnCopiarPrompt").addEventListener("click", () => {
    const bar = inpBar.value;
    const mes = document.getElementById("inpMes").value;
    const criterios = readCritFromForm();
    const total = Object.values(criterios).reduce((s, c) => s + c.puntaje, 0);
    const aprobado = total >= 80;

    const lineas = CRITERIOS.map(c => {
      const cd = criterios[c.key];
      return `- ${c.label}: ${cd.puntaje}/${cd.max}${cd.comentario ? " — " + cd.comentario : ""}`;
    }).join("\n");

    const prompt = `Actuá como auditor de redes sociales de TEMPLE (cadena de bares en Argentina). Con estos puntajes de la auditoría mensual de @${bar} (${mes || "mes actual"}), redactá un plan de acción de 2 a 4 puntos, concretos y accionables, priorizados por impacto en el puntaje del próximo mes.

Puntajes de este mes:
${lineas}
Total: ${total}/100 — ${aprobado ? "Aprobado" : "No aprobado"} (umbral de aprobación: 80/100)

Devolvé ÚNICAMENTE un array JSON de strings con el plan de acción, sin texto adicional, sin markdown. Ejemplo de formato: ["Punto 1", "Punto 2", "Punto 3"]`;

    navigator.clipboard.writeText(prompt).then(() => {
      const statusEl = document.getElementById("auditoriaStatus");
      statusEl.textContent = "Prompt copiado. Pegalo en una pestaña de Claude, copiá su respuesta y pegala abajo en \"Plan de acción\".";
      statusEl.className = "status-msg ok";
    }).catch(() => {
      alert("No se pudo copiar automáticamente. Prompt:\n\n" + prompt);
    });
  });

  document.getElementById("btnGuardarAuditoria").addEventListener("click", async () => {
    const bar = inpBar.value;
    const mes = document.getElementById("inpMes").value;
    const statusEl = document.getElementById("auditoriaStatus");

    if (!mes) { statusEl.textContent = "Falta el mes."; statusEl.className = "status-msg err"; return; }
    if (!config.token) { statusEl.textContent = "Necesitás configurar tu token en ⚙ Config."; statusEl.className = "status-msg err"; return; }

    const criterios = readCritFromForm();
    const puntaje_total = Object.values(criterios).reduce((s, c) => s + c.puntaje, 0);
    const aprobado = puntaje_total >= 80;

    let plan_de_accion = [];
    const rawPlan = document.getElementById("inpPlanRaw").value.trim();
    if (rawPlan) {
      try {
        const parsed = JSON.parse(rawPlan);
        if (Array.isArray(parsed)) plan_de_accion = parsed.map(String);
      } catch {
        plan_de_accion = rawPlan.split("\n").map(s => s.replace(/^[-*\d.)\s]+/, "").trim()).filter(Boolean);
      }
    }

    const record = {
      bar, mes, criterios, puntaje_total, aprobado, plan_de_accion,
      fecha_auditoria: editingRecord?.fecha_auditoria || new Date().toISOString(),
      fecha_edicion: editingRecord ? new Date().toISOString() : undefined
    };

    statusEl.textContent = "Guardando…";
    statusEl.className = "status-msg";
    try {
      const path = `data/${bar}-${mes}.json`;
      const content = btoa(unescape(encodeURIComponent(JSON.stringify(record, null, 2))));
      const body = { message: `Auditoría ${bar} ${mes}`, content };
      if (editingRecord?.__sha) body.sha = editingRecord.__sha;

      const res = await fetch(`https://api.github.com/repos/${config.owner}/${config.repo}/contents/${path}`, {
        method: "PUT",
        headers: {
          "Authorization": `Bearer ${config.token}`,
          "Accept": "application/vnd.github+json",
          "Content-Type": "application/json"
        },
        body: JSON.stringify(body)
      });

      if (res.ok) {
        statusEl.textContent = "Guardado en el repo.";
        statusEl.className = "status-msg ok";
        setTimeout(() => { modalAuditoria.classList.remove("open"); fetchData(); }, 700);
      } else {
        const errBody = await res.text();
        statusEl.textContent = `Error (${res.status}): ${errBody}`;
        statusEl.className = "status-msg err";
      }
    } catch (e) {
      statusEl.textContent = "Error de red: " + e.message;
      statusEl.className = "status-msg err";
    }
  });

  // ---------- Modal config ----------
  const modalConfig = document.getElementById("modalConfig");
  function openConfigModal(hint) {
    config = loadConfig();
    document.getElementById("cfgOwner").value = config.owner;
    document.getElementById("cfgRepo").value = config.repo;
    document.getElementById("cfgToken").value = config.token;
    const hintEl = document.getElementById("configHint");
    if (hint) { hintEl.textContent = hint; hintEl.className = "hint warn"; }
    else { hintEl.textContent = 'El token queda guardado solo en tu navegador (localStorage), nunca se sube al repo. Necesita permiso "Contents: Read and write" sobre este repositorio.'; hintEl.className = "hint"; }
    modalConfig.classList.add("open");
  }
  document.getElementById("btnConfig").addEventListener("click", () => openConfigModal());
  document.getElementById("btnCancelarConfig").addEventListener("click", () => modalConfig.classList.remove("open"));
  document.getElementById("btnGuardarConfig").addEventListener("click", () => {
    const cfg = {
      owner: document.getElementById("cfgOwner").value.trim(),
      repo: document.getElementById("cfgRepo").value.trim(),
      token: document.getElementById("cfgToken").value.trim()
    };
    saveConfig(cfg);
    config = cfg;
    document.getElementById("repoLabel").textContent = cfg.owner && cfg.repo ? `${cfg.owner}/${cfg.repo}` : "(configurá el repo)";
    modalConfig.classList.remove("open");
    fetchData();
  });

  fetchData();
</script>

</body>
</html>
