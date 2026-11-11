 <!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>YGP Motors – पिंपरी चिंचवड</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Archivo:wght@500;700;800&family=Noto+Sans+Devanagari:wght@400;600;700&display=swap">
<style>
:root{--bg:#f4f4f1;--surface:#fff;--ink:#1b1f24;--muted:#5b636d;--line:#d9dbd6;--accent:#e4570f;--accent-ink:#fff;--ph:#e7e9e4;color-scheme:light}
@media (prefers-color-scheme:dark){:root{--bg:#15181c;--surface:#1e2227;--ink:#f1f2ee;--muted:#a3abb5;--line:#323840;--accent:#ff7a33;--accent-ink:#15181c;--ph:#2a3037;color-scheme:dark}}
*,*::before,*::after{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font-family:"Archivo","Noto Sans Devanagari",system-ui,sans-serif;line-height:1.5}
main{max-width:56rem;margin:0 auto;padding:0 1rem 6rem}
.top{display:flex;justify-content:space-between;align-items:center;padding:1rem 0;border-bottom:3px solid var(--ink);gap:.5rem}
.logo{font-weight:800;font-size:1.4rem;letter-spacing:-.02em}.logo span{color:var(--accent)}
.logo small{display:block;font-size:.75rem;font-weight:500;color:var(--muted)}
.nav{display:flex;gap:.5rem}
.btn{border:0;cursor:pointer;font:inherit;font-weight:700;background:var(--accent);color:var(--accent-ink);padding:.65rem 1.1rem;border-radius:.5rem;text-decoration:none;display:inline-block;text-align:center}
.btn.alt{background:var(--ink);color:var(--bg)}
.btn.ghost{background:transparent;color:var(--ink);border:1px solid var(--line)}
.tools{display:grid;gap:.75rem;padding:1rem 0}
input,select{font:inherit;padding:.7rem .8rem;border:1px solid var(--line);border-radius:.5rem;background:var(--surface);color:var(--ink);width:100%}
.chips{display:flex;gap:.5rem;overflow-x:auto}
.chip{flex:none;font:inherit;font-weight:600;border:1px solid var(--line);background:var(--surface);color:var(--ink);padding:.4rem 1rem;border-radius:2rem;cursor:pointer}
.chip[aria-pressed="true"]{background:var(--ink);color:var(--bg);border-color:var(--ink)}
.count{color:var(--muted);font-size:.9rem;margin:0 0 .75rem}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(10.5rem,1fr));gap:.9rem}
.card{background:var(--surface);border:1px solid var(--line);border-radius:.6rem;overflow:hidden;cursor:pointer;text-align:left;padding:0;font:inherit;color:inherit;display:block;width:100%}
.ph{aspect-ratio:4/3;background:var(--ph);display:grid;place-items:center;font-size:3rem;overflow:hidden}
.ph img{width:100%;height:100%;object-fit:cover}
.info{padding:.65rem .75rem .8rem}
.price{font-weight:800;font-size:1.15rem}
.name{font-weight:600;margin:.1rem 0}
.meta{color:var(--muted);font-size:.85rem;margin:.2rem 0}
dialog{border:0;border-radius:.8rem;padding:0;width:min(34rem,94vw);max-height:90vh;background:var(--surface);color:var(--ink)}
dialog::backdrop{background:rgba(0,0,0,.55)}
.dbody{padding:1.1rem}
.dbody h2{margin:.2rem 0 .4rem}
.close{float:right;background:none;border:0;font-size:1.6rem;cursor:pointer;color:var(--ink)}
.acts{display:grid;grid-template-columns:1fr 1fr;gap:.6rem;margin-top:1rem}
.acts .full{grid-column:1/-1}
form{display:grid;gap:.8rem}
label{display:grid;gap:.25rem;font-weight:600;font-size:.9rem}
.row{display:grid;grid-template-columns:1fr 1fr;gap:.8rem}
.empty{text-align:center;color:var(--muted);padding:2.5rem 0;grid-column:1/-1}
.fab{position:fixed;right:1rem;bottom:1rem;box-shadow:0 4px 14px rgba(0,0,0,.3);padding:.9rem 1.4rem;border-radius:3rem}
.gal{display:flex;overflow-x:auto;scroll-snap-type:x mandatory;gap:.5rem;border-radius:.5rem}.gal .ph{flex:none;width:100%;scroll-snap-align:center}
.vh{position:absolute;width:1px;height:1px;opacity:0;overflow:hidden;clip:rect(0 0 0 0)}
.prev{display:flex;gap:.4rem;flex-wrap:wrap;margin-top:.4rem}.prev img{width:3.5rem;height:3.5rem;object-fit:cover;border-radius:.4rem}
.msgs{display:flex;flex-direction:column;gap:.4rem;height:50vh;overflow-y:auto;padding:.5rem;background:var(--bg);border-radius:.5rem;margin:.6rem 0}
.m{max-width:80%;padding:.45rem .75rem;border-radius:.8rem;background:var(--surface);border:1px solid var(--line);word-break:break-word}
.m.me{align-self:flex-end;background:var(--accent);color:var(--accent-ink);border-color:var(--accent)}
.send{display:grid;grid-template-columns:1fr auto;gap:.5rem}
.err{color:#d32f2f;font-size:.9rem;margin:0;min-height:1.2em}
.inbox button{display:block;width:100%;text-align:left;font:inherit;color:inherit;background:var(--bg);border:1px solid var(--line);border-radius:.5rem;padding:.7rem;margin-bottom:.5rem;cursor:pointer}
</style>
</head>
<body>
<main>
<div class="top">
<div class="logo">YGP <span>Motors</span><small>पिंपरी चिंचवड · ग्राहक से ग्राहक</small></div>
<div class="nav"><button class="btn ghost" id="inboxBtn">चैट</button><button class="btn alt" id="authBtn">लॉगिन</button></div>
</div>
<div class="tools">
<input id="q" type="search" placeholder="गाड़ी खोजें: Honda, Activa, Swift…" aria-label="खोजें">
<div class="chips" id="chips"></div>
</div>
<p class="count" id="count">लोड हो रहा है…</p>
<div class="grid" id="grid"></div>
<button class="btn fab" id="sellBtn">+ गाड़ी बेचें</button>
</main>

<dialog id="detail"><div class="dbody" id="dbody"></div></dialog>

<dialog id="auth"><div class="dbody">
<button class="close" data-close aria-label="बंद करें">×</button>
<h2>लॉगिन करें</h2>
<form id="af">
<label>ईमेल<input id="email" type="email" required autocomplete="email"></label>
<label>पासवर्ड (कम से कम 6 अक्षर)<input id="pass" type="password" required minlength="6" autocomplete="current-password"></label>
<p class="err" id="aerr"></p>
<button class="btn" type="submit">लॉगिन</button>
<button class="btn ghost" type="button" id="signup">नया खाता बनाएँ</button>
</form></div></dialog>

<dialog id="sell"><div class="dbody">
<button class="close" data-close aria-label="बंद करें">×</button>
<h2>अपनी गाड़ी डालें</h2>
<form id="f">
<label>गाड़ी का प्रकार<select id="type"><option>बाइक</option><option>स्कूटर</option><option>कार</option></select></label>
<div class="row"><label>कंपनी<input id="make" required placeholder="Honda"></label><label>मॉडल<input id="model" required placeholder="Activa"></label></div>
<div class="row"><label>साल<input id="year" required inputmode="numeric" placeholder="2019"></label><label>किलोमीटर<input id="km" required inputmode="numeric" placeholder="25000"></label></div>
<div class="row"><label>कीमत (₹)<input id="price" required inputmode="numeric" placeholder="45000"></label><label>इलाका<input id="area" required placeholder="Chinchwad"></label></div>
<label>फोन नंबर (ज़रूरी नहीं)<input id="phone" inputmode="tel" autocomplete="tel"></label>
<div><label for="photo" class="btn alt" style="display:block;cursor:pointer">📷 फोटो चुनें (8 तक)</label><input id="photo" class="vh" type="file" accept="image/*" multiple><p class="meta" id="pcount">कोई फोटो नहीं चुनी</p><div class="prev" id="prev"></div></div>
<p class="err" id="serr"></p>
<button class="btn" type="submit" id="sbtn">लिस्टिंग डालें</button>
</form></div></dialog>

<dialog id="chat"><div class="dbody">
<button class="close" data-close aria-label="बंद करें">×</button>
<h2 id="ctitle"></h2>
<div class="msgs" id="msgs"></div>
<form class="send" id="cf"><input id="ctext" required placeholder="संदेश लिखें…" autocomplete="off"><button class="btn" type="submit">भेजें</button></form>
</div></dialog>

<dialog id="inbox"><div class="dbody">
<button class="close" data-close aria-label="बंद करें">×</button>
<h2>मेरी चैट</h2>
<div class="inbox" id="ilist"></div>
</div></dialog>

<script type="module">
import {initializeApp} from "https://www.gstatic.com/firebasejs/10.14.1/firebase-app.js";
import {getAuth,onAuthStateChanged,createUserWithEmailAndPassword,signInWithEmailAndPassword,signOut} from "https://www.gstatic.com/firebasejs/10.14.1/firebase-auth.js";
import {getFirestore,collection,doc,addDoc,setDoc,deleteDoc,query,where,orderBy,onSnapshot,serverTimestamp} from "https://www.gstatic.com/firebasejs/10.14.1/firebase-firestore.js";

const app=initializeApp({
  apiKey:"AIzaSyAomz0EUBrZ1HM0BDlAUSLNYNoXna11QRE",
  authDomain:"ygpmotorschichwad-a6e12.firebaseapp.com",
  projectId:"ygpmotorschichwad-a6e12",
  storageBucket:"ygpmotorschichwad-a6e12.firebasestorage.app",
  messagingSenderId:"285016887959",
  appId:"1:285016887959:web:d4d6abc41acc53cb734fd2"
});
const auth=getAuth(app),db=getFirestore(app);
const $=i=>document.getElementById(i);
const esc=s=>{const d=document.createElement('div');d.textContent=s==null?'':s;return d.innerHTML};
const inr=n=>'₹'+Number(n).toLocaleString('en-IN');
const ICON={'बाइक':'🏍️','स्कूटर':'🛵','कार':'🚗'};
let user=null,listings=[],type='सभी',unM=null,unI=null,curChat=null;

onAuthStateChanged(auth,u=>{user=u;$('authBtn').textContent=u?'लॉगआउट':'लॉगिन'});
$('authBtn').onclick=()=>user?signOut(auth):$('auth').showModal();
function needLogin(){if(user)return false;$('auth').showModal();return true}

const aerr=e=>({'auth/invalid-credential':'ईमेल या पासवर्ड गलत है।','auth/email-already-in-use':'ये ईमेल पहले से इस्तेमाल में है।','auth/weak-password':'पासवर्ड कम से कम 6 अक्षर का रखें।','auth/invalid-email':'ईमेल सही नहीं है।','auth/operation-not-allowed':'Firebase में Email/Password चालू नहीं है।','auth/network-request-failed':'इंटरनेट जाँचें।'}[e.code]||('गड़बड़ हुई: '+e.code));
$('af').onsubmit=async e=>{e.preventDefault();$('aerr').textContent='';
try{await signInWithEmailAndPassword(auth,$('email').value.trim(),$('pass').value);$('af').reset();$('auth').close()}catch(x){$('aerr').textContent=aerr(x)}};
$('signup').onclick=async()=>{$('aerr').textContent='';
if(!$('email').value||$('pass').value.length<6){$('aerr').textContent='ईमेल और 6 अक्षर का पासवर्ड भरें।';return}
try{await createUserWithEmailAndPassword(auth,$('email').value.trim(),$('pass').value);$('af').reset();$('auth').close()}catch(x){$('aerr').textContent=aerr(x)}};

['सभी','बाइक','स्कूटर','कार'].forEach(t=>{
const b=document.createElement('button');b.className='chip';b.textContent=t;b.setAttribute('aria-pressed',t===type);
b.onclick=()=>{type=t;[].forEach.call($('chips').children,c=>c.setAttribute('aria-pressed',c===b));render()};
$('chips').appendChild(b)});
$('q').oninput=render;

onSnapshot(query(collection(db,'listings'),orderBy('createdAt','desc')),
s=>{listings=s.docs.map(d=>({id:d.id,...d.data()}));render()},
()=>{$('count').textContent='लिस्टिंग नहीं खुल पाईं। इंटरनेट या Firestore rules जाँचें।'});

const thumb=v=>{const s=v.imgs&&v.imgs[0];return s?'<img alt="" src="'+s+'">':ICON[v.type]};
const gallery=v=>{const a=v.imgs||[];if(!a.length)return '<div class="ph" style="border-radius:.5rem">'+ICON[v.type]+'</div>';
return '<div class="gal">'+a.map(s=>'<div class="ph"><img alt="" src="'+s+'"></div>').join('')+'</div>'+(a.length>1?'<p class="meta">'+a.length+' फोटो, सरकाकर देखें</p>':'')};

function render(){
const q=$('q').value.toLowerCase().trim();
const list=listings.filter(v=>(type==='सभी'||v.type===type)&&((v.make+' '+v.model+' '+v.area).toLowerCase().indexOf(q)>-1));
$('count').textContent=list.length+' गाड़ियाँ';
$('grid').innerHTML=list.length?'':'<p class="empty">'+(listings.length?'कोई गाड़ी नहीं मिली।':'अभी कोई गाड़ी नहीं है। पहली गाड़ी आप डालिए।')+'</p>';
list.forEach(v=>{const c=document.createElement('button');c.className='card';
c.innerHTML='<div class="ph">'+thumb(v)+'</div><div class="info"><div class="price">'+inr(v.price)+'</div><div class="name">'+esc(v.make+' '+v.model)+'</div><div class="meta">'+esc(v.year+' · '+Number(v.km).toLocaleString('en-IN')+' km')+'<br>'+esc(v.area)+'</div></div>';
c.onclick=()=>show(v);$('grid').appendChild(c)})}

function show(v){
const own=user&&user.uid===v.uid,ph=(v.phone||'').replace(/\D/g,'');
$('dbody').innerHTML='<button class="close" data-close aria-label="बंद करें">×</button>'+gallery(v)+'<h2>'+esc(v.make+' '+v.model)+'</h2><div class="price">'+inr(v.price)+'</div><p class="meta">'+esc(v.type+' · '+v.year+' · '+Number(v.km).toLocaleString('en-IN')+' km · '+v.area)+'</p><div class="acts">'+
(own?'<button class="btn ghost full" id="del">मेरी लिस्टिंग हटाएँ</button>':'<button class="btn full" id="chatBtn">💬 विक्रेता से चैट करें</button>'+(ph?'<a class="btn alt" href="tel:+'+(ph.length===10?'91':'')+ph+'">कॉल करें</a><a class="btn alt" target="_blank" rel="noopener" href="https://wa.me/'+(ph.length===10?'91':'')+ph+'">WhatsApp</a>':''))+'</div>';
$('detail').showModal();
if(own)$('del').onclick=async()=>{if(confirm('ये लिस्टिंग हटा दें?')){await deleteDoc(doc(db,'listings',v.id));$('detail').close()}};
else $('chatBtn').onclick=async()=>{if(needLogin())return;
const id=v.id+'_'+user.uid;
try{await setDoc(doc(db,'chats',id),{lid:v.id,title:v.make+' '+v.model,users:[v.uid,user.uid],updatedAt:serverTimestamp()},{merge:true});$('detail').close();openChat(id,v.make+' '+v.model)}catch(x){alert('चैट नहीं खुली: '+x.code)}}}

function openChat(id,title){
curChat=id;$('ctitle').textContent=title;$('msgs').innerHTML='';$('chat').showModal();
unM&&unM();
unM=onSnapshot(query(collection(db,'chats',id,'messages'),orderBy('createdAt')),s=>{
$('msgs').innerHTML='';s.docs.forEach(d=>{const m=d.data(),el=document.createElement('div');el.className='m'+(user&&m.from===user.uid?' me':'');el.textContent=m.text;$('msgs').appendChild(el)});
$('msgs').scrollTop=$('msgs').scrollHeight},()=>{});}
$('chat').addEventListener('close',()=>{unM&&unM();unM=null});
$('cf').onsubmit=async e=>{e.preventDefault();const t=$('ctext').value.trim();if(!t||!curChat||!user)return;$('ctext').value='';
try{await addDoc(collection(db,'chats',curChat,'messages'),{from:user.uid,text:t,createdAt:serverTimestamp()});
await setDoc(doc(db,'chats',curChat),{updatedAt:serverTimestamp()},{merge:true})}catch(x){alert('संदेश नहीं गया: '+x.code)}};

$('inboxBtn').onclick=()=>{if(needLogin())return;$('inbox').showModal();unI&&unI();
unI=onSnapshot(query(collection(db,'chats'),where('users','array-contains',user.uid)),s=>{
const a=s.docs.map(d=>({id:d.id,...d.data()})).sort((x,y)=>(y.updatedAt&&y.updatedAt.toMillis?y.updatedAt.toMillis():0)-(x.updatedAt&&x.updatedAt.toMillis?x.updatedAt.toMillis():0));
$('ilist').innerHTML=a.length?'':'<p class="empty">अभी कोई चैट नहीं है।</p>';
a.forEach(c=>{const b=document.createElement('button');b.textContent='💬 '+c.title;b.onclick=()=>{$('inbox').close();openChat(c.id,c.title)};$('ilist').appendChild(b)})},()=>{})};
$('inbox').addEventListener('close',()=>{unI&&unI();unI=null});

$('sellBtn').onclick=()=>{if(needLogin())return;$('sell').showModal()};
document.addEventListener('click',e=>{if(e.target.closest('[data-close]'))e.target.closest('dialog').close();else if(e.target.tagName==='DIALOG')e.target.close()});

$('photo').onchange=function(){const fs=[].slice.call(this.files,0,8);
$('pcount').textContent=fs.length?fs.length+' फोटो चुनी':'कोई फोटो नहीं चुनी';$('prev').innerHTML='';
fs.forEach(f=>{const im=document.createElement('img');im.alt='';im.src=URL.createObjectURL(f);$('prev').appendChild(im)})};

const resize=f=>new Promise(res=>{const r=new FileReader();r.onload=()=>{const im=new Image();
im.onload=()=>{const s=Math.min(1,480/im.width),c=document.createElement('canvas');c.width=im.width*s;c.height=im.height*s;
c.getContext('2d').drawImage(im,0,0,c.width,c.height);res(c.toDataURL('image/jpeg',.65))};
im.onerror=()=>res('');im.src=r.result};r.onerror=()=>res('');r.readAsDataURL(f)});

$('f').onsubmit=async e=>{e.preventDefault();if(!user)return;
$('serr').textContent='';$('sbtn').disabled=true;$('sbtn').textContent='डाल रहे हैं…';
try{
const imgs=(await Promise.all([].slice.call($('photo').files,0,8).map(resize))).filter(Boolean);
await addDoc(collection(db,'listings'),{uid:user.uid,type:$('type').value,make:$('make').value.trim(),model:$('model').value.trim(),year:$('year').value.trim(),km:$('km').value.replace(/\D/g,''),price:$('price').value.replace(/\D/g,''),area:$('area').value.trim(),phone:$('phone').value.trim(),imgs,createdAt:serverTimestamp()});
$('f').reset();$('prev').innerHTML='';$('pcount').textContent='कोई फोटो नहीं चुनी';$('sell').close();
}catch(x){$('serr').textContent='लिस्टिंग नहीं डल पाई: '+(x.code||x.message)}
$('sbtn').disabled=false;$('sbtn').textContent='लिस्टिंग डालें'};
</script>
</body>
</html
