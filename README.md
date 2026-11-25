# NEXORA-<!doctype html>
<html lang="pt-BR">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#090d1b">
<title>NEXORA 2.1 — O app que facilita sua vida</title>
<style>
:root{--bg:#090d1b;--panel:#111a30;--panel2:#172341;--line:#263657;--text:#f3f6ff;--muted:#a9b6d2;--blue:#4d8dff;--purple:#9664ff;--green:#46d6a0}
*{box-sizing:border-box}body{margin:0;background:radial-gradient(circle at 80% 0%,#1c2450 0,transparent 35%),var(--bg);color:var(--text);font:15px system-ui,-apple-system,Segoe UI,Roboto,sans-serif;min-height:100vh}
button,input,textarea,select{font:inherit}button{cursor:pointer;border:0;border-radius:12px;padding:11px 15px;color:white;background:linear-gradient(110deg,var(--blue),var(--purple));font-weight:650}
button.secondary{background:#202d4c;border:1px solid var(--line)}button.danger{background:#5a263b}
.app{display:grid;grid-template-columns:250px 1fr;min-height:100vh}.side{padding:24px 16px;background:#0d1427;border-right:1px solid var(--line);position:sticky;top:0;height:100vh}
.brand{font-size:25px;font-weight:900;letter-spacing:2px;background:linear-gradient(90deg,#65b4ff,#ad79ff);background-clip:text;color:transparent;margin:4px 10px 5px}.tag{color:var(--muted);font-size:11px;margin:0 10px 28px;letter-spacing:1px}
.nav{display:grid;gap:7px}.nav button{background:transparent;text-align:left;color:#bdc9e3;border:1px solid transparent;font-weight:550}.nav button.active,.nav button:hover{background:#1a2747;border-color:#31466f;color:white}
.sidefoot{position:absolute;bottom:20px;left:25px;color:#8090b1;font-size:12px}
main{padding:30px;max-width:1100px;width:100%;margin:auto}.top{display:flex;justify-content:space-between;align-items:center;gap:15px;margin-bottom:25px}.eyebrow{color:#8da8df;font-size:12px;text-transform:uppercase;letter-spacing:1.5px}.title{font-size:30px;margin:4px 0}.muted{color:var(--muted)}.card{background:linear-gradient(145deg,#141f39,#10182c);border:1px solid var(--line);border-radius:18px;padding:20px;margin-bottom:16px;box-shadow:0 12px 35px #0002}
.grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:15px}.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}.stat{padding:16px;background:#172341;border:1px solid var(--line);border-radius:15px}.stat b{font-size:23px;display:block;margin-top:7px}
input,textarea,select{width:100%;background:#0b1326;color:white;border:1px solid #304365;border-radius:11px;padding:12px;outline:none}textarea{min-height:95px;resize:vertical}.formrow{display:flex;gap:9px;margin-top:10px}.formrow>*{flex:1;min-width:0}h2{font-size:18px;margin:0 0 14px}h3{font-size:16px;margin:0 0 8px}.item{display:flex;align-items:center;gap:10px;padding:12px 0;border-bottom:1px solid #263657}.item:last-child{border:0}.item .grow{flex:1;min-width:0}.item small{display:block;color:var(--muted);margin-top:3px}.item button{padding:7px 10px;font-size:12px}.done{text-decoration:line-through;color:#8290aa}.pill{display:inline-block;border:1px solid #3d5482;background:#1b2b50;border-radius:30px;padding:5px 9px;font-size:12px;color:#b9d2ff}
.chat{height:300px;overflow:auto;background:#0b1326;border:1px solid var(--line);border-radius:14px;padding:14px;margin-bottom:12px}.bubble{padding:11px 13px;border-radius:13px;margin:8px 0;max-width:90%;line-height:1.45}.bot{background:#1a2948}.user{background:#3c3c87;margin-left:auto}.hidden{display:none}.menuBtn{display:none}.empty{color:#8e9bb7;padding:12px 0}
@media(max-width:760px){.app{display:block}.side{position:relative;height:auto;padding:14px;border-right:0;border-bottom:1px solid var(--line)}.brand{font-size:22px;margin-left:4px}.tag{margin:0 4px 12px}.nav{display:flex;overflow:auto;padding-bottom:4px}.nav button{white-space:nowrap;padding:9px 12px}.sidefoot{display:none}main{padding:20px 14px}.title{font-size:25px}.grid,.stats{grid-template-columns:1fr}.top{align-items:flex-start}}
</style>
</head>
<body>
<div class="app">
<aside class="side">
  <div class="brand">NEXORA</div><div class="tag">O APP QUE FACILITA SUA VIDA</div>
  <nav class="nav" id="nav">
    <button class="active" data-page="home">⌂ Início</button>
    <button data-page="ai">✦ NEXORA IA</button>
    <button data-page="routine">✓ Minha rotina</button>
    <button data-page="shopping">▣ Compras</button>
    <button data-page="finance">＄ Financeiro</button>
    <button data-page="notes">▤ Anotações</button>
    <button data-page="account">◉ Minha conta</button>
    <button data-page="support">♡ Apoie o NEXORA</button>
  </nav>
  <div class="sidefoot">NEXORA 2.1 • versão simples</div>
</aside>
<main>
  <div class="top"><div><div class="eyebrow">Seu espaço digital</div><h1 class="title" id="pageTitle">Bem-vindo ao NEXORA</h1><div class="muted" id="pageSub">Tudo organizado em um só lugar.</div></div><span class="pill">● Salvo neste aparelho</span></div>
  <section id="home" class="page">
    <div class="card"><div class="eyebrow">Painel principal</div><h2 style="font-size:23px;margin-top:8px">Olá! Este é o seu NEXORA.</h2><p class="muted">Organize tarefas, compras, finanças e ideias em um só lugar. Use o menu para abrir cada área.</p><button onclick="showPage('routine')">Organizar minha rotina</button></div>
    <div class="stats"><div class="stat"><span class="muted">Tarefas</span><b id="taskCount">0</b><small class="muted">na sua rotina</small></div><div class="stat"><span class="muted">Compras</span><b id="buyCount">0</b><small class="muted">na sua lista</small></div><div class="stat"><span class="muted">Anotações</span><b id="noteCount">0</b><small class="muted">guardadas</small></div></div>
    <div class="card" style="margin-top:16px"><h2>Comece por aqui</h2><div class="grid"><button class="secondary" onclick="showPage('ai')">Conversar com a NEXORA IA</button><button class="secondary" onclick="showPage('notes')">Criar uma anotação</button></div></div>
  </section>
  <section id="ai" class="page hidden"><div class="card"><h2>✦ NEXORA IA</h2><p class="muted">Área de conversa demonstrativa. A conexão com uma IA online será ativada numa próxima etapa.</p><div class="chat" id="chat"><div class="bubble bot">Olá! Sou a NEXORA. Nesta versão de demonstração posso ajudar com ideias e organização. A IA online ainda não está conectada.</div></div><div class="formrow"><input id="prompt" placeholder="Digite sua mensagem..." onkeydown="if(event.key==='Enter')sendMessage()"><button onclick="sendMessage()">Enviar</button></div></div></section>
  <section id="routine" class="page hidden"><div class="card"><h2>✓ Minha rotina</h2><p class="muted">Adicione tarefas e marque quando concluir.</p><div class="formrow"><input id="taskInput" placeholder="Ex.: estudar matemática"><button onclick="addItem('tasks','taskInput')">Adicionar</button></div><div id="taskList"></div></div></section>
  <section id="shopping" class="page hidden"><div class="card"><h2>▣ Lista de compras</h2><div class="formrow"><input id="buyInput" placeholder="O que você precisa comprar?"><button onclick="addItem('buys','buyInput')">Adicionar</button></div><div id="buyList"></div></div></section>
  <section id="finance" class="page hidden"><div class="card"><h2>＄ Financeiro</h2><p class="muted">Registre entradas e despesas para acompanhar seus valores.</p><div class="formrow"><input id="moneyDesc" placeholder="Descrição"><input id="moneyValue" type="number" min="0" step=".01" placeholder="Valor (R$)"></div><div class="formrow"><select id="moneyType"><option value="in">Entrada</option><option value="out">Despesa</option></select><button onclick="addMoney()">Registrar</button></div><div class="stats" style="margin-top:15px"><div class="stat">Entradas<b id="income">R$ 0,00</b></div><div class="stat">Despesas<b id="expense">R$ 0,00</b></div><div class="stat">Saldo<b id="balance">R$ 0,00</b></div></div><div id="moneyList" style="margin-top:12px"></div></div></section>
  <section id="notes" class="page hidden"><div class="card"><h2>▤ Anotações</h2><input id="noteTitle" placeholder="Título da anotação"><div style="height:9px"></div><textarea id="noteBody" placeholder="Escreva sua ideia aqui..."></textarea><div style="margin-top:10px"><button onclick="addNote()">Salvar anotação</button></div><div id="noteList" style="margin-top:12px"></div></div></section>
  <section id="support" class="page hidden">
    <div class="card" style="text-align:center">
      <div style="font-size:42px">💙</div>
      <div class="eyebrow">Faça parte dessa evolução</div>
      <h2 style="font-size:25px;margin-top:8px">Apoie o NEXORA</h2>
      <p class="muted">Se você gosta do projeto e deseja ajudar no desenvolvimento de novas funcionalidades, sua contribuição voluntária será muito bem-vinda.</p>
      <div style="background:#0b1326;border:1px solid #304365;border-radius:14px;padding:16px;margin:18px 0">
        <div class="muted" style="font-size:12px;margin-bottom:8px">CHAVE PIX</div>
        <div id="pixKey" style="font-size:22px;font-weight:800;letter-spacing:1px">63991079519</div>
      </div>
      <button onclick="copyPix()">♡ Copiar chave Pix</button>
      <p id="pixFeedback" class="muted" style="font-size:12px;margin-top:12px">Contribuição voluntária. Obrigado por apoiar o NEXORA!</p>
      <p class="muted" style="font-size:11px">A chave Pix foi incluída com autorização da responsável pela conta.</p>
    </div>
  </section>
  <section id="account" class="page hidden"><div class="card"><h2>◉ Minha conta</h2><p class="muted">Esta versão simples não pede cadastro nem senha. Seus dados ficam guardados no armazenamento local deste navegador e aparelho.</p><label class="muted">Como podemos chamar você?</label><div class="formrow"><input id="userName" placeholder="Seu nome"><button onclick="saveName()">Salvar</button></div><p id="savedName" class="muted"></p><hr style="border-color:#263657;margin:20px 0"><h3>Sobre esta versão</h3><p class="muted">Para facilitar a abertura, este é um único arquivo HTML. O login Google, sincronização entre aparelhos e IA conectada à internet ainda não estão ativos.</p><button class="danger" onclick="clearData()">Apagar dados deste aparelho</button></div></section>
</main>
</div>
<script>
const titles={home:['Bem-vindo ao NEXORA','Tudo organizado em um só lugar.'],ai:['NEXORA IA','Converse com sua assistente.'],routine:['Minha rotina','Organize suas tarefas.'],shopping:['Compras','Sua lista de compras.'],finance:['Financeiro','Acompanhe entradas e despesas.'],notes:['Anotações','Guarde suas ideias.'],account:['Minha conta','Configurações desta versão.'],support:['Apoie o NEXORA','Ajude o projeto a crescer.']};
let data={tasks:[],buys:[],money:[],notes:[],name:''};
try{data={...data,...JSON.parse(localStorage.getItem('nexora_data')||'{}')}}catch(e){}
function save(){localStorage.setItem('nexora_data',JSON.stringify(data));render()}
function showPage(p){document.querySelectorAll('.page').forEach(x=>x.classList.add('hidden'));document.getElementById(p).classList.remove('hidden');document.querySelectorAll('.nav button').forEach(x=>x.classList.toggle('active',x.dataset.page===p));document.getElementById('pageTitle').textContent=titles[p][0];document.getElementById('pageSub').textContent=titles[p][1]}
document.getElementById('nav').addEventListener('click',e=>{let b=e.target.closest('button[data-page]');if(b)showPage(b.dataset.page)});
function addItem(key,id){let el=document.getElementById(id),v=el.value.trim();if(!v)return;data[key].push({text:v,done:false});el.value='';save()}
function removeItem(key,i){data[key].splice(i,1);save()}
function toggleItem(key,i){data[key][i].done=!data[key][i].done;save()}
function renderList(key,id){let el=document.getElementById(id);el.innerHTML=data[key].length?data[key].map((x,i)=>`<div class="item"><input style="width:auto" type="checkbox" ${x.done?'checked':''} onchange="toggleItem('${key}',${i})"><div class="grow ${x.done?'done':''}">${esc(x.text)}</div><button class="danger" onclick="removeItem('${key}',${i})">Excluir</button></div>`).join(''):'<div class="empty">Ainda não há itens por aqui.</div>'}
function addMoney(){let desc=document.getElementById('moneyDesc').value.trim(),v=Number(document.getElementById('moneyValue').value),type=document.getElementById('moneyType').value;if(!desc||!v||v<0)return;data.money.push({desc,v,type});document.getElementById('moneyDesc').value='';document.getElementById('moneyValue').value='';save()}
function addNote(){let title=document.getElementById('noteTitle').value.trim(),body=document.getElementById('noteBody').value.trim();if(!title&&!body)return;data.notes.push({title:title||'Anotação',body});document.getElementById('noteTitle').value='';document.getElementById('noteBody').value='';save()}
function removeNote(i){data.notes.splice(i,1);save()}
function saveName(){data.name=document.getElementById('userName').value.trim();save()}
function money(v){return v.toLocaleString('pt-BR',{style:'currency',currency:'BRL'})}
function esc(s){return String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]))}
function render(){renderList('tasks','taskList');renderList('buys','buyList');document.getElementById('taskCount').textContent=data.tasks.length;document.getElementById('buyCount').textContent=data.buys.length;document.getElementById('noteCount').textContent=data.notes.length;
let inc=data.money.filter(x=>x.type==='in').reduce((a,x)=>a+x.v,0),out=data.money.filter(x=>x.type==='out').reduce((a,x)=>a+x.v,0);document.getElementById('income').textContent=money(inc);document.getElementById('expense').textContent=money(out);document.getElementById('balance').textContent=money(inc-out);
document.getElementById('moneyList').innerHTML=data.money.length?data.money.map((x,i)=>`<div class="item"><div class="grow">${esc(x.desc)}<small>${x.type==='in'?'Entrada':'Despesa'}</small></div><b>${x.type==='in'?'+':'−'} ${money(x.v)}</b><button class="danger" onclick="data.money.splice(${i},1);save()">Excluir</button></div>`).join(''):'<div class="empty">Nenhum lançamento registrado.</div>';
document.getElementById('noteList').innerHTML=data.notes.length?data.notes.map((x,i)=>`<div class="item"><div class="grow"><b>${esc(x.title)}</b><small>${esc(x.body)}</small></div><button class="danger" onclick="removeNote(${i})">Excluir</button></div>`).join(''):'<div class="empty">Suas anotações aparecerão aqui.</div>';document.getElementById('userName').value=data.name||'';document.getElementById('savedName').textContent=data.name?'Nome salvo: '+data.name:''}
function copyPix(){
  const key='63991079519';
  if(navigator.clipboard && window.isSecureContext){
    navigator.clipboard.writeText(key).then(()=>{document.getElementById('pixFeedback').textContent='Chave Pix copiada! Obrigado pelo apoio 💙';}).catch(()=>fallbackCopy(key));
  } else { fallbackCopy(key); }
}
function fallbackCopy(value){
  const field=document.createElement('textarea');field.value=value;document.body.appendChild(field);field.select();
  try{document.execCommand('copy');document.getElementById('pixFeedback').textContent='Chave Pix copiada! Obrigado pelo apoio 💙';}
  catch(e){document.getElementById('pixFeedback').textContent='Não foi possível copiar automaticamente. Selecione e copie a chave acima.';}
  field.remove();
}
function sendMessage(){let el=document.getElementById('prompt'),v=el.value.trim();if(!v)return;let chat=document.getElementById('chat');chat.innerHTML+=`<div class="bubble user">${esc(v)}</div><div class="bubble bot">Recebi sua mensagem! Nesta versão de demonstração, a IA online ainda não está conectada. Posso guardar suas tarefas e anotações nas outras áreas do NEXORA.</div>`;el.value='';chat.scrollTop=chat.scrollHeight}
function clearData(){if(confirm('Tem certeza de que deseja apagar os dados salvos neste aparelho?')){localStorage.removeItem('nexora_data');data={tasks:[],buys:[],money:[],notes:[],name:''};render()}}
render();
</script>
</body></html>