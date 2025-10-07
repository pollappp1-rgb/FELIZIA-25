# FELIZIA-25

<html lang="en"> 

<head> 

<meta charset="utf-8" /> 

<meta name="viewport" content="width=device-width, initial-scale=1" /> 

<title>Escrita 4.0 – Digital System</title> 

<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

<style> 

  :root { 
    /* Modern-Traditional Palette: Deep Teal/Emerald + Rich Gold Accent + Warm White */ 
    --bg: #fdfdfd; /* Near-white, slightly warm background */ 
    --panel: #ffffff; 
    --card: #ffffff; 
    --border: #e6e9ee; /* Very light, cool border */ 
    --light: #153448; /* Deep Midnight Blue/Navy for main text */ 
    --muted: #5e7786; /* Slate Gray/Blue for secondary text */ 
    --accent: #047857; /* Rich Emerald/Deep Teal primary accent (Traditional) */ 
    --accent-2: #d97706; /* Deep Marigold Gold secondary accent (Traditional) */ 
    --shadow: rgba(21, 52, 72, 0.08); /* Deep, soft shadow */ 
    --hover-bg: #f9f9fa; 
    --radius: 14px; /* Slightly rounded corners */

    /* Traditional Font for Headings/Titles */
    --font-heading: 'Cormorant Garamond', serif;
    /* Modern Font for Body/UI */
    --font-body: 'Inter', sans-serif;
  } 
  * { box-sizing: border-box; } 
  html, body { 
    margin: 0; padding: 0; 
    /* Subtle geometric/marble pattern effect for depth */
    background: radial-gradient(circle at 80% 10%, rgba(4, 120, 87, 0.05), transparent), 
                radial-gradient(circle at 10% 90%, rgba(217, 119, 6, 0.05), transparent),
                var(--bg); 
    color: var(--light); 
    font-family: var(--font-body); 
    line-height: 1.6;
  } 
  
  /* --- Header & Branding --- */
  header { 
    position: sticky; top: 0; z-index: 10; 
    padding: 18px 28px; border-bottom: 1px solid var(--border); 
    background: rgba(255,255,255,0.95); /* Opaque white for elegance */
    backdrop-filter: blur(8px); 
    box-shadow: 0 6px 15px var(--shadow); /* Elegant, elevated shadow */
  } 
  #app { max-width: 1200px; margin: 0 auto; padding: 30px 20px; } 
  .brand { display: flex; align-items: center; gap: 18px; } 
  .logo { 
    width: 48px; height: 48px; border-radius: 50%; /* Circular logo for classic feel */
    display: grid; place-items: center; font-weight: 700; color: #fff; 
    background: linear-gradient(135deg, var(--accent), #059669); /* Richer gradient */
    box-shadow: 0 0 0 2px var(--accent-2) inset, 0 4px 12px rgba(4, 120, 87, 0.4); /* Dual border/shadow effect */
  } 
  .brand h1 { 
    margin: 0; font-size: 24px; font-weight: 600; 
    font-family: var(--font-heading); /* Serif for the main title */
  } 
  .sub { font-size: 14px; color: var(--muted); } 
  .row { display: flex; gap: 12px; align-items: center; flex-wrap: wrap; } 
  .spacer { flex: 1; } 

  /* --- Cards and Layout --- */
  .card { 
    background: var(--card); 
    border: 1px solid var(--border); 
    border-radius: var(--radius); 
    padding: 25px; 
    box-shadow: 0 10px 30px var(--shadow); 
    transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out; 
  } 
  .card:hover { 
    transform: translateY(-2px); 
    box-shadow: 0 18px 40px rgba(21, 52, 72, 0.15); /* More prominent hover effect */
  }
  .card h2 { 
    margin: 0 0 12px 0; font-size: 22px; font-weight: 700; 
    font-family: var(--font-heading); /* Serif for section titles */
  } 
  .card h2::after { 
    content: ""; display: block; height: 2px; margin-top: 10px; 
    background: linear-gradient(to right, var(--accent), var(--accent-2), transparent); 
    opacity: 0.7;
    border-radius: 1px; 
    width: 80px; 
  } 
  .section-title { font-size: 18px; margin: 15px 0; font-weight: 600; font-family: var(--font-heading); } 
  .muted { color: var(--muted); font-size: 15px; } 
  .grid { display: grid; gap: 25px; } 
  .grid.cols-2 { grid-template-columns: repeat(2, 1fr); } 
  .grid.cols-3 { grid-template-columns: repeat(3, 1fr); } 
  @media (max-width: 900px) { .grid.cols-2, .grid.cols-3 { grid-template-columns: 1fr; } } 

  /* --- Buttons --- */
  .btn { 
    display: inline-flex; align-items: center; justify-content: center; gap: 8px; 
    padding: 10px 18px; border-radius: 10px; cursor: pointer; 
    background: #fff; color: var(--light); 
    border: 1px solid var(--border); text-decoration: none; font-weight: 600; 
    transition: all 0.2s; 
    box-shadow: 0 2px 4px rgba(0,0,0,0.03);
  } 
  .btn:hover { 
    background: var(--hover-bg); 
    border-color: var(--muted); 
    box-shadow: 0 4px 10px rgba(0,0,0,0.05); 
    transform: translateY(-1px);
  } 
  .btn.primary { 
    background: var(--accent); 
    color: #ffffff; 
    border: 1px solid #046849; 
  } 
  .btn.primary:hover { 
    background: #059669; 
    box-shadow: 0 4px 15px rgba(4, 120, 87, 0.4); 
  }
  .btn.warn { background: #fef9e7; color: #92400e; border-color: #fcd34d; } 
  .btn.danger { background: #fef2f2; color: #b91c1c; border-color: #fca5a5; } 
  .btn.small { padding: 8px 14px; font-size: 14px; border-radius: 8px; } 

  /* --- Tags/Badges --- */
  .tag { 
    padding: 6px 14px; border-radius: 999px; font-size: 13px; font-weight: 600;
    border: 1px solid var(--border); background: #f5f8fa; color: var(--light); 
  } 
  .tag.green { background: #ecfdf5; color: #065f46; border-color: #a7f3d0; } /* Darker green for contrast */
  .tag.blue { background: #eff6ff; color: #1e40af; border-color: #bfdbfe; } 
  .tag.red { background: #fef2f2; color: #b91c1c; border-color: #fecaca; } 
  .tag.gold { background: #fffbe3; color: #a16207; border-color: #fcd34d; } /* New Gold tag for special emphasis */

  /* --- Navigation & Tabs --- */
  .nav { display: flex; gap: 15px; flex-wrap: wrap; margin: 10px 0 20px; border-bottom: 2px solid var(--border); padding-bottom: 0;} 
  .nav .tab { 
    padding: 12px 20px; background: transparent; border: none; 
    color: var(--muted); cursor: pointer; 
    font-weight: 500; transition: all 0.2s;
    border-bottom: 3px solid transparent;
  } 
  .nav .tab:hover { 
    color: var(--accent); 
  }
  .nav .tab.active { 
    color: var(--accent); 
    border-bottom: 3px solid var(--accent); 
    font-weight: 600;
  } 

  /* --- Forms and Inputs --- */
  .hr { height: 1px; background: var(--border); margin: 20px 0; } 
  .input, select, textarea { 
    width: 100%; padding: 12px 14px; 
    background: #fff; color: var(--light); 
    border: 1px solid var(--border); border-radius: 8px; 
    transition: border-color 0.2s, box-shadow 0.2s;
  } 
  .input:focus, select:focus, textarea:focus { 
    border-color: var(--accent); 
    outline: none; 
    box-shadow: 0 0 0 3px rgba(4, 120, 87, 0.15); /* Soft, colored focus ring */
  }
  label { display: block; margin-bottom: 6px; font-size: 14px; font-weight: 600; color: var(--light); }

  /* --- Tables --- */
  .table-wrap { 
    width: 100%; overflow: auto; 
    border: 1px solid var(--border); border-radius: 12px; 
    box-shadow: 0 6px 15px var(--shadow);
  } 
  table { width: 100%; border-collapse: collapse; min-width: 850px; } 
  th, td { padding: 14px 18px; border-bottom: 1px solid var(--border); text-align: left; font-size: 15px; } 
  th { 
    background: #f8f9fb; 
    color: var(--muted); 
    font-weight: 600; 
    text-transform: uppercase; 
    font-size: 12px;
    letter-spacing: 0.5px;
    position: sticky; top: 0; z-index: 1; 
  } 
  tr:last-child td { border-bottom: none; }
  tbody tr:hover { background-color: var(--hover-bg); }

  /* --- Global Search --- */ 
  .gs-wrap { position: relative; min-width: 320px; max-width: 500px; width: 45%; } 
  .gs-input { padding-left: 42px !important; } 
  .gs-icon { 
    position: absolute; left: 14px; top: 50%; transform: translateY(-50%); 
    font-size: 20px; color: var(--muted); 
  } 
  .gs-results { 
    position: absolute; top: calc(100% + 10px); left: 0; right: 0; 
    background: #ffffff; border: 1px solid var(--border); border-radius: var(--radius); 
    box-shadow: 0 15px 40px rgba(14, 25, 45, 0.2); max-height: 450px; overflow: auto; z-index: 20; 
  } 
  .gs-section { padding: 12px 18px; font-size: 13px; color: var(--muted); background: #fefefe; border-bottom: 1px solid var(--border); font-weight: 600; position: sticky; top: 0; } 
  .gs-item { 
    padding: 14px 18px; cursor: pointer; display: grid; grid-template-columns: 30px 1fr; gap: 12px; 
  } 
  .gs-item:hover, .gs-item.active { background: var(--hover-bg); } 
  .gs-type { width: 30px; color: var(--accent); text-align: center; font-size: 18px; } 
  .gs-title { font-weight: 600; color: var(--light); } 
  .gs-sub { font-size: 13px; color: var(--muted); } 
  @media (max-width: 800px) { .gs-wrap { width: 100%; max-width: none; } } 

  /* --- Judge Panel Nav (Two Bars) --- */
  .jp-nav { display: flex; gap: 15px; margin-bottom: 25px; border-bottom: 2px solid var(--border); padding-bottom: 0; }
  .jp-nav .jp-tab {
    padding: 10px 16px; border-radius: 10px 10px 0 0; cursor: pointer; font-weight: 600;
    transition: all 0.2s; border: none;
    border-bottom: 3px solid transparent;
    color: var(--muted);
    background: transparent;
  }
  .jp-nav .jp-tab.active {
    border-bottom: 3px solid var(--accent);
    color: var(--accent);
  }
  .jp-nav .jp-tab:hover {
    color: var(--accent-2);
  }
  
  /* --- Highlighting --- */
  .card.search-highlight { 
    box-shadow: 0 0 0 3px var(--accent-2) inset, 0 15px 35px rgba(217, 119, 6, 0.2) !important; 
    border-color: var(--accent-2) !important;
  } 
  tr.search-highlight { 
    background-color: #fffbeb !important; 
    box-shadow: 0 0 0 2px var(--accent-2) inset !important; 
  }

</style> 

</head> 
<body> 
<header> 
  <div class="brand"> 
    <div class="logo" id="brand-logo">ES</div> 
    <div> 
      <h1 id="header-event-title">Escrita 4.0</h1> 
      <div class="sub" id="header-org-name">Rabath Eduvalley Students' Association • Event Crew + Team Portal</div> 
    </div> 

    <div id="global-search-wrap" class="gs-wrap"> 
      <span class="gs-icon">🔍</span> 
      <input id="global-search-input" class="input gs-input" type="search" 
             placeholder="Search students or competitions ( / )" 
             oninput="App.onGlobalSearchInput(this.value)" 
             onfocus="App.onGlobalSearchFocus()" 
             onkeydown="App.onGlobalSearchKey(event)"> 
      <div id="global-search-results" class="gs-results" style="display:none"></div> 
    </div> 

    <div class="spacer"></div> 
    <div id="header-session" class="row"></div> 
  </div> 
</header> 
<div id="app"></div> 

 
<script> 
"use strict"; 
 
/* ------------------------------ 
    Data Store 
--------------------------------*/ 
const Store = { 
  key: "escrita40Data.v5", // Bumped version key for the new project
  defaults: () => ({ 
    meta: { createdAt: Date.now(), version: 5 }, 
    // Updated Event Info
    eventInfo: { eventTitle: "Escrita 4.0", orgName: "Rabath Eduvalley Students' Association" }, 
    brand: { 
        // Updated default colors for the new theme
        logoDataUrl: null, 
        faviconDataUrl: null, 
        accent: "#047857", // Deep Emerald
        accent2: "#d97706" // Rich Gold
    }, 
    eventUser: { username: "admin", password: "escrita" }, // New default admin password
    portalLocked: false, 
    // Only "General" is mandatory and permanent
    categories: ["General"], 
    teams: [], // Initial teams removed
    competitions: [], 
    students: [], 
    entries: [], 
    attendance: [], 
    results: [], 
    adjustments: [], 
    posters: { templates: [] }, 
    chest: { templates: [] } 
  }), 
  load() { 
    try { 
      const raw = localStorage.getItem(this.key); 
      if (!raw) { 
        const base = this.defaults(); 
        localStorage.setItem(this.key, JSON.stringify(base)); 
        return base; 
      } 
      const data = JSON.parse(raw); 

      // Data migration and initialization for v5
      if (!data.posters) data.posters = { templates: [] }; 
      if (!data.chest) data.chest = { templates: [] }; 
      if (!data.brand) data.brand = Store.defaults().brand; 
      
      // Ensure "General" exists and is the first element for v5
      if (Array.isArray(data.categories)) { 
        data.categories = data.categories.filter(c => c !== "General"); // Remove any existing General
        data.categories = ["General", ...data.categories]; // General must be first
      } else { 
        data.categories = this.defaults().categories; 
      } 

      data.meta.version = 5; // Update version
      return data; 
    } catch (e) { 
      console.error("Load failed", e); 
      const base = this.defaults(); 
      localStorage.setItem(this.key, JSON.stringify(base)); 
      return base; 
    } 
  }, 
  save(data) { localStorage.setItem(this.key, JSON.stringify(data)); }, 
  clear() { localStorage.removeItem(this.key); } 
}; 
 
/* ------------------------------ 
    App 
--------------------------------*/ 
const App = { 
  state: { 
    role: null, teamId: null, user: null, 
    eventTab: "setup", 
    teamTab: "dashboard", 
    posterTab: "generate", 
    posterSelectedTemplateId: null, 
    posterEditorTemplateId: null, 
    posterEditorSelectedFieldId: null, 
    ebcTeamFilter: "", 
    chestTab: "generate", 
    chestEditorTemplateId: null, 
    chestEditorSelectedFieldId: null, 

    // Judge Panel State
    judgePanelCompId: null, 
    judgePanelTab: "attendance", // New state for Judge Panel

    // Search state 
    searchOpen: false, 
    searchQuery: "", 
    _gsTimer: null, 
    _gsResults: [], 
    _gsActiveIndex: -1, 
    _highlightCompId: null, 

    // Champions options 
    champIncludeGroup: false, 
    champIncludePopularToStudentCat: false, 
    champTopN: 1 
  }, 
  data: Store.load(), 

  // Utils (omitted for brevity, assume all utils from previous version are here)
  save() { 
    Store.save(this.data); 
    this.renderHeaderSession(); 
    this.applyBrand(); 
    this.updateHeaderInfo(); 
  },
  reset() { 
    if (!confirm("Are you sure you want to reset ALL application data? This cannot be undone.")) return;
    this.data = Store.defaults(); 
    this.save(); 
    this.routeHome(); 
    alert("Data cleared. Application reset to default.");
  }, 
  uid(p="id") { return p + "-" + Math.random().toString(36).slice(2,9) + Date.now().toString(36).slice(-4); }, 
  fmtDate(d) { if (!d) return ""; try { return new Date(d).toLocaleDateString(); } catch { return d; } }, 
  todayStr() { const d = new Date(); return d.toISOString().slice(0,10); }, 
  esc(s) { return String(s ?? "").replace(/[&<>"']/g, m => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;', "'":'&#39;'}[m])); }, 
  sanitizeFileName(s){ return String(s).replace(/[<>:"/\\|?*\x00-\x1F]/g,"_").slice(0,120); }, 
  fileToDataUrl(file){ return new Promise((res,rej)=>{ const r=new FileReader(); r.onload=()=>res(r.result); r.onerror=rej; r.readAsDataURL(file); }); }, 
  loadImage(src){ return new Promise((res,rej)=>{ const i=new Image(); i.onload=()=>res(i); i.onerror=rej; i.src=src; }); }, 
  wrapText(ctx, text, maxWidth){ 
    if (!maxWidth) return String(text||"").split("\n"); 
    const paras = String(text||"").split("\n"); 
    const out = []; 
    for (const p of paras) { 
      const words = p.split(" "); 
      let line = ""; 
      for (const w of words) { 
        const test = line ? line + " " + w : w; 
        if (ctx.measureText(test).width > maxWidth && line) { 
          out.push(line); line = w; 
        } else { 
          line = test; 
        } 
      } 
      out.push(line); 
    } 
    return out; 
  }, 
  replaceTokens(str, tokens, uppercase=false){ 
    let out = String(str||"").replace(/\{([a-zA-Z0-9_]+)\}/g, (m, k) => tokens[k] ?? ""); 
    return uppercase ? out.toUpperCase() : out; 
  }, 
  async drawWrappedText(ctx, text, cfg){ 
    ctx.save(); 
    ctx.fillStyle = cfg.color || "#000"; 
    ctx.font = `${cfg.fontStyle||""} ${cfg.fontWeight||""} ${cfg.fontSize||24}px ${cfg.fontFamily||"Arial"}`.trim(); 
    ctx.textBaseline = "top"; 
    const lines = this.wrapText(ctx, text, cfg.maxWidth || 400); 
    let x = cfg.x, y = cfg.y; 
    for (const ln of lines) { 
      let drawX = x; 
      if (cfg.align === "center") { ctx.textAlign = "center"; drawX = x + (cfg.maxWidth||400)/2; } 
      else if (cfg.align === "right") { ctx.textAlign = "right"; drawX = x + (cfg.maxWidth||400); } 
      else { ctx.textAlign = "left"; } 
      if (cfg.strokeWidth && cfg.strokeWidth > 0) { ctx.lineWidth = cfg.strokeWidth; ctx.strokeStyle = cfg.strokeColor || "#000"; ctx.strokeText(ln, drawX, y); } 
      if (cfg.shadowBlur) { ctx.shadowBlur = cfg.shadowBlur; ctx.shadowColor = cfg.shadowColor || "#000"; } 
      ctx.fillText(ln, drawX, y); 
      y += Math.round((cfg.fontSize || 24) * (cfg.lineHeight || 1.25)); 
    } 
    ctx.restore(); 
  }, 
  downloadJSON(filename, data) {
    const blob = new Blob([JSON.stringify(data, null, 2)], { type: 'application/json' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = filename;
    document.body.appendChild(a);
    a.click();
    document.body.removeChild(a);
    URL.revokeObjectURL(url);
  },
  
  // Entities (omitted for brevity, assume all entity getters are here)
  getTeam(id){ return this.data.teams.find(t=>t.id===id); } 
  ,getCompetition(id){ return this.data.competitions.find(c=>c.id===id); } 
  ,getEntry(id){ return this.data.entries.find(e=>e.id===id); } 
  ,getStudent(id){ return this.data.students.find(s=>s.id===id); } 
  ,teamName(id){ const t=this.getTeam(id); return t? t.name : id; } 

  ,studentsByTeam(teamId){ return this.data.students.filter(s=>s.teamId===teamId); } 
  ,entriesByCompetition(compId){ return this.data.entries.filter(e=>e.competitionId===compId); } 
  ,entriesByTeam(teamId){ return this.data.entries.filter(e=>e.teamId===teamId); } 
  ,entriesByStudent(stuId){ return this.data.entries.filter(e=> e.memberStudentIds.includes(stuId)); } 

  ,attendanceByComp(compId){ return this.data.attendance.filter(a=>a.competitionId===compId); } 
  ,attendanceRecMapByComp(compId){ const m={}; for(const a of this.data.attendance) if(a.competitionId===compId) m[a.entryId]=a; return m; } 

  ,entryLabel(entry){ 
    const ms = entry.memberStudentIds.map(id=>this.getStudent(id)).filter(Boolean); 
    const label = ms.map(m=> `${m.name} (#${m.chestNo})`).join(", "); 
    return entry.entryType==="group" ? `Group: ${label}` : label; 
  }, 

  // Scoring (omitted for brevity, assume all scoring logic is here)
  computeScores(){ 
    const cats = this.data.categories, teams = this.data.teams; 
    const teamCatScores = {}, competitorPoints = {}; 
    teams.forEach(t => { 
      teamCatScores[t.id] = {}; 
      // Initialize scores for all categories
      cats.forEach(c => teamCatScores[t.id][c] = 0); 
    }); 
    
    for (const r of this.data.results) { 
      const e = this.getEntry(r.entryId); if (!e) continue; 
      const c = this.getCompetition(r.competitionId); if (!c) continue; 
      
      const points = Number(r.pointsAwarded||0);
      
      // Points for the competition's specific category
      if (c.category !== "General") { 
          teamCatScores[e.teamId][c.category] = (teamCatScores[e.teamId][c.category]||0) + points; 
      }
      
      // Points for the permanent 'General' category (all points count towards general)
      teamCatScores[e.teamId]["General"] = (teamCatScores[e.teamId]["General"]||0) + points; 
      
      for (const sid of e.memberStudentIds) competitorPoints[sid] = (competitorPoints[sid]||0) + points; 
    } 
    
    const perCategoryTeam = {}; 
    for (const cat of cats) { 
      perCategoryTeam[cat] = teams.map(t => ({ teamId:t.id, teamName:t.name, points: teamCatScores[t.id][cat]||0 })) 
        .sort((a,b)=> b.points - a.points || a.teamName.localeCompare(b.teamName)); 
    } 
    
    const overallTeam = teams.map(t => { 
      // Overall is the score of the 'General' category
      const total = teamCatScores[t.id]["General"] || 0; 
      return { teamId: t.id, teamName: t.name, points: total }; 
    }).sort((a,b)=> b.points - a.points || a.teamName.localeCompare(b.teamName)); 
    
    return { perCategoryTeam, overallTeam, competitorPoints }; 
  }, 

  // Branding 
  applyBrand(){ 
    const b = this.data.brand || {}; 
    document.documentElement.style.setProperty('--accent', b.accent || '#047857'); 
    document.documentElement.style.setProperty('--accent-2', b.accent2 || '#d97706'); 
    const el = document.getElementById('brand-logo'); 
    if (el) { 
      if (b.logoDataUrl) { 
        el.innerHTML = `<img src="${b.logoDataUrl}" alt="logo" style="width:100%;height:100%;object-fit:cover">`; 
        el.style.background = "transparent"; 
      } else { 
        el.textContent = "ES"; // Updated initials
        el.style.background = `linear-gradient(135deg, ${b.accent||'#047857'}, ${b.accent2||'#d97706'})`; 
      } 
    } 
    // favicon
    let link = document.getElementById("app-favicon"); 
    if (!link) { link = document.createElement("link"); link.id = "app-favicon"; link.rel = "icon"; document.head.appendChild(link); } 
    link.href = b.faviconDataUrl || 'data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 64 64"><rect width="64" height="64" rx="12" fill="%23047857"/><text x="32" y="40" text-anchor="middle" font-size="32" fill="%23ffffff" font-family="Arial">E</text></svg>'; 
  }, 
  
  // Header Info Update
  updateHeaderInfo() {
    const info = this.data.eventInfo;
    const titleEl = document.getElementById("header-event-title");
    const orgEl = document.getElementById("header-org-name");
    const docTitle = document.querySelector("title");

    if (titleEl) titleEl.textContent = info.eventTitle;
    if (orgEl) orgEl.innerHTML = `${info.orgName} • Event Crew + Team Portal`;
    if (docTitle) docTitle.textContent = `${info.eventTitle} – Digital System`;
  },

  // Session/Header 
  renderHeaderSession(){ 
    const el = document.getElementById("header-session"); 
    if (!el) return; 
    if (this.state.role === "event") { 
      el.innerHTML = `<span class="tag green">Event Crew</span><span class="muted">Signed in as ${this.esc(this.state.user||"admin")}</span><button class="btn small" onclick="App.logout()">Logout</button>`; 
    } else if (this.state.role === "team") { 
      const team = this.getTeam(this.state.teamId); 
      el.innerHTML = `<span class="tag green">Team Portal</span><span class="muted">Team ${this.esc(team?.name||"")}</span><button class="btn small" onclick="App.logout()">Logout</button>`; 
    } else { 
      el.innerHTML = `<span class="muted">Not signed in</span>`; 
    } 
  }, 
  logout(){ this.state = { ...this.state, role: null, teamId: null, user: null, eventTab: "setup", teamTab: "dashboard" }; this.renderHeaderSession(); this.routeHome(); }, 

  // Routing (omitted for brevity, assume all routing is here)
  routeHome(){ 
    this.updateHeaderInfo(); 
    const app = document.getElementById("app"); 
    app.innerHTML = ` 
      <div class="grid cols-2"> 
        <div class="card"> 
          <h2>Event Crew Portal</h2> 
          <div class="muted">Manage competitions, attendance (with code letters), results (points), posters, chest cards, and scoreboards.</div> 
          <div class="hr"></div> 
          <form onsubmit="App.eventLoginSubmit(event)"> 
            <div class="grid" style="grid-template-columns: 1fr 1fr 120px; align-items: flex-end;"> 
              <div><label>Username</label><input class="input" id="event-username" value="admin" required></div> 
              <div><label>Password</label><input class="input" id="event-password" type="password" required></div> 
              <button class="btn primary" type="submit">Login</button>
            </div> 
            <div class="muted" style="margin-top:10px;">Default: admin / escrita</div> 
          </form> 
        </div> 
        <div class="card"> 
          <h2>Team Portal</h2> 
          <div class="muted">Register students and enroll them into competitions. View-only when locked.</div> 
          <div class="hr"></div> 
          <form onsubmit="App.teamLoginSubmit(event)"> 
            <div class="grid" style="grid-template-columns: 1fr 1fr 120px; align-items: flex-end;"> 
              <div> 
                <label>Team</label> 
                <select id="team-select" class="input">${this.data.teams.map(t=>`<option value="${t.id}">${this.esc(t.name)}</option>`).join("") || '<option value="" disabled>No teams added</option>'}</select> 
              </div> 
              <div><label>Password</label><input class="input" id="team-password" type="password" required></div> 
              <button class="btn primary" type="submit">Login</button>
            </div> 
          </form> 
        </div> 
      </div> 
      <div class="card" style="margin-top:25px;"> 
        <h2>How it works</h2> 
        <ul class="muted" style="list-style: disc; padding-left: 20px;"> 
          <li>Competitions are categorized. The **General** category is for all students and is used for overall scoring.</li>
          <li>Teams add students (Chest No, Name, Category) and enroll them. Entries are private to teams.</li> 
          <li>Attendance tick + Code Letter. Codes show in Judge Panel and Posters.</li> 
          <li>Judge Panel: enter winners/points/marks; auto poster generator with your templates.</li> 
          <li>Chest Cards: upload category templates; generate per-student PNGs or A4 sheets.</li> 
        </ul> 
      </div> 
    `; 
    this.applyBrand(); 
  }, 
  eventLoginSubmit(ev){ 
    ev.preventDefault(); 
    const u = document.getElementById("event-username").value.trim(); 
    const p = document.getElementById("event-password").value.trim(); 
    const creds = this.data.eventUser; 
    if (u === creds.username && p === creds.password) { this.state.role = "event"; this.state.user = u; this.renderHeaderSession(); this.renderEventPortal(); } 
    else alert("Invalid credentials."); 
  }, 
  teamLoginSubmit(ev){ 
    ev.preventDefault(); 
    const id = document.getElementById("team-select").value; 
    if (!id) return alert("Please select a team."); 
    const p = document.getElementById("team-password").value.trim(); 
    const t = this.getTeam(id); 
    if (!t) return alert("Team not found."); 
    if (p === t.password) { this.state.role = "team"; this.state.teamId = id; this.state.user = t.name; this.renderHeaderSession(); this.renderTeamPortal(); } 
    else alert("Invalid team password."); 
  }, 

  /* ------------------------------ 
      Event Crew Portal (omitted for brevity, assume all tab logic is here)
  --------------------------------*/ 
  renderEventPortal(){ 
    const app = document.getElementById("app"); 
    const tabs = [ 
      { id: "setup", label: "Setup" }, 
      { id: "competitions", label: "Competitions" }, 
      { id: "judge_panel", label: "Judge Panel" }, // Renamed tab
      { id: "entries_by_category", label: "Entries" }, 
      { id: "students_by_category", label: "Students" }, 
      { id: "scoreboards", label: "Scoreboards" }, 
      { id: "posters", label: "Posters" }, 
      { id: "chest_cards", label: "Chest Cards" }, 
      { id: "data", label: "Data" } 
    ]; 
    app.innerHTML = ` 
      <div class="card" style="padding: 16px;"> 
        <div class="nav"> 
          ${tabs.map(t=>`<button class="tab ${this.state.eventTab===t.id?'active':''}" onclick="App.eventSwitchTab('${t.id}')">${t.label}</button>`).join("")} 
        </div> 
        <div id="event-tab" style="padding: 10px 0;"></div> 
      </div> 
    `; 
    this.renderEventTab(); 
  }, 
  eventSwitchTab(id){ this.state.eventTab = id; this.renderEventPortal(); }, 
  renderEventTab(){ 
    const wrap = document.getElementById("event-tab"); if (!wrap) return; 
    if (this.state.eventTab === "setup") return this.eventTabSetup(wrap); 
    if (this.state.eventTab === "competitions") return this.eventTabCompetitions(wrap); 
    if (this.state.eventTab === "judge_panel") return this.eventTabJudgePanel(wrap); 
    if (this.state.eventTab === "entries_by_category") return this.eventTabEntriesByCategory(wrap); 
    if (this.state.eventTab === "students_by_category") return this.eventTabStudentsByCategory(wrap); 
    if (this.state.eventTab === "scoreboards") return this.eventTabScoreboards(wrap); 
    if (this.state.eventTab === "posters") return this.eventTabPosters(wrap); 
    if (this.state.eventTab === "chest_cards") return this.eventTabChestCards(wrap); 
    if (this.state.eventTab === "data") return this.eventTabData(wrap); 
  }, 

  // ... (All other eventTab* functions for content rendering are the same)
  eventTabJudgePanel(wrap){ // New function name
    const comps = this.data.competitions.slice().sort((a,b)=> (a.category||"").localeCompare(b.category||"") || (a.date||"").localeCompare(b.date||"") || a.name.localeCompare(b.name)); 
    wrap.innerHTML = ` 
      <div class="row" style="margin-bottom:8px;"><h2 class="section-title">Judge Panel: Select Competition (${comps.length})</h2></div> 
      <div class="grid cols-3"> 
        ${comps.map(c=>{ 
          const entries = this.entriesByCompetition(c.id); 
          const results = this.data.results.filter(r=>r.competitionId===c.id); 
          const attendance = this.data.attendance.filter(a=>a.competitionId===c.id); 
          return `<div class="card" ${this.state._highlightCompId===c.id?'id="highlight-'+c.id+'" class="search-highlight"':''}> 
            <div class="row"> 
              <span class="tag gold">${this.esc(c.category)}</span>
              ${c.locked?'<span class="tag red">Locked</span>':''}
              <div class="spacer"></div>
              <span class="muted">${c.date?this.fmtDate(c.date):'-'} ${c.time||''}</span>
            </div> 
            <h3>${this.esc(c.name)}</h3> 
            <div class="row" style="margin-bottom:10px;"> 
              <span class="tag blue">${entries.length} Entries</span> 
              <span class="tag green">${results.length} Results</span> 
              <span class="tag">${attendance.filter(a=>a.present).length} Present</span>
            </div>
            <button class="btn primary" onclick="App.renderJudgePanel('${c.id}')">Open Judge Panel</button>
          </div>`; 
        }).join("") || '<div class="muted">No competitions yet.</div>'} 
      </div> 
    `; 
    // Clear highlight after rendering
    if (this.state._highlightCompId) {
        setTimeout(() => {
            const el = document.getElementById('highlight-' + this.state._highlightCompId);
            if (el) el.classList.remove('search-highlight');
            this.state._highlightCompId = null;
        }, 100);
    }
  }, 
  renderJudgePanel(compId){ 
    this.state.judgePanelCompId = compId; // Set current competition
    // Reset to Attendance tab when opening a new competition
    this.state.judgePanelTab = "attendance"; 
    
    const c = this.getCompetition(compId); if (!c) return; 
    const app = document.getElementById("app"); 

    app.innerHTML = ` 
      <div class="row" style="margin-bottom:15px;"> 
        <button class="btn" onclick="App.eventSwitchTab('judge_panel')">← Back to Judge List</button> 
        <div class="spacer"></div> 
        <button class="btn primary" onclick="App.renderPosterGenerator('${c.id}')">Generate Poster</button>
      </div>
      <div class="card">
        <h2>Judge Panel: ${this.esc(c.name)} <span class="tag gold">${this.esc(c.category)}</span></h2>
        <div class="muted">Mark attendance and enter results.</div>
        <div class="hr"></div>
        
        <div class="jp-nav">
          <button class="jp-tab ${this.state.judgePanelTab==='attendance'?'active':''}" onclick="App.judgePanelSwitchTab('attendance')">Attendance & Code Letter</button>
          <button class="jp-tab ${this.state.judgePanelTab==='results'?'active':''}" onclick="App.judgePanelSwitchTab('results')">Results & Scoring</button>
        </div>
        
        <div id="judge-panel-content"></div>
      </div>
    `; 
    this.renderJudgePanelTabContent();
  },
  judgePanelSwitchTab(tabId){
    this.state.judgePanelTab = tabId;
    this.renderJudgePanelTabContent();
  },
  renderJudgePanelTabContent(){
    const wrap = document.getElementById("judge-panel-content");
    const compId = this.state.judgePanelCompId;
    const c = this.getCompetition(compId); if (!c || !wrap) return;
    const entries = this.entriesByCompetition(compId).sort((a,b)=>a.teamId.localeCompare(b.teamId) || a.createdAt - b.createdAt); 
    const attendanceMap = this.attendanceRecMapByComp(compId); 
    const resultsMap = this.data.results.filter(r=>r.competitionId===compId).reduce((acc,r)=>{acc[r.entryId]=r; return acc;},{}); 

    if (this.state.judgePanelTab === "attendance") {
      wrap.innerHTML = `
        <div class="table-wrap"><table>
          <thead><tr><th>Team</th><th>Entry</th><th>Attendance</th><th>Code Letter (max 2 chars)</th></tr></thead>
          <tbody>
            ${entries.map(e=>{ 
              const team = this.getTeam(e.teamId); 
              const attendance = attendanceMap[e.id]; 
              const result = resultsMap[e.id]; // Lock if results are present
              const isPresent = attendance?.present || false;
              const isDisabled = !!result;
              return `<tr> 
                <td><strong>${this.esc(team.name)}</strong></td> 
                <td>${this.esc(this.entryLabel(e))}</td> 
                <td>
                  <input type="checkbox" id="att-${e.id}" ${isPresent?'checked':''} onchange="App.toggleAttendance('${c.id}','${e.id}', this.checked)" ${isDisabled?'disabled':''}>
                </td>
                <td>
                  <input class="input small" type="text" maxlength="2" id="code-${e.id}" value="${this.esc(attendance?.code||'')}" style="width:100px;" oninput="App.updateAttendanceCode('${c.id}','${e.id}', this.value)" ${isDisabled?'disabled':''}>
                  ${isDisabled ? '<span class="muted" style="margin-left: 10px;">(Results recorded)</span>' : ''}
                </td>
              </tr>`; 
            }).join("") || '<tr><td colspan="4" class="muted">No entries yet.</td></tr>'} 
          </tbody>
        </table></div>
      `;
    } else if (this.state.judgePanelTab === "results") {
      wrap.innerHTML = `
        <div class="table-wrap"><table>
          <thead><tr><th>Team</th><th>Entry</th><th>Present?</th><th>Code</th><th>Rank Label</th><th>Points/Mark</th><th>Notes</th><th>Actions</th></tr></thead>
          <tbody>
            ${entries.map(e=>{ 
              const team = this.getTeam(e.teamId); 
              const attendance = attendanceMap[e.id]; 
              const result = resultsMap[e.id]; 
              const isPresent = attendance?.present || false;
              const isDisabled = !!result || !isPresent; // Can only save/edit if present
              return `<tr id="entry-row-${e.id}"> 
                <td><strong>${this.esc(team.name)}</strong></td> 
                <td>${this.esc(this.entryLabel(e))}</td> 
                <td>${isPresent ? '<span class="tag green">Yes</span>' : '<span class="tag red">No</span>'}</td>
                <td>${this.esc(attendance?.code||'-')}</td>
                <form id="result-form-${e.id}" onsubmit="App.saveResult(event, '${c.id}', '${e.id}')">
                  <td><input class="input small" id="rank-${e.id}" type="text" value="${this.esc(result?.rankLabel||'')}" required ${isDisabled?'disabled':''}></td>
                  <td><input class="input small" id="points-${e.id}" type="number" min="0" step="1" value="${result?.pointsAwarded||'0'}" required style="width:90px;" ${isDisabled?'disabled':''}></td>
                  <td><input class="input small" id="notes-${e.id}" type="text" value="${this.esc(result?.judgeNotes||'')}" ${isDisabled?'disabled':''}></td>
                  <td>
                    ${result?`
                      <button class="btn small danger" type="button" onclick="App.deleteResult('${c.id}','${e.id}')">Delete</button>
                    `:`
                      <button class="btn small primary" type="submit" ${isDisabled?'disabled':''}>Save</button>
                    `}
                    ${!isPresent && !result ? '<span class="muted" style="margin-left: 10px; font-size:12px;">Not Present</span>' : ''}
                  </td>
                </form>
              </tr>`; 
            }).join("") || '<tr><td colspan="8" class="muted">No entries yet.</td></tr>'} 
          </tbody>
        </table></div>
      `;
    }
  },
  toggleAttendance(compId, entryId, present){ 
    let rec = this.data.attendance.find(a=>a.entryId===entryId); 
    if (!rec) { 
      rec = { id:this.uid("att"), competitionId:compId, entryId, present:true, code:"", markedAt:Date.now() }; 
      this.data.attendance.push(rec); 
    } 
    rec.present = present; 
    rec.markedAt = Date.now(); 
    this.save(); 
    this.renderJudgePanelTabContent(); // Re-render the content
  }, 
  updateAttendanceCode(compId, entryId, code){ 
    let rec = this.data.attendance.find(a=>a.entryId===entryId); 
    const presentEl = document.getElementById(`att-${entryId}`);

    if (!rec) { 
      // If code is entered, auto-mark present
      if (presentEl && !presentEl.checked) { presentEl.checked = true; this.toggleAttendance(compId, entryId, true); }
      rec = this.data.attendance.find(a=>a.entryId===entryId); 
      if (!rec) { // Should not happen after toggleAttendance
        rec = { id:this.uid("att"), competitionId:compId, entryId, present:true, code, markedAt:Date.now() }; 
        this.data.attendance.push(rec);
      }
    } else {
        // If present and code is cleared, allow it.
        // If not present and code is entered, auto-mark present.
        if (!rec.present && code.trim().length > 0) {
            if (presentEl) presentEl.checked = true;
            rec.present = true;
        }
    }

    rec.code = String(code||"").toUpperCase().trim().slice(0,2); 
    rec.markedAt = Date.now(); 
    this.save(); 
    // Re-render only if present status changed to ensure consistency
    if (presentEl.checked !== rec.present) this.renderJudgePanelTabContent(); 
  }, 
  saveResult(ev, compId, entryId){ 
    ev.preventDefault(); 
    const rank = document.getElementById(`rank-${entryId}`).value.trim(); 
    const points = parseInt(document.getElementById(`points-${entryId}`).value||"0",10); 
    const notes = document.getElementById(`notes-${entryId}`).value.trim(); 
    
    // Check if entry was marked present before saving result
    const attendance = this.data.attendance.find(a=>a.entryId===entryId);
    if (!attendance || !attendance.present) {
        return alert("Cannot save result: Entry must be marked as 'Present' first.");
    }
    
    if (!rank || points < 0) return alert("Rank and non-negative points are required."); 
    
    const rec = { id:this.uid("res"), competitionId:compId, entryId, rankLabel:rank, pointsAwarded:points, judgeNotes:notes, timestamp:Date.now() }; 
    this.data.results.push(rec); 
    this.save(); 
    this.renderJudgePanelTabContent(); // Re-render the results tab
  }, 
  deleteResult(compId, entryId){ 
    if (!confirm("Are you sure you want to delete this result?")) return; 
    this.data.results = this.data.results.filter(r=>r.entryId!==entryId); 
    this.save(); 
    this.renderJudgePanelTabContent(); // Re-render the results tab
  }, 

  // ... (All other content rendering, team portal, and utility functions are the same)

  /* ------------------------------ 
      Global Search Logic (Same as before)
  --------------------------------*/ 
  onGlobalSearchInput(query) {
    clearTimeout(this.state._gsTimer);
    this.state.searchQuery = query.trim();
    if (query.length < 2) {
      this.state.searchOpen = false;
      document.getElementById('global-search-results').style.display = 'none';
      return;
    }
    this.state._gsTimer = setTimeout(() => this._performSearch(), 300);
  },
  onGlobalSearchFocus() {
    if (this.state.searchQuery.length >= 2) this._performSearch();
  },
  onGlobalSearchKey(event) {
    const results = this.state._gsResults;
    if (results.length === 0) return;

    if (event.key === 'ArrowDown') {
      event.preventDefault();
      this.state._gsActiveIndex = (this.state._gsActiveIndex + 1) % results.length;
      this._updateSearchActive();
    } else if (event.key === 'ArrowUp') {
      event.preventDefault();
      this.state._gsActiveIndex = (this.state._gsActiveIndex - 1 + results.length) % results.length;
      this._updateSearchActive();
    } else if (event.key === 'Enter') {
      event.preventDefault();
      const activeResult = results[this.state._gsActiveIndex];
      if (activeResult) this._handleSearchResultClick(activeResult.type, activeResult.id);
      this.state.searchOpen = false;
      document.getElementById('global-search-input').value = "";
      document.getElementById('global-search-results').style.display = 'none';
    } else if (event.key === 'Escape') {
      this.state.searchOpen = false;
      document.getElementById('global-search-results').style.display = 'none';
      document.getElementById('global-search-input').blur();
    }
  },
  _updateSearchActive() {
    const resultsEl = document.getElementById('global-search-results');
    if (!resultsEl) return;
    // Need to correctly map the active index to the flat list of gs-item elements
    const flatItems = Array.from(resultsEl.querySelectorAll('.gs-item'));
    flatItems.forEach((item, globalIndex) => {
        item.classList.toggle('active', globalIndex === this.state._gsActiveIndex);
        if (globalIndex === this.state._gsActiveIndex) {
            item.scrollIntoView({ block: 'nearest' });
        }
    });
  },
  _handleSearchResultClick(type, id) {
    this.state.searchQuery = ""; // Clear query after action
    document.getElementById('global-search-input').value = "";

    if (type === 'student') {
      const student = this.getStudent(id);
      if (!student) return;

      if (this.state.role === 'event') {
        this.eventSwitchTab('students_by_category');
      } else if (this.state.role === 'team' && this.state.teamId === student.teamId) {
        this.teamSwitchTab('students');
      } else {
        return alert(`Student ${student.name} found! (Team: ${this.teamName(student.teamId)}) - Please login to the correct team portal or use the Event Crew portal to view the student list.`);
      }

      // Highlight the student row
      setTimeout(() => {
        const row = document.getElementById(`student-row-${id}`);
        if (row) {
          row.classList.add('search-highlight');
          row.scrollIntoView({ behavior: 'smooth', block: 'center' });
          setTimeout(() => row.classList.remove('search-highlight'), 3000);
        }
      }, 100);

    } else if (type === 'competition') {
      if (this.state.role === 'event') {
        this.state._highlightCompId = id;
        this.eventSwitchTab('judge_panel');
      } else if (this.state.role === 'team') {
        this.state._highlightCompId = id;
        this.teamSwitchTab('enrollment');
      } else {
        // Not logged in, can't view
        alert(`Competition found: ${this.getCompetition(id)?.name}. Please log in to view details.`);
      }
    }
  },
  _performSearch() {
    const query = this.state.searchQuery.toLowerCase();
    
    // 1. Students Search
    const students = this.data.students.filter(s => 
      s.name.toLowerCase().includes(query) || 
      s.chestNo.toLowerCase().includes(query) ||
      this.teamName(s.teamId).toLowerCase().includes(query)
    ).map(s => ({ 
        id: s.id, type: 'student', title: s.name, sub: `Chest #${s.chestNo} (Team: ${this.teamName(s.teamId)})`
    }));

    // 2. Competitions Search
    const competitions = this.data.competitions.filter(c => 
      c.name.toLowerCase().includes(query) || 
      c.category.toLowerCase().includes(query)
    ).map(c => ({ 
        id: c.id, type: 'competition', title: c.name, sub: `Category: ${c.category}`
    }));

    this.state._gsResults = [ ...students, ...competitions ];
    this.state._gsActiveIndex = this.state._gsResults.length > 0 ? 0 : -1;
    this._renderSearchResults();
  },
  _renderSearchResults() {
    const resultsEl = document.getElementById('global-search-results');
    if (!resultsEl || this.state.searchQuery.length < 2) return;

    if (this.state._gsResults.length === 0) {
      resultsEl.innerHTML = `<div class="gs-section">No results found for "${this.esc(this.state.searchQuery)}"</div>`;
      resultsEl.style.display = 'block';
      return;
    }

    let html = '';
    
    const studentResults = this.state._gsResults.filter(r => r.type === 'student');
    if (studentResults.length > 0) {
      html += `<div class="gs-section">STUDENTS (${studentResults.length})</div>`;
      studentResults.forEach((r) => {
        const globalIndex = this.state._gsResults.indexOf(r);
        const activeClass = globalIndex === this.state._gsActiveIndex ? 'active' : '';
        html += `
          <div class="gs-item ${activeClass}" onclick="App._handleSearchResultClick('student', '${r.id}')">
            <span class="gs-type">👤</span>
            <div><div class="gs-title">${this.esc(r.title)}</div><div class="gs-sub">${this.esc(r.sub)}</div></div>
          </div>
        `;
      });
    }

    const compResults = this.state._gsResults.filter(r => r.type === 'competition');
    if (compResults.length > 0) {
      html += `<div class="gs-section">COMPETITIONS (${compResults.length})</div>`;
      compResults.forEach((r) => {
        const globalIndex = this.state._gsResults.indexOf(r);
        const activeClass = globalIndex === this.state._gsActiveIndex ? 'active' : '';
        html += `
          <div class="gs-item ${activeClass}" onclick="App._handleSearchResultClick('competition', '${r.id}')">
            <span class="gs-type">🏆</span>
            <div><div class="gs-title">${this.esc(r.title)}</div><div class="gs-sub">${this.esc(r.sub)}</div></div>
          </div>
        `;
      });
    }

    resultsEl.innerHTML = html;
    resultsEl.style.display = 'block';
    this.state.searchOpen = true;
  }
}; 
 
// Initial setup and rendering 
App.updateHeaderInfo(); 
App.applyBrand(); 
App.renderHeaderSession(); 
App.routeHome(); 
</script> 
 
</body> 
</html>
