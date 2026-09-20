# nlsrc530.github.io
[학원생_온라인테스트 (6).html](https://github.com/user-attachments/files/32433226/_.6.html)
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>아카데미 온라인 테스트</title>
<style>
:root{--bg:#0f172a;--card:#fff;--ink:#1e293b;--muted:#64748b;--brand:#4f46e5;--brand2:#6366f1;--ok:#16a34a;--bad:#dc2626;--line:#e2e8f0;--soft:#f1f5f9;--warn:#f59e0b}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Malgun Gothic','Apple SD Gothic Neo',system-ui,sans-serif;background:linear-gradient(135deg,#4f46e5,#818cf8 60%,#a5b4fc);min-height:100vh;color:var(--ink);padding:24px}
.wrap{max-width:860px;margin:0 auto}
.brandbar{display:flex;align-items:center;gap:12px;color:#fff;margin-bottom:20px}
.brandbar .logo{width:44px;height:44px;border-radius:12px;background:rgba(255,255,255,.2);display:grid;place-items:center;font-size:24px}
.brandbar h1{font-size:22px;font-weight:800}
.brandbar p{font-size:13px;opacity:.85}
.card{background:var(--card);border-radius:18px;padding:28px;box-shadow:0 20px 50px rgba(15,23,42,.25);animation:pop .3s ease}
@keyframes pop{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}
h2{font-size:20px;margin-bottom:6px}
.sub{color:var(--muted);font-size:14px;margin-bottom:20px}
label{display:block;font-size:13px;font-weight:700;margin:14px 0 6px}
input,select,textarea{width:100%;padding:12px 14px;border:1.5px solid var(--line);border-radius:10px;font-size:15px;font-family:inherit;transition:.15s}
input:focus,select:focus,textarea:focus{outline:none;border-color:var(--brand)}
.btn{display:inline-flex;align-items:center;justify-content:center;gap:8px;background:var(--brand);color:#fff;border:none;padding:13px 22px;border-radius:10px;font-size:15px;font-weight:700;cursor:pointer;transition:.15s;font-family:inherit}
.btn:hover{background:var(--brand2);transform:translateY(-1px)}
.btn.ghost{background:var(--soft);color:var(--ink)}
.btn.ghost:hover{background:#e2e8f0}
.btn.sm{padding:8px 14px;font-size:13px}
.btn.danger{background:var(--bad)}
.row{display:flex;gap:10px;flex-wrap:wrap}
.row.between{justify-content:space-between;align-items:center}
.hide{display:none!important}
.testlist{display:grid;gap:12px;margin-top:8px}
.testitem{border:1.5px solid var(--line);border-radius:12px;padding:16px;display:flex;justify-content:space-between;align-items:center;transition:.15s;cursor:pointer}
.testitem:hover{border-color:var(--brand);background:#f8faff}
.testitem h3{font-size:16px}
.testitem .meta{color:var(--muted);font-size:13px;margin-top:4px}
.pill{font-size:12px;font-weight:700;padding:4px 10px;border-radius:999px;background:var(--soft);color:var(--muted)}
.pill.blue{background:#e0e7ff;color:var(--brand)}
.banner{background:#eef2ff;border:1.5px solid #c7d2fe;border-radius:12px;padding:14px 16px;margin-bottom:18px;font-size:14px;color:var(--brand)}
.qtop{display:flex;justify-content:space-between;align-items:center;margin-bottom:18px}
.timer{background:var(--soft);padding:8px 16px;border-radius:999px;font-weight:800;font-variant-numeric:tabular-nums;color:var(--brand)}
.timer.warn{background:#fef3c7;color:var(--warn);animation:blink 1s infinite}
@keyframes blink{50%{opacity:.5}}
.progress{height:8px;background:var(--soft);border-radius:999px;overflow:hidden;margin-bottom:20px}
.progress>span{display:block;height:100%;background:var(--brand);transition:.3s}
.qnum{color:var(--brand);font-weight:800;font-size:13px}
.qtext{font-size:18px;font-weight:700;margin:8px 0 18px;line-height:1.5}
.qimg{width:100%;max-height:440px;object-fit:contain;border:1.5px solid var(--line);border-radius:12px;background:#fff;margin:6px 0 18px}
.expimg{width:100%;max-height:380px;object-fit:contain;border:1.5px solid var(--line);border-radius:10px;background:#fff;margin-top:10px}
.uploader{border:2px dashed #c7d2fe;border-radius:12px;padding:18px;text-align:center;cursor:pointer;background:#f8faff;transition:.15s;color:var(--brand);font-weight:700;font-size:14px}
.uploader:hover{background:#eef2ff;border-color:var(--brand)}
.thumb{width:100%;max-height:220px;object-fit:contain;border:1.5px solid var(--line);border-radius:10px;background:#fff;margin-top:8px}
.ansgrid{display:flex;gap:10px;flex-wrap:wrap;margin-top:4px}
.ansbtn{width:52px;height:52px;border-radius:12px;border:1.5px solid var(--line);background:#fff;font-weight:800;font-size:18px;cursor:pointer;transition:.12s;display:grid;place-items:center}
.ansbtn:hover{border-color:var(--brand2);background:#f8faff}
.ansbtn.sel{background:var(--brand);color:#fff;border-color:var(--brand)}
.ansbtn.correct{background:var(--ok);color:#fff;border-color:var(--ok)}
.ansbtn.wrong{background:var(--bad);color:#fff;border-color:var(--bad)}
.short-input{width:100%;padding:14px 16px;border:1.5px solid var(--brand);border-radius:10px;font-size:16px}
.short-ans{background:#f0fdf4;border:1.5px solid var(--ok);border-radius:8px;padding:10px 12px;font-size:14px;margin-top:8px}
.seg{display:inline-flex;background:var(--soft);border-radius:10px;padding:4px;gap:4px}
.seg button{border:none;background:transparent;padding:8px 16px;border-radius:8px;font-weight:700;font-size:13px;cursor:pointer;color:var(--muted)}
.seg button.on{background:var(--brand);color:#fff}
#cropRoot .cm{position:fixed;inset:0;background:rgba(15,23,42,.88);z-index:999;display:flex;flex-direction:column;padding:16px}
#cropRoot .cm .tip{color:#fff;text-align:center;margin-bottom:8px;font-size:14px}
#cropRoot .stage{flex:1;overflow:auto;display:flex;align-items:flex-start;justify-content:center}
#cropRoot .cwrap{position:relative;display:inline-block;touch-action:none}
#cropRoot img{max-width:100%;display:block;-webkit-user-select:none;user-select:none}
#cropRoot .sel{position:absolute;border:2px solid #fff;box-shadow:0 0 0 9999px rgba(15,23,42,.5);background:transparent;display:none}
.opts{display:grid;gap:10px}
.opt{border:1.5px solid var(--line);border-radius:10px;padding:14px 16px;cursor:pointer;display:flex;align-items:center;gap:12px;transition:.12s;font-size:15px}
.opt:hover{border-color:var(--brand2);background:#f8faff}
.opt.sel{border-color:var(--brand);background:#eef2ff}
.opt .mk{width:26px;height:26px;border-radius:50%;border:2px solid var(--line);display:grid;place-items:center;font-weight:800;font-size:13px;flex-shrink:0}
.opt.sel .mk{background:var(--brand);color:#fff;border-color:var(--brand)}
.opt.correct{border-color:var(--ok);background:#f0fdf4}
.opt.correct .mk{background:var(--ok);color:#fff;border-color:var(--ok)}
.opt.wrong{border-color:var(--bad);background:#fef2f2}
.opt.wrong .mk{background:var(--bad);color:#fff;border-color:var(--bad)}
.navbtns{display:flex;justify-content:space-between;margin-top:24px;gap:10px}
.score-ring{width:150px;height:150px;border-radius:50%;margin:10px auto 20px;display:grid;place-items:center;background:conic-gradient(var(--brand) var(--deg,0deg),var(--soft) 0)}
.score-ring .inner{width:118px;height:118px;border-radius:50%;background:#fff;display:grid;place-items:center;text-align:center}
.score-ring .inner b{font-size:34px;color:var(--brand)}
.score-ring .inner small{color:var(--muted);font-size:12px}
.stat{display:flex;gap:12px;justify-content:center;margin-bottom:16px;flex-wrap:wrap}
.stat .box{background:var(--soft);border-radius:12px;padding:12px 20px;text-align:center;min-width:84px}
.stat .box b{display:block;font-size:22px}
.stat .box small{color:var(--muted);font-size:12px}
.cmp{background:var(--soft);border-radius:12px;padding:16px;margin-bottom:20px}
.cmp .bar{position:relative;height:34px;background:#e2e8f0;border-radius:8px;margin:8px 0}
.cmp .fill{position:absolute;left:0;top:0;height:100%;border-radius:8px;display:flex;align-items:center;padding:0 10px;color:#fff;font-weight:800;font-size:13px}
.cmp .avgmark{position:absolute;top:-4px;bottom:-4px;width:3px;background:var(--warn)}
.cmp .lbl{display:flex;justify-content:space-between;font-size:12px;color:var(--muted)}
.review-q{border:1.5px solid var(--line);border-radius:12px;padding:16px;margin-bottom:12px}
.review-q .rq{font-weight:700;margin-bottom:8px}
.explain{background:#f8faff;border-left:3px solid var(--brand);border-radius:6px;padding:10px 12px;margin-top:10px;font-size:14px;line-height:1.6;color:#334155}
.lecture-link{display:inline-flex;align-items:center;gap:6px;margin-top:10px;background:#eef2ff;color:var(--brand);padding:8px 14px;border-radius:8px;font-size:13px;font-weight:700;text-decoration:none;transition:.15s}
.lecture-link:hover{background:#e0e7ff}
.badge{font-size:12px;font-weight:800;padding:3px 10px;border-radius:999px}
.badge.ok{background:#dcfce7;color:var(--ok)}
.badge.no{background:#fee2e2;color:var(--bad)}
.tabs{display:flex;gap:8px;margin-bottom:18px;flex-wrap:wrap}
.tab{padding:8px 16px;border-radius:999px;background:var(--soft);cursor:pointer;font-weight:700;font-size:14px;color:var(--muted)}
.tab.active{background:var(--brand);color:#fff}
.qedit{border:1.5px solid var(--line);border-radius:12px;padding:14px;margin-bottom:12px;background:#fafbff}
.qedit .opts4{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-top:8px}
.linkbox{display:flex;gap:8px;align-items:center;background:var(--soft);border-radius:8px;padding:8px 10px;margin-top:8px}
.linkbox input{border:none;background:transparent;font-size:12px;color:var(--muted);padding:4px}
.foot{text-align:center;color:#fff;opacity:.7;font-size:12px;margin-top:20px}
.empty{text-align:center;color:var(--muted);padding:40px 0}
table{width:100%;border-collapse:collapse;font-size:13px;margin-top:8px}
th,td{padding:8px;border-bottom:1px solid var(--line)}
thead tr{background:var(--soft)}
@media(max-width:600px){.qedit .opts4{grid-template-columns:1fr}.card{padding:20px}}
</style>
</head>
<body>
<div class="wrap">
  <div class="brandbar">
    <div class="logo">📚</div>
    <div><h1>아카데미 온라인 테스트</h1><p>학원생 전용 평가 시스템</p></div>
  </div>
  <div id="app"></div>
  <div id="cropRoot"></div>
  <div class="foot">© Academy Online Test · 모든 기록은 이 브라우저에만 저장됩니다</div>
</div>
<script>
/* Academy Online Test v2 – cafe-link entry, explanations + lecture links, averages */
const LS_TESTS='acad_tests_v2', LS_RESULTS='acad_results_v2';
const el=document.getElementById('app');
const esc=s=>String(s==null?'':s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const nlabel=i=>'('+(i+1)+')';

const SEED=[
 {id:'t1',title:'중등 수학 - 기초 연산',subject:'수학',minutes:10,questions:[
   {q:'12 × 8 의 값은?',opts:['84','96','108','88'],ans:1,explain:'12 × 8 = 12 × 8 = 96. 12를 8번 더하면 96입니다.',lecture:'https://www.youtube.com/results?search_query=곱셈+기초'},
   {q:'분수 1/2 + 1/4 은?',opts:['2/6','3/4','1/6','2/4'],ans:1,explain:'통분하면 2/4 + 1/4 = 3/4 입니다.',lecture:'https://www.youtube.com/results?search_query=분수+덧셈'},
   {q:'144 ÷ 12 은?',opts:['11','12','13','14'],ans:1,explain:'12 × 12 = 144 이므로 144 ÷ 12 = 12.',lecture:'https://www.youtube.com/results?search_query=나눗셈+연습'},
   {q:'직각삼각형에서 가장 긴 변을 무엇이라 하는가?',opts:['높이','밑변','빗변','직각변'],ans:2,explain:'직각의 맞은편에 있는 가장 긴 변을 빗변이라 합니다.',lecture:'https://www.youtube.com/results?search_query=직각삼각형+빗변'},
   {q:'2의 5제곱은?',opts:['16','25','32','64'],ans:2,explain:'2×2×2×2×2 = 32 입니다.',lecture:'https://www.youtube.com/results?search_query=거듭제곱+계산'},
 ]},
 {id:'t2',title:'영어 - 기초 어휘 & 문법',subject:'영어',minutes:8,questions:[
   {q:'"apple"의 뜻은?',opts:['바나나','사과','포도','오렌지'],ans:1,explain:'apple = 사과 입니다.',lecture:'https://www.youtube.com/results?search_query=기초+영단어+과일'},
   {q:'She ___ a teacher. 빈칸에 알맞은 것은?',opts:['am','is','are','be'],ans:1,explain:'3인칭 단수 주어 She에는 is를 씁니다.',lecture:'https://www.youtube.com/results?search_query=be동사+is+am+are'},
   {q:'복수형이 올바른 것은?',opts:['childs','childrens','children','childes'],ans:2,explain:'child의 불규칙 복수형은 children 입니다.',lecture:'https://www.youtube.com/results?search_query=불규칙+복수형'},
   {q:'"good"의 비교급은?',opts:['gooder','more good','better','best'],ans:2,explain:'good-better-best. 비교급은 better 입니다.',lecture:'https://www.youtube.com/results?search_query=형용사+비교급'},
   {q:'I ___ to school every day. (현재)',opts:['go','went','going','gone'],ans:0,explain:'현재 시제 일반동사는 go 입니다.',lecture:'https://www.youtube.com/results?search_query=현재시제+동사'},
 ]},
 {id:'t3',title:'과학 - 생활 과학',subject:'과학',minutes:8,questions:[
   {q:'물이 끓는 온도는?',opts:['50℃','80℃','100℃','120℃'],ans:2,explain:'1기압에서 물은 100℃에서 끓습니다.',lecture:'https://www.youtube.com/results?search_query=물의+끓는점'},
   {q:'지구에서 가장 가까운 별은?',opts:['달','태양','화성','금성'],ans:1,explain:'별(항성) 중 가장 가까운 것은 태양입니다. 달은 위성입니다.',lecture:'https://www.youtube.com/results?search_query=태양계+별'},
   {q:'식물이 햇빛으로 영양분을 만드는 과정은?',opts:['호흡','증산','광합성','소화'],ans:2,explain:'식물이 빛을 이용해 양분을 만드는 것을 광합성이라 합니다.',lecture:'https://www.youtube.com/results?search_query=광합성+원리'},
 ]},
];

function loadTests(){try{const d=JSON.parse(localStorage.getItem(LS_TESTS));return d&&d.length?d:SEED;}catch(e){return SEED;}}
function saveTests(t){localStorage.setItem(LS_TESTS,JSON.stringify(t));}
function loadResults(){try{return JSON.parse(localStorage.getItem(LS_RESULTS))||[];}catch(e){return[];}}
function saveResults(r){localStorage.setItem(LS_RESULTS,JSON.stringify(r));}

let student=null, tests=loadTests();
let curTest=null, curIdx=0, answers=[], timerID=null, timeLeft=0;
let adminTab='list', editData=null, entryTestId=null;

function getParam(k){
  const h=(location.hash||'').replace(/^#/,'');
  const hp=new URLSearchParams(h).get(k);
  if(hp)return hp;
  return new URLSearchParams(location.search).get(k);
}
function buildLink(tid){
  const base=location.href.split('#')[0].split('?')[0];
  return base+'#test='+tid;
}

/* ============ ENTRY / LOGIN ============ */
function viewLogin(){
  stopTimer();
  const t=entryTestId?loadTests().find(x=>x.id===entryTestId):null;
  const banner=t?`<div class="banner">🏫 학원 카페 링크로 입장했어요<br><b>“${esc(t.title)}”</b> 시험 (${t.questions.length}문항 · ${t.minutes}분)</div>`:'';
  el.innerHTML=`<div class="card">
    <h2>👋 학생 입장</h2>
    <p class="sub">이름과 학생 번호를 입력하면 시험을 시작합니다.</p>
    ${banner}
    <label>이름</label><input id="nm" placeholder="예: 김학생" autocomplete="off">
    <label>학생 번호</label><input id="sid" placeholder="예: 2026-001" autocomplete="off">
    <div class="row" style="margin-top:22px">
      <button class="btn" onclick="doLogin()">${t?'시험 시작 →':'입장 →'}</button>
      ${entryTestId?'':'<button class="btn ghost" onclick="viewAdmin()">강사 모드</button>'}
    </div>
  </div>`;
}
window.doLogin=function(){
  const n=document.getElementById('nm').value.trim(),i=document.getElementById('sid').value.trim();
  if(!n){alert('이름을 입력해 주세요.');return;}
  student={name:n,id:i||'-'};
  if(entryTestId){const t=loadTests().find(x=>x.id===entryTestId);if(t){startTest(entryTestId);return;}}
  viewHome();
};
window.logout=function(){student=null;viewLogin();};

/* ============ HOME ============ */
function viewHome(){
  stopTimer(); tests=loadTests();
  const list=tests.map(t=>`<div class="testitem" onclick="startTest('${t.id}')">
    <div><h3>${esc(t.title)}</h3><div class="meta">${t.questions.length}문항 · 제한시간 ${t.minutes}분</div></div>
    <span class="pill blue">${esc(t.subject)}</span></div>`).join('');
  el.innerHTML=`<div class="card">
    <div class="row between">
      <div><h2>안녕하세요, ${esc(student.name)}님 👋</h2>
      <p class="sub" style="margin:4px 0 0">학번 ${esc(student.id)} · 응시할 시험을 선택하세요</p></div>
      <button class="btn ghost sm" onclick="logout()">로그아웃</button>
    </div>
    <div class="testlist">${list||'<div class="empty">등록된 시험이 없습니다.</div>'}</div>
    <div class="row" style="margin-top:18px"><button class="btn ghost sm" onclick="viewMyResults()">📊 내 성적 · 평균 보기</button></div>
  </div>`;
}

/* ============ TEST TAKING ============ */
window.startTest=function(tid){
  tests=loadTests();
  curTest=tests.find(t=>t.id===tid);
  if(!curTest){alert('시험을 찾을 수 없습니다.');return;}
  curIdx=0; answers=curTest.questions.map(q=>q.type==='short'?'':-1);
  timeLeft=curTest.minutes*60;
  renderQuestion();
  timerID=setInterval(()=>{
    timeLeft--;
    const te=document.getElementById('tm');
    if(te){te.textContent=fmtTime(timeLeft);te.className='timer'+(timeLeft<=30?' warn':'');}
    if(timeLeft<=0){stopTimer();submitTest();}
  },1000);
};
function renderQuestion(){
  const q=curTest.questions[curIdx], total=curTest.questions.length, L='ABCDE';
  const pct=((curIdx+1)/total*100).toFixed(0);
  const content=q.img?`<img class="qimg" src="${q.img}" alt="문제 이미지">`:`<div class="qtext">${esc(q.q)}</div>`;
  let opts;
  if(q.type==='short'){
    opts=`<div style="font-size:13px;color:var(--muted);margin-bottom:6px">정답을 입력하세요 (단답형)</div><input class="short-input" value="${esc(answers[curIdx]||'')}" oninput="setShort(this.value)" placeholder="예: 42" autocomplete="off">`;
  }else if(q.opts){
    opts=`<div class="opts">${q.opts.map((o,i)=>`<div class="opt${answers[curIdx]===i?' sel':''}" onclick="pick(${i})"><span class="mk">${nlabel(i)}</span><span>${esc(o)}</span></div>`).join('')}</div>`;
  }else{
    const n=q.choices||5;
    opts=`<div style="font-size:13px;color:var(--muted);margin-bottom:6px">정답을 선택하세요</div><div class="ansgrid">${Array.from({length:n},(_,i)=>`<button class="ansbtn${answers[curIdx]===i?' sel':''}" onclick="pick(${i})">${nlabel(i)}</button>`).join('')}</div>`;
  }
  el.innerHTML=`<div class="card">
    <div class="qtop"><span class="qnum">문항 ${curIdx+1} / ${total}</span><span id="tm" class="timer">${fmtTime(timeLeft)}</span></div>
    <div class="progress"><span style="width:${pct}%"></span></div>
    ${content}
    ${opts}
    <div class="navbtns">
      <button class="btn ghost" onclick="prevQ()" ${curIdx===0?'disabled style="opacity:.4"':''}>← 이전</button>
      ${curIdx===total-1?'<button class="btn" onclick="submitTest()">✅ 제출하기</button>':'<button class="btn" onclick="nextQ()">다음 →</button>'}
    </div>
  </div>`;
}
window.pick=function(i){answers[curIdx]=i;renderQuestion();};
window.prevQ=function(){if(curIdx>0){curIdx--;renderQuestion();}};
window.nextQ=function(){if(curIdx<curTest.questions.length-1){curIdx++;renderQuestion();}};
function fmtTime(s){s=Math.max(0,s);const m=Math.floor(s/60),x=s%60;return `${String(m).padStart(2,'0')}:${String(x).padStart(2,'0')}`;}
window.setShort=function(v){answers[curIdx]=v;};
function normShort(s){return String(s==null?'':s).trim().toLowerCase().replace(/\s+/g,'');}
function acceptsOf(q){return String(q.ansText||'').split(/[,，|]/).map(normShort).filter(Boolean);}
function isCorrect(q,a){if(q.type==='short'){const v=normShort(a);return v!==''&&acceptsOf(q).includes(v);}return a===q.ans;}
function unanswered(q,a){return q.type==='short'?(a==null||String(a).trim()===''):(a<0);}
function stopTimer(){if(timerID){clearInterval(timerID);timerID=null;}}

/* ============ SUBMIT + STATS ============ */
function statsFor(testId){
  const rs=loadResults().filter(r=>r.testId===testId);
  if(!rs.length)return{count:0,avg:0,max:0,min:0};
  const sc=rs.map(r=>r.score);
  return{count:rs.length,avg:Math.round(sc.reduce((a,b)=>a+b,0)/sc.length),max:Math.max(...sc),min:Math.min(...sc)};
}
window.submitTest=function(){
  stopTimer();
  const qs=curTest.questions; let correct=0;
  qs.forEach((q,i)=>{if(isCorrect(q,answers[i]))correct++;});
  const un=qs.filter((q,i)=>unanswered(q,answers[i])).length;
  const score=Math.round(correct/qs.length*100);
  const result={testId:curTest.id,testTitle:curTest.title,student:student.name,sid:student.id,
    date:new Date().toLocaleString('ko-KR'),score,correct,total:qs.length,un,answers:answers.slice(),timeUsed:curTest.minutes*60-timeLeft};
  const results=loadResults(); results.push(result); saveResults(results);
  renderResult(result,results.length-1);
};
function renderResult(r,idx){
  const deg=r.score*3.6;
  const un=r.un!=null?r.un:r.answers.filter(a=>a<0).length;
  const emoji=r.score>=90?'🏆':r.score>=70?'👍':r.score>=50?'😅':'😢';
  const msg=r.score>=90?'훌륭해요!':r.score>=70?'잘 했어요!':r.score>=50?'조금만 더!':'다시 도전해봐요!';
  const st=statsFor(r.testId);
  const better=st.count>1?Math.round(loadResults().filter(x=>x.testId===r.testId&&x.score<r.score).length/st.count*100):null;
  const cmp=`<div class="cmp">
    <div class="lbl"><span>학급 평균 비교</span><span>응시 인원 ${st.count}명</span></div>
    <div class="bar"><div class="fill" style="width:${Math.max(r.score,12)}%;background:${r.score>=st.avg?'var(--ok)':'var(--brand)'}">내 점수 ${r.score}</div>
      <div class="avgmark" style="left:${st.avg}%" title="평균 ${st.avg}"></div></div>
    <div class="lbl"><span>평균 <b style="color:var(--warn)">${st.avg}점</b></span><span>최고 ${st.max}점</span></div>
    ${better!=null?`<div style="margin-top:8px;font-size:13px;color:var(--muted)">상위 <b style="color:var(--brand)">${100-better}%</b> · 나보다 낮은 점수 ${better}%</div>`:''}
  </div>`;
  el.innerHTML=`<div class="card">
    <h2>📊 시험 결과</h2>
    <p class="sub">${esc(r.testTitle)} · ${esc(r.date)}</p>
    <div class="score-ring" style="--deg:${deg}deg"><div class="inner"><b>${r.score}</b><small>점</small></div></div>
    <p style="text-align:center;font-size:20px;margin-bottom:14px">${emoji} ${msg}</p>
    <div class="stat">
      <div class="box"><b style="color:var(--ok)">${r.correct}</b><small>정답</small></div>
      <div class="box"><b style="color:var(--bad)">${r.total-r.correct}</b><small>오답</small></div>
      <div class="box"><b>${un}</b><small>미응답</small></div>
      <div class="box"><b>${fmtTime(r.timeUsed)}</b><small>소요시간</small></div>
    </div>
    ${cmp}
    <div class="row" style="justify-content:center;gap:10px">
      <button class="btn" onclick="viewReview('${r.testId}',${idx})">📝 해설 · 강의 확인</button>
      <button class="btn ghost" onclick="viewMyResults()">📈 내 성적</button>
      ${entryTestId?'':'<button class="btn ghost" onclick="viewHome()">🏠 홈</button>'}
    </div>
  </div>`;
}

/* ============ REVIEW (해설 + 강의 링크) ============ */
window.viewReview=function(tid,idx){
  stopTimer();
  const results=loadResults(), r=results[idx];
  const test=loadTests().find(t=>t.id===tid);
  if(!test||!r){alert('결과를 찾을 수 없습니다.');return;}
  const L='ABCDE';
  const review=test.questions.map((q,i)=>{
    const ua=r.answers[i], ok=isCorrect(q,ua);
    const content=q.img?`<img class="qimg" src="${q.img}" alt="문제">`:`<div class="qtext" style="font-size:16px">${esc(q.q)}</div>`;
    let optsHtml, ansLine;
    if(q.type==='short'){
      optsHtml=`<div class="short-ans">정답: <b>${esc(q.ansText||'')}</b></div>`;
      ansLine=`<div style="margin-top:8px;font-size:13px;color:var(--muted)">내 답: ${ua&&String(ua).trim()!==''?esc(ua):'미응답'}</div>`;
    }else if(q.opts){
      optsHtml=q.opts.map((o,j)=>{let cls=j===q.ans?'correct':(j===ua&&!ok?'wrong':'');return `<div class="opt ${cls}"><span class="mk">${nlabel(j)}</span><span>${esc(o)}</span></div>`;}).join('');
      ansLine=`<div style="margin-top:8px;font-size:13px;color:var(--muted)">내 답: ${ua>=0?nlabel(ua):'미응답'} · 정답: ${nlabel(q.ans)}</div>`;
    }else{
      const n=q.choices||5;
      optsHtml=`<div class="ansgrid">${Array.from({length:n},(_,j)=>{let cls=j===q.ans?'correct':(j===ua&&!ok?'wrong':'');return `<button class="ansbtn ${cls}">${nlabel(j)}</button>`;}).join('')}</div>`;
      ansLine=`<div style="margin-top:8px;font-size:13px;color:var(--muted)">내 답: ${ua>=0?nlabel(ua):'미응답'} · 정답: ${nlabel(q.ans)}</div>`;
    }
    const expImg=q.explainImg?`<img class="expimg" src="${q.explainImg}" alt="해설">`:'';
    const expTxt=q.explain?`<div class="explain">💡 ${esc(q.explain)}</div>`:'';
    const lec=q.lecture?`<a class="lecture-link" href="${esc(q.lecture)}" target="_blank" rel="noopener noreferrer">🎥 관련 강의 보기</a>`:'';
    return `<div class="review-q">
      <div class="rq">문항 ${i+1} <span class="badge ${ok?'ok':'no'}">${ok?'정답':'오답'}</span></div>
      ${content}
      ${optsHtml}
      ${ansLine}
      ${expTxt}${expImg}${lec}
    </div>`;
  }).join('');
  el.innerHTML=`<div class="card">
    <h2>📝 해설 & 강의 확인</h2>
    <p class="sub">${esc(r.testTitle)} · ${esc(r.student)} · ${r.score}점</p>
    ${review}
    <div class="row" style="margin-top:12px">
      <button class="btn ghost" onclick="viewMyResults()">📈 내 성적</button>
      ${entryTestId?'':'<button class="btn ghost" onclick="viewHome()">🏠 홈</button>'}
    </div>
  </div>`;
};

/* ============ MY RESULTS + AVERAGES ============ */
window.viewMyResults=function(){
  stopTimer();
  const all=loadResults();
  const mine=all.filter(r=>r.sid===student.id&&r.student===student.name);
  let head='';
  if(mine.length){
    const myAvg=Math.round(mine.reduce((a,b)=>a+b.score,0)/mine.length);
    const best=Math.max(...mine.map(r=>r.score));
    head=`<div class="stat">
      <div class="box"><b style="color:var(--brand)">${myAvg}</b><small>내 평균</small></div>
      <div class="box"><b style="color:var(--ok)">${best}</b><small>최고점</small></div>
      <div class="box"><b>${mine.length}</b><small>응시 횟수</small></div>
    </div>`;
  }
  const rows=mine.slice().reverse().map(r=>{
    const st=statsFor(r.testId);
    const idx=all.indexOf(r);
    const diff=r.score-st.avg;
    const dtxt=diff>0?`<span style="color:var(--ok)">+${diff}</span>`:diff<0?`<span style="color:var(--bad)">${diff}</span>`:'0';
    return `<tr>
      <td>${esc(r.testTitle)}</td>
      <td style="text-align:center"><b style="color:${r.score>=70?'var(--ok)':'var(--bad)'}">${r.score}점</b></td>
      <td style="text-align:center">${st.avg}점</td>
      <td style="text-align:center">${dtxt}</td>
      <td style="text-align:center">${r.correct}/${r.total}</td>
      <td style="text-align:center"><button class="btn ghost sm" onclick="viewReview('${r.testId}',${idx})">해설</button></td>
    </tr>`;
  }).join('');
  el.innerHTML=`<div class="card">
    <h2>📊 내 성적 · 평균</h2>
    <p class="sub">${esc(student.name)} (${esc(student.id)})</p>
    ${head}
    ${mine.length?`<table><thead><tr><th style="text-align:left">시험</th><th>내점수</th><th>평균</th><th>편차</th><th>정답률</th><th>해설</th></tr></thead><tbody>${rows}</tbody></table>`:'<div class="empty">아직 응시 기록이 없어요.</div>'}
    <div class="row" style="margin-top:18px">
      ${entryTestId?'<button class="btn ghost" onclick="logout()">마침하기</button>':'<button class="btn ghost" onclick="viewHome()">🏠 홈으로</button>'}
    </div>
  </div>`;
};

/* ============ ADMIN ============ */
window.viewAdmin=function(){stopTimer();adminTab='list';renderAdmin();};
function renderAdmin(){
  if(adminTab==='edit'){renderEdit();return;}
  tests=loadTests();
  let body='';
  if(adminTab==='list'){
    const list=tests.map(t=>`<div class="testitem">
      <div style="flex:1"><h3>${esc(t.title)}</h3><div class="meta">${t.questions.length}문항 · ${t.minutes}분 · ${esc(t.subject)}</div>
        <div class="linkbox"><span>🔗</span><input readonly value="${esc(buildLink(t.id))}" onclick="this.select()">
          <button class="btn sm" onclick="copyLink('${t.id}')">복사</button></div>
      </div>
      <div class="row" style="flex-direction:column;gap:6px">
        <button class="btn ghost sm" onclick="editTest('${t.id}')">✏️ 편집</button>
        <button class="btn ghost sm" onclick="delTest('${t.id}')">🗑 삭제</button>
      </div></div>`).join('');
    body=`<div class="banner">💡 각 시험의 링크를 복사해 학원 카페에 올리세요. 학생이 링크를 누르면 해당 시험으로 바로 입장합니다.</div>
      <div class="testlist">${list||'<div class="empty">등록된 시험이 없습니다.</div>'}</div>
      <button class="btn" style="margin-top:14px" onclick="newTest()">➕ 새 시험 만들기</button>`;
  } else {
    const results=loadResults();
    if(!results.length)body='<div class="empty">응시 기록이 없습니다.</div>';
    else{
      const byTest={};results.forEach(r=>{(byTest[r.testId]=byTest[r.testId]||[]).push(r);});
      const summary=Object.keys(byTest).map(tid=>{const st=statsFor(tid);const ti=byTest[tid][0].testTitle;
        return `<tr><td>${esc(ti)}</td><td style="text-align:center">${st.count}명</td><td style="text-align:center"><b>${st.avg}점</b></td><td style="text-align:center">${st.max}점</td><td style="text-align:center">${st.min}점</td></tr>`;}).join('');
      const rows=results.slice().reverse().map(r=>`<tr><td>${esc(r.student)} (${esc(r.sid)})</td><td>${esc(r.testTitle)}</td><td style="text-align:center"><b style="color:${r.score>=70?'var(--ok)':'var(--bad)'}">${r.score}점</b></td><td style="text-align:center">${r.correct}/${r.total}</td><td>${esc(r.date)}</td></tr>`).join('');
      body=`<h3 style="margin:4px 0 6px">시험별 평균</h3>
        <table><thead><tr><th style="text-align:left">시험</th><th>응시</th><th>평균</th><th>최고</th><th>최저</th></tr></thead><tbody>${summary}</tbody></table>
        <h3 style="margin:18px 0 6px">전체 응시 기록</h3>
        <table><thead><tr><th style="text-align:left">학생</th><th style="text-align:left">시험</th><th>점수</th><th>정답률</th><th>응시일</th></tr></thead><tbody>${rows}</tbody></table>`;
    }
  }
  el.innerHTML=`<div class="card">
    <div class="row between"><h2>👨‍🏫 강사 관리</h2><button class="btn ghost sm" onclick="backToStudent()">← 학생 모드</button></div>
    <div class="tabs">
      <span class="tab ${adminTab==='list'?'active':''}" onclick="adminTab='list';renderAdmin()">📋 시험/링크 관리</span>
      <span class="tab ${adminTab==='results'?'active':''}" onclick="adminTab='results';renderAdmin()">📊 성적 · 평균</span>
    </div>${body}
  </div>`;
}
window.renderAdmin=renderAdmin;
window.backToStudent=function(){entryTestId=null;viewLogin();};
window.copyLink=function(tid){
  const link=buildLink(tid);
  navigator.clipboard&&navigator.clipboard.writeText(link).then(()=>alert('링크가 복사되었어요!\n'+link),()=>prompt('복사하세요:',link))||prompt('복사하세요:',link);
};

/* ============ IMAGE + CROP HELPERS ============ */
function readFileToDataURL(file,cb){const r=new FileReader();r.onload=e=>cb(e.target.result);r.onerror=()=>alert('이미지를 읽을 수 없습니다.');r.readAsDataURL(file);}
window.onQFile=function(inp,i){const f=inp.files[0];if(!f)return;readFileToDataURL(f,d=>openCropper('q',i,d));inp.value='';};
window.onExpFile=function(inp,i){const f=inp.files[0];if(!f)return;readFileToDataURL(f,d=>openCropper('exp',i,d));inp.value='';};
window.clearQImg=function(i){editData.questions[i].img='';renderEdit();};
window.clearExpImg=function(i){editData.questions[i].explainImg='';renderEdit();};
window.setType=function(i,t){editData.questions[i].type=t;if(t==='choice'){editData.questions[i].choices=5;if(editData.questions[i].ans==null||editData.questions[i].ans<0)editData.questions[i].ans=0;}renderEdit();};

/* ---- Cropper ---- */
let crop={kind:null,idx:0,drag:false,sx:0,sy:0,rect:null};
function openCropper(kind,idx,dataURL){
  crop={kind,idx,drag:false,sx:0,sy:0,rect:null};
  const root=document.getElementById('cropRoot');
  root.innerHTML=`<div class="cm">
    <div class="tip">📐 이미지에서 원하는 문제 영역을 <b>드래그</b>로 선택하세요</div>
    <div class="stage"><div class="cwrap" id="cwrap"><img id="cimg" draggable="false"><div class="sel" id="csel"></div></div></div>
    <div class="row" style="justify-content:center;margin-top:10px">
      <button class="btn" onclick="applyCrop()">✂️ 선택 영역 자르기</button>
      <button class="btn ghost" onclick="applyWhole()">전체 이미지 사용</button>
      <button class="btn ghost" onclick="closeCrop()">취소</button>
    </div></div>`;
  const img=document.getElementById('cimg');
  img.onload=()=>bindCropEvents();
  img.src=dataURL;
}
function bindCropEvents(){
  const wrap=document.getElementById('cwrap'), sel=document.getElementById('csel'), img=document.getElementById('cimg');
  const pos=e=>{const r=img.getBoundingClientRect();const cx=(e.touches?e.touches[0].clientX:e.clientX)-r.left;const cy=(e.touches?e.touches[0].clientY:e.clientY)-r.top;return{x:Math.max(0,Math.min(cx,img.clientWidth)),y:Math.max(0,Math.min(cy,img.clientHeight))};};
  const down=e=>{e.preventDefault();const p=pos(e);crop.drag=true;crop.sx=p.x;crop.sy=p.y;sel.style.display='block';sel.style.left=p.x+'px';sel.style.top=p.y+'px';sel.style.width='0px';sel.style.height='0px';crop.rect=null;};
  const move=e=>{if(!crop.drag)return;e.preventDefault();const p=pos(e);const x=Math.min(p.x,crop.sx),y=Math.min(p.y,crop.sy),w=Math.abs(p.x-crop.sx),h=Math.abs(p.y-crop.sy);sel.style.left=x+'px';sel.style.top=y+'px';sel.style.width=w+'px';sel.style.height=h+'px';crop.rect={x,y,w,h};};
  const up=()=>{crop.drag=false;};
  wrap.onmousedown=down;window.onmousemove=move;window.onmouseup=up;
  wrap.ontouchstart=down;wrap.ontouchmove=move;wrap.ontouchend=up;
}
function cropToDataURL(){
  const img=document.getElementById('cimg');
  const scale=img.naturalWidth/img.clientWidth;
  let r=crop.rect;
  if(!r||r.w<8||r.h<8)return null;
  const sx=r.x*scale, sy=r.y*scale, sw=r.w*scale, sh=r.h*scale;
  const outW=Math.min(sw,1100), k=outW/sw;
  const cv=document.createElement('canvas');cv.width=Math.round(sw*k);cv.height=Math.round(sh*k);
  cv.getContext('2d').drawImage(img,sx,sy,sw,sh,0,0,cv.width,cv.height);
  return cv.toDataURL('image/jpeg',0.85);
}
function wholeToDataURL(){
  const img=document.getElementById('cimg');
  const k=Math.min(1,1100/img.naturalWidth);
  const cv=document.createElement('canvas');cv.width=Math.round(img.naturalWidth*k);cv.height=Math.round(img.naturalHeight*k);
  cv.getContext('2d').drawImage(img,0,0,cv.width,cv.height);
  return cv.toDataURL('image/jpeg',0.85);
}
function assignCrop(d){if(!d)return;if(crop.kind==='q')editData.questions[crop.idx].img=d;else editData.questions[crop.idx].explainImg=d;closeCrop();renderEdit();}
window.applyCrop=function(){const d=cropToDataURL();if(!d){alert('먼저 자를 영역을 드래그로 선택하세요.');return;}assignCrop(d);};
window.applyWhole=function(){assignCrop(wholeToDataURL());};
window.closeCrop=function(){window.onmousemove=null;window.onmouseup=null;document.getElementById('cropRoot').innerHTML='';};

/* ============ EDIT / CRUD (이미지 기반) ============ */
function blankQ(){return{img:'',type:'choice',choices:5,ans:0,ansText:'',explain:'',explainImg:'',lecture:''};}
window.newTest=function(){editData={id:'t'+Date.now(),title:'',subject:'',minutes:10,questions:[blankQ()]};adminTab='edit';renderAdmin();};
window.editTest=function(tid){editData=JSON.parse(JSON.stringify(loadTests().find(t=>t.id===tid)));editData.questions.forEach(q=>{if(q.explain==null)q.explain='';if(q.lecture==null)q.lecture='';if(q.explainImg==null)q.explainImg='';if(q.img==null)q.img='';if(q.ansText==null)q.ansText='';if(!q.type)q.type=q.opts?'choice':'choice';if(q.type==='choice'&&!q.choices&&!q.opts)q.choices=5;});adminTab='edit';renderAdmin();};
window.delTest=function(tid){if(!confirm('이 시험을 삭제하시겠습니까?'))return;saveTests(loadTests().filter(t=>t.id!==tid));renderAdmin();};
function renderEdit(){
  if(!editData)return;
  const L='ABCDE';
  const qs=editData.questions.map((q,i)=>{
    const legacy=!!q.opts;
    const type=q.type||(legacy?'choice':'choice');
    const n=q.opts?q.opts.length:(q.choices||5);
    const qImgBox=legacy?`<label>문제(텍스트)</label><input value="${esc(q.q||'')}" oninput="editData.questions[${i}].q=this.value">`
      :(q.img?`<img class="thumb" src="${q.img}"><button class="btn ghost sm" style="margin-top:6px" onclick="clearQImg(${i})">문제 이미지 다시 선택/삭제</button>`
        :`<label class="uploader" for="qf${i}">📂 문제 이미지 불러오기 → 영역 드래그 선택</label><input id="qf${i}" type="file" accept="image/*" style="display:none" onchange="onQFile(this,${i})">`);
    const typeSeg=legacy?'':`<label>정답 유형</label><div class="seg"><button class="${type==='choice'?'on':''}" onclick="setType(${i},'choice')">5지선다형</button><button class="${type==='short'?'on':''}" onclick="setType(${i},'short')">단답형</button></div>`;
    let ansBox;
    if(type==='short'){
      ansBox=`<label>정답 (단답형 · 여러 개는 쉼표로 구분)</label><input placeholder="예: 42, 사십이" value="${esc(q.ansText||'')}" oninput="editData.questions[${i}].ansText=this.value">`;
    }else{
      ansBox=`<label>정답 (5지선다형)</label><div class="ansgrid">${Array.from({length:5},(_,j)=>`<button class="ansbtn${q.ans===j?' sel':''}" onclick="editData.questions[${i}].ans=${j};renderEdit()">${nlabel(j)}</button>`).join('')}</div>`;
    }
    const expImgBox=q.explainImg?`<img class="thumb" src="${q.explainImg}"><button class="btn ghost sm" style="margin-top:6px" onclick="clearExpImg(${i})">해설 이미지 다시 선택/삭제</button>`
      :`<label class="uploader" for="ef${i}">🖼️ 해설 이미지 불러오기 → 영역 선택 (선택사항)</label><input id="ef${i}" type="file" accept="image/*" style="display:none" onchange="onExpFile(this,${i})">`;
    return `<div class="qedit">
      <div class="row between"><b>문항 ${i+1}</b><button class="btn ghost sm" onclick="rmQ(${i})">🗑</button></div>
      ${qImgBox}
      ${typeSeg}
      ${ansBox}
      <label>해설 (텍스트, 선택)</label><textarea rows="2" oninput="editData.questions[${i}].explain=this.value">${esc(q.explain||'')}</textarea>
      <label>해설 이미지</label>${expImgBox}
      <label>강의 링크 (URL, 선택)</label><input placeholder="https://..." value="${esc(q.lecture||'')}" oninput="editData.questions[${i}].lecture=this.value">
    </div>`;
  }).join('');
  el.innerHTML=`<div class="card">
    <h2>${editData.title?'✏️ 시험 수정':'➕ 새 시험'}</h2>
    <div class="banner">💡 문제/해설 이미지를 불러온 뒤 <b>여러 문제 중 원하는 부분을 박스로 드래그</b>하면 그 영역만 잘라서 올라갑니다. 정답은 5지선다형 또는 단답형으로 입력합니다.</div>
    <label>시험 제목</label><input value="${esc(editData.title)}" oninput="editData.title=this.value">
    <label>과목</label><input value="${esc(editData.subject)}" oninput="editData.subject=this.value">
    <label>제한 시간(분)</label><input type="number" min="1" value="${editData.minutes}" oninput="editData.minutes=+this.value">
    <h2 style="margin-top:22px">문항 목록</h2>${qs}
    <button class="btn ghost" style="margin-top:10px" onclick="addQ()">➕ 문항 추가</button>
    <div class="row" style="margin-top:20px"><button class="btn" onclick="saveEdit()">💾 저장</button><button class="btn ghost" onclick="adminTab='list';renderAdmin()">취소</button></div>
  </div>`;
}
window.addQ=function(){editData.questions.push(blankQ());renderEdit();};
window.rmQ=function(i){if(editData.questions.length<=1){alert('최소 1문항 필요');return;}editData.questions.splice(i,1);renderEdit();};
window.saveEdit=function(){
  const t=editData; t.title=(t.title||'').trim(); t.subject=(t.subject||'').trim();
  if(!t.title){alert('시험 제목을 입력하세요.');return;}
  for(let k=0;k<t.questions.length;k++){const q=t.questions[k];
    if(q.opts){if(!q.q||!q.q.trim()){alert(`${k+1}번 문제가 비어있어요.`);return;}}
    else if(!q.img){alert(`${k+1}번 문제 이미지를 올려주세요.`);return;}
    if((q.type==='short')&&(!q.ansText||!q.ansText.trim())){alert(`${k+1}번 단답형 정답을 입력해주세요.`);return;}
  }
  const list=loadTests(); const idx=list.findIndex(x=>x.id===t.id);
  if(idx>=0)list[idx]=t;else list.push(t);
  try{saveTests(list);}catch(e){alert('저장 용량을 초과했어요. 이미지 수를 줄이거나 크기를 줄여주세요.');return;}
  adminTab='list'; renderAdmin();
};

/* ============ INIT ============ */
(function init(){
  const tid=getParam('test');
  if(tid&&loadTests().find(t=>t.id===tid)){entryTestId=tid;}
  window.addEventListener('hashchange',()=>{
    const t=getParam('test');
    if(t&&loadTests().find(x=>x.id===t)&&!student){entryTestId=t;viewLogin();}
  });
  viewLogin();
})();

</script>
</body>
</html>
