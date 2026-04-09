<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>초등 단원평가 문항 생성기</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:-apple-system,BlinkMacSystemFont,sans-serif;background:#f8fafc;color:#1e293b;font-size:14px}
.wrap{max-width:860px;margin:0 auto;padding:20px}
.card{background:#fff;border-radius:12px;border:1px solid #e2e8f0;padding:20px;margin-bottom:14px}
h1{font-size:20px;font-weight:600;margin-bottom:4px}
.sub{font-size:12px;color:#94a3b8}
.upload-zone{border:2px dashed #cbd5e1;border-radius:10px;padding:28px;text-align:center;cursor:pointer;transition:.2s}
.upload-zone:hover{border-color:#3b82f6;background:#eff6ff}
.file-item{display:flex;align-items:center;justify-content:space-between;background:#f8fafc;padding:10px 12px;border-radius:8px;margin-top:6px}
.rm{border:none;background:none;color:#ef4444;cursor:pointer;font-size:18px;padding:0 4px}
.prog-wrap{background:#dbeafe;border-radius:6px;height:6px;margin-top:8px;overflow:hidden}
.prog-bar{height:6px;background:#3b82f6;border-radius:6px;transition:width .3s;width:0}
.status{font-size:12px;color:#3b82f6;font-weight:500;margin-top:6px}
.img-grid{display:grid;grid-template-columns:repeat(5,1fr);gap:8px;max-height:300px;overflow-y:auto;margin-top:10px}
.thumb{border-radius:8px;border:1px solid #e2e8f0;overflow:hidden;cursor:pointer}
.thumb img{width:100%;height:72px;object-fit:contain;background:#f8fafc;display:block}
.thumb-label{font-size:9px;color:#64748b;text-align:center;padding:3px 2px;background:#fff;border-top:1px solid #e2e8f0;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.thumb:hover{border-color:#3b82f6}
.btn-main{width:100%;padding:12px;border-radius:8px;border:none;font-size:14px;font-weight:600;cursor:pointer;margin-top:12px;display:flex;align-items:center;justify-content:center;gap:8px;transition:.2s;background:#3b82f6;color:#fff}
.btn-main:hover{background:#2563eb}
.btn-main:disabled{background:#cbd5e1;cursor:not-allowed}
.export-row{display:flex;gap:8px}
.btn-s{flex:1;padding:10px;border-radius:8px;border:1px solid;font-size:13px;font-weight:500;cursor:pointer;background:#fff}
.btn-g{color:#059669;border-color:#6ee7b7}.btn-g:hover{background:#ecfdf5}
.btn-p{color:#7c3aed;border-color:#c4b5fd}.btn-p:hover{background:#f5f3ff}
.q-card{background:#fff;border-radius:12px;border:1px solid #e2e8f0;padding:20px;margin-bottom:10px}
.q-top{display:flex;align-items:center;justify-content:space-between;margin-bottom:10px}
.q-num{display:flex;align-items:center;gap:8px;font-weight:600;font-size:15px}
.badge{font-size:11px;padding:2px 8px;border-radius:20px;font-weight:500}
.bm{background:#fef9c3;color:#854d0e}.bh{background:#fee2e2;color:#991b1b}.be{background:#dcfce7;color:#166534}
.edit-btn{font-size:12px;padding:5px 10px;border-radius:6px;border:1px solid #e2e8f0;background:#f8fafc;color:#64748b;cursor:pointer}
.q-meta{font-size:11px;color:#94a3b8;margin-bottom:8px;white-space:pre-wrap;font-family:monospace}
.q-content{font-size:13px;line-height:1.8;white-space:pre-wrap}
.q-imgs{margin-top:10px;display:flex;flex-wrap:wrap;gap:10px}
.q-img{border:1px solid #e2e8f0;border-radius:8px;overflow:hidden;cursor:pointer;max-width:300px}
.q-img img{width:100%;max-height:180px;object-fit:contain;background:#f8fafc;display:block}
.q-img-lbl{font-size:11px;color:#64748b;text-align:center;padding:4px;border-top:1px solid #e2e8f0}
.q-ans{margin-top:12px;padding-top:12px;border-top:1px solid #f1f5f9}
.q-ans-txt{font-size:13px;font-weight:400;color:#1e293b;white-space:pre-wrap}
.q-expl{font-size:12px;color:#64748b;margin-top:4px;white-space:pre-wrap}
.lbox{position:fixed;inset:0;background:rgba(0,0,0,.8);display:none;align-items:center;justify-content:center;z-index:1000;flex-direction:column}
.lbox img{max-width:90vw;max-height:80vh;border-radius:8px;object-fit:contain}
.lbox-lbl{color:#fff;font-size:12px;margin-top:10px;opacity:.8}
.ph{display:flex;align-items:center;justify-content:space-between;margin-bottom:8px}
.tgl{font-size:12px;color:#3b82f6;cursor:pointer;border:none;background:none}
.sec{font-size:13px;font-weight:600;color:#475569;margin-bottom:8px}
.dragging{opacity:.5}
.drag-over{border-top:3px solid #3b82f6}
.stream{background:#f8fafc;border:1px solid #e2e8f0;border-radius:8px;padding:12px;margin-top:12px;font-size:12px;color:#475569;max-height:120px;overflow-y:auto;white-space:pre-wrap;display:none}
</style>
</head>
<body>
<div class="wrap">
  <div class="card">
    <h1>초등 단원평가 문항 생성기</h1>
    <div class="sub">PDF 업로드 → 이미지 추출 → AI 문항 자동 생성</div>
  </div>

  <div class="card">
    <label for="fi">
      <div class="upload-zone">
        <svg width="40" height="40" style="margin:0 auto 8px;display:block;color:#94a3b8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M15 13l-3-3m0 0l-3 3m3-3v12"/>
        </svg>
        <div style="font-size:13px;color:#64748b">개념정리 PDF를 업로드하세요 (여러 개 가능)</div>
      </div>
      <input type="file" id="fi" accept=".pdf" multiple style="display:none">
    </label>

    <div id="sb" style="display:none;margin-top:10px">
      <div class="status" id="st">처리 중...</div>
      <div class="prog-wrap"><div class="prog-bar" id="pb"></div></div>
    </div>

    <div id="fl" style="display:none;margin-top:10px">
      <div class="sec" id="fc"></div>
      <div id="fi2"></div>
    </div>

    <div id="ip" style="display:none;margin-top:14px">
      <div class="ph">
        <div class="sec" style="margin:0">추출된 이미지 <span id="ic" style="color:#3b82f6"></span>개</div>
        <button class="tgl" id="tg" onclick="toggleImg()">접기 ▲</button>
      </div>
      <div id="ig" class="img-grid"></div>
    </div>

    <button class="btn-main" id="gb" disabled>
      <svg width="16" height="16" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
      <span id="gt">문항 생성하기</span>
    </button>
    <div class="stream" id="stream"></div>
  </div>

  <div class="card" id="ec" style="display:none">
    <div class="export-row">
      <button class="btn-s btn-g" onclick="copyAll()">전체 복사</button>
      <button class="btn-s btn-p" onclick="dlTxt()">TXT 다운로드</button>
    </div>
  </div>

  <div id="ql"></div>
</div>

<div class="lbox" id="lb" onclick="closeLb()">
  <img id="li" src="" alt="">
  <div class="lbox-lbl" id="ll"></div>
</div>

<script>
pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';

var MIN_PX = 100;
var imgs = {};
var files = [];
var qs = [];
var dragIdx = null;
var imgVis = true;

document.getElementById('fi').addEventListener('change', function(e) {
  var fs = Array.from(e.target.files).filter(function(f) { return f.type === 'application/pdf'; });
  if (!fs.length) { alert('PDF 파일만 업로드 가능합니다.'); return; }
  files = fs;
  imgs = {};
  qs = [];
  document.getElementById('gb').disabled = true;
  document.getElementById('ip').style.display = 'none';
  document.getElementById('ec').style.display = 'none';
  document.getElementById('ql').innerHTML = '';
  setStatus('PDF 분석 중...', 0);
  processFiles();
});

function toggleImg() {
  imgVis = !imgVis;
  document.getElementById('ig').style.display = imgVis ? '' : 'none';
  document.getElementById('tg').textContent = imgVis ? '접기 ▲' : '펼치기 ▼';
}

function setStatus(txt, pct) {
  document.getElementById('sb').style.display = 'block';
  document.getElementById('st').textContent = txt;
  document.getElementById('pb').style.width = pct + '%';
}

function hideStatus() {
  document.getElementById('pb').style.width = '100%';
  setTimeout(function() { document.getElementById('sb').style.display = 'none'; }, 1000);
}

function baseName(n) { return n.replace(/\.[^/.]+$/, ''); }

function extractUnit(txt) {
  var m = txt.match(/개념유닛\s*코드[^0-9A-Za-z]*([0-9A-Za-z]{5,20})/);
  if (m) return m[1];
  var m2 = txt.match(/\b(\d{2}[A-Z]{2,5}\d{4,6})\b/);
  return m2 ? m2[1] : null;
}

function extractCt(name) {
  var mn = name.match(/_(CT|CI)_(\d+)/i);
  if (mn) return parseInt(mn[2], 10);
  var mt = name.match(/_(CT|CI)/i);
  if (mt) return mt[1].toUpperCase() === 'CT' ? 0 : 1;
  return 999;
}

async function processFiles() {
  try {
    var pages = [];
    var total = 0;
    var done = 0;
    var pdfs = [];

    for (var i = 0; i < files.length; i++) {
      var buf = await files[i].arrayBuffer();
      var pdf = await pdfjsLib.getDocument({ data: buf }).promise;
      pdfs.push({ pdf: pdf, file: files[i] });
      total += pdf.numPages;
    }

    for (var pi = 0; pi < pdfs.length; pi++) {
      var pdf = pdfs[pi].pdf;
      var file = pdfs[pi].file;
      var ct = extractCt(file.name);
      for (var pn = 1; pn <= pdf.numPages; pn++) {
        var page = await pdf.getPage(pn);
        var tc = await page.getTextContent();
        var txt = tc.items.map(function(x) { return x.str; }).join(' ');
        var unit = extractUnit(txt);
        pages.push({ page: page, pageNum: pn, unit: unit, ct: ct, fname: file.name });
        done++;
        setStatus('페이지 분석 중... ' + file.name + ' (' + pn + '/' + pdf.numPages + ')', Math.round(done / total * 50));
      }
    }

    pages.sort(function(a, b) {
      var ua = a.unit || '', ub = b.unit || '';
      if (ua !== ub) return ua.localeCompare(ub);
      return (a.ct || 0) - (b.ct || 0);
    });

    var numMap = {};
    var sortN = 0;
    done = 0;

    for (var gi = 0; gi < pages.length; gi++) {
      var pg = pages[gi];
      setStatus('이미지 추출 중... ' + pg.fname + ' ' + pg.pageNum + '페이지', 50 + Math.round(done / pages.length * 50));
      if (!(pg.fname in numMap)) numMap[pg.fname] = 1;
      var extracted = await extractImgs(pg.page);
      var bn = baseName(pg.fname);
      for (var ei = 0; ei < extracted.length; ei++) {
        var img = extracted[ei];
        var num = numMap[pg.fname]++;
        sortN++;
        var key = bn + ' (' + num + ')';
        imgs[key] = { dataUrl: img.dataUrl, key: key, unit: pg.unit, sortN: sortN, w: img.w, h: img.h, fname: pg.fname, pn: pg.pageNum };
      }
      done++;
    }

    hideStatus();
    renderFiles();
    renderImgPanel();
    document.getElementById('gb').disabled = false;
  } catch(err) {
    hideStatus();
    alert('PDF 처리 오류: ' + err.message);
    console.error(err);
  }
}

async function extractImgs(page) {
  var results = [];
  var ops = await page.getOperatorList();
  var OPS = pdfjsLib.OPS;
  var imgNames = new Set();
  for (var i = 0; i < ops.fnArray.length; i++) {
    var fn = ops.fnArray[i];
    if (fn === OPS.paintImageXObject || fn === OPS.paintJpegXObject) {
      var nm = ops.argsArray[i][0];
      if (nm) imgNames.add(nm);
    }
  }
  for (var name of imgNames) {
    try {
      var imgData = await new Promise(function(res, rej) {
        page.objs.get(name, function(obj) {
          if (obj) res(obj); else rej(new Error('no obj'));
        });
      });
      var w = imgData.width, h = imgData.height;
      if (!w || !h || w < MIN_PX || h < MIN_PX) continue;
      var cv = document.createElement('canvas');
      cv.width = w; cv.height = h;
      var ctx = cv.getContext('2d');
      if (imgData instanceof ImageData) {
        ctx.putImageData(imgData, 0, 0);
      } else if (imgData.data && imgData.data instanceof Uint8ClampedArray) {
        ctx.putImageData(new ImageData(imgData.data, w, h), 0, 0);
      } else if (imgData.bitmap) {
        ctx.drawImage(imgData.bitmap, 0, 0, w, h);
      } else { continue; }
      results.push({ dataUrl: cv.toDataURL('image/jpeg', 0.9), w: w, h: h });
    } catch(e) {}
  }
  results.sort(function(a, b) { return (b.w * b.h) - (a.w * a.h); });
  return results;
}

function renderFiles() {
  document.getElementById('fl').style.display = 'block';
  document.getElementById('fc').textContent = '업로드된 파일 (' + files.length + '개)';
  document.getElementById('fi2').innerHTML = files.map(function(f, i) {
    return '<div class="file-item"><span style="font-size:13px">' + f.name + '</span><button class="rm" onclick="rmFile(' + i + ')">×</button></div>';
  }).join('');
}

function rmFile(i) {
  files.splice(i, 1);
  if (!files.length) {
    imgs = {};
    document.getElementById('fl').style.display = 'none';
    document.getElementById('ip').style.display = 'none';
    document.getElementById('gb').disabled = true;
  } else renderFiles();
}

function renderImgPanel() {
  var entries = Object.entries(imgs).sort(function(a, b) { return a[1].sortN - b[1].sortN; });
  document.getElementById('ic').textContent = entries.length;
  document.getElementById('ig').innerHTML = entries.length
    ? entries.map(function(e) {
        var key = e[0], info = e[1];
        return '<div class="thumb" onclick="openLb(\'' + esc(key) + '\')">' +
          '<img src="' + info.dataUrl + '" alt="' + key + '">' +
          '<div class="thumb-label">' + key + '</div></div>';
      }).join('')
    : '<div style="grid-column:1/-1;color:#94a3b8;text-align:center;padding:20px;font-size:12px">추출된 이미지가 없습니다</div>';
  document.getElementById('ip').style.display = 'block';
}

function esc(k) { return k.replace(/\\/g, '\\\\').replace(/'/g, "\\'"); }

function openLb(key) {
  var info = imgs[key]; if (!info) return;
  document.getElementById('li').src = info.dataUrl;
  document.getElementById('ll').textContent = key + ' · ' + info.w + 'x' + info.h + 'px';
  document.getElementById('lb').style.display = 'flex';
}
function closeLb() { document.getElementById('lb').style.display = 'none'; }

document.getElementById('gb').addEventListener('click', async function() {
  if (!Object.keys(imgs).length) { alert('PDF를 먼저 업로드해주세요.'); return; }
  var btn = document.getElementById('gb');
  var gt = document.getElementById('gt');
  var stream = document.getElementById('stream');
  btn.disabled = true; gt.textContent = '문항 생성 중...';
  stream.style.display = 'block'; stream.textContent = 'AI가 문항을 작성하고 있습니다...';

  try {
    var b64s = await Promise.all(files.map(function(f) {
      return new Promise(function(res, rej) {
        var r = new FileReader();
        r.onload = function() { res(r.result.split(',')[1]); };
        r.onerror = function() { rej(new Error('읽기 실패')); };
        r.readAsDataURL(f);
      });
    }));

    var imgList = Object.entries(imgs)
      .sort(function(a, b) { return a[1].sortN - b[1].sortN; })
      .map(function(e) { return e[0] + ' (' + e[1].w + 'x' + e[1].h + 'px) - ' + e[1].fname + ' ' + e[1].pn + '페이지'; })
      .join('\n');

    var docs = b64s.map(function(d) {
      return { type: 'document', source: { type: 'base64', media_type: 'application/pdf', data: d } };
    });

    var rules = [
      '당신은 초등학교 단원평가 문항 개발 전문가입니다.',
      '제공된 PDF 내용만 사용하여 20개의 단원평가 문항을 작성하세요.',
      'PDF에 없는 내용 사용 금지. 출력 전 모든 규칙 준수 여부를 검토 후 출력할 것.',
      '',
      '[출제 금지]',
      '2지선다(지2), 3지선다(지3), 영역02 출제 금지',
      '잘못 말한 친구 이름을 쓰는 문제 출제 금지',
      '',
      '[메타데이터 형식 - 반드시 두 줄로 작성, 엔터로 분리]',
      '1행: ^^문제유형 / 인지능력 / 개념유닛코드 / 출제비율 / 제2커리큘럼 / 키보드 / 정답 / 범례',
      '2행: L+문제번호두자리-난이도-1',
      '',
      '규칙:',
      '- ^^ 로 시작, 각 항목은 앞뒤 공백 포함 슬래시로 구분',
      '- 빈칸이어도 슬래시 생략 금지. 단원평가는 제2커리큘럼 항상 빈칸',
      '- 제2커리큘럼과 키보드 모두 비면 정답 앞 슬래시 3개',
      '- 인지능력: 4자리 쉼표 구분, 합계 100. 해당없으면 0 쓰지 않되 쉼표 생략 금지',
      '- 난이도: 1=하 2=중 3=상. 단원평가는 학습코너별유형 항상 1',
      '',
      '[문제유형 코드]',
      '지5=5지선다 지4=4지선다 자선=자유선지 단유=단답유순 단무=단답무순 단그=단답그룹',
      '드래00=드래그드롭 영역04=X표시 영역08=O표시 선=선잇기',
      '',
      '[정답 형식]',
      '- 지선다: 해당번호(①②③④⑤)',
      '- 단유/단무: 텍스트 그대로',
      '- 중복정답: 세미콜론 구분 (예: ③ ; ④)',
      '- 영역04/08: 선택지수만큼 ; 로 자리만들고 정답위치에 1',
      '- 선잇기: A:1-B:2 ; A:2-B:1 형식',
      '- 드래그드롭: a:값 , b:값 형식',
      '- 범례있으면 | 로 구분 (예: ㉠|㉡|㉢), 없으면 슬래시 구분기호 생략',
      '',
      '[문항 본문 규칙]',
      '- ~습니다 체 사용',
      '- (문제) 뒤 띄어쓰기 없이 바로 텍스트',
      '- 괄호안에 들어갈 말 지문: 괄호 안 4칸 띄어쓰기',
      '- 선다형 보기: 한줄 띄고 ① ② ③ ④ ⑤ (보기 앞 한 칸 띄기 하지 않음)',
      '- 보기 항목은 길이순으로 짧은 것이 앞 번호에 오도록 정렬',
      '- 사진/그림 있는 선다형: 문제 끝을 ~모습입니다. 로',
      '- 표 있는 선다형: 문제 끝을 ~표입니다. 로',
      '- 보기박스: [보기] 기호 넣고 다음 줄에 텍스트',
      '- (정답) 뒤 띄어쓰기 없이 바로 정답',
      '- (해설) 뒤 줄바꿈 후 해설 텍스트',
      '- PDF에서 실험 페이지와 개념 페이지의 비율을 파악하여 그 비율에 맞게 문항 출제.',
      '  예: 실험 페이지 40% 개념 페이지 60%면 문항도 실험 관련 8문항, 개념 관련 12문항.',
      '  실험 문항: 실험 과정을 보고 결과를 도출하거나 실험 방법을 묻는 문항 포함.',
      '',
      imgList,
      '',
      '[응답 형식 - JSON 배열만, 마크다운 없이]',
      '[{"number":1,"difficulty":"중","metadata":"^^지5 / 100, 20, 60, 20 / 22SCE62013 / 62013, 100 / / / ③ /\\nL01-2-1","content":"(문제)내용\\n\\n ①보기1\\n②보기2\\n③보기3\\n④보기4\\n⑤보기5","imageRefs":[],"answer":"(정답)③","explanation":"(해설)\\n해설내용"}]'
    ].join('\n');

    var body = {
      model: 'claude-sonnet-4-20250514',
      max_tokens: 16000,
      messages: [{ role: 'user', content: docs.concat([{ type: 'text', text: rules }]) }]
    };

    var res = await fetch('https://api.anthropic.com/v1/messages', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(body)
    });

    if (!res.ok) {
      var err = await res.json().catch(function() { return {}; });
      throw new Error((err.error && err.error.message) || ('상태 코드 ' + res.status));
    }

    var data = await res.json();
    var txt = data.content.filter(function(x) { return x.type === 'text'; }).map(function(x) { return x.text; }).join('\n');
    stream.textContent = txt.slice(0, 300) + '...';
    qs = JSON.parse(txt.replace(/```json\n?/g, '').replace(/```\n?/g, '').trim());
    stream.style.display = 'none';
    renderQs();
    document.getElementById('ec').style.display = 'block';

  } catch(err) {
    console.error(err);
    var isOverload = err.message && err.message.toLowerCase().indexOf('overload') !== -1;
    stream.textContent = '오류: ' + err.message + (isOverload ? '\n\n잠시 후 다시 시도해 주세요.' : '');
    if (isOverload) {
      var retryMsg = '서버가 혼잡합니다. 30초 후 자동 재시도합니다...';
      stream.textContent = retryMsg;
      var countdown = 30;
      var timer = setInterval(function() {
        countdown--;
        if (countdown <= 0) {
          clearInterval(timer);
          stream.textContent = '재시도 중...';
          document.getElementById('gb').click();
        } else {
          stream.textContent = '서버가 혼잡합니다. ' + countdown + '초 후 자동 재시도합니다...';
        }
      }, 1000);
    } else {
      alert('문항 생성 오류: ' + err.message);
    }
  } finally {
    btn.disabled = false; gt.textContent = '문항 생성하기';
  }
});

function renderQs() {
  document.getElementById('ql').innerHTML = qs.map(function(q, i) {
    var refs = q.imageRefs || [];
    var imgHtml = refs.length ? '<div class="q-imgs">' + refs.map(function(key) {
      var info = imgs[key];
      return info
        ? '<div class="q-img" onclick="openLb(\'' + esc(key) + '\')">' +
          '<img src="' + info.dataUrl + '" alt="' + key + '">' +
          '<div class="q-img-lbl">' + key + '</div></div>'
        : '<span style="font-size:12px;color:#ef4444;background:#fee2e2;padding:4px 8px;border-radius:6px">' + key + ': 없음</span>';
    }).join('') + '</div>' : '';

    return '<div class="q-card" draggable="true" data-index="' + i + '">' +
      '<div class="q-top">' +
      '<div class="q-num"><span style="color:#cbd5e1;font-size:12px">⠿</span>' + q.number + '번' +
      '<span class="badge ' + (q.difficulty === '상' ? 'bh' : q.difficulty === '하' ? 'be' : 'bm') + '">' + q.difficulty + '</span></div>' +
      '<button class="edit-btn" onclick="editQ(' + i + ')">✏ 수정</button></div>' +
      (q.metadata ? '<div class="q-meta">' + q.metadata + '</div>' : '') +
      '<div class="q-content">' + q.content + '</div>' +
      imgHtml +
      '<div class="q-ans"><div class="q-ans-txt">' + q.answer + '</div>' +
      '<div class="q-expl">' + q.explanation + '</div></div></div>';
  }).join('');
  setupDrag();
}

function editQ(i) {
  var q = qs[i];
  var txt = q.content + '\n\n' + q.answer + '\n' + q.explanation;
  var nw = prompt('문항을 수정하세요:', txt);
  if (!nw || nw === txt) return;
  var lines = nw.split('\n');
  var content = [], answer = [], expl = [], sec = 'content';
  for (var li = 0; li < lines.length; li++) {
    var l = lines[li];
    if (l.startsWith('(정답)')) { sec = 'answer'; answer.push(l); }
    else if (l.startsWith('(해설)')) { sec = 'expl'; expl.push(l); }
    else if (sec === 'content') content.push(l);
    else if (sec === 'answer') answer.push(l);
    else expl.push(l);
  }
  qs[i] = Object.assign({}, q, { content: content.join('\n').trim(), answer: answer.join('\n').trim(), explanation: expl.join('\n').trim() });
  renderQs();
}

function setupDrag() {
  document.querySelectorAll('[draggable="true"]').forEach(function(el) {
    el.addEventListener('dragstart', function(e) { dragIdx = +e.currentTarget.dataset.index; e.currentTarget.classList.add('dragging'); });
    el.addEventListener('dragover', function(e) { e.preventDefault(); e.currentTarget.classList.add('drag-over'); });
    el.addEventListener('dragleave', function(e) { e.currentTarget.classList.remove('drag-over'); });
    el.addEventListener('drop', function(e) {
      e.preventDefault(); e.currentTarget.classList.remove('drag-over');
      var di = +e.currentTarget.dataset.index;
      if (dragIdx !== di) {
        var it = qs.splice(dragIdx, 1)[0];
        qs.splice(di, 0, it);
        qs.forEach(function(q, i) { q.number = i + 1; });
        renderQs();
      }
    });
    el.addEventListener('dragend', function(e) {
      e.currentTarget.classList.remove('dragging');
      document.querySelectorAll('[draggable]').forEach(function(x) { x.classList.remove('drag-over'); });
    });
  });
}

function copyAll() {
  var txt = qs.map(function(q) { return q.metadata + '\n' + q.content + '\n\n' + q.answer + '\n' + q.explanation; }).join('\n\n---\n\n');
  navigator.clipboard.writeText(txt).then(function() { alert('복사되었습니다.'); });
}

function dlTxt() {
  var txt = qs.map(function(q) { return q.metadata + '\n' + q.content + '\n\n' + q.answer + '\n' + q.explanation; }).join('\n\n---\n\n');
  var a = document.createElement('a');
  a.href = URL.createObjectURL(new Blob([txt], { type: 'text/plain;charset=utf-8' }));
  a.download = '단원평가_문항.txt';
  a.click();
  URL.revokeObjectURL(a.href);
}
</script>
</body>
</html>
