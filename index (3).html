<!DOCTYPE html>
<html lang="ru"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,user-scalable=no">
<title>Labyrinth EV3</title>
<style>
*{box-sizing:border-box;-webkit-tap-highlight-color:transparent}
body{margin:0;background:radial-gradient(circle at 50% 0,#0e2a4a,#05080f 70%) fixed;color:#dff;font-family:system-ui,Segoe UI,sans-serif;user-select:none;overflow-x:hidden}
.scr{display:none;flex-direction:column;align-items:center;padding:12px;min-height:100vh;gap:10px}
.scr.on{display:flex}
h1{margin:30px 0 0;font-size:clamp(26px,6vw,46px);color:#4df;text-shadow:0 0 18px #09f;text-align:center}
h1 span{color:#f80;text-shadow:0 0 18px #f80}
h2{color:#4df;margin:6px}
.btn{background:#0b1a2e;color:#cff;border:1px solid #0cf;border-radius:10px;padding:11px 20px;font-size:17px;cursor:pointer;box-shadow:0 0 10px #0cf6;transition:.15s;min-width:230px}
.btn:hover{background:#0c3a5a;transform:translateY(-2px);box-shadow:0 0 18px #0cf}
.btn.o{border-color:#f80;box-shadow:0 0 10px #f806}
.btn.sm{min-width:0;padding:6px 12px;font-size:14px}
.btn.act{background:#0a5a8a;border-color:#fff}
.row{display:flex;gap:8px;flex-wrap:wrap;justify-content:center}
#lg{display:grid;grid-template-columns:repeat(auto-fill,minmax(64px,1fr));gap:8px;max-width:720px;width:100%}
.lv{padding:10px 0;border-radius:10px;border:1px solid #567;background:#1b222c;color:#889;font-size:18px;cursor:pointer;text-align:center}
.lv.ok{background:#0a3a22;border-color:#3f6;color:#9fb;box-shadow:0 0 8px #3f66}
.lv.cur{background:#0a5a8a;border-color:#4df;color:#fff;box-shadow:0 0 14px #4df;animation:pl 1s infinite alternate}
.lv small{display:block;font-size:12px;color:#fd2;min-height:14px}
@keyframes pl{to{box-shadow:0 0 24px #4df}}
#hud{display:flex;gap:6px 14px;flex-wrap:wrap;justify-content:center;align-items:center;font-size:15px;background:#0a1626;border:1px solid #0cf5;border-radius:10px;padding:6px 12px;max-width:100%}
#eb{width:110px;height:12px;border:1px solid #3f6;border-radius:6px;overflow:hidden;background:#021}
#ef{display:block;height:100%;background:linear-gradient(90deg,#f80,#3f6);width:100%}
#cv{background:#000;border:2px solid #0cf;border-radius:6px;box-shadow:0 0 20px #0cf6;max-width:100%}
#fxs{font-size:13px;color:#fd2;min-height:16px}
#task{font-size:14px;color:#8fc;min-height:18px;text-align:center}
#dp{display:grid;grid-template-columns:repeat(3,58px);grid-template-rows:repeat(2,52px);gap:6px;grid-template-areas:". u ." "l d r";touch-action:none}
#dp button{background:#0b1a2e;color:#4df;border:1px solid #0cf;border-radius:10px;font-size:24px;box-shadow:0 0 8px #0cf6;touch-action:none}
#dp button:active{background:#0a5a8a}
#toast{position:fixed;left:50%;top:14%;transform:translateX(-50%);background:#000c;border:1px solid #4df;padding:8px 16px;border-radius:20px;opacity:0;transition:.3s;pointer-events:none;z-index:30}
#toast.on{opacity:1}
#modal{display:none;position:fixed;inset:0;background:#000a;z-index:25;align-items:center;justify-content:center;padding:10px}
#modal.on{display:flex}
.box{background:#0a1626;border:1px solid #0cf;border-radius:14px;padding:18px;max-width:440px;width:100%;max-height:92vh;overflow:auto;display:flex;flex-direction:column;gap:10px;align-items:center;text-align:center;box-shadow:0 0 30px #0cf6}
.box label{display:flex;gap:8px;align-items:center;justify-content:space-between;width:100%}
.fact{color:#8fc;font-size:14px}
</style></head><body>
<div style="position:fixed;top:8px;right:8px;z-index:20" class="row"><button class="btn sm" onclick="setLang('kk')">Қаз</button><button class="btn sm" onclick="setLang('ru')">Рус</button></div>

<!-- Главное меню -->
<div id="menu" class="scr on"><div id="pb"></div>
 <h1>LABYRINTH <span>EV3</span></h1><div data-i="title" style="color:#8cf;font-size:20px"></div>
 <canvas id="mr" width="260" height="150"></canvas>
 <button class="btn" data-i="start" onclick="start(1)"></button>
 <button class="btn" data-i="cont" onclick="start(Math.min(S.un,50))"></button>
 <button class="btn" data-i="lv" onclick="showLevels()"></button>
 <button class="btn o" data-i="daily" onclick="start(0,1)"></button>
 <div class="row"><button class="btn sm" data-i="shop" onclick="modal(shopM)"></button><button class="btn sm" data-i="prof" onclick="modal(profM)"></button><button class="btn sm" data-i="rank" onclick="modal(rankM)"></button></div>
 <div><span data-i="diff"></span>:</div>
 <div class="row"><button class="btn sm" id="d0" data-i="d0" onclick="setDiff(0)"></button><button class="btn sm" id="d1" data-i="d1" onclick="setDiff(1)"></button><button class="btn sm" id="d2" data-i="d2" onclick="setDiff(2)"></button></div>
 <div class="row"><button class="btn sm" data-i="set" onclick="modal(setM)"></button><button class="btn sm" data-i="ach" onclick="modal(achM)"></button><button class="btn sm" data-i="info" onclick="modal(infoM)"></button></div>
</div>

<!-- Выбор уровня -->
<div id="lvs" class="scr"><h1 data-i="lv"></h1><div id="lg"></div><button class="btn" data-i="back" onclick="show('menu')"></button></div>

<!-- Игра -->
<div id="game" class="scr" style="padding:6px;gap:6px">
 <div id="hud"><span id="hL"></span><span id="hS"></span><span id="hB"></span><span id="hT"></span><div id="eb"><i id="ef"></i></div></div>
 <div id="fxs"></div><div id="task"></div>
 <canvas id="cv"></canvas>
 <div class="row"><button class="btn sm" id="hb" onclick="useHint()"></button><button class="btn sm" data-i="pause" onclick="togglePause()"></button><button class="btn sm" data-i="restart" onclick="restart()"></button><button class="btn sm" data-i="menu" onclick="toMenu()"></button></div>
 <div id="dp">
  <button style="grid-area:u" onpointerdown="ptr=[0,-1]" onpointerup="ptr=null" onpointerleave="ptr=null" onpointercancel="ptr=null">▲</button>
  <button style="grid-area:l" onpointerdown="ptr=[-1,0]" onpointerup="ptr=null" onpointerleave="ptr=null" onpointercancel="ptr=null">◀</button>
  <button style="grid-area:d" onpointerdown="ptr=[0,1]" onpointerup="ptr=null" onpointerleave="ptr=null" onpointercancel="ptr=null">▼</button>
  <button style="grid-area:r" onpointerdown="ptr=[1,0]" onpointerup="ptr=null" onpointerleave="ptr=null" onpointercancel="ptr=null">▶</button>
 </div>
</div>
<div id="toast"></div><div id="modal"><div class="box" id="mb"></div></div>

<script>
// ===== Тексты (рус / қаз) =====
const T={ru:{title:'Путь робота',start:'Начать игру',cont:'Продолжить',lv:'Выбор уровня',diff:'Сложность',d0:'Легкий',d1:'Средний',d2:'Сложный',set:'Настройки',ach:'Достижения',info:'Информация об игре',daily:'Ежедневное испытание',level:'Уровень',score:'Очки',bonus:'Бонусы',time:'Время',hint:'Подсказка',pause:'Пауза',resume:'Продолжить',restart:'Перезапуск',menu:'Главное меню',win:'Уровень пройден!',next:'Следующий уровень',again:'Повторить',stars:'Звёзды',lose:'Энергия закончилась!',snd:'Громкость звуков',mus:'Музыка',anim:'Анимации',spd:'Скорость робота',tmr:'Таймер',hints:'Подсказки',full:'Полноэкранный режим',lang:'Язык',close:'Закрыть',back:'Назад',
battery:'Батарея',boost:'Ускоритель',scan:'Сканер',magnet:'Магнит',shield:'Щит',gear:'Золотая шестеренка',chip:'Микросхема',key:'Ключ',shieldlost:'Щит поглотил удар!',hit:'Столкновение! −энергия',door:'Дверь открыта!',needkey:'Нужен ключ!',nohint:'Подсказки закончились',
infotxt:'Управляй роботом EV3 стрелками, WASD или кнопками на экране. Доберись до зарядной станции, собирай бонусы, избегай охранников, лазеров и ловушек. Ключ открывает дверь. Энергия расходуется при движении — собирай батареи. Пробел — пауза.',
a1:'Первый шаг: пройди уровень 1',a2:'Пройди 10 уровней',a3:'Собери 50 звёзд',a4:'Пройди все 50 уровней',
tasks:['Найди правильный маршрут к станции.','Определи направление движения: куда повернуть?','Найди кратчайший путь.','Используй датчик расстояния: избегай охранников.'],
facts:['Датчик расстояния EV3 помогает роботу обнаруживать препятствия перед собой.','Блок EV3 — «мозг» робота: в нём процессор и экран.','Алгоритм — это последовательность команд для решения задачи.','Гироскопический датчик измеряет угол поворота робота.']},
kk:{title:'Роботтың жолы',start:'Ойынды бастау',cont:'Жалғастыру',lv:'Деңгей таңдау',diff:'Күрделілік',d0:'Жеңіл',d1:'Орташа',d2:'Қиын',set:'Баптаулар',ach:'Жетістіктер',info:'Ойын туралы',daily:'Күнделікті сынақ',level:'Деңгей',score:'Ұпай',bonus:'Бонустар',time:'Уақыт',hint:'Кеңес',pause:'Пауза',resume:'Жалғастыру',restart:'Қайта бастау',menu:'Басты мәзір',win:'Деңгей аяқталды!',next:'Келесі деңгей',again:'Қайталау',stars:'Жұлдыздар',lose:'Қуат таусылды!',snd:'Дыбыс деңгейі',mus:'Музыка',anim:'Анимациялар',spd:'Робот жылдамдығы',tmr:'Таймер',hints:'Кеңестер',full:'Толық экран',lang:'Тіл',close:'Жабу',back:'Артқа',
battery:'Батарея',boost:'Үдеткіш',scan:'Сканер',magnet:'Магнит',shield:'Қалқан',gear:'Алтын тісті доңғалақ',chip:'Микросхема',key:'Кілт',shieldlost:'Қалқан соққыны сіңірді!',hit:'Соқтығысу! Қуат азайды',door:'Есік ашылды!',needkey:'Кілт керек!',nohint:'Кеңестер таусылды',
infotxt:'EV3 роботын көрсеткілермен, WASD немесе экрандағы батырмалармен басқар. Зарядтау станциясына жет, бонустар жина, күзетшілерден, лазерлерден және тұзақтардан аулақ бол. Кілт есікті ашады. Қуат қозғалысқа жұмсалады — батареяларды жина. Бос орын — пауза.',
a1:'Алғашқы қадам: 1-деңгейді өт',a2:'10 деңгей өт',a3:'50 жұлдыз жина',a4:'Барлық 50 деңгейді өт',
tasks:['Станцияға апаратын дұрыс жолды тап.','Қозғалыс бағытын анықта: қайда бұрылу керек?','Ең қысқа жолды тап.','Қашықтық датчигін пайдалан: күзетшілерден аулақ бол.'],
facts:['EV3 қашықтық датчигі роботқа алдындағы кедергілерді анықтауға көмектеседі.','EV3 блогы — роботтың «миы»: онда процессор мен экран бар.','Алгоритм — міндетті шешуге арналған командалар тізбегі.','Гироскоп датчигі роботтың бұрылу бұрышын өлшейді.']}};
const DIR=[[1,0],[-1,0],[0,1],[0,-1]];
const $=s=>document.querySelector(s);
// ===== Сохранение =====
const DS={vol:.6,mus:false,anim:true,spd:1,tm:true,hint:true};
let KEY=localStorage.getItem('ev3_last')||'ev3';
let S={lang:'ru',diff:0,un:1,st:{},sc:{},chips:0,set:{...DS}};
try{const o=JSON.parse(localStorage.getItem(KEY));if(o){Object.assign(S,o);S.set={...DS,...o.set}}}catch(e){}
const save=()=>{try{localStorage.setItem(KEY,JSON.stringify(S))}catch(e){}};
const t=k=>(T[S.lang]||T.ru)[k]||k;
let G=null,ptr=null,hk=[],M=null,toastT;
const KM={ArrowUp:[0,-1],KeyW:[0,-1],ArrowDown:[0,1],KeyS:[0,1],ArrowLeft:[-1,0],KeyA:[-1,0],ArrowRight:[1,0],KeyD:[1,0]};
const dirNow=()=>ptr||(hk.length?KM[hk[hk.length-1]]:null);
// ===== Интерфейс, язык, окна =====
function applyLang(){document.documentElement.lang=S.lang=='kk'?'kk':'ru';document.querySelectorAll('[data-i]').forEach(e=>e.textContent=t(e.dataset.i));
 for(let i=0;i<3;i++)$('#d'+i).classList.toggle('act',S.diff==i);if($('#lvs').classList.contains('on'))buildLevels();if(M&&$('#modal').classList.contains('on'))render()}
function setLang(l){S.lang=l;save();applyLang()}
function setDiff(d){S.diff=d;save();snd(600,.05);applyLang()}
function show(id){document.querySelectorAll('.scr').forEach(e=>e.classList.toggle('on',e.id==id));snd(500,.05);if(id=='menu'&&G)G.over=1}
function modal(fn){M=fn;render();$('#modal').classList.add('on');snd(500,.05)}
function render(){$('#mb').innerHTML=M()}
function closeModal(){$('#modal').classList.remove('on');M=null}
function toast(m){const e=$('#toast');e.textContent=m;e.classList.add('on');clearTimeout(toastT);toastT=setTimeout(()=>e.classList.remove('on'),1400)}
const infoM=()=>`<h2>${t('info')}</h2><p>${t('infotxt')}</p><button class="btn" onclick="closeModal()">${t('close')}</button>`;
function achM(){const n=Object.keys(S.st).length,st=Object.values(S.st).reduce((a,b)=>a+b,0);
 const L=[[n>=1,'a1'],[n>=10,'a2'],[st>=50,'a3'],[n>=50,'a4']];
 return `<h2>${t('ach')}</h2>`+L.map(([ok,k])=>`<div style="color:${ok?'#3f6':'#889'}">${ok?'✔':'🔒'} ${t(k)}</div>`).join('')+`<div>${t('stars')}: ${st}/150</div><button class="btn" onclick="closeModal()">${t('close')}</button>`}
function setM(){const s=S.set;return `<h2>${t('set')}</h2>
<div class="row"><button class="btn sm ${S.lang=='kk'?'act':''}" onclick="setLang('kk')">Қаз</button><button class="btn sm ${S.lang=='ru'?'act':''}" onclick="setLang('ru')">Рус</button></div>
<label>${t('snd')}<input type=range min=0 max=1 step=.1 value=${s.vol} oninput="S.set.vol=+this.value;save();snd(700,.08)"></label>
<label>${t('spd')}<input type=range min=.5 max=2 step=.25 value=${s.spd} oninput="S.set.spd=+this.value;save()"></label>
<label>${t('mus')}<input type=checkbox ${s.mus?'checked':''} onchange="S.set.mus=this.checked;save();music()"></label>
<label>${t('anim')}<input type=checkbox ${s.anim?'checked':''} onchange="S.set.anim=this.checked;save()"></label>
<label>${t('tmr')}<input type=checkbox ${s.tm?'checked':''} onchange="S.set.tm=this.checked;save()"></label>
<label>${t('hints')}<input type=checkbox ${s.hint?'checked':''} onchange="S.set.hint=this.checked;save()"></label>
<button class="btn sm" onclick="fs()">${t('full')}</button><button class="btn" onclick="closeModal()">${t('close')}</button>`}
function fs(){try{document.fullscreenElement?document.exitFullscreen():document.documentElement.requestFullscreen()}catch(e){}}
function showLevels(){buildLevels();show('lvs')}
function buildLevels(){let h='';for(let i=1;i<=50;i++){const c=S.st[i]?'ok':i==S.un?'cur':'';const lock=i>S.un;
 h+=`<div class="lv ${c}" ${lock?'':`onclick="start(${i})"`}>${lock?'🔒':i}<small>${'★'.repeat(S.st[i]||0)}</small></div>`}$('#lg').innerHTML=h}
// ===== Звук (Web Audio) =====
let AC,mi;
function snd(f,d=.1,ty='square',v=.15,sl){if(S.set.vol<=0)return;try{AC=AC||new(window.AudioContext||window.webkitAudioContext)();if(AC.state=='suspended')AC.resume();
 const o=AC.createOscillator(),g=AC.createGain();o.type=ty;o.frequency.value=f;if(sl)o.frequency.exponentialRampToValueAtTime(sl,AC.currentTime+d);
 g.gain.value=v*S.set.vol;g.gain.exponentialRampToValueAtTime(.001,AC.currentTime+d);o.connect(g);g.connect(AC.destination);o.start();o.stop(AC.currentTime+d)}catch(e){}}
function music(){clearInterval(mi);if(S.set.mus){let k=0;const N=[262,330,392,523,392,330,294,349,440,349];mi=setInterval(()=>snd(N[k++%N.length],.25,'triangle',.06),320)}}
// ===== Генератор лабиринтов, BFS =====
const rng=a=>()=>{a|=0;a=a+0x6D2B79F5|0;let t=Math.imul(a^a>>>15,1|a);t=t+Math.imul(t^t>>>7,61|t)^t;return((t^t>>>14)>>>0)/4294967296};
// Заливка (BFS) от точки: массив расстояний, -1 = недостижимо
function flood(g,sx,sy,blk){const D=g.map(r=>r.map(()=>-1)),q=[[sx,sy]];D[sy][sx]=0;
 for(let i=0;i<q.length;i++){const[x,y]=q[i];for(const[dx,dy]of DIR){const a=x+dx,b=y+dy;if(g[b]&&g[b][a]===0&&D[b][a]<0&&!(blk&&blk(a,b))){D[b][a]=D[y][x]+1;q.push([a,b])}}}return D}
function pathTo(D,ex,ey){if(D[ey][ex]<0)return null;const p=[[ex,ey]];let x=ex,y=ey;
 while(D[y][x]>0){for(const[dx,dy]of DIR){const a=x+dx,b=y+dy;if(D[b]&&D[b][a]===D[y][x]-1){x=a;y=b;p.push([x,y]);break}}}return p.reverse()}
function build(L,seed,daily){
 const d=S.diff,rnd=rng(seed);let n=Math.min(23,Math.max(7,7+2*Math.floor((L+2)/5)+(d-1)*2));if(daily)n=15;
 const g=[];for(let y=0;y<n;y++)g.push(Array(n).fill(1));
 const st=[[1,1]];g[1][1]=0; // DFS-прокладка коридоров
 while(st.length){const[x,y]=st[st.length-1];const nb=[[2,0],[-2,0],[0,2],[0,-2]].filter(([dx,dy])=>{const a=x+dx,b=y+dy;return a>0&&b>0&&a<n-1&&b<n-1&&g[b][a]});
  if(!nb.length){st.pop();continue}const[dx,dy]=nb[rnd()*nb.length|0];g[y+dy/2][x+dx/2]=0;g[y+dy][x+dx]=0;st.push([x+dx,y+dy])}
 const op=Math.floor(n*n*[.06,.035,.015][d]); // проломы стен: меньше тупиков на лёгком
 for(let i=0;i<op;i++){const x=1+(rnd()*(n-2)|0),y=1+(rnd()*(n-2)|0);if(g[y][x]&&((!g[y][x-1]&&!g[y][x+1])||(!g[y-1][x]&&!g[y+1][x])))g[y][x]=0}
 const D0=flood(g,1,1),P=pathTo(D0,n-2,n-2);
 if(!P)return build(L,seed+1,daily); // проверка проходимости
 const key=(x,y)=>x+','+y,onP=new Set(P.map(p=>key(p[0],p[1])));
 let F=[];for(let y=0;y<n;y++)for(let x=0;x<n;x++)if(!g[y][x]&&!(x==1&&y==1)&&!(x==n-2&&y==n-2))F.push([x,y]);
 for(let i=F.length-1;i>0;i--){const j=rnd()*(i+1)|0;[F[i],F[j]]=[F[j],F[i]]}
 const take=f=>{const i=F.findIndex(f||(()=>1));return i<0?null:F.splice(i,1)[0]};
 const items=[],hz=[.5,2.5,3.75][d];let door=null;
 if(L>=11&&L%2==1&&P.length>8){const q=P[Math.floor(P.length*.55)];door={x:q[0],y:q[1],open:0};F=F.filter(c=>!(c[0]==q[0]&&c[1]==q[1]));
  const D2=flood(g,1,1,(x,y)=>x==q[0]&&y==q[1]);const c=take(c=>D2[c[1]][c[0]]>3);if(c)items.push({t:'key',x:c[0],y:c[1]});else door=null}
 const types=[];const add=(k,c)=>{for(let i=0;i<c;i++)types.push(k)};
 add('battery',Math.round((2+(L>30?1:0))*[1.5,1,.8][d]));add('boost',1);add('scan',1);add('gear',2+(L%3==0?1:0));
 if(L>5)add('magnet',1);if(L>10)add('shield',1);if(L%5==0)add('chip',1);
 types.forEach(k=>{const c=take();if(c)items.push({t:k,x:c[0],y:c[1]})});
 const total=items.filter(i=>i.t!='key').length;
 let ng=L>=11?Math.min(Math.floor(n*n/20),Math.round((1+(L-11)/10)*hz)):0;if(d>=1&&L>=4)ng=Math.max(ng,1);
 const guards=[];for(let i=0;i<ng;i++){const c=take(c=>D0[c[1]][c[0]]>=6)||take();if(c)guards.push({x:c[0],y:c[1],fx:c[0],fy:c[1],lx:-1,ly:-1,t:rnd()*300,iv:[550,450,350][d]})}
 const lasers=[],traps=[],nl=L>=21?Math.min(Math.floor(n*n/25),Math.round((L-16)/5*hz)):0,nt=L>=21?Math.min(Math.floor(n*n/25),Math.round((L-16)/4*hz)):0;
 for(let i=0;i<nl;i++){const c=take();if(c)lasers.push({x:c[0],y:c[1],ph:rnd()*3000})}
 for(let i=0;i<nt;i++){const c=take(c=>!onP.has(key(c[0],c[1])))||take();if(c)traps.push({x:c[0],y:c[1]})}
 const cost=[0,.25,.5][d]+(L>30?.25:0),enMax=Math.max(100,Math.ceil(P.length*cost*1.7+40));
 return{L,daily,g,n,items,total,guards,lasers,traps,door,P,cost,enMax,en:enMax,rx:1,ry:1,px:1,py:1,ang:0,tang:0,mv:null,wp:0,hasKey:0,score:0,coll:0,hits:0,time:0,boost:0,scan:0,mag:0,inv:0,hintT:0,glow:0,shield:0,fx:[],nt:0,
  hints:[5,3,1][d],par:P.length*.35+15,paused:0,over:0,task:5000,s:20}}
// ===== Запуск уровня =====
function start(L,daily){closeModal();const seed=daily?Number(new Date().toISOString().slice(0,10).replace(/-/g,'')):L*7919+S.diff*101+13;
 G=build(daily?24:L,seed,daily);G.seed=seed;G.reqL=L;show('game');layout();$('#task').textContent=t('tasks')[G.L%4];snd(400,.2,'sine',.15,800)}
function restart(){closeModal();start(G.reqL,G.daily)}
function toMenu(){closeModal();if(G)G.over=1;show('menu')}
function layout(){if(!G||!$('#game').classList.contains('on'))return;const n=G.n,av=Math.min(innerWidth-12,innerHeight-(innerWidth<innerHeight?330:280));
 G.s=Math.max(10,Math.floor(Math.max(200,av)/n));const s=G.s,cv=$('#cv');cv.width=cv.height=s*n;
 const b=G.bg=document.createElement('canvas');b.width=b.height=s*n;const c=b.getContext('2d');
 for(let y=0;y<n;y++)for(let x=0;x<n;x++){if(G.g[y][x]){c.fillStyle='#16314f';c.fillRect(x*s,y*s,s,s);c.strokeStyle='#2bd8';c.lineWidth=1;c.strokeRect(x*s+1.5,y*s+1.5,s-3,s-3)}
  else{c.fillStyle=(x+y)%2?'#0b1828':'#0d1d31';c.fillRect(x*s,y*s,s,s)}}
 c.fillStyle='#0a5a2a';c.fillRect(s,s,s,s);c.strokeStyle='#3f6';c.lineWidth=2;c.strokeRect(s+2,s+2,s-4,s-4)}
addEventListener('resize',layout);
// ===== Рисование =====
const IC={battery:'#3f6',boost:'#fa0',scan:'#4df',magnet:'#f4a',shield:'#69f',gear:'#fd2',chip:'#a6f',key:'#ff6'};
function drawItem(c,k,x,y,r,tm){const col=IC[k];c.save();c.translate(x,y+Math.sin(tm/300+x)*r*.12);c.shadowColor=col;c.shadowBlur=r;c.fillStyle=col;c.strokeStyle=col;c.lineWidth=Math.max(1.5,r*.22);
 if(k=='battery'){c.fillRect(-r*.6,-r*.4,r*1.2,r*.8);c.fillRect(r*.6,-r*.15,r*.2,r*.3)}
 else if(k=='boost'||k=='gear'){c.beginPath();for(let i=0;i<8;i++){const a=i*Math.PI/4+tm/600;c.moveTo(0,0);c.lineTo(Math.cos(a)*r,Math.sin(a)*r)}c.stroke();c.beginPath();c.arc(0,0,r*.6,0,7);k=='gear'?c.fill():c.stroke()}
 else if(k=='scan'){c.beginPath();c.arc(0,0,r*.7,0,7);c.stroke();c.beginPath();c.arc(0,0,r*.22,0,7);c.fill()}
 else if(k=='magnet'){c.beginPath();c.moveTo(-r*.6,-r*.7);c.lineTo(-r*.6,0);c.arc(0,0,r*.6,Math.PI,0,true);c.lineTo(r*.6,-r*.7);c.stroke()}
 else if(k=='shield'){c.beginPath();c.moveTo(-r*.7,-r*.7);c.lineTo(r*.7,-r*.7);c.lineTo(r*.7,0);c.quadraticCurveTo(r*.6,r*.7,0,r*.9);c.quadraticCurveTo(-r*.6,r*.7,-r*.7,0);c.closePath();c.fill()}
 else if(k=='chip'){c.fillRect(-r*.5,-r*.5,r,r);c.beginPath();for(let i=-1;i<=1;i++){c.moveTo(i*r*.3,-r*.8);c.lineTo(i*r*.3,r*.8);c.moveTo(-r*.8,i*r*.3);c.lineTo(r*.8,i*r*.3)}c.stroke()}
 else{c.beginPath();c.arc(-r*.4,0,r*.35,0,7);c.stroke();c.beginPath();c.moveTo(-r*.05,0);c.lineTo(r*.8,0);c.moveTo(r*.5,0);c.lineTo(r*.5,r*.4);c.stroke()}
 c.restore()}
// Робот EV3: корпус, экран, кнопки, датчик, колёса с протектором
function drawRobot(c,x,y,s,ang,wp,glow,happy,tm){c.save();c.translate(x,y);c.rotate(ang);const u=s/10;if(glow){c.shadowColor=glow;c.shadowBlur=u*5}
 c.fillStyle='#111';c.fillRect(-3.8*u,-5*u,7.6*u,2*u);c.fillRect(-3.8*u,3*u,7.6*u,2*u);
 c.strokeStyle='#888';c.lineWidth=Math.max(1,u*.4);const ph=(wp%1.4+1.4)%1.4;c.beginPath();
 for(let k=0;k<5;k++){const lx=(-3.5+k*1.4+ph)*u;if(lx<3.8*u){c.moveTo(lx,-5*u);c.lineTo(lx,-3*u);c.moveTo(lx,3*u);c.lineTo(lx,5*u)}}c.stroke();
 c.fillStyle=(window.SKC||'#b8bcc4');c.fillRect(-3*u,-3.2*u,6*u,6.4*u);c.fillStyle=(window.SKS||'#d22');c.fillRect(-3*u,-3.2*u,1.4*u,6.4*u);
 c.fillStyle='#222';c.fillRect(-1.2*u,-2*u,3.4*u,2.6*u);c.fillStyle=happy&&Math.floor(tm/250)%2?'#ff0':'#7f9';c.fillRect(-.9*u,-1.7*u,2.8*u,2*u);
 c.fillStyle='#222';for(let i=-1;i<=1;i++)c.fillRect(2.4*u,i*1.5*u-.4*u,.8*u,.8*u);
 c.fillStyle='#222';c.fillRect(3*u,-1.8*u,1.7*u,3.6*u);c.fillStyle='#f33';c.beginPath();c.arc(4.2*u,-.8*u,.5*u,0,7);c.arc(4.2*u,.8*u,.5*u,0,7);c.fill();c.restore()}
function lon(l){return(G.time*1000+l.ph)%3000>1800}
function draw(now){const c=$('#cv').getContext('2d'),s=G.s,n=G.n,tm=now;c.drawImage(G.bg,0,0);
 const fx=(n-2)*s,pu=.5+.5*Math.sin(tm/250);c.save();c.shadowColor='#4df';c.shadowBlur=10+pu*10;c.fillStyle='#074';c.fillRect(fx+2,fx+2,s-4,s-4);c.strokeStyle='#4df';c.lineWidth=2;c.strokeRect(fx+3,fx+3,s-6,s-6);
 c.fillStyle='#ff6';c.beginPath();c.moveTo(fx+s*.55,fx+s*.15);c.lineTo(fx+s*.3,fx+s*.55);c.lineTo(fx+s*.48,fx+s*.55);c.lineTo(fx+s*.42,fx+s*.88);c.lineTo(fx+s*.7,fx+s*.45);c.lineTo(fx+s*.52,fx+s*.45);c.fill();c.restore();
 if(G.door&&!G.door.open){c.fillStyle='#c60';c.fillRect(G.door.x*s+2,G.door.y*s+2,s-4,s-4);c.fillStyle='#ff6';c.fillRect(G.door.x*s+s*.4,G.door.y*s+s*.35,s*.2,s*.3)}
 for(const o of G.traps){c.strokeStyle=Math.random()<.7?'#fa0':'#ff6';c.lineWidth=2;c.beginPath();c.moveTo(o.x*s+3,o.y*s+3);c.lineTo(o.x*s+s*.6,o.y*s+s*.45);c.lineTo(o.x*s+s*.4,o.y*s+s*.55);c.lineTo(o.x*s+s-3,o.y*s+s-3);c.stroke()}
 for(const l of G.lasers){const on=lon(l),w=(G.time*1000+l.ph)%3000>1300;c.fillStyle=on?'#f22':w&&Math.floor(tm/120)%2?'#f228':'#411';c.fillRect(l.x*s+(on?0:s*.35),l.y*s+s*.4,on?s:s*.3,s*.2);c.fillStyle='#888';c.fillRect(l.x*s,l.y*s+s*.3,s*.15,s*.4);c.fillRect(l.x*s+s*.85,l.y*s+s*.3,s*.15,s*.4)}
 if(G.scan>0||G.hintT>0){const D=flood(G.g,G.rx,G.ry),p=pathTo(D,n-2,n-2);if(p){c.fillStyle='#4df9';c.shadowColor='#4df';c.shadowBlur=8;for(const q of p){c.beginPath();c.arc((q[0]+.5)*s,(q[1]+.5)*s,s*.16,0,7);c.fill()}c.shadowBlur=0}}
 for(const i of G.items)drawItem(c,i.t,(i.x+.5)*s,(i.y+.5)*s,s*.3,tm);
 for(const o of G.guards){const e=Math.min(1,o.t/(o.iv*.5)),x=(o.fx+(o.x-o.fx)*e+.5)*s,y=(o.fy+(o.y-o.fy)*e+.5)*s;c.save();c.shadowColor='#f40';c.shadowBlur=8;c.fillStyle='#833';c.fillRect(x-s*.32,y-s*.32,s*.64,s*.64);c.fillStyle='#f40';c.fillRect(x-s*.32,y-s*.32,s*.64,s*.14);c.fillStyle='#ff0';c.beginPath();c.arc(x,y+s*.05,s*.14,0,7);c.fill();c.restore()}
 if(!(G.inv>0&&Math.floor(tm/90)%2)){drawRobot(c,(G.px+.5)*s,(G.py+.5)*s,s*.82,G.ang,G.wp,G.glow>0?'#4f8':G.boost>0?'#fa0':null,0,tm);
  if(G.shield){c.strokeStyle='#69f';c.lineWidth=2;c.beginPath();c.arc((G.px+.5)*s,(G.py+.5)*s,s*.55,0,7);c.stroke()}}
 if(S.set.anim)for(const f of G.fx){c.strokeStyle=f.c;c.globalAlpha=Math.max(0,1-f.t);c.lineWidth=2;c.beginPath();c.arc((f.x+.5)*s,(f.y+.5)*s,s*(.3+f.t*1.1),0,7);c.stroke();c.globalAlpha=1}}
function mini(id,now){const e=document.getElementById(id);if(!e||!e.offsetParent)return;const c=e.getContext('2d');c.clearRect(0,0,e.width,e.height);
 c.strokeStyle='#0cf5';c.beginPath();c.moveTo(0,e.height*.85);c.lineTo(e.width,e.height*.85);c.stroke();
 const hap=id=='wr';drawRobot(c,e.width/2,e.height*.5,e.height*.7,hap?0:-.35+Math.sin(now/700)*.35,now/120,hap?'#4f8':'#0cf',hap,now)}
// ===== Игровая логика =====
function hud(){const m=Math.floor(G.time/60),s=Math.floor(G.time%60);
 $('#hL').textContent=`${t('level')} ${G.daily?'★':G.L} · ${t('d'+S.diff)}`;$('#hS').textContent=`${t('score')}: ${G.score}`;$('#hB').textContent=`${t('bonus')}: ${G.coll}/${G.total}`;
 $('#hT').textContent=S.set.tm?`${t('time')}: ${m}:${String(s).padStart(2,'0')}`:'';$('#ef').style.width=Math.max(0,G.en/G.enMax*100)+'%';
 $('#hb').style.display=S.set.hint?'':'none';$('#hb').textContent=`${t('hint')} (${G.hints})`;
 const f=[];if(G.boost>0)f.push(t('boost')+' '+Math.ceil(G.boost/1000));if(G.scan>0)f.push(t('scan')+' '+Math.ceil(G.scan/1000));if(G.mag>0)f.push(t('magnet')+' '+Math.ceil(G.mag/1000));if(G.shield)f.push(t('shield'));if(G.hasKey&&!(G.door&&G.door.open))f.push(t('key'));
 $('#fxs').textContent=f.join(' · ')}
function pickup(i){G.items.splice(G.items.indexOf(i),1);const k=i.t;let p=20;
 if(k=='battery')G.en=Math.min(G.enMax,G.en+G.enMax*.3);else if(k=='boost')G.boost=8000;else if(k=='scan')G.scan=4000;else if(k=='magnet')G.mag=8000;else if(k=='shield')G.shield=1;
 else if(k=='gear')p=50;else if(k=='chip'){p=30;S.chips++;save()}else if(k=='key'){G.hasKey=1;p=10}
 if(k!='key')G.coll++;G.score+=p;G.glow=500;G.fx.push({x:i.x,y:i.y,t:0,c:IC[k]});toast(`${t(k)} +${p}`);snd(880,.08,'sine');setTimeout(()=>snd(1320,.1,'sine'),70)}
function hurt(){if(G.shield){G.shield=0;toast(t('shieldlost'));snd(500,.2,'sine');G.inv=1200;return}
 G.en=Math.max(0,G.en-20);G.hits++;G.inv=1500;toast(t('hit'));snd(120,.3,'sawtooth',.2,60);if(G.en<=0)lose()}
function tryMove(dx,dy){G.tang=Math.atan2(dy,dx);const nx=G.rx+dx,ny=G.ry+dy;if(G.g[ny][nx])return;
 const D=G.door;if(D&&!D.open&&nx==D.x&&ny==D.y){if(G.hasKey){D.open=1;toast(t('door'));snd(300,.3,'sawtooth',.15,700)}else{if(G.nt<=0){toast(t('needkey'));G.nt=900;snd(150,.15)}return}}
 G.mv={fx:G.rx,fy:G.ry,tx:nx,ty:ny,p:0,dur:160/S.set.spd/(G.boost>0?1.8:1)};G.rx=nx;G.ry=ny;G.en-=G.cost;snd(140,.04,'square',.05)}
function arrive(){for(const i of G.items.slice())if(i.x==G.rx&&i.y==G.ry)pickup(i);
 if(G.rx==G.n-2&&G.ry==G.n-2)return win();if(G.en<=0)lose()}
function gStep(o){const ok=DIR.filter(([dx,dy])=>{const a=o.x+dx,b=o.y+dy;return!G.g[b][a]&&!(G.door&&!G.door.open&&G.door.x==a&&G.door.y==b)});
 const f=ok.filter(([dx,dy])=>!(o.x+dx==o.lx&&o.y+dy==o.ly)),l=f.length?f:ok,[dx,dy]=l[Math.random()*l.length|0];o.lx=o.x;o.ly=o.y;o.fx=o.x;o.fy=o.y;o.x+=dx;o.y+=dy}
function upd(dt){if(G.paused||G.over)return;G.time+=dt/1000;
 for(const k of['boost','scan','mag','inv','hintT','glow','nt'])if(G[k]>0)G[k]-=dt;
 if(G.task>0){G.task-=dt;if(G.task<=0)$('#task').textContent=''}
 G.fx.forEach(f=>f.t+=dt/500);G.fx=G.fx.filter(f=>f.t<1);
 for(const o of G.guards){o.t+=dt;if(o.t>=o.iv){o.t=0;gStep(o)}}
 let da=((G.tang-G.ang+3*Math.PI)%(2*Math.PI))-Math.PI;G.ang+=da*Math.min(1,dt/70);
 if(G.mv){const m=G.mv;m.p+=dt/m.dur;G.wp+=dt*.012;if(m.p>=1){G.px=m.tx;G.py=m.ty;G.mv=null;arrive()}else{G.px=m.fx+(m.tx-m.fx)*m.p;G.py=m.fy+(m.ty-m.fy)*m.p}}
 if(!G.mv&&!G.over){const d=dirNow();if(d)tryMove(d[0],d[1])}
 if(G.over)return;
 if(G.mag>0)for(const i of G.items.slice())if(Math.abs(i.x-G.rx)+Math.abs(i.y-G.ry)<=3)pickup(i);
 const cx=G.mv&&G.mv.p<.5?G.mv.fx:G.rx,cy=G.mv&&G.mv.p<.5?G.mv.fy:G.ry;
 if(G.inv<=0&&(G.guards.some(o=>o.x==cx&&o.y==cy)||G.traps.some(o=>o.x==cx&&o.y==cy)||G.lasers.some(l=>l.x==cx&&l.y==cy&&lon(l))))hurt()}
function useHint(){if(!G||G.over||G.paused)return;if(G.hints<=0)return toast(t('nohint'));G.hints--;G.hintT=3000;snd(700,.1,'sine')}
function togglePause(){if(!G||G.over)return;if(G.paused){G.paused=0;closeModal()}else{G.paused=1;modal(()=>`<h2>${t('pause')}</h2><button class="btn" onclick="togglePause()">${t('resume')}</button><button class="btn" onclick="restart()">${t('restart')}</button><button class="btn o" onclick="toMenu()">${t('menu')}</button>`)}}
const stars=n=>'★'.repeat(n)+'☆'.repeat(3-n);
function win(){G.over=1;const half=G.coll>=Math.ceil(G.total/2);let st=half?2:1;if(half&&!G.hits&&G.time<=G.par)st=3;
 G.score+=100+Math.max(0,Math.floor(G.par-G.time))*2+(G.hits?0:50);
 if(!G.daily){S.st[G.L]=Math.max(S.st[G.L]||0,st);S.sc[G.L]=Math.max(S.sc[G.L]||0,G.score);S.un=Math.max(S.un,Math.min(50,G.L+1))}save();
 [523,659,784,1047].forEach((f,i)=>setTimeout(()=>snd(f,.2,'triangle',.2),i*130));const fact=t('facts')[(G.L+G.score)%4];
 setTimeout(()=>modal(()=>`<canvas id="wr" width="220" height="110"></canvas><h2>${t('win')}</h2>
 <div>${t('time')}: ${G.time.toFixed(1)}s · ${t('score')}: ${G.score}</div><div>${t('bonus')}: ${G.coll}/${G.total}</div>
 <div style="font-size:28px;color:#fd2">${stars(st)}</div><div class="fact">${fact}</div>
 ${!G.daily&&G.L<50?`<button class="btn" onclick="start(${G.L+1})">${t('next')}</button>`:''}
 <button class="btn" onclick="restart()">${t('again')}</button><button class="btn o" onclick="toMenu()">${t('menu')}</button>`),500)}
function lose(){if(G.over)return;G.over=1;snd(200,.6,'sawtooth',.2,50);setTimeout(()=>modal(()=>`<h2>${t('lose')}</h2><button class="btn" onclick="restart()">${t('restart')}</button><button class="btn o" onclick="toMenu()">${t('menu')}</button>`),400)}
// ===== Главный цикл и ввод =====
let last=0;
function loop(now){requestAnimationFrame(loop);const dt=Math.min(50,now-last||16);last=now;
 if(G&&$('#game').classList.contains('on')){try{upd(dt);draw(now);hud()}catch(e){console.error(e)}}mini('mr',now);mini('wr',now)}
addEventListener('keydown',e=>{if(e.code=='Space'){e.preventDefault();if(G&&$('#game').classList.contains('on'))togglePause();return}
 if(KM[e.code]){e.preventDefault();if(!hk.includes(e.code))hk.push(e.code)}});
addEventListener('keyup',e=>{hk=hk.filter(k=>k!=e.code)});
addEventListener('blur',()=>{hk=[];ptr=null});
addEventListener('pointerup',()=>ptr=null);
addEventListener('pointerdown',()=>{if(AC&&AC.state=='suspended')AC.resume()});
applyLang();music();requestAnimationFrame(loop);
</script><script>
// ===== ULTIMATE: профиль, магазин, достижения, сюжет, рейтинг =====
const L2=(r,k)=>{Object.assign(T.ru,r);Object.assign(T.kk,k)};
L2({shop:'Магазин',prof:'Профиль',rank:'Рейтинг',congrats:'ПОЗДРАВЛЯЕМ!',coins:'Монеты',xp:'Опыт',buy:'Купить',equip:'Применить',equipped:'Выбрано',claim:'Получить награду',create:'Создать аккаунт',login:'Войти',guest:'Играть как гость',nick:'Никнейм',user:'Имя пользователя',pass:'Пароль',exp:'Экспорт',imp:'Импорт',reset:'Сбросить прогресс',sure:'Удалить весь локальный прогресс этого профиля?',logout:'Сменить профиль',badpw:'Неверное имя или пароль',taken:'Имя занято',nocrypto:'Шифрование недоступно — играйте как гость',fill:'Заполните все поля',goal:'Цель',newach:'Новые достижения',noc:'Не хватает монет',bad:'Неверный код',rk0:'Новичок',rk1:'Ученик робототехника',rk2:'Инженер',rk3:'Программист EV3',rk4:'Мастер робототехники',rk5:'Эксперт',rk6:'Легенда EV3',r0:'Обычный',r1:'Редкий',r2:'Эпический',ca0:'Прогресс',ca1:'Сбор',ca2:'Мастерство',loc:'Локальный рейтинг (без сервера)',cl:'Пройдено уровней',bs:'Лучшие очки',bt:'Лучшее время',tb:'Бонусов собрано',nh:'Уровней без столкновений',stt:'Звёзд',
ch:['Глава 1: Сбой системы. ИИ лаборатории дал сбой и заблокировал все двери. Ты — EV3, и только ты можешь всё исправить.','Глава 2: Закрытые секторы. Охранные роботы патрулируют коридоры. Ищи ключи и не попадайся.','Глава 3: Опасные цеха. Лазеры и электрические ловушки охраняют микросхемы данных.','Глава 4: Энергетический кризис. Батарей мало — планируй маршрут заранее.','Глава 5: Ядро ИИ. Последний рывок к главному серверу лаборатории!'],fin:'Лаборатория восстановлена! ИИ снова работает, а EV3 стал легендой робототехники.',
A_first:'Первый шаг: пройди 1 уровень',A_expl:'Исследователь: пройди 10 уровней',A_mast:'Мастер лабиринтов: пройди 25 уровней',A_leg:'Легенда EV3: пройди 50 уровней',A_coll:'Коллекционер: собери 100 бонусов',A_clean:'Без ошибок: 5 уровней без столкновений',A_hard:'Непобедимый: 10 сложных уровней',A_rich:'Миллионер деталей: заработай 10 000 монет'},
{shop:'Дүкен',prof:'Профиль',rank:'Рейтинг',congrats:'ҚҰТТЫҚТАЙМЫЗ!',coins:'Тиындар',xp:'Тәжірибе',buy:'Сатып алу',equip:'Қолдану',equipped:'Таңдалған',claim:'Сыйлықты алу',create:'Аккаунт жасау',login:'Кіру',guest:'Қонақ ретінде ойнау',nick:'Лақап ат',user:'Пайдаланушы аты',pass:'Құпиясөз',exp:'Экспорт',imp:'Импорт',reset:'Прогресті тазалау',sure:'Осы профильдің барлық жергілікті прогресі жойылсын ба?',logout:'Профильді ауыстыру',badpw:'Аты немесе құпиясөз қате',taken:'Бұл ат бос емес',nocrypto:'Шифрлау қолжетімсіз — қонақ ретінде ойна',fill:'Барлық өрісті толтыр',goal:'Мақсат',newach:'Жаңа жетістіктер',noc:'Тиын жеткіліксіз',bad:'Код қате',rk0:'Жаңадан бастаушы',rk1:'Робототехника оқушысы',rk2:'Инженер',rk3:'EV3 бағдарламашысы',rk4:'Робототехника шебері',rk5:'Сарапшы',rk6:'EV3 аңызы',r0:'Қарапайым',r1:'Сирек',r2:'Эпикалық',ca0:'Прогресс',ca1:'Жинау',ca2:'Шеберлік',loc:'Жергілікті рейтинг (серверсіз)',cl:'Өтілген деңгей',bs:'Үздік ұпай',bt:'Үздік уақыт',tb:'Жиналған бонус',nh:'Соқтығыссыз деңгей',stt:'Жұлдыз',
ch:['1-тарау: Жүйе ақауы. Зертхана ЖИ-і бұзылып, барлық есікті жауып тастады. Сен — EV3, бәрін тек сен түзей аласың.','2-тарау: Жабық секторлар. Күзетші роботтар дәліздерді күзетеді. Кілттерді тап, ұсталма.','3-тарау: Қауіпті цехтар. Лазерлер мен электр тұзақтары деректер микросхемаларын қорғайды.','4-тарау: Қуат дағдарысы. Батарея аз — жолды алдын ала жоспарла.','5-тарау: ЖИ өзегі. Зертхананың басты серверіне соңғы бет алыс!'],fin:'Зертхана қалпына келді! ЖИ қайта жұмыс істейді, ал EV3 робототехника аңызына айналды.',
A_first:'Алғашқы қадам: 1 деңгей өт',A_expl:'Зерттеуші: 10 деңгей өт',A_mast:'Лабиринт шебері: 25 деңгей өт',A_leg:'EV3 аңызы: 50 деңгей өт',A_coll:'Коллекционер: 100 бонус жина',A_clean:'Қатесіз: 5 деңгейді соқтығыссыз өт',A_hard:'Жеңілмес: 10 қиын деңгей өт',A_rich:'Бөлшектер миллионері: 10 000 тиын тап'});
const SK=[['red','Классический EV3','Классикалық EV3',0,'#b8bcc4','#d22'],['blue','Синий EV3','Көк EV3',0,'#79b','#26f'],['green','Зелёный EV3','Жасыл EV3',0,'#9c9','#0a4'],['ice','Ледяной EV3','Мұзды EV3',200,'#cff','#4df'],['dark','Тёмный EV3','Қараңғы EV3',250,'#445','#a4f'],['space','Космический EV3','Ғарыштық EV3',300,'#238','#f4a'],['fire','Огненный EV3','Отты EV3',350,'#e83','#f20'],['gold','Золотой EV3','Алтын EV3',500,'#fd2','#a60'],['cyber','Кибернетический EV3','Кибернетикалық EV3',600,'#3a8','#0ff']];
const skn=id=>{const k=SK.find(x=>x[0]==id);return k[S.lang=='kk'?2:1]};
const AV=['🤖','🦾','🚀','⚡','🔧','🧠'],RX=[0,100,300,700,1500,3000,6000],rankIdx=x=>RX.filter(v=>x>=v).length-1;
const defP=()=>({name:'Гость',av:0,user:'',coins:0,xp:0,own:['red'],eq:'red',cl:{},story:{},s:{coll:0,clean:0,hd:{},earned:0}});
const defS=()=>({lang:'ru',diff:0,un:1,st:{},sc:{},rec:{},chips:0,set:{...DS}});
function fixP(){S.p=Object.assign(defP(),S.p);S.p.s=Object.assign(defP().s,S.p.s);S.rec=S.rec||{}}
function skinApply(id){const k=SK.find(x=>x[0]==id)||SK[0];window.SKC=k[4];window.SKS=k[5]}
// Достижения: [id, значок, статистика, цель, награда, ru, kk, категория]
const aval=k=>k=='lv'?Object.keys(S.st).length:k=='hard'?Object.keys(S.p.s.hd).length:S.p.s[k]||0;
const ACH=[['first','⭐','lv',1,20,0,0,0],['expl','🧭','lv',10,50,0,0,0],['mast','🏆','lv',25,150,0,0,0],['leg','👑','lv',50,500,0,0,0],['coll','🔩','coll',100,100,0,0,1],['clean','🛡','clean',5,80,0,0,2],['hard','🔥','hard',10,300,0,0,2],['rich','💰','earned',10000,1000,0,0,1]];
const dn=()=>ACH.filter(a=>aval(a[2])>=a[3]).map(a=>a[0]);
function claim(id){const a=ACH.find(x=>x[0]==id);if(aval(a[2])<a[3]||S.p.cl[id])return;S.p.cl[id]=1;S.p.coins+=a[4];S.p.s.earned+=a[4];save();updatePB();snd(1000,.3,'triangle');if(M)render()}
function achM(){return `<h2>${t('ach')}</h2>`+ACH.map(a=>{const v=Math.min(a[3],aval(a[2])),d=v>=a[3],c=S.p.cl[a[0]];return `<div style="width:100%;text-align:left;border:1px solid ${d?'#3f6':'#456'};border-radius:8px;padding:6px"><b>${a[1]} ${t('A_'+a[0])}</b> <small>(${t('ca'+a[7])})</small><div style="background:#123;height:8px;border-radius:4px"><i style="display:block;height:100%;width:${v/a[3]*100}%;background:#3f6"></i></div><small>${v}/${a[3]} · ${t('goal')}: ${a[3]} · +${a[4]} ${t('coins')}</small> ${d&&!c?`<button class="btn sm" onclick="claim('${a[0]}')">${t('claim')}</button>`:c?'✔':''}</div>`}).join('')+`<button class="btn" onclick="closeModal()">${t('close')}</button>`}
// Магазин
let shopSel='red';
function shopM(){const P=S.p;skinApply(shopSel);return `<h2>${t('shop')}</h2><div>${t('coins')}: ${P.coins}</div><canvas id="wr" width="220" height="110"></canvas><div style="width:100%;max-height:250px;overflow:auto">`+SK.map(k=>{const o=P.own.includes(k[0]);return `<div class="row" style="justify-content:space-between;align-items:center;border:1px solid ${shopSel==k[0]?'#4df':'#345'};border-radius:8px;padding:5px;margin:3px 0;cursor:pointer" onclick="shopSel='${k[0]}';render()"><span><i style="display:inline-block;width:14px;height:14px;background:${k[4]};border-bottom:4px solid ${k[5]}"></i> ${skn(k[0])} <small>(${t('r'+(k[3]>=300?2:k[3]>=150?1:0))})</small></span><span>${o?(P.eq==k[0]?t('equipped'):`<button class="btn sm" onclick="event.stopPropagation();equip('${k[0]}')">${t('equip')}</button>`):`<button class="btn sm o" onclick="event.stopPropagation();buy('${k[0]}')">${t('buy')} ${k[3]}</button>`}</span></div>`}).join('')+`</div><button class="btn" onclick="closeModal()">${t('close')}</button>`}
function buy(id){const k=SK.find(x=>x[0]==id),P=S.p;if(P.own.includes(id))return;if(P.coins<k[3])return toast(t('noc'));P.coins-=k[3];P.own.push(id);P.eq=id;save();updatePB();snd(900,.15,'triangle');render()}
function equip(id){S.p.eq=id;save();snd(600,.05);render()}
// Профиль, рейтинг, сохранения
function profM(){const P=S.p,r=rankIdx(P.xp);return `<h2>${AV[P.av]} ${P.name}</h2><div>${t('rk'+r)} · ${t('xp')}: ${P.xp} · ${t('coins')}: ${P.coins}</div><div>${t('cl')}: ${Object.keys(S.st).length}/50 · ${t('ach')}: ${dn().length}/${ACH.length}</div><div>${skn(P.eq)}</div>
<textarea id="sv" rows=3 style="width:100%" placeholder="JSON">${JSON.stringify(S).replace(/</g,'&lt;')}</textarea>
<div class="row"><button class="btn sm" onclick="doImp()">${t('imp')}</button><button class="btn sm o" onclick="resetP()">${t('reset')}</button><button class="btn sm" onclick="modal(authM)">${t('logout')}</button></div><button class="btn" onclick="closeModal()">${t('close')}</button>`}
function doImp(){try{const o=JSON.parse($('#sv').value.replace(/&lt;/g,'<'));if(!o.st||!o.p)throw 0;S=o;S.set={...DS,...o.set};fixP();save();skinApply(S.p.eq);applyLang();closeModal()}catch(e){toast(t('bad'))}}
function resetP(){if(!confirm(t('sure')))return;const o=S.p,l=S.lang;S=defS();S.lang=l;S.p={...defP(),name:o.name,user:o.user,av:o.av};save();skinApply('red');applyLang();closeModal()}
function rankM(){const v=Object.values(S.rec),st=Object.values(S.st).reduce((a,b)=>a+b,0),bs=Math.max(0,...Object.values(S.sc));return `<h2>${t('rank')}</h2><small>${t('loc')}</small><div>${t('cl')}: ${Object.keys(S.st).length}</div><div>${t('stt')}: ${st}</div><div>${t('bs')}: ${bs}</div><div>${t('bt')}: ${v.length?Math.min(...v)+' s':'—'}</div><div>${t('tb')}: ${S.p.s.coll}</div><div>${t('nh')}: ${S.p.s.clean}</div><button class="btn" onclick="closeModal()">${t('close')}</button>`}
function updatePB(){const P=S.p,r=rankIdx(P.xp),n=RX[r+1]||P.xp,b=RX[r],e=$('#pb');if(e)e.innerHTML=`<span style="font-size:26px">${AV[P.av]}</span><b>${P.name}</b><span>${t('rk'+r)}</span><span style="width:70px;height:8px;background:#123;border-radius:4px;display:inline-block"><i style="display:block;height:100%;width:${r>=6?100:(P.xp-b)/(n-b)*100}%;background:#4df"></i></span><span style="color:#fd2">● ${P.coins}</span>`}
// Локальные аккаунты (пароль хранится только как PBKDF2-хеш с солью)
const hex=b=>[...new Uint8Array(b)].map(x=>x.toString(16).padStart(2,'0')).join(''),unhex=h=>new Uint8Array(h.match(/../g).map(x=>parseInt(x,16)));
async function hash(p,salt){const k=await crypto.subtle.importKey('raw',new TextEncoder().encode(p),'PBKDF2',false,['deriveBits']);return hex(await crypto.subtle.deriveBits({name:'PBKDF2',salt,iterations:100000,hash:'SHA-256'},k,256))}
function loadKey(key,fresh){const l=S.lang;KEY=key;localStorage.setItem('ev3_last',key);S=defS();S.lang=l;if(!fresh)try{const o=JSON.parse(localStorage.getItem(key));if(o){Object.assign(S,o);S.set={...DS,...o.set}}}catch(e){}fixP()}
let authTab=0;
function authM(){const c=authTab==0;return `<h2>LABYRINTH EV3</h2><div class="row"><button class="btn sm ${c?'act':''}" onclick="authTab=0;render()">${t('create')}</button><button class="btn sm ${c?'':'act'}" onclick="authTab=1;render()">${t('login')}</button></div>${c?`<input id="au_n" placeholder="${t('nick')}">`:''}<input id="au_u" placeholder="${t('user')}"><input type="password" id="au_p" placeholder="${t('pass')}">${c?`<div class="row"><select id="au_a">${AV.map((a,i)=>`<option value=${i}>${a}</option>`)}</select><select id="au_r">${SK.slice(0,3).map(k=>`<option value=${k[0]}>${skn(k[0])}</option>`)}</select></div>`:''}<button class="btn" onclick="doAuth()">${c?t('create'):t('login')}</button><button class="btn o" onclick="guest()">${t('guest')}</button><div id="au_e" style="color:#f66"></div>`}
async function doAuth(){const u=$('#au_u').value.trim().toLowerCase(),p=$('#au_p').value,E=m=>$('#au_e').textContent=m;if(!u||!p)return E(t('fill'));if(!(window.crypto&&crypto.subtle))return E(t('nocrypto'));
 const A=JSON.parse(localStorage.getItem('ev3acc')||'{}');
 if(authTab==0){const n=$('#au_n').value.trim();if(!n)return E(t('fill'));if(A[u])return E(t('taken'));const salt=crypto.getRandomValues(new Uint8Array(16));A[u]={salt:hex(salt),hash:await hash(p,salt)};localStorage.setItem('ev3acc',JSON.stringify(A));
  loadKey('ev3_u_'+u,true);const r=$('#au_r').value;S.p={...defP(),name:n,user:u,av:+$('#au_a').value,own:[r],eq:r};save()}
 else{const a=A[u];if(!a||await hash(p,unhex(a.salt))!==a.hash)return E(t('badpw'));loadKey('ev3_u_'+u)}enter()}
function guest(){loadKey('ev3');enter()}
function enter(){localStorage.setItem('ev3_seen',1);closeModal();applyLang()}
function closeModal(){$('#modal').classList.remove('on');M=null;if(S.p)skinApply(S.p.eq)}
// Обёртки поверх базовой игры
const _al=applyLang;applyLang=function(){_al();updatePB()};
const _sm=setM;setM=function(){return _sm().replace('<button class="btn" onclick="closeModal()">',`<button class="btn sm o" onclick="resetP()">${t('reset')}</button><button class="btn" onclick="closeModal()">`)};
const _pk=pickup;pickup=function(i){_pk(i);if(i.t=='gear')G.gc=(G.gc||0)+10};
const _st=start;start=function(L,d){if(!d&&L%10==1&&!S.p.story[L]){S.p.story[L]=1;save();modal(()=>`<h2>${t('ch')[(L-1)/10].split(':')[0]}</h2><p>${t('ch')[(L-1)/10].split(':').slice(1).join(':')}</p><button class="btn" onclick="_st(${L})">▶</button>`)}else _st(L,d)};
function win(){G.over=1;const half=G.coll>=Math.ceil(G.total/2);let st=half?2:1;if(half&&!G.hits&&G.time<=G.par)st=3;
 G.score+=100+Math.max(0,Math.floor(G.par-G.time))*2+(G.hits?0:50);
 const P=S.p,old=S.st[G.L]||0,b4=dn(),r0=rankIdx(P.xp);let coins=0,xp=0;
 if(!G.daily){if(!old){coins=20+15*st+(G.gc||0);xp=30+G.L*2+G.coll*3}else if(st>old){coins=15*(st-old);xp=10*(st-old)} // награды не повторяются
  S.st[G.L]=Math.max(old,st);S.sc[G.L]=Math.max(S.sc[G.L]||0,G.score);S.rec[G.L]=Math.min(S.rec[G.L]||1e9,+G.time.toFixed(1));S.un=Math.max(S.un,Math.min(50,G.L+1));
  if(!G.hits&&!old)P.s.clean++;if(S.diff==2)P.s.hd[G.L]=1}
 P.s.coll+=G.coll;P.coins+=coins;P.s.earned+=coins;P.xp+=xp;const na=dn().filter(x=>!b4.includes(x)),rk=rankIdx(P.xp)>r0;save();updatePB();
 [523,659,784,1047].forEach((f,i)=>setTimeout(()=>snd(f,.2,'triangle',.2),i*130));if(na.length)setTimeout(()=>[1047,1319,1568].forEach((f,i)=>setTimeout(()=>snd(f,.25,'sine',.2),i*120)),700);
 const fact=t('facts')[(G.L+G.score)%4];
 setTimeout(()=>modal(()=>`<canvas id="wr" width="220" height="110"></canvas><h2>${t('congrats')}</h2><div>${t('win')} ${G.daily?'★':G.L}</div>
 <div>${t('time')}: ${G.time.toFixed(1)}s · ${t('score')}: ${G.score}</div><div>${t('bonus')}: ${G.coll}/${G.total}</div><div style="font-size:28px;color:#fd2">${stars(st)}</div>
 <div style="color:#fd2">+${coins} ${t('coins')} · +${xp} ${t('xp')}</div>${rk?`<div style="color:#4f8">▲ ${t('rk'+rankIdx(P.xp))}</div>`:''}
 ${na.length?`<div style="color:#3f6;border:1px solid #3f6;border-radius:8px;padding:6px">${t('newach')}:<br>${na.map(x=>t('A_'+x)).join('<br>')}<br><button class="btn sm" onclick="modal(achM)">${t('ach')}</button></div>`:''}
 <div class="fact">${G.L==50&&!G.daily?t('fin'):fact}</div>
 ${!G.daily&&G.L<50?`<button class="btn" onclick="start(${G.L+1})">${t('next')}</button>`:''}<button class="btn" onclick="restart()">${t('again')}</button><button class="btn o" onclick="toMenu()">${t('menu')}</button>`),500)}
document.head.insertAdjacentHTML('beforeend','<style>input,select,textarea{background:#05101c;color:#cff;border:1px solid #0cf;border-radius:8px;padding:8px;font-size:15px;width:100%}select{width:auto}#pb{position:absolute;top:8px;left:8px;display:flex;gap:8px;align-items:center;font-size:14px;z-index:5}.box{animation:pop .25s}@keyframes pop{from{transform:scale(.9);opacity:0}}</style>');
fixP();skinApply(S.p.eq);applyLang();if(!localStorage.getItem('ev3_seen'))modal(authM);
</script></body></html>
