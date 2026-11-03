<!doctype html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<title>Rifa del 17 de Noviembre</title>
<style>:root{color-scheme:light;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}body{margin:0}img{max-width:100%}[hidden]{display:none!important}</style>
</head>
<body>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@700;800&family=Figtree:wght@400;500;700&display=swap">
<style id="app-style">
/* Layout: una boleta de rifa arriba (talón con el premio + datos), tablero 00-99 y hoja inferior para apartar */
:root{
  --bg:#EDF0F7;
  --surface:#FFFFFF;
  --ink:#0E1A3B;
  --muted:#4F5B7A;
  --line:#C3CCE0;
  --accent:#FFC72C;
  --accent-ink:#0E1A3B;
  --sold-bg:#0E1A3B;
  --sold-fg:#A9B3D1;
  --res-line:#9A6B00;
  --res-fg:#5C4300;
  --danger:#B3261E;
  --font-display:"Big Shoulders Display","Arial Narrow",Impact,sans-serif;
  --font-body:"Figtree",system-ui,-apple-system,"Segoe UI",sans-serif;
}
@media (prefers-color-scheme: dark){
  :root:not([data-theme="light"]){
    --bg:#0A1022;
    --surface:#121B36;
    --ink:#EEF1FA;
    --muted:#9AA6C6;
    --line:#2C3862;
    --accent:#FFC72C;
    --accent-ink:#0E1A3B;
    --sold-bg:#2C3862;
    --sold-fg:#8F9BBD;
    --res-line:#FFC72C;
    --res-fg:#FFE08A;
    --danger:#FF8A80;
    color-scheme:dark;
  }
}
:root[data-theme="dark"]{
  --bg:#0A1022;
  --surface:#121B36;
  --ink:#EEF1FA;
  --muted:#9AA6C6;
  --line:#2C3862;
  --accent:#FFC72C;
  --accent-ink:#0E1A3B;
  --sold-bg:#2C3862;
  --sold-fg:#8F9BBD;
  --res-line:#FFC72C;
  --res-fg:#FFE08A;
  --danger:#FF8A80;
  color-scheme:dark;
}
*{box-sizing:border-box}
body{background:var(--bg);color:var(--ink);font:16px/1.5 var(--font-body);padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));padding-block:20px 48px}
body.has-sheet{padding-bottom:300px}
.wrap{max-width:760px;margin:0 auto;display:flex;flex-direction:column;gap:20px}
h1,h2,h3{margin:0;text-wrap:balance}
button,input,select{font:inherit;color:inherit}
:focus-visible{outline:3px solid var(--accent);outline-offset:2px}

/* Boleta */
.ticket{position:relative;display:grid;grid-template-columns:minmax(0,1fr);background:var(--surface);border-radius:14px;border:1px solid var(--line)}
.stub{position:relative;background:var(--sold-bg);color:var(--accent);padding:18px 22px;border-radius:13px 13px 0 0;display:flex;flex-direction:column;gap:2px}
.stub .lbl{font-size:12px;letter-spacing:.14em;text-transform:uppercase;color:var(--sold-fg);font-weight:700}
.stub .prize{font-family:var(--font-display);font-weight:800;font-size:clamp(44px,13vw,64px);line-height:1;font-variant-numeric:tabular-nums}
.stub::before,.stub::after{content:"";position:absolute;width:22px;height:22px;border-radius:50%;background:var(--bg);bottom:-11px;z-index:2}
.stub::before{left:-12px}
.stub::after{right:-12px}
.tmain{padding:20px 22px 22px;border-top:2px dashed var(--line);display:flex;flex-direction:column;gap:10px;min-width:0}
.tmain h1{font-family:var(--font-display);font-weight:800;font-size:clamp(30px,8vw,40px);line-height:1.05;text-transform:uppercase;letter-spacing:.01em}
.tmain p{margin:0;color:var(--muted)}
.tmain p strong{color:var(--ink)}
.chips{display:flex;flex-wrap:wrap;gap:8px}
.chip{display:inline-flex;align-items:center;gap:6px;padding:4px 12px;border-radius:999px;border:1px solid var(--line);font-size:14px;font-weight:500;background:var(--bg)}
.chip.hot{background:var(--accent);border-color:var(--accent);color:var(--accent-ink);font-weight:700}
@media (min-width:640px){
  .ticket{grid-template-columns:minmax(210px,auto) minmax(0,1fr)}
  .stub{border-radius:13px 0 0 13px;justify-content:center}
  .stub::before,.stub::after{bottom:auto;left:auto;right:-11px}
  .stub::before{top:-12px}
  .stub::after{bottom:-12px}
  .tmain{border-top:0;border-left:2px dashed var(--line)}
}
.winner{background:var(--accent);color:var(--accent-ink);border-radius:12px;padding:14px 18px;display:flex;align-items:baseline;gap:12px;flex-wrap:wrap}
.winner b{font-family:var(--font-display);font-size:44px;line-height:1;font-weight:800}

/* Tablero */
.board{display:flex;flex-direction:column;gap:12px}
.board-head{display:flex;align-items:baseline;justify-content:space-between;gap:12px;flex-wrap:wrap}
.board-head h2{font-family:var(--font-display);font-size:28px;font-weight:800;text-transform:uppercase}
.legend{display:flex;flex-wrap:wrap;gap:14px;font-size:14px;color:var(--muted)}
.legend span{display:inline-flex;align-items:center;gap:6px}
.sw{width:16px;height:16px;border-radius:4px;border:1.5px solid var(--ink);background:var(--surface)}
.sw.res{border:1.5px dashed var(--res-line);background:repeating-linear-gradient(135deg,transparent 0 3px,var(--line) 3px 5px)}
.sw.sold{background:var(--sold-bg);border-color:var(--sold-bg)}
.grid{display:grid;grid-template-columns:repeat(5,minmax(0,1fr));gap:8px}
@media (min-width:520px){.grid{grid-template-columns:repeat(10,minmax(0,1fr))}}
.cell{position:relative;aspect-ratio:1/1;min-width:0;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:0;border-radius:8px;border:1.5px solid var(--ink);background:var(--surface);cursor:pointer;font-family:var(--font-display);font-weight:700;font-size:clamp(22px,5.5vw,28px);line-height:1;padding:0;font-variant-numeric:tabular-nums}
.cell small{font:500 10px/1.1 var(--font-body);max-width:90%;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;margin-top:2px}
.cell:hover{background:var(--bg)}
.cell.res{border:1.5px dashed var(--res-line);color:var(--res-fg);background:repeating-linear-gradient(135deg,transparent 0 5px,var(--line) 5px 7px);cursor:not-allowed}
.cell.sold{background:var(--sold-bg);border-color:var(--sold-bg);color:var(--sold-fg);text-decoration:line-through;cursor:not-allowed}
.cell.sel{background:var(--accent);border-color:var(--accent);color:var(--accent-ink);box-shadow:0 0 0 3px var(--bg),0 0 0 5px var(--ink)}
.cell.win{box-shadow:0 0 0 3px var(--bg),0 0 0 6px var(--accent)}
.cell.ed{box-shadow:0 0 0 3px var(--bg),0 0 0 5px var(--ink)}
.cell.owner.res,.cell.owner.sold{cursor:pointer}

/* Cómo participar */
.how{background:var(--surface);border:1px solid var(--line);border-radius:14px;padding:18px 22px;display:flex;flex-direction:column;gap:10px}
.how h2{font-family:var(--font-display);font-size:24px;font-weight:800;text-transform:uppercase}
.how ol{margin:0;padding-left:22px;display:flex;flex-direction:column;gap:6px}
.how li::marker{font-weight:700;color:var(--muted)}
.how p{margin:0;color:var(--muted);font-size:14px}
.permit{font-size:13px;color:var(--muted);text-align:center;margin:0}

/* Controles */
.btn{display:inline-flex;align-items:center;justify-content:center;gap:8px;min-height:46px;padding:10px 18px;border-radius:10px;border:1.5px solid var(--accent);background:var(--accent);color:var(--accent-ink);font-weight:700;cursor:pointer;text-decoration:none;text-align:center}
.btn.sec{background:transparent;border-color:var(--line);color:var(--ink);font-weight:500}
.btn[aria-disabled="true"],.btn:disabled{opacity:.5;cursor:not-allowed}
.btn.sm{min-height:36px;padding:6px 12px;font-size:14px}
input[type=text],input[type=number],input[type=date],input[type=tel]{width:100%;min-height:44px;padding:9px 12px;border-radius:8px;border:1.5px solid var(--line);background:var(--bg);color:var(--ink)}
label.f{display:flex;flex-direction:column;gap:4px;font-size:14px;font-weight:500;min-width:0}
.hint{font-size:13px;color:var(--muted);margin:0}
.err{color:var(--danger);font-size:14px;margin:0}

/* Hoja inferior */
#sheet{position:fixed;left:0;right:0;bottom:0;z-index:20;background:var(--surface);border-top:2px solid var(--ink);padding:14px max(16px,env(safe-area-inset-left,0px)) calc(14px + env(safe-area-inset-bottom,0px)) max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px));box-shadow:0 -8px 24px rgba(0,0,0,.18)}
.sheet-in{max-width:760px;margin:0 auto;display:flex;flex-direction:column;gap:10px}
.sheet-row{display:flex;gap:8px;flex-wrap:wrap;align-items:center;justify-content:space-between}
.sheet-row .tot{font-family:var(--font-display);font-size:28px;font-weight:800;line-height:1;font-variant-numeric:tabular-nums}
.pick{display:inline-flex;align-items:center;gap:6px;padding:2px 4px 2px 12px;border-radius:999px;background:var(--accent);color:var(--accent-ink);font-weight:700;font-family:var(--font-display);font-size:20px}
.pick button{border:0;background:transparent;width:28px;height:28px;border-radius:50%;cursor:pointer;font-size:18px;line-height:1;color:inherit}
.picks{display:flex;gap:6px;flex-wrap:wrap}
.msgbox{width:100%;min-height:70px;padding:8px 10px;border-radius:8px;border:1.5px solid var(--line);background:var(--bg);color:var(--ink);font-size:14px}
.seg{display:flex;gap:6px;flex-wrap:wrap}
.seg label{display:inline-flex}
.seg input{position:absolute;opacity:0;pointer-events:none}
.seg span{padding:8px 14px;border-radius:999px;border:1.5px solid var(--line);cursor:pointer;font-weight:500}
.seg input:checked+span{background:var(--accent);border-color:var(--accent);color:var(--accent-ink);font-weight:700}
.seg input:focus-visible+span{outline:3px solid var(--accent);outline-offset:2px}

/* Panel del organizador */
.owner{background:var(--surface);border:2px solid var(--ink);border-radius:14px;padding:16px 18px;display:flex;flex-direction:column;gap:12px}
.owner h2{font-family:var(--font-display);font-size:24px;font-weight:800;text-transform:uppercase}
.owner-head{display:flex;justify-content:space-between;gap:10px;flex-wrap:wrap;align-items:center}
.stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(110px,1fr));gap:8px}
.stat{border:1px solid var(--line);border-radius:10px;padding:8px 12px;background:var(--bg)}
.stat b{display:block;font-family:var(--font-display);font-size:28px;line-height:1.1;font-variant-numeric:tabular-nums}
.stat span{font-size:12px;color:var(--muted);text-transform:uppercase;letter-spacing:.08em}
.fields{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:12px}
details summary{cursor:pointer;font-weight:700;padding:6px 0}
@media (prefers-reduced-motion:no-preference){.cell{transition:background .12s,transform .12s}.cell:active{transform:scale(.96)}}
</style>
<div id="app" class="wrap"></div>
<div id="sheet" hidden></div>
<!--
  AJUSTES DE LA RIFA (edita solo la línea de abajo, entre las llaves):
  prize   = premio en pesos            price  = valor por número
  drawDate= fecha del sorteo (AAAA-MM-DD)   lottery= nombre de la lotería
  phone   = tu WhatsApp con código de país, solo números (ej. "573001234567")
  permit  = autorización de la rifa (opcional)   winner = número ganador, ej. "07" (después del sorteo)
  numbers = números ocupados, ej. {"07":{"name":"Juan","status":"vendido"},"23":{"name":"Ana","status":"apartado"}}
  status puede ser "vendido" o "apartado". Los demás números quedan disponibles.
-->
<script type="application/json" id="state">{"prize":500000,"price":10000,"drawDate":"2026-11-17","lottery":"Sinuano Noche","phone":"573024660747","permit":"","winner":"","numbers":{}}</script>
<script id="app-script">
(function(){
  var S = JSON.parse(document.getElementById('state').textContent);
  var owner = false, ownerView = true, dirty = false;
  var sel = new Set(), edit = null, editStatus = 'libre', buyer = '', pubMsg = '', claudeArt = null;
  var COP = new Intl.NumberFormat('es-CO', {style:'currency', currency:'COP', maximumFractionDigits:0});
  var $ = function(id){ return document.getElementById(id); };
  var pad = function(n){ return String(n).padStart(2,'0'); };

  function h(tag, attrs){
    var e = document.createElement(tag);
    var a = attrs || {};
    Object.keys(a).forEach(function(k){
      var v = a[k];
      if (v == null || v === false) return;
      if (k === 'class') e.className = v;
      else if (k === 'text') e.textContent = v;
      else if (k.slice(0,2) === 'on') e.addEventListener(k.slice(2), v);
      else e.setAttribute(k, v === true ? '' : v);
    });
    for (var i = 2; i < arguments.length; i++){
      var kids = [].concat(arguments[i]);
      kids.forEach(function(c){ if (c == null || c === false) return; e.append(c.nodeType ? c : document.createTextNode(c)); });
    }
    return e;
  }

  function dateObj(){ return new Date(S.drawDate + 'T12:00:00'); }
  function longDate(){ return dateObj().toLocaleDateString('es-CO', {day:'numeric', month:'long', year:'numeric'}); }
  function dayMonth(){ return dateObj().toLocaleDateString('es-CO', {day:'numeric', month:'long'}); }
  function daysLeft(){
    var t = new Date(); t.setHours(0,0,0,0);
    var d = new Date(S.drawDate + 'T00:00:00');
    return Math.round((d - t) / 86400000);
  }
  function countdown(){
    var n = daysLeft();
    if (n > 1) return 'Faltan ' + n + ' días';
    if (n === 1) return 'El sorteo es mañana';
    if (n === 0) return 'El sorteo es hoy';
    return 'Sorteo realizado';
  }
  function counts(){
    var sold = 0, res = 0;
    Object.keys(S.numbers).forEach(function(k){ if (S.numbers[k].status === 'vendido') sold++; else res++; });
    return {sold:sold, res:res, free:100 - sold - res};
  }
  function state(n){ var e = S.numbers[pad(n)]; return e ? (e.status === 'vendido' ? 'sold' : 'res') : 'free'; }
  function stateWord(s){ return s === 'sold' ? 'vendido' : s === 'res' ? 'apartado' : 'disponible'; }

  /* ---------- Encabezado ---------- */
  function renderHeader(){
    var box = $('hd'); box.replaceChildren();
    box.append(
      h('div', {class:'ticket'},
        h('div', {class:'stub'},
          h('span', {class:'lbl', text:'Premio'}),
          h('span', {class:'prize', text:COP.format(S.prize)})
        ),
        h('div', {class:'tmain'},
          h('h1', {text:'Rifa del ' + dayMonth()}),
          h('p', {}, 'Gana el número que coincida con las dos últimas cifras del premio mayor.'),
          h('p', {}, h('strong', {text:'Lotería: '}), S.lottery || 'se anunciará antes del sorteo'),
          h('div', {class:'chips'},
            h('span', {class:'chip hot', text:countdown()}),
            h('span', {class:'chip', text:longDate()}),
            h('span', {class:'chip', text:'Cada número ' + COP.format(S.price)})
          )
        )
      )
    );
    if (S.winner){
      var w = S.numbers[S.winner];
      box.append(h('div', {class:'winner', style:'margin-top:20px'},
        h('span', {text:'Número ganador'}), h('b', {text:S.winner}),
        w && w.name ? h('span', {text:w.name}) : null));
    }
  }

  /* ---------- Tablero ---------- */
  function renderBoard(){
    var box = $('bd'); box.replaceChildren();
    var c = counts();
    var isOwner = owner && ownerView;
    var grid = h('div', {class:'grid', role:'group', 'aria-label':'Números del 00 al 99'});
    for (var i = 0; i < 100; i++){
      (function(i){
        var s = state(i), key = pad(i), entry = S.numbers[key];
        var cls = 'cell' + (s !== 'free' ? ' ' + s : '') + (sel.has(key) ? ' sel' : '') + (S.winner === key ? ' win' : '') + (isOwner ? ' owner' : '') + (edit === key ? ' ed' : '');
        var blocked = !isOwner && s !== 'free';
        var b = h('button', {type:'button', class:cls, disabled:blocked, 'aria-pressed':sel.has(key) ? 'true' : 'false', 'aria-label':'Número ' + key + ', ' + stateWord(s) + (sel.has(key) ? ', seleccionado' : ''),
          onclick:function(){ onCell(key, s); }},
          key, isOwner && entry && entry.name ? h('small', {text:entry.name}) : null);
        grid.append(b);
      })(i);
    }
    box.append(
      h('div', {class:'board-head'},
        h('h2', {text:'Escoge tu número'}),
        h('span', {class:'hint', text:c.free + ' disponibles de 100'})
      ),
      h('div', {class:'legend'},
        h('span', {}, h('i', {class:'sw'}), 'Disponible'),
        h('span', {}, h('i', {class:'sw res'}), 'Apartado'),
        h('span', {}, h('i', {class:'sw sold'}), 'Vendido')
      ),
      grid
    );
  }
  function onCell(key, s){
    if (owner && ownerView){
      edit = key; editStatus = s === 'sold' ? 'vendido' : s === 'res' ? 'apartado' : 'libre';
    } else {
      if (s !== 'free') return;
      if (sel.has(key)) sel.delete(key); else sel.add(key);
    }
    renderBoard(); renderSheet();
  }

  /* ---------- Cómo participar ---------- */
  function renderHow(){
    var box = $('hw'); box.replaceChildren();
    box.append(
      h('h2', {text:'Cómo participar'}),
      h('ol', {},
        h('li', {text:'Toca uno o varios números disponibles.'}),
        h('li', {text:'Escribe tu nombre.'}),
        h('li', {text:'Envía el mensaje por WhatsApp al organizador.'}),
        h('li', {text:'Paga ' + COP.format(S.price) + ' por número. El organizador confirma y tu número aparece como vendido.'})
      ),
      h('p', {text:'Mientras el organizador no confirme, el número puede seguir apareciendo disponible. Si dos personas piden el mismo, se asigna al primero que pague.'})
    );
    if (S.permit) box.append(h('p', {class:'permit', text:'Autorización: ' + S.permit}));
  }

  /* ---------- Hoja inferior ---------- */
  function msgText(){
    var nums = Array.from(sel).sort();
    var base = 'Hola, quiero apartar ' + (nums.length > 1 ? 'los números ' : 'el número ') + nums.join(', ') + ' de la rifa del ' + dayMonth() + '.';
    return buyer.trim() ? base + ' Mi nombre es ' + buyer.trim() + '.' : base;
  }
  function waHref(){ return 'https://wa.me/' + S.phone + '?text=' + encodeURIComponent(msgText()); }

  function buyNode(){
    var nums = Array.from(sel).sort();
    var link = null, copyStatus = h('p', {class:'hint', 'aria-live':'polite'});
    var nameIn = h('input', {type:'text', id:'buyer-name', autocomplete:'name', placeholder:'Tu nombre', value:buyer,
      oninput:function(e){ buyer = e.target.value; updLink(); }});
    var ready = function(){ return buyer.trim().length >= 2; };
    function updLink(){
      if (!link) return;
      link.setAttribute('aria-disabled', ready() ? 'false' : 'true');
      link.setAttribute('href', waHref());
      msgBox.value = msgText();
    }
    var msgBox = h('textarea', {class:'msgbox', readonly:true, hidden:true, 'aria-label':'Mensaje para el organizador'});
    msgBox.value = msgText();
    if (S.phone){
      link = h('a', {class:'btn', href:waHref(), target:'_blank', rel:'noopener', 'aria-disabled':ready() ? 'false' : 'true',
        onclick:function(e){ if (!ready()){ e.preventDefault(); copyStatus.textContent = 'Escribe tu nombre para continuar.'; nameIn.focus(); } }}, 'Apartar por WhatsApp');
    }
    var copyBtn = h('button', {type:'button', class:'btn sec', onclick:function(){
      msgBox.value = msgText();
      var done = function(){ copyStatus.textContent = 'Mensaje copiado. Pégalo en WhatsApp.'; };
      var fail = function(){ msgBox.hidden = false; msgBox.focus(); msgBox.select(); copyStatus.textContent = 'Copia el mensaje manualmente.'; };
      try { navigator.clipboard.writeText(msgText()).then(done, fail); } catch(e){ fail(); }
    }}, 'Copiar mensaje');
    return h('div', {class:'sheet-in'},
      h('div', {class:'sheet-row'},
        h('div', {class:'picks'}, nums.map(function(k){
          return h('span', {class:'pick'}, k, h('button', {type:'button', 'aria-label':'Quitar el número ' + k, onclick:function(){ sel.delete(k); renderBoard(); renderSheet(); }}, '×'));
        })),
        h('span', {class:'tot', text:COP.format(nums.length * S.price)})
      ),
      h('label', {class:'f', for:'buyer-name'}, 'Tu nombre', nameIn),
      h('div', {class:'sheet-row'}, link, copyBtn),
      S.phone
        ? h('p', {class:'hint'}, 'Se abre WhatsApp con el mensaje listo para +' + S.phone + '. Tu número queda apartado cuando el organizador lo confirme.')
        : h('p', {class:'hint'}, 'El organizador aún no ha publicado su WhatsApp. Copia el mensaje y envíaselo por el medio que él te indicó.'),
      copyStatus, msgBox
    );
  }

  function editorNode(){
    var key = edit, entry = S.numbers[key] || {};
    var nameIn = h('input', {type:'text', id:'ed-name', placeholder:'Nombre de quien lo compró', value:entry.name || ''});
    var seg = h('div', {class:'seg', role:'radiogroup', 'aria-label':'Estado'});
    [['libre','Libre'],['apartado','Apartado'],['vendido','Vendido']].forEach(function(o){
      seg.append(h('label', {}, h('input', {type:'radio', name:'ed-status', value:o[0], checked:editStatus === o[0], onchange:function(){ editStatus = o[0]; }}), h('span', {text:o[1]})));
    });
    return h('div', {class:'sheet-in'},
      h('div', {class:'sheet-row'}, h('h3', {text:'Número ' + key, style:'font-family:var(--font-display);font-size:28px;font-weight:800'}),
        h('button', {type:'button', class:'btn sec sm', onclick:function(){ edit = null; renderBoard(); renderSheet(); }}, 'Cerrar')),
      seg,
      h('label', {class:'f', for:'ed-name'}, 'Nombre', nameIn),
      h('div', {class:'sheet-row'},
        h('button', {type:'button', class:'btn', onclick:function(){
          if (editStatus === 'libre'){ delete S.numbers[key]; }
          else { S.numbers[key] = {name:nameIn.value.trim(), status:editStatus}; }
          edit = null; dirty = true; renderBoard(); renderOwner(); renderSheet();
        }}, 'Aplicar al tablero'))
    );
  }

  function publishNode(){
    return h('div', {class:'sheet-in'},
      h('div', {class:'sheet-row'},
        h('span', {text:'Tienes cambios sin publicar.'}),
        h('button', {type:'button', class:'btn', id:'pub-btn', onclick:publish}, 'Publicar cambios')),
      h('p', {class:pubMsg ? 'err' : 'hint', 'aria-live':'polite', text:pubMsg || 'Los participantes verán el tablero actualizado.'})
    );
  }

  function renderSheet(){
    var sh = $('sheet'); sh.replaceChildren();
    var show = false;
    if (owner && ownerView){
      if (edit != null){ show = true; sh.append(editorNode()); }
      else if (dirty){ show = true; sh.append(publishNode()); }
    } else if (sel.size){ show = true; sh.append(buyNode()); }
    sh.hidden = !show;
    document.body.classList.toggle('has-sheet', show);
  }

  /* ---------- Panel del organizador ---------- */
  function field(label, id, type, val, onchange, extra){
    var inp = h('input', {type:type, id:id, value:val, inputmode:extra && extra.inputmode, placeholder:extra && extra.ph, min:extra && extra.min, onchange:function(e){ onchange(e.target.value); dirty = true; renderHeader(); renderHow(); renderSheet(); renderOwnerStats(); }});
    return h('label', {class:'f', for:id}, label, inp, extra && extra.hint ? h('span', {class:'hint', text:extra.hint}) : null);
  }
  function normPhone(v){
    var d = String(v).replace(/\D/g, '');
    if (d.length === 10 && d.charAt(0) === '3') d = '57' + d;
    return d;
  }
  function renderOwnerStats(){
    var el = $('ow-stats'); if (!el) return;
    var c = counts();
    el.replaceChildren(
      h('div', {class:'stat'}, h('b', {text:String(c.sold)}), h('span', {text:'Vendidos'})),
      h('div', {class:'stat'}, h('b', {text:String(c.res)}), h('span', {text:'Apartados'})),
      h('div', {class:'stat'}, h('b', {text:String(c.free)}), h('span', {text:'Libres'})),
      h('div', {class:'stat'}, h('b', {text:COP.format(c.sold * S.price)}), h('span', {text:'Recaudado'})),
      h('div', {class:'stat'}, h('b', {text:COP.format(c.sold * S.price - S.prize)}), h('span', {text:'Frente al premio'}))
    );
  }
  function renderOwner(){
    var box = $('ow'); box.replaceChildren();
    if (!owner) { box.hidden = true; return; }
    box.hidden = false;
    if (!ownerView){
      box.className = '';
      box.append(h('button', {type:'button', class:'btn sec sm', onclick:function(){ ownerView = true; sel.clear(); renderAll(); }}, 'Volver al panel del organizador'));
      return;
    }
    box.className = 'owner';
    box.append(
      h('div', {class:'owner-head'},
        h('h2', {text:'Panel del organizador'}),
        h('button', {type:'button', class:'btn sec sm', onclick:function(){ ownerView = false; edit = null; renderAll(); }}, 'Ver como participante')),
      h('p', {class:'hint', text:'Toca un número del tablero para marcarlo como apartado o vendido. Al terminar, publica los cambios.'}),
      h('div', {class:'stats', id:'ow-stats'}),
      h('details', {},
        h('summary', {text:'Ajustes de la rifa'}),
        h('div', {class:'fields', style:'margin-top:8px'},
          field('Premio (COP)', 'f-prize', 'number', S.prize, function(v){ S.prize = Math.max(0, Number(v) || 0); }, {inputmode:'numeric', min:'0'}),
          field('Valor por número (COP)', 'f-price', 'number', S.price, function(v){ S.price = Math.max(0, Number(v) || 0); }, {inputmode:'numeric', min:'0'}),
          field('Fecha del sorteo', 'f-date', 'date', S.drawDate, function(v){ if (v) S.drawDate = v; }),
          field('Lotería', 'f-lot', 'text', S.lottery, function(v){ S.lottery = v.trim(); }, {ph:'Ej. Lotería de Medellín'}),
          field('Tu WhatsApp', 'f-phone', 'tel', S.phone, function(v){ S.phone = normPhone(v); document.getElementById('f-phone').value = S.phone; }, {inputmode:'tel', ph:'573001234567', hint:'Con código de país, solo números.'}),
          field('Número ganador', 'f-win', 'text', S.winner, function(v){ var d = v.replace(/\D/g, '').slice(0,2); S.winner = d ? pad(d) : ''; document.getElementById('f-win').value = S.winner; renderBoard(); }, {inputmode:'numeric', ph:'Se llena después del sorteo'}),
          field('Autorización de la rifa', 'f-permit', 'text', S.permit, function(v){ S.permit = v.trim(); }, {ph:'Entidad y número de resolución', hint:'Se muestra al final de la página.'})
        )
      )
    );
    renderOwnerStats();
  }

  /* ---------- Publicar ---------- */
  var LT = '<';
  var FONTS = '<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Big+Shoulders+Display:wght@700;800&family=Figtree:wght@400;500;700&display=swap">';
  function buildDoc(){
    var css = document.getElementById('app-style').textContent;
    var js = document.getElementById('app-script').textContent;
    var json = JSON.stringify(S).replace(/</g, '\\u003c');
    var reset = ':root{color-scheme:light;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}body{margin:0;font:14px system-ui,sans-serif}img{max-width:100%}[hidden]{display:none!important}';
    return '<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>' + reset + LT + '/style></head><body>' +
      '<title>Rifa del 17 de Noviembre' + LT + '/title>' +
      '<meta name="claude:viewport-fit-sides" content="cover">' + FONTS +
      '<style id="app-style">' + css + LT + '/style>' +
      '<div id="app" class="wrap">' + LT + '/div><div id="sheet" hidden>' + LT + '/div>' +
      '<script type="application/json" id="state">' + json + LT + '/script>' +
      '<script id="app-script">' + js + LT + '/script>' +
      '</body></html>';
  }
  async function publish(){
    if (!claudeArt) return;
    pubMsg = ''; var b = $('pub-btn'); if (b){ b.disabled = true; b.textContent = 'Publicando…'; }
    try {
      await claudeArt.publish(buildDoc());
    } catch (e){
      var code = e && e.code;
      pubMsg = code === 'conflict' ? 'Otra versión se publicó antes. La página se recargó con ella; repite tu cambio.'
        : (code === 'not_granted' || code === 'not_writer') ? 'Tu cuenta no puede publicar en esta página.'
        : 'No se pudo publicar. Intenta de nuevo.';
      renderSheet();
    }
  }

  /* ---------- Arranque ---------- */
  function renderAll(){ renderHeader(); renderBoard(); renderHow(); renderOwner(); renderSheet(); }
  var app = $('app');
  app.append(h('div', {id:'ow', hidden:true}), h('div', {id:'hd'}), h('section', {id:'bd', class:'board'}), h('section', {id:'hw', class:'how'}));
  renderAll();

  (async function(){
    try {
      if (!(window.claude && window.claude.use)) return;
      var u = await window.claude.use('user');
      var a = await window.claude.use('artifact');
      if (u && a){
        var isOwner = await u.isOwner();
        var canEdit = await u.canEdit();
        if (isOwner || canEdit){ owner = true; claudeArt = a; renderAll(); }
      }
    } catch (e) { /* la página funciona igual sin capacidades */ }
  })();
})();
</script>

</body>
</html>
