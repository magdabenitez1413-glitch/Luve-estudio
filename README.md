# Luve-estudio
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>LUVÉ Studio — Creative Lab</title>
<style>
:root{--bg:#f3f0eb;--paper:#fffdf9;--ink:#201e1b;--muted:#817a72;--line:#e5dfd6;--accent:#9c775c}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font-family:Arial,sans-serif}
button,input,select,textarea{font:inherit}
button{cursor:pointer}
header{height:76px;padding:0 5%;display:flex;align-items:center;justify-content:space-between;background:var(--paper);border-bottom:1px solid var(--line)}
.logo{font:32px Georgia,serif;letter-spacing:7px}
.tag{font-size:10px;letter-spacing:2px;color:var(--muted)}
.status{font-size:11px;color:#55765c}
.layout{display:grid;grid-template-columns:215px minmax(0,1fr);min-height:calc(100vh - 76px)}
aside{padding:25px 16px;border-right:1px solid var(--line);background:#f8f5f0}
.group{margin-bottom:28px}
.group h4{font-size:10px;color:var(--muted);letter-spacing:2px;margin:0 10px 12px}
.nav{width:100%;padding:12px 10px;border:0;border-radius:8px;text-align:left;background:transparent;color:#635d56;margin:2px 0;font-size:13px}
.nav.active,.nav:hover{background:#e9e0d6;color:#211d19}
.nav span{display:inline-block;width:27px;font-size:16px}
main{padding:30px 4%;min-width:0;max-width:1500px;width:100%;margin:auto}
.eyebrow{font-size:10px;letter-spacing:2px;color:var(--accent);text-transform:uppercase}
h1{font:normal clamp(29px,4vw,48px) Georgia,serif;letter-spacing:-1px;margin:8px 0}
.lead{font-size:13px;color:var(--muted);margin:0 0 26px}
.topline{display:flex;justify-content:space-between;align-items:center;gap:15px;flex-wrap:wrap}
.btn{padding:11px 16px;border:1px solid var(--ink);border-radius:5px;background:var(--ink);color:white;font-size:12px}
.btn.light{background:transparent;color:var(--ink);border-color:var(--line)}
.workspace{display:grid;grid-template-columns:minmax(0,1.35fr) minmax(260px,.75fr);gap:18px}
.card{background:var(--paper);border:1px solid var(--line);padding:18px;border-radius:8px;margin-bottom:18px;min-width:0}
.cardhead{display:flex;justify-content:space-between;align-items:center;margin-bottom:15px}
.cardhead h2{font:normal 20px Georgia,serif;margin:0}
.small{font-size:11px;color:var(--muted)}
.canvas{background:#e7dfd5;min-height:360px;display:flex;justify-content:center;align-items:center;position:relative;overflow:hidden}
.canvas img,.canvas video{max-width:100%;max-height:580px;object-fit:contain;display:block}
.empty{text-align:center;padding:35px;color:#786f66}
.empty b{display:block;font:26px Georgia,serif;margin-bottom:10px}
.thumbs{display:flex;gap:8px;overflow-x:auto;padding:12px 0 2px}
.thumb{flex:0 0 63px;height:63px;border:2px solid transparent;padding:0;background:#eee;overflow:hidden}
.thumb.active{border-color:var(--accent)}
.thumb img{width:100%;height:100%;object-fit:cover}
.fields{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.field{margin-bottom:14px}
.field label{font-size:11px;color:var(--muted);display:flex;justify-content:space-between;margin-bottom:7px}
input[type=text],select,textarea{width:100%;padding:11px;border:1px solid var(--line);background:white;border-radius:4px;color:var(--ink)}
input[type=range]{width:100%;accent-color:var(--accent)}
.looks{display:grid;grid-template-columns:repeat(3,1fr);gap:7px}
.look{padding:10px 4px;border:1px solid var(--line);background:white;font-size:11px}
.look.active{border-color:var(--accent);background:#f1e7dc}
.divider{border:0;border-top:1px solid var(--line);margin:18px 0}
.formatgrid{display:grid;grid-template-columns:repeat(4,1fr);gap:7px}
.format{border:1px solid var(--line);padding:10px 3px;background:white;font-size:10px}
.format.active{border-color:var(--accent);background:#f1e7dc}
#overlay{position:absolute;left:6%;right:6%;bottom:8%;text-align:center;color:white;font:600 clamp(18px,3vw,34px) Georgia,serif;text-shadow:0 2px 10px #000;pointer-events:none;overflow-wrap:anywhere}
#upload{display:none}
.notice{font-size:11px;color:var(--muted);line-height:1.6;margin-top:14px}
.toolsgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:20px}
.tooltile{padding:17px;border:1px solid var(--line);background:var(--paper);text-align:left;color:var(--ink)}
.tooltile strong{display:block;font:18px Georgia,serif;margin:12px 0 5px}
.tooltile span{font-size:11px;color:var(--muted);line-height:1.5}
.hidden{display:none!important}
@media(max-width:850px){.layout{grid-template-columns:1fr}aside{border-right:0;border-bottom:1px solid var(--line);padding:10px;display:flex;overflow-x:auto;gap:8px}.group{display:flex;gap:4px;margin:0;align-items:center}.group h4{display:none}.nav{white-space:nowrap;width:auto;padding:11px}.workspace{grid-template-columns:1fr}main{padding:23px 14px}.canvas{min-height:260px}.toolsgrid{grid-template-columns:1fr 1fr}}
@media(max-width:430px){.fields{grid-template-columns:1fr}.formatgrid{grid-template-columns:repeat(2,1fr)}.toolsgrid{grid-template-columns:1fr}.tag{display:none}header{padding:0 18px}}
</style>
</head>
<body>
<header>
  <div class="logo">LUVÉ</div>
  <div class="tag">CREATIVE IMAGE & MOTION STUDIO</div>
  <div class="status">● ESTUDIO PERSONAL</div>
</header>
<div class="layout">
<aside>
  <div class="group">
    <h4>CREAR</h4>
    <button class="nav active" data-view="editor"><span>◈</span>Estudio editorial</button>
    <button class="nav" data-view="campaign"><span>✳</span>Campañas</button>
    <button class="nav" data-view="before"><span>▧</span>Antes y después</button>
    <button class="nav" data-view="motion"><span>▷</span>Vídeo / Motion</button>
  </div>
</aside>
<main>
<section id="editorView">
  <div class="topline">
    <div><div class="eyebrow">LUVÉ / CREATIVE DESK</div><h1>El arte de tu imagen.</h1><p class="lead">Fotografía, belleza y comunicación visual en un solo espacio.</p></div>
    <label class="btn" for="upload">＋ Añadir archivos</label>
    <input id="upload" type="file" accept="image/*,video/*" multiple>
  </div>
  <div class="workspace">
    <div>
      <section class="card">
        <div class="cardhead"><h2>Área de creación</h2><span class="small" id="counter">SIN ARCHIVOS</span></div>
        <div class="canvas" id="canvas"><div class="empty"><b>Tu próxima portada empieza aquí.</b>Selecciona una o varias fotos o un vídeo.</div></div>
        <div id="thumbs" class="thumbs"></div>
        <div class="small" id="filename">Tus archivos no se suben a ningún servidor en esta versión.</div>
      </section>
      <section class="card">
        <div class="cardhead"><h2>Formato de publicación</h2><span class="small">SALIDA</span></div>
        <div class="formatgrid">
          <button class="format active" data-ratio="1:1">POST 1:1</button>
          <button class="format" data-ratio="4:5">RETRATO 4:5</button>
          <button class="format" data-ratio="9:16">STORY 9:16</button>
          <button class="format" data-ratio="16:9">HORIZONTAL 16:9</button>
        </div>
        <hr class="divider">
        <div class="fields">
          <div class="field"><label for="headline">Titular editorial</label><input id="headline" type="text" placeholder="La belleza de lo natural"></div>
          <div class="field"><label for="subline">Subtítulo / marca</label><input id="subline" type="text" placeholder="LUVÉ BEAUTY STUDIO"></div>
        </div>
        <div class="field"><label for="position">Estilo de texto</label><select id="position"><option value="bottom">Editorial · inferior</option><option value="top">Portada · superior</option><option value="middle">Campaña · centrado</option></select></div>
        <div class="actions"><button class="btn" id="export">Exportar diseño JPG</button> <button class="btn light" id="clearText">Quitar textos</button></div>
      </section>
    </div>
    <div>
      <section class="card">
        <div class="cardhead"><h2>Tratamiento visual</h2><span class="small">AJUSTES</span></div>
        <div class="looks">
          <button class="look active" data-look="natural">Natural</button>
          <button class="look" data-look="glow">Soft glow</button>
          <button class="look" data-look="film">Film</button>
          <button class="look" data-look="warm">Warm</button>
          <button class="look" data-look="mono">Monochrome</button>
          <button class="look" data-look="contrast">Contrast</button>
        </div>
        <hr class="divider">
        <div class="field"><label>Brillo <span id="bv">100%</span></label><input id="brightness" type="range" min="50" max="150" value="100"></div>
        <div class="field"><label>Contraste <span id="cv">100%</span></label><input id="contrast" type="range" min="50" max="160" value="100"></div>
        <div class="field"><label>Saturación <span id="sv">100%</span></label><input id="saturation" type="range" min="0" max="180" value="100"></div>
        <div class="field"><label>Sepia / calidez <span id="wv">0%</span></label><input id="warmth" type="range" min="0" max="70" value="0"></div>
        <div class="notice">Los estilos son tratamientos de color aplicados a la vista previa y al JPG exportado. No alteran permanentemente el archivo original.</div>
      </section>
      <section class="card">
        <div class="cardhead"><h2>Dirección creativa</h2></div>
        <div class="field"><label for="preset">Concepto de campaña</label><select id="preset"><option value="beauty">Beauty editorial</option><option value="salon">Hair studio luxury</option><option value="minimal">Minimal magazine</option><option value="promo">Promoción comercial</option></select></div>
        <button class="btn light" id="applyPreset">Aplicar propuesta de texto</button>
        <p class="notice">Esta versión ofrece herramientas creativas locales. La generación de imágenes nuevas con IA, el retoque inteligente y la creación de vídeos publicitarios con música y transiciones requieren integrar servicios adicionales.</p>
      </section>
    </div>
  </div>
  <section class="toolsgrid">
    <button class="tooltile" data-go="campaign">✳<strong>Campaña publicitaria</strong><span>Prepara una composición promocional con titular y marca.</span></button>
    <button class="tooltile" data-go="before">▧<strong>Antes / después</strong><span>Prepara una comparativa de dos fotografías.</span></button>
    <button class="tooltile" data-go="motion">▷<strong>Vídeo promocional</strong><span>Previsualiza clips y prepara una selección para montaje.</span></button>
  </section>
</section>
<section id="campaignView" class="hidden">
  <div class="eyebrow">LUVÉ / AD CAMPAIGN</div><h1>Una historia. Una campaña.</h1>
  <p class="lead">Prepara el material visual para tu próxima publicación.</p>
  <div class="card"><h2>Kit de campaña</h2><p class="small">Selecciona tus imágenes en el Estudio editorial y añade el texto de tu campaña.</p><button class="btn" data-go="editor">Abrir estudio editorial</button><hr class="divider"><p>Formatos disponibles en el estudio: publicación cuadrada, retrato, story y horizontal.</p></div>
</section>
<section id="beforeView" class="hidden">
  <div class="eyebrow">LUVÉ / TRANSFORMATION</div><h1>El cambio habla por sí solo.</h1>
  <p class="lead">Carga primero la imagen del antes y después la del resultado final.</p>
  <div class="card"><div class="fields"><div><h2>ANTES</h2><div id="beforeBox" class="canvas"><div class="empty">Imagen original</div></div><label class="btn light" for="beforeFile">Elegir foto del antes</label><input id="beforeFile" type="file" accept="image/*"></div><div><h2>DESPUÉS</h2><div id="afterBox" class="canvas"><div class="empty">Resultado final</div></div><label class="btn light" for="afterFile">Elegir foto del después</label><input id="afterFile" type="file" accept="image/*"></div></div><p class="notice">Esta herramienta muestra las dos imágenes lado a lado. El archivo de comparación descargable se puede añadir en una siguiente ampliación.</p></div>
</section>
<section id="motionView" class="hidden">
  <div class="eyebrow">LUVÉ / MOTION STUDIO</div><h1>Movimiento con intención.</h1>
  <p class="lead">Selecciona clips para previsualizarlos y organizar el material publicitario.</p>
  <div class="card"><label class="btn" for="videoFiles">＋ Seleccionar vídeos</label><input id="videoFiles" type="file" accept="video/*" multiple><div id="videoList" class="thumbs"></div><p class="notice">La versión actual permite reproducir los clips seleccionados. No monta, mezcla audio ni exporta un vídeo final. Esas funciones requieren un motor de edición de vídeo.</p></div>
</section>
</main>
</div>
<script>
const $=s=>document.querySelector(s);
let files=[],selected=-1,ratio='1:1',videoUrls=[];
function imageFile(f){return f&&f.type.startsWith('image/')}
function filterString(){return `brightness(${$('#brightness').value}%) contrast(${$('#contrast').value}%) saturate(${$('#saturation').value}%) sepia(${$('#warmth').value}%)`}
function updateFilters(){[['brightness','bv','%'],['contrast','cv','%'],['saturation','sv','%'],['warmth','wv','%']].forEach(([a,b,c])=>$('#'+b).textContent=$('#'+a).value+c);const media=$('#canvas').querySelector('img,#mainVideo');if(media)media.style.filter=filterString()}
function render(){const c=$('#canvas');c.innerHTML='';if(selected<0||!files[selected]){c.innerHTML='<div class="empty"><b>Tu próxima portada empieza aquí.</b>Selecciona una o varias fotos o un vídeo.</div>';$('#filename').textContent='Tus archivos se procesan localmente.';$('#counter').textContent='SIN ARCHIVOS';return}const f=files[selected];$('#filename').textContent=f.name;$('#counter').textContent=(selected+1)+' / '+files.length;if(imageFile(f)){const im=document.createElement('img');im.src=URL.createObjectURL(f);im.id='mainImage';im.style.filter=filterString();c.append(im);const ov=document.createElement('div');ov.id='overlay';const h=$('#headline').value,s=$('#subline').value;ov.style.top=$('#position').value==='top'?'8%':$('#position').value==='middle'?'40%':'auto';ov.style.bottom=$('#position').value==='top'?'auto':$('#position').value==='middle'?'auto':'8%';ov.innerHTML='<div>'+escapeHtml(h)+'</div><div style="font:10px Arial;letter-spacing:3px;margin-top:9px">'+escapeHtml(s)+'</div>';c.append(ov)}else if(f.type.startsWith('video/')){const v=document.createElement('video');v.id='mainVideo';v.src=URL.createObjectURL(f);v.controls=true;v.playsInline=true;v.style.filter=filterString();c.append(v)}else{c.innerHTML='<div class="empty">Formato no compatible.</div>'}}
function escapeHtml(s){return String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]))}
function thumbs(){const t=$('#thumbs');t.innerHTML='';files.forEach((f,i)=>{const b=document.createElement('button');b.className='thumb'+(i===selected?' active':'');if(imageFile(f)){const im=document.createElement('img');im.src=URL.createObjectURL(f);b.append(im)}else b.textContent='▶';b.onclick=()=>{selected=i;thumbs();render()};t.append(b)})}
$('#upload').onchange=e=>{files=files.concat(Array.from(e.target.files));selected=files.findIndex(imageFile);if(selected<0&&files.length)selected=0;thumbs();render()};
['brightness','contrast','saturation','warmth'].forEach(id=>$('#'+id).oninput=updateFilters);
['headline','subline','position'].forEach(id=>$('#'+id).addEventListener('input',render));
document.querySelectorAll('[data-ratio]').forEach(b=>b.onclick=()=>{ratio=b.dataset.ratio;document.querySelectorAll('[data-ratio]').forEach(x=>x.classList.toggle('active',x===b));const [w,h]=ratio.split(':').map(Number);$('#canvas').style.aspectRatio=w+'/'+h;$('#canvas').style.minHeight=ratio==='9:16'?'420px':'260px'});
const looks={natural:[100,100,100,0],glow:[108,94,112,8],film:[96,110,85,15],warm:[104,100,105,28],mono:[100,110,0,0],contrast:[100,130,110,0]};
document.querySelectorAll('[data-look]').forEach(b=>b.onclick=()=>{document.querySelectorAll('[data-look]').forEach(x=>x.classList.toggle('active',x===b));looks[b.dataset.look].forEach((v,i)=>$('#'+['brightness','contrast','saturation','warmth'][i]).value=v);updateFilters();render()});
$('#clearText').onclick=()=>{$('#headline').value='';$('#subline').value='';render()};
$('#applyPreset').onclick=()=>{const p=$('#preset').value;const data={beauty:['The art of beauty','BEAUTY EDITION'],salon:['Color. Texture. You.','LUVÉ HAIR STUDIO'],minimal:['Less, but better.','THE EDIT'],promo:['Tu nuevo look empieza aquí','RESERVA TU CITA']};$('#headline').value=data[p][0];$('#subline').value=data[p][1];render()};
$('#export').onclick=()=>{if(selected<0||!imageFile(files[selected])){alert('Selecciona una fotografía para exportar el diseño.');return}const img=new Image();img.onload=()=>{const [rw,rh]=ratio.split(':').map(Number);let w=1200,h=Math.round(w*rh/rw);if(h>1800){h=1800;w=Math.round(h*rw/rh)}const c=document.createElement('canvas');c.width=w;c.height=h;const x=c.getContext('2d');x.fillStyle='#e7dfd5';x.fillRect(0,0,w,h);const scale=Math.max(w/img.width,h/img.height),dw=img.width*scale,dh=img.height*scale;x.filter=filterString();x.drawImage(img,(w-dw)/2,(h-dh)/2,dw,dh);x.filter='none';const title=$('#headline').value,sub=$('#subline').value;const top=$('#position').value==='top'?h*.12:$('#position').value==='middle'?h*.47:h*.86;x.textAlign='center';x.textBaseline='middle';x.fillStyle='#fff';x.shadowColor='#0009';x.shadowBlur=12;x.font='bold '+Math.round(w*.055)+'px Georgia';if(title)x.fillText(title,w/2,top,w*.86);x.font='500 '+Math.round(w*.018)+'px Arial';if(sub)x.fillText(sub,w/2,top+Math.round(w*.07),w*.85);c.toBlob(blob=>{const a=document.createElement('a');a.href=URL.createObjectURL(blob);a.download='luve-editorial.jpg';a.click();setTimeout(()=>URL.revokeObjectURL(a.href),2000)},'image/jpeg',.94)};img.src=URL.createObjectURL(files[selected])};
function showView(name){['editor','campaign','before','motion'].forEach(n=>$('#'+n+'View').classList.toggle('hidden',n!==name));document.querySelectorAll('.nav').forEach(b=>b.classList.toggle('active',b.dataset.view===name));}
document.querySelectorAll('[data-view]').forEach(b=>b.onclick=()=>showView(b.dataset.view));
document.querySelectorAll('[data-go]').forEach(b=>b.onclick=()=>showView(b.dataset.go));
function previewFile(file,box){if(!file)return;const url=URL.createObjectURL(file);box.innerHTML='';const im=document.createElement('img');im.src=url;box.append(im)}
$('#beforeFile').onchange=e=>previewFile(e.target.files[0],$('#beforeBox'));
$('#afterFile').onchange=e=>previewFile(e.target.files[0],$('#afterBox'));
$('#videoFiles').onchange=e=>{const list=$('#videoList');list.innerHTML='';videoUrls.forEach(URL.revokeObjectURL);videoUrls=[];Array.from(e.target.files).forEach(f=>{const url=URL.createObjectURL(f);videoUrls.push(url);const v=document.createElement('video');v.src=url;v.controls=true;v.playsInline=true;v.style.width='180px';v.style.maxHeight='240px';list.append(v)})};
render();
</script>
</body>
</html>
