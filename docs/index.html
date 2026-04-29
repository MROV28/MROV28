<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title> MG </title>
<style>
  :root{
    --bg:#000;
    --pink:#ff9bbd;
    --pink2:#ffb3cb;
    --green:#79df79;
    --green2:#5fcf63;
    --gold:#ffd76a;
  }

  *{ box-sizing:border-box; margin:0; padding:0; }

  html, body{
    width:100%;
    height:100%;
    overflow:hidden;
    background:var(--bg);
    font-family: Arial, Helvetica, sans-serif;
  }

  body{
    perspective:1400px;
  }

  #stars{
    position:fixed;
    inset:0;
    pointer-events:none;
    z-index:0;
  }

  .star{
    position:absolute;
    border-radius:50%;
    background:#fff;
    opacity:.85;
    animation:twinkle linear infinite;
  }

  @keyframes twinkle{
    0%,100%{ opacity:.12; transform:scale(.8); }
    50%{ opacity:1; transform:scale(1.2); }
  }

  .stage{
    position:fixed;
    left:50%;
    top:50%;
    width:min(92vw, 980px);
    height:min(92vh, 980px);
    transform:translate(-50%, -52%);
    animation:floatBob 7s ease-in-out infinite;
    z-index:1;
  }

  @keyframes floatBob{
    0%,100%{ transform:translate(-50%, -52%) translateY(0px); }
    50%{ transform:translate(-50%, -52%) translateY(-10px); }
  }

  .scene{
    position:relative;
    width:100%;
    height:100%;
    transform-style:preserve-3d;
    transform-origin:center center;
    animation:sceneSpin 44s linear infinite;
  }

  @keyframes sceneSpin{
    0%{ transform:rotateY(0deg) rotateX(5deg); }
    100%{ transform:rotateY(360deg) rotateX(5deg); }
  }

  .glow{
    position:absolute;
    left:50%;
    top:50%;
    width:260px;
    height:260px;
    transform:translate(-50%, -50%);
    border-radius:50%;
    background:radial-gradient(circle, rgba(255,155,189,.18), rgba(255,155,189,0) 70%);
    filter:blur(18px);
    pointer-events:none;
    z-index:-1;
    animation:glowPulse 5s ease-in-out infinite;
  }

  @keyframes glowPulse{
    0%,100%{ opacity:.7; transform:translate(-50%, -50%) scale(1); }
    50%{ opacity:1; transform:translate(-50%, -50%) scale(1.08); }
  }

  .piece{
    position:absolute;
    left:50%;
    top:50%;
    white-space:nowrap;
    user-select:none;
    transform-style:preserve-3d;
    line-height:1;
    letter-spacing:-0.02em;
    opacity:0;
    animation:fadeInOpacity 1.1s ease forwards;
    will-change:transform, opacity;
    pointer-events:none;
  }

  @keyframes fadeInOpacity{
    from{ opacity:0; }
    to{ opacity:1; }
  }

  .petal{ color:var(--pink2); text-shadow:0 0 6px rgba(255,155,189,.5); }
  .stem{ color:var(--green); text-shadow:0 0 4px rgba(119,217,119,.35); }
  .leaf{ color:var(--green2); text-shadow:0 0 4px rgba(119,217,119,.25); }
  .center{ color:var(--gold); text-shadow:0 0 6px rgba(255,215,106,.55); }
  .ribbon{ color:var(--pink); text-shadow:0 0 4px rgba(255,155,189,.38); }
  .spark{ color:#fff; text-shadow:0 0 8px rgba(255,255,255,.8); }
</style>
</head>
<body>
  <div id="stars"></div>
  <div class="stage">
    <div class="scene" id="scene">
      <div class="glow"></div>
    </div>
  </div>

<script>
const scene = document.getElementById('scene');
const stars = document.getElementById('stars');
const letters = ['I','L','O','V','E','Y','O','U'];

function rand(a,b){ return Math.random()*(b-a)+a; }
function pick(a){ return a[Math.floor(Math.random()*a.length)]; }

for(let i=0;i<170;i++){
  const s=document.createElement('div');
  s.className='star';
  const size=rand(1,2.5);
  s.style.width=size+'px';
  s.style.height=size+'px';
  s.style.left=Math.random()*100+'%';
  s.style.top=Math.random()*100+'%';
  s.style.animationDuration=rand(2,6)+'s';
  s.style.animationDelay=rand(0,4)+'s';
  stars.appendChild(s);
}

let delayCounter = 0;
function addPiece(t,c,x,y,z=0,size=14,rot=0,opacity=1){
  const el=document.createElement('div');
  el.className='piece '+c;
  el.textContent=t;
  el.style.fontSize=size+'px';
  el.style.opacity=opacity;
  el.style.transform=`translate(-50%, -50%) translate3d(${x}px, ${y}px, ${z}px) rotate(${rot}deg)`;
  el.style.animationDelay = (delayCounter * 0.002) + 's';
  delayCounter++;
  scene.appendChild(el);
}

function curve(p0,p1,p2,t){
  const mt=1-t;
  return{
    x:mt*mt*p0.x+2*mt*t*p1.x+t*t*p2.x,
    y:mt*mt*p0.y+2*mt*t*p1.y+t*t*p2.y
  };
}

const yShift = -18;

// Tallos principales del ramo
const base={x:0,y:195+yShift};
const ends=[-150,-112,-78,-42,0,42,78,112,150];
ends.forEach((x)=>{
  for(let j=0;j<20;j++){
    const t=j/19;
    const p=curve(base,{x:x*0.22,y:82+yShift},{x:x,y:-110+yShift},t);
    const sway = Math.sin(t*Math.PI) * rand(-5, 5);
    addPiece(pick(letters),'stem',p.x+sway,p.y,rand(-5,5),13,rand(-8,8),rand(.84,1));
  }
});

// Tallo central fino
for(let j=0;j<24;j++){
  const t=j/23;
  const y=184-t*305+yShift;
  const x=Math.sin(t*Math.PI*2)*2;
  addPiece(pick(['I','L','O','V','E']),'stem',x,y,rand(-4,4),12,rand(-10,10),rand(.88,1));
}

function addPetalCluster(cx, cy, rx, ry, count){
  for(let j=0;j<count;j++){
    const a=Math.random()*Math.PI*2;
    const r=Math.sqrt(Math.random());
    const x=cx+Math.cos(a)*rx*r;
    const y=cy+Math.sin(a)*ry*r+yShift;
    addPiece(pick(letters),'petal',x,y,rand(-8,8),rand(14,17),rand(-18,18),rand(.8,1));
  }
}

function addCenterCluster(cx, cy, rx, ry, count){
  for(let j=0;j<count;j++){
    const a=Math.random()*Math.PI*2;
    const r=Math.sqrt(Math.random());
    const x=cx+Math.cos(a)*rx*r;
    const y=cy+Math.sin(a)*ry*r+yShift;
    addPiece('❤','center',x,y,rand(-3,5),rand(11,15),rand(-10,10),rand(.9,1));
  }
}

function addLeafCurve(p0,p1,p2,count,flip=1){
  for(let i=0;i<count;i++){
    const t=i/(count-1);
    const p=curve(p0,p1,p2,t);
    const dx=2*(1-t)*(p1.x-p0.x)+2*t*(p2.x-p1.x);
    const dy=2*(1-t)*(p1.y-p0.y)+2*t*(p2.y-p1.y);
    const len=Math.hypot(dx,dy)||1;
    const nx=(-dy/len)*flip;
    const ny=(dx/len)*flip;
    const spread=8*Math.sin(t*Math.PI);
    addPiece(pick(['I','L','O','V','E']),'leaf',p.x+nx*rand(-spread,spread),p.y+ny*rand(-spread,spread)+yShift,rand(-4,4),rand(11,14),rand(-20,20),rand(.76,1));
  }
}

// Hojas laterales suaves
addLeafCurve({x:-5,y:132},{x:-72,y:92},{x:-112,y:22},13,1);
addLeafCurve({x: 5,y:128},{x: 70,y:88},{x: 114,y:18},13,-1);
addLeafCurve({x:-8,y:108},{x:-76,y:60},{x:-128,y:8},11,1);
addLeafCurve({x: 8,y:104},{x: 78,y:58},{x:126,y:4},11,-1);

// Flores (más aireadas y redonditas)
const flowers=[
  {x:-145,y:-86,rx:38,ry:30},
  {x:-110,y:-118,rx:40,ry:32},
  {x:-76,y:-140,rx:42,ry:33},
  {x:-34,y:-156,rx:44,ry:34},
  {x: 12,y:-162,rx:45,ry:35},
  {x: 56,y:-156,rx:44,ry:34},
  {x: 96,y:-140,rx:42,ry:33},
  {x: 130,y:-118,rx:40,ry:32},
  {x: 160,y:-86,rx:38,ry:30},
  {x:-72,y:-72,rx:34,ry:28},
  {x:-18,y:-90,rx:36,ry:29},
  {x: 32,y:-92,rx:36,ry:29},
  {x: 84,y:-74,rx:34,ry:28}
];
flowers.forEach(f=>{
  addPetalCluster(f.x,f.y,f.rx,f.ry,16);
  addCenterCluster(f.x,f.y,10,8,4);
});

// Flor central
addPetalCluster(0,-102,58,48,20);
addCenterCluster(0,-102,16,13,6);

// Corazón sutil para dar vida
for(let i=0;i<8;i++){
  const a=i/8*Math.PI*2;
  addPiece('❤','center',Math.cos(a)*13,-102+Math.sin(a)*9+yShift,rand(-2,3),13,rand(-8,8),.8);
}

// Moño elegante
for(let i=0;i<8;i++){
  addPiece('♡','ribbon',rand(-32,32),rand(124,144)+yShift,rand(-4,4),rand(17,22),rand(-35,35),rand(.84,1));
}
for(let i=0;i<6;i++){
  addPiece(pick(['I','L','O','V','E']),'ribbon',rand(-14,14),rand(140,166)+yShift,rand(-3,3),rand(12,15),rand(-18,18),rand(.9,1));
}

// Cintas colgantes más delicadas
for(let i=0;i<8;i++){
  const t=i/7;
  addPiece(pick(['I','L','O','V','E']),'ribbon',-14+Math.sin(t*Math.PI)*1.5,134+t*66+yShift,rand(-2,2),rand(11,14),rand(-12,12),.88);
  addPiece(pick(['I','L','O','V','E']),'ribbon', 14+Math.sin(t*Math.PI)*1.5,134+t*68+yShift,rand(-2,2),rand(11,14),rand(-12,12),.88);
}

// Destellos suaves
for(let i=0;i<10;i++){
  addPiece('✦','spark',rand(-175,175),rand(-190,200)+yShift,rand(-10,10),rand(9,12),rand(0,360),rand(.35,.7));
}
</script>
</body>
</html>
