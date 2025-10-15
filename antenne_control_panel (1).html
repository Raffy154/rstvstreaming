<!doctype html>
<html lang="it">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Pannello di Controllo Antenne TV</title>
  <style>
    body{margin:0;font-family:Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;background:linear-gradient(180deg,#071025 0%,#0f1724 100%);color:#e6f0ff;}
    .login-box{position:fixed;top:0;left:0;width:100%;height:100%;background:#0b1220;display:flex;flex-direction:column;align-items:center;justify-content:center;z-index:999;}
    input{width:200px;padding:10px;margin:10px 0;border:none;border-radius:8px;background:#1e293b;color:white;text-align:center;font-size:16px;}
    button{background:#1d9bf0;color:white;border:none;padding:10px 16px;border-radius:8px;cursor:pointer;width:100%;font-weight:bold;}
    .hidden{display:none;}
    .container{max-width:1000px;margin:0 auto;padding:20px;}
    h1{margin-bottom:20px;}
    .antenna-list{margin-top:20px;}
    .antenna-item{padding:10px;background:#0b1220;margin-bottom:8px;border-radius:8px;display:flex;justify-content:space-between;align-items:center;cursor:pointer;transition:all 0.3s ease;}
    .antenna-item.online{border-left:4px solid #22c55e;}
    .antenna-item.offline{border-left:4px solid #ef4444;}
    .controls{margin-top:20px;}
    .controls label{display:block;margin-top:10px;}
  </style>
</head>
<body>

<div class="login-box" id="loginBox">
  <h2>Inserisci PIN di accesso</h2>
  <input type="password" id="pinInput" placeholder="PIN" maxlength="6" />
  <button id="loginBtn">Accedi</button>
  <div id="errorMsg" style="color:#ef4444;margin-top:8px;display:none;">PIN errato</div>
</div>

<div class="container hidden" id="fullPanel">
  <h1>Pannello di Controllo Antenne TV</h1>
  <button id="addAntennaBtn">Aggiungi antenna</button>
  <div class="antenna-list" id="antennaList"></div>
  <div class="controls">
    <h3>Dettagli antenna selezionata</h3>
    <label>Azimut: <span id="azVal">0</span>°</label>
    <input type="range" id="azimuth" min="0" max="360" step="1">
    <label>Potenza trasmissione: <span id="powerVal">50</span>%</label>
    <input type="range" id="power" min="0" max="100" step="1">
    <button id="applyBtn">Applica modifiche</button>
  </div>
</div>

<script>
const loginBtn = document.getElementById('loginBtn');
const pinInput = document.getElementById('pinInput');
const loginBox = document.getElementById('loginBox');
const errorMsg = document.getElementById('errorMsg');
const fullPanel = document.getElementById('fullPanel');

loginBtn.addEventListener('click', ()=> {
  const pin = pinInput.value.trim();
  if(pin === '111315'){
    loginBox.classList.add('hidden');
    fullPanel.classList.remove('hidden');
    document.title = 'Pannello di Controllo Antenne TV';
    initPanel();
  } else {
    errorMsg.style.display = 'block';
  }
});

pinInput.addEventListener('keydown', e => { if(e.key==='Enter') loginBtn.click(); });

function initPanel(){
  const antennaList = document.getElementById('antennaList');
  const azimuth = document.getElementById('azimuth');
  const azVal = document.getElementById('azVal');
  const power = document.getElementById('power');
  const powerVal = document.getElementById('powerVal');
  const applyBtn = document.getElementById('applyBtn');

  let antennas = [];
  let selectedIndex = null;

  function renderAntennas(){
    antennaList.innerHTML = '';
    antennas.forEach((a, i)=>{
      const div = document.createElement('div');
      div.className = 'antenna-item '+(a.online?'online':'offline');
      div.innerHTML = `<span>${a.name} (Az:${a.az}° | Power:${a.power}%)</span> <span>${a.online?'Online':'Offline'}</span>`;
      div.addEventListener('click', ()=> selectAntenna(i));
      antennaList.appendChild(div);
    });
  }

  function selectAntenna(index){
    selectedIndex = index;
    const a = antennas[index];
    azimuth.value = a.az;
    azVal.textContent = a.az;
    power.value = a.power;
    powerVal.textContent = a.power;
  }

  document.getElementById('addAntennaBtn').addEventListener('click', ()=>{
    const name = prompt('Nome nuova antenna:');
    if(!name) return;
    antennas.push({name, az:0, power:50, online:true});
    renderAntennas();
  });

  azimuth.addEventListener('input', ()=>{ 
    if(selectedIndex!==null){ 
      antennas[selectedIndex].az = Number(azimuth.value);
      azVal.textContent = azimuth.value; 
      renderAntennas();
    } 
  });

  power.addEventListener('input', ()=>{ 
    if(selectedIndex!==null){ 
      antennas[selectedIndex].power = Number(power.value);
      powerVal.textContent = power.value; 
      renderAntennas();
    } 
  });

  applyBtn.addEventListener('click', ()=>{
    if(selectedIndex===null) return;
    antennas[selectedIndex].az = Number(azimuth.value);
    antennas[selectedIndex].power = Number(power.value);
    renderAntennas();
  });

  renderAntennas();
}
</script>

</body>
</html>
