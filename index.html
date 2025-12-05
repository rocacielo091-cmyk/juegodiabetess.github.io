<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Un día con Estela y Esteban — Juego educativo</title>
  <style>
    :root {
      --card-yellow-start: #fff7d6;
      --card-yellow-end: #fff3b0;
      --accent-green: #16a34a;
      --accent-red: #c53030;
      --soft-bg: rgba(255,255,255,0.92);
      --container-width: 1100px;
    }
    html,body { height:100%; margin:0; font-family: Inter, Roboto, Arial, sans-serif; background:#e6f0ff; }
    .page {
      min-height:100vh;
      padding:24px;
      box-sizing:border-box;
      display:flex;
      justify-content:center;
      align-items:flex-start;
      gap:18px;
      background-image: url('fondo-salon.png');
      background-size: cover;
      background-position: center;
    }
    .container {
      width:100%;
      max-width: var(--container-width);
      background: var(--soft-bg);
      border-radius:14px;
      padding:18px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.12);
    }
    header { display:flex; justify-content:space-between; align-items:center; margin-bottom:12px; }
    h1 { margin:0; font-size:20px; }
    .sub { color:#374151; font-size:13px; margin-top:6px; }

    .panel { display:flex; gap:18px; align-items:flex-start; }
    .avatar-box { display:flex; gap:18px; align-items:center; }
    .avatar-card { text-align:center; cursor:pointer; }
    .avatar-card img { width:160px; border-radius:12px; box-shadow: 0 8px 18px rgba(0,0,0,0.12); border:4px solid transparent; transition: transform .15s, border-color .15s; }
    .avatar-card img:hover { transform: translateY(-4px); }
    .avatar-card.selected img { border-color: #ffdd57; transform: scale(1.02); }

    .map-row { display:flex; gap:8px; margin-top:8px; }
    .map-cell { width:40px; height:40px; border-radius:8px; display:flex; align-items:center; justify-content:center; font-weight:700; }
    .map-done { background:#48bb78; color:white; }
    .map-current { background:#f6e05e; color:#111827; }
    .map-pending { background:#e2e8f0; color:#111827; }

    .main { display:flex; gap:18px; margin-top:12px; }
    .left { flex:1; }
    .right { width:300px; }

    .question-card { padding:12px; border-radius:12px; margin-bottom:12px; background:linear-gradient(180deg,#f7fafc,#eef2ff); box-shadow: inset 0 1px 0 rgba(255,255,255,0.6); }
    .options-grid { display:grid; grid-template-columns: 1fr 1fr; gap:12px; }
    .option {
      background: linear-gradient(180deg,var(--card-yellow-start),var(--card-yellow-end));
      padding:12px; border-radius:12px; cursor:pointer;
      box-shadow: 0 6px 12px rgba(0,0,0,0.06);
      display:flex; align-items:center; justify-content:space-between; font-weight:700;
      transition: transform .12s, opacity .12s, box-shadow .12s;
      min-height:64px;
    }
    .option:hover { transform: translateY(-4px); box-shadow: 0 10px 18px rgba(0,0,0,0.12); }
    .option.wrong { opacity:0.6; }
    .xmark { color: var(--accent-red); font-size:28px; margin-left:12px; }

    .inventory { margin-top:8px; display:flex; gap:8px; flex-wrap:wrap; }
    .chip { background:#ecfccb; padding:6px 10px; border-radius:999px; font-size:13px; }

    .controls { margin-top:12px; display:flex; gap:8px; flex-direction:column; }
    button { padding:10px 12px; border-radius:10px; border:none; cursor:pointer; font-weight:700; }
    .btn-primary { background:#4f46e5; color:white; }
    .btn-muted { background:#efefef; }

    .footer { margin-top:16px; display:flex; justify-content:space-between; align-items:center; color:#6b7280; font-size:13px; }

    .center { text-align:center; padding:18px; }

    .celebrate { font-size:28px; color:#059669; font-weight:800; }

    /* responsive */
    @media (max-width:900px) {
      .main { flex-direction:column; }
      .right { width:100%; }
      .options-grid { grid-template-columns: 1fr; }
      .avatar-box { flex-direction:column; align-items:center; }
      .map-row { justify-content:center; }
    }
  </style>
</head>
<body>
  <div class="page">
    <div class="container" id="app">
      <header>
        <div>
          <h1>Un día con Estela y Esteban — Juego educativo</h1>
          <div class="sub" id="message">Elige tu avatar para comenzar (esto también inicia la música).</div>
        </div>
        <div style="text-align:right;">
          <div id="livesDisplay">Vidas: <span id="hearts">❤️❤️❤️</span></div>
          <div style="font-weight:700; margin-top:6px;" id="scoreDisplay">Puntaje: 0 / 20</div>
        </div>
      </header>

      <!-- Avatar selection -->
      <div id="stageAvatar" style="display:block;">
        <div class="panel">
          <div class="avatar-box">
            <div class="avatar-card" id="cardEstela">
              <img src="Estela.png" alt="Estela" id="imgEstela" />
              <div style="margin-top:8px; font-weight:700;">Estela</div>
            </div>

            <div class="avatar-card" id="cardEsteban">
              <img src="Esteban.png" alt="Esteban" id="imgEsteban" />
              <div style="margin-top:8px; font-weight:700;">Esteban</div>
            </div>
          </div>

          <div style="margin-left:22px; flex:1;">
            <div style="font-weight:700; margin-bottom:6px;">Mapa del día (vista rápida)</div>
            <div class="map-row" id="mapQuick"></div>

            <div style="margin-top:12px;">
              <div style="font-weight:700, margin-bottom:6px;">Inventario</div>
              <div id="inventoryQuick" style="min-height:40px; color:#6b7280;">Aún no has recogido nada.</div>
            </div>
          </div>
        </div>
      </div>

      <!-- Gameplay -->
      <div id="stagePlay" style="display:none;">
        <div class="main">
          <div class="left">
            <div style="display:flex; gap:12px; align-items:center; margin-bottom:12px;">
              <img id="avatarImg" src="" alt="avatar" style="width:120px; border-radius:10px; box-shadow:0 8px 18px rgba(0,0,0,0.12)"/>
              <div>
                <div id="avatarName" style="font-size:18px; font-weight:800">Avatar</div>
                <div id="levelInfo" style="font-size:13px; color:#374151">Nivel 1 — Pregunta 1 / 10</div>
              </div>
            </div>

            <div class="question-card">
              <div id="questionTitle" style="font-weight:700; margin-bottom:8px;">Pregunta</div>
              <div class="options-grid" id="optionsGrid"></div>
            </div>

            <div style="margin-top:6px;">
              <div style="font-weight:700; margin-bottom:6px;">Mapa del día</div>
              <div class="map-row" id="mapRow"></div>
            </div>
          </div>

          <div class="right">
            <div style="font-weight:700; margin-bottom:8px;">Inventario</div>
            <div style="min-height:120px; background:#ffffff; padding:12px; border-radius:10px; box-shadow: inset 0 2px 6px rgba(0,0,0,0.04);" id="inventoryBox">
              <div id="inventoryEmpty" style="color:#6b7280">Aún no has recogido nada.</div>
            </div>

            <div class="controls">
              <button id="btnToggleMusic" class="btn-muted">🎵 Reproducir / Pausar música</button>
              <button id="btnHint" class="btn-muted">💡 Pedir pista</button>
            </div>
          </div>
        </div>
      </div>

      <!-- Finished -->
      <div id="stageFinished" style="display:none;" class="center">
        <div class="celebrate">🎉 ¡Felicidades! 🎉</div>
        <div style="margin-top:12px; font-size:18px" id="finalScore">Puntaje final: 0 / 20</div>
        <div style="margin-top:12px;"><img id="finalAvatar" src="" alt="winner" style="width:200px; border-radius:12px;" /></div>
        <div style="margin-top:16px;">
          <button id="btnPlayAgain" class="btn-primary">Jugar otra vez</button>
        </div>
      </div>

      <!-- Game Over -->
      <div id="stageGameOver" style="display:none;" class="center">
        <div style="font-size:26px; color:#c53030; font-weight:800">💔 Game Over</div>
        <div style="margin-top:12px; font-size:16px" id="gameOverScore">Puntaje: 0 / 20</div>
        <div style="margin-top:16px;">
          <button id="btnRetry" class="btn-primary" style="background:#f59e0b">Reintentar Nivel 1</button>
          <button id="btnChooseAvatar" class="btn-muted" style="margin-left:10px">Elegir avatar</button>
        </div>
      </div>

      <div class="footer">
        <div>Consejo: una sola opción es la ideal por pregunta. ¡Intenta completar los 2 niveles!</div>
        <div><button id="btnMute" class="btn-muted">🔈 Silenciar</button></div>
      </div>
    </div>
  </div>

<script>
/* Data */
const LEVEL1 = [
  { q: "Desayuno", correct: { text: "Avena con fruta", tag: "Avena" }, wrong: ["Donut", "Gaseosa", "Pan dulce"] },
  { q: "Media mañana", correct: { text: "Yogur natural sin azúcar", tag: "Yogur" }, wrong: ["Chocolatina", "Galletas", "Caramelos"] },
  { q: "Snack", correct: { text: "Fruta (manzana)", tag: "Manzana" }, wrong: ["Papas fritas", "Pastel", "Refresco"] },
  { q: "Almuerzo", correct: { text: "Pollo a la plancha y ensalada", tag: "Pollo" }, wrong: ["Pizza grande", "Hamburguesa", "Arroz con gaseosa"] },
  { q: "Merienda", correct: { text: "Palitos de zanahoria", tag: "Zanahoria" }, wrong: ["Galletas rellenas", "Dulces", "Helado"] },
  { q: "Actividad tarde", correct: { text: "Jugar en el parque 30 min", tag: "Parque" }, wrong: ["Tablet 2 horas", "Dormir toda la tarde", "Ver TV 3 horas"] },
  { q: "Hidratación", correct: { text: "Agua natural", tag: "Agua" }, wrong: ["Bebida azucarada", "Jugo envasado", "Chocolate caliente con azúcar"] },
  { q: "Post-almuerzo", correct: { text: "Una porción pequeña de fruta", tag: "Fruta" }, wrong: ["Pastel", "Gaseosa", "Dulces"] },
  { q: "Cena", correct: { text: "Sopa de verduras ligera", tag: "Sopa" }, wrong: ["Pizza nocturna", "Papas fritas", "Torta"] },
  { q: "Antes de dormir", correct: { text: "Caminar 10 min", tag: "Caminar" }, wrong: ["Comer pastel", "Beber refresco", "Ver pantalla"] },
];

const LEVEL2 = [
  { q: "Desayuno 2", correct: { text: "Huevos revueltos + pan integral", tag: "Huevos" }, wrong: ["Croissant azucarado", "Donut", "Gaseosa"] },
  { q: "Media mañana 2", correct: { text: "Puñado de nueces (sin sal)", tag: "Nueces" }, wrong: ["Caramelo", "Galletas", "Refresco"] },
  { q: "Snack 2", correct: { text: "Yogur con avena sin azúcar", tag: "Yogur2" }, wrong: ["Helado", "Papas fritas", "Pastel"] },
  { q: "Almuerzo 2", correct: { text: "Pescado + verduras al vapor", tag: "Pescado" }, wrong: ["Hamburguesa con papas", "Pizza", "Soda"] },
  { q: "Actividad tarde 2", correct: { text: "Bailar 20 min", tag: "Bailar" }, wrong: ["Jugar sentado", "Ver TV 2h", "Dormir toda la tarde"] },
  { q: "Hidratación 2", correct: { text: "Agua con rodaja de limón", tag: "Agua2" }, wrong: ["Bebida energética", "Jugo envasado", "Gaseosa"] },
  { q: "Post-almuerzo 2", correct: { text: "Fruta fresca (pera)", tag: "Pera" }, wrong: ["Chocolate", "Donut", "Caramelos"] },
  { q: "Cena 2", correct: { text: "Ensalada con proteína magra", tag: "Ensalada" }, wrong: ["Pizza", "Taco frito", "Pastel"] },
  { q: "Noche 2", correct: { text: "Preparar mochila y acostarse a tiempo", tag: "Rutina" }, wrong: ["Comer snack pesado", "Jugar sin parar", "Beber soda"] },
  { q: "Actividad extra", correct: { text: "Estiramientos 10 min", tag: "Estiramientos" }, wrong: ["Comer helado", "Pasar 3h en pantalla", "Dormir todo el día"] },
];

function shuffle(array) {
  const a = array.slice();
  for (let i = a.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [a[i], a[j]] = [a[j], a[i]];
  }
  return a;
}

/* State */
let state = {
  stage: 'avatar',
  avatar: null,
  level: 1,
  index: 0,
  score: 0,
  lives: 3,
  inventory: [],
  options: [],
  showWrong: null,
  musicStarted: false,
  message: 'Elige tu avatar para comenzar (esto también inicia la música).'
};

/* Audio (REEMPLAZAR) */
const music = new Audio('game-music.mp3'); // pon aquí tu mp3 local llamado EXACTAMENTE game-music.mp3
music.loop = true;
music.volume = 0.45;

const soundCorrect = new Audio('correct.mp3'); // archivo local correct.mp3
const soundWrong = new Audio('wrong.mp3');     // archivo local wrong.mp3
const soundClick = new Audio('click.mp3');     // archivo local click.mp3 (opcional)

[soundCorrect, soundWrong, soundClick].forEach(s => { if(s) s.volume = 0.8; });

/* Start music when user interacts anywhere on the page.
   This avoids browser autoplay blocking. The handler runs once. */
function enableAudioOnInteraction() {
  if (state.musicStarted) return;
  const start = () => {
    // try to play music; browsers allow play after user gesture
    music.play().then(() => {
      state.musicStarted = true;
    }).catch(err => {
      // si falla, al menos intentamos de nuevo más tarde
      console.log("Reproducción bloqueada o fallida:", err);
    });
    // remove listener (solo queremos que ocurra 1 vez)
    document.body.removeEventListener("click", start);
  };
  document.body.addEventListener("click", start);
}

/* Helper to start immediately (called when user explicitly clicks avatar) */
function startMusicOnce() {
  if (state.musicStarted) return;
  // ensure audio is allowed: try to play; if blocked, enableAudioOnInteraction will catch next click
  music.play().then(() => {
    state.musicStarted = true;
  }).catch(() => {
    enableAudioOnInteraction();
  });
}

/* DOM references */
const messageEl = document.getElementById('message');
const heartsEl = document.getElementById('hearts');
const scoreEl = document.getElementById('scoreDisplay');
const mapQuickEl = document.getElementById('mapQuick');
const inventoryQuickEl = document.getElementById('inventoryQuick');

const stageAvatarEl = document.getElementById('stageAvatar');
const stagePlayEl = document.getElementById('stagePlay');
const stageFinishedEl = document.getElementById('stageFinished');
const stageGameOverEl = document.getElementById('stageGameOver');

const cardEstela = document.getElementById('cardEstela');
const cardEsteban = document.getElementById('cardEsteban');

const avatarImg = document.getElementById('avatarImg');
const avatarName = document.getElementById('avatarName');
const levelInfo = document.getElementById('levelInfo');
const questionTitle = document.getElementById('questionTitle');
const optionsGrid = document.getElementById('optionsGrid');
const mapRow = document.getElementById('mapRow');

const inventoryBox = document.getElementById('inventoryBox');
const inventoryEmpty = document.getElementById('inventoryEmpty');

const btnToggleMusic = document.getElementById('btnToggleMusic');
const btnHint = document.getElementById('btnHint');

const finalScore = document.getElementById('finalScore');
const finalAvatar = document.getElementById('finalAvatar');
const btnPlayAgain = document.getElementById('btnPlayAgain');
const btnRetry = document.getElementById('btnRetry');
const btnChooseAvatar = document.getElementById('btnChooseAvatar');
const btnMute = document.getElementById('btnMute');

/* Init */
function init() {
  // render quick map 10 empty steps
  mapQuickEl.innerHTML = '';
  for (let i=0;i<10;i++){
    const d = document.createElement('div');
    d.className = 'map-cell map-current';
    d.style.width = '36px';
    d.style.height = '36px';
    d.style.display = 'flex';
    d.style.alignItems = 'center';
    d.style.justifyContent = 'center';
    d.style.borderRadius = '8px';
    d.innerText = (i+1);
    mapQuickEl.appendChild(d);
  }

  // avatar clicks
  cardEstela.onclick = () => selectAvatar('Estela');
  cardEsteban.onclick = () => selectAvatar('Esteban');

  btnToggleMusic.onclick = toggleMusic;
  btnHint.onclick = showHint;
  btnPlayAgain.onclick = restartFromAvatar;
  btnRetry.onclick = retryLevel;
  btnChooseAvatar.onclick = restartFromAvatar;
  btnMute.onclick = () => { music.muted = !music.muted; btnMute.innerText = music.muted ? '🔇 Silenciado' : '🔈 Silenciar'; };

  updateHUD();
}
init();

/* Functions */
function startMusicOnce() {
  if (state.musicStarted) return;
  music.play().catch(()=>{});
  state.musicStarted = true;
}
function selectAvatar(name) {
  state.avatar = name;
  document.querySelectorAll('.avatar-card').forEach(c => c.classList.remove('selected'));
  (name === 'Estela' ? cardEstela : cardEsteban).classList.add('selected');
  try{ soundClick.play(); }catch(e){}
  startMusicOnce();
  state.stage = 'play';
  state.level = 1;
  state.index = 0;
  state.score = 0;
  state.lives = 3;
  state.inventory = [];
  state.options = prepareOptionsForCurrent();
  state.showWrong = null;
  state.message = name + ' lista/o. ¡Comencemos!';
  renderPlay();
  updateHUD();
}

function prepareOptionsForCurrent() {
  const pool = state.level === 1 ? LEVEL1 : LEVEL2;
  const node = pool[state.index];
  if (!node) return [];
  const opts = [node.correct.text, ...node.wrong];
  return shuffle(opts);
}

function renderPlay() {
  stageAvatarEl.style.display = 'none';
  stagePlayEl.style.display = 'block';
  stageFinishedEl.style.display = 'none';
  stageGameOverEl.style.display = 'none';

  avatarImg.src = state.avatar === 'Estela' ? 'Estela.png' : 'Esteban.png';
  avatarName.innerText = state.avatar;
  levelInfo.innerText = (state.level === 1 ? 'Nivel 1' : 'Nivel 2') + ' — Pregunta ' + (state.index+1) + ' / 10';

  state.options = prepareOptionsForCurrent();
  state.showWrong = null;
  renderOptions();
  renderMap();
  renderInventory();
  updateHUD();
}

function renderOptions() {
  optionsGrid.innerHTML = '';
  const pool = state.level === 1 ? LEVEL1 : LEVEL2;
  const node = pool[state.index];
  questionTitle.innerText = node.q;
  state.options.forEach(optText => {
    const card = document.createElement('div');
    card.className = 'option';
    if (state.showWrong === optText) card.classList.add('wrong');
    const label = document.createElement('div');
    label.innerText = optText;
    const right = document.createElement('div');
    if (state.showWrong === optText) right.innerHTML = '<span class="xmark">✘</span>';
    card.appendChild(label);
    card.appendChild(right);
    card.onclick = () => handleOptionClick(optText);
    optionsGrid.appendChild(card);
  });
}

function renderMap() {
  mapRow.innerHTML = '';
  const pool = state.level === 1 ? LEVEL1 : LEVEL2;
  for (let i=0;i<10;i++){
    const cell = document.createElement('div');
    let stateCls = 'map-pending';
    if (i < state.index) stateCls = 'map-done';
    else if (i === state.index) stateCls = 'map-current';
    cell.className = 'map-cell ' + stateCls;
    cell.innerText = i+1;
    mapRow.appendChild(cell);
  }
}

function renderInventory() {
  inventoryBox.innerHTML = '';
  if (state.inventory.length === 0) {
    inventoryBox.appendChild(inventoryEmpty);
    inventoryEmpty.style.display = 'block';
  } else {
    inventoryEmpty.style.display = 'none';
    state.inventory.forEach(tag => {
      const chip = document.createElement('div');
      chip.className = 'chip';
      chip.style.display = 'inline-block';
      chip.style.marginBottom = '6px';
      chip.innerText = tag;
      inventoryBox.appendChild(chip);
    });
  }
}

function updateHUD() {
  heartsEl.innerText = '❤️'.repeat(Math.max(0, state.lives));
  scoreEl.innerText = 'Puntaje: ' + state.score + ' / 20';
  messageEl.innerText = state.message || ' ';
  inventoryQuickEl.innerText = state.inventory.length === 0 ? 'Aún no has recogido nada.' : state.inventory.join(', ');
  mapQuickEl.innerHTML = '';
  for (let i=0;i<10;i++){
    const d = document.createElement('div');
    d.className = 'map-cell ' + (i===0?'map-current':'map-pending');
    d.style.width='36px'; d.style.height='36px'; d.style.display='flex'; d.style.alignItems='center'; d.style.justifyContent='center'; d.style.borderRadius='8px';
    d.innerText = i+1;
    mapQuickEl.appendChild(d);
  }
}

function handleOptionClick(optText) {
  try{ soundClick.play(); }catch(e){}
  const pool = state.level === 1 ? LEVEL1 : LEVEL2;
  const node = pool[state.index];
  const correctText = node.correct.text;
  if (optText === correctText) {
    try{ soundCorrect.play(); }catch(e){}
    state.score += 1;
    if (!state.inventory.includes(node.correct.tag)) state.inventory.push(node.correct.tag);
    state.message = "¡Buena elección! +1 punto";
    updateHUD();
    setTimeout(() => {
      if (state.index + 1 < 10) {
        state.index += 1;
        state.options = prepareOptionsForCurrent();
        state.showWrong = null;
        renderPlay();
      } else {
        if (state.level === 1) {
          state.level = 2;
          state.index = 0;
          state.options = prepareOptionsForCurrent();
          state.message = "Has completado el Nivel 1. Comienza Nivel 2.";
          renderPlay();
        } else {
          state.stage = 'finished';
          stagePlayEl.style.display = 'none';
          stageFinishedEl.style.display = 'block';
          finalScore.innerText = 'Puntaje final: ' + state.score + ' / 20';
          finalAvatar.src = state.avatar === 'Estela' ? 'Estela.png' : 'Esteban.png';
          if (music) music.volume = 0.55;
        }
      }
    }, 700);
  } else {
    try{ soundWrong.play(); }catch(e){}
    state.showWrong = optText;
    state.lives -= 1;
    state.message = '✘ Opción no recomendada. Pierdes 1 vida.';
    if (state.lives <= 0) {
      setTimeout(() => {
        state.stage = 'gameover';
        stagePlayEl.style.display = 'none';
        stageGameOverEl.style.display = 'block';
        document.getElementById('gameOverScore').innerText = 'Puntaje: ' + state.score + ' / 20';
      }, 700);
    } else {
      setTimeout(() => {
        renderOptions();
        updateHUD();
      }, 300);
    }
    updateHUD();
    renderOptions();
  }
}

function toggleMusic() {
  if (!state.musicStarted) { startMusicOnce(); }
  if (music.paused) music.play().catch(()=>{}); else music.pause();
}
function showHint() {
  const pool = state.level === 1 ? LEVEL1 : LEVEL2;
  const correct = pool[state.index].correct.text;
  state.message = 'Pista: la mejor opción es \"' + correct + '\".';
  updateHUD();
}
function restartFromAvatar() {
  try { music.pause(); music.currentTime = 0; music.volume = 0.4; } catch(e){}
  state = { stage:'avatar', avatar:null, level:1, index:0, score:0, lives:3, inventory:[], options:[], showWrong:null, musicStarted:false, message: 'Elige tu avatar para comenzar (esto también inicia la música).' };
  document.querySelectorAll('.avatar-card').forEach(c=>c.classList.remove('selected'));
  stageAvatarEl.style.display = 'block';
  stagePlayEl.style.display = 'none';
  stageFinishedEl.style.display = 'none';
  stageGameOverEl.style.display = 'none';
  updateHUD();
}
function retryLevel() {
  state.stage = 'play';
  state.level = 1;
  state.index = 0;
  state.score = 0;
  state.lives = 3;
  state.inventory = [];
  state.options = prepareOptionsForCurrent();
  state.showWrong = null;
  startMusicOnce();
  renderPlay();
  updateHUD();
}

btnPlayAgain.onclick = () => { restartFromAvatar(); };

updateHUD();
</script>
</body>
</html>
