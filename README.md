<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Usman Arshad Virk — Developer Profile</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --muted:#9aa7bd; --accent:#7c3aed; --glass: rgba(255,255,255,0.04);
      --glass-2: rgba(255,255,255,0.02);
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Inter,system-ui,Segoe UI,Roboto,-apple-system,'Helvetica Neue',Arial;color:#e6eef8;background:linear-gradient(180deg,#071028 0%, #07182a 50%, #061020 100%);}
    .container{max-width:1100px;margin:36px auto;padding:28px;border-radius:18px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));box-shadow:0 10px 30px rgba(2,6,23,0.6);border:1px solid rgba(255,255,255,0.03);}

    /* Header */
    .header{display:flex;gap:20px;align-items:center}
    .avatar{width:120px;height:120px;border-radius:16px;overflow:hidden;border:2px solid rgba(255,255,255,0.06);box-shadow:0 8px 30px rgba(12,18,28,0.6);position:relative}
    .avatar img{width:100%;height:100%;object-fit:cover;display:block}
    .intro{flex:1}
    h1{margin:0;font-size:28px;letter-spacing:-0.4px}
    h2{margin:6px 0 0;font-weight:600;color:var(--muted);font-size:14px}
    p.lead{color:var(--muted);margin-top:12px;max-width:70%}

    /* buttons */
    .links{margin-top:14px;display:flex;gap:10px;flex-wrap:wrap}
    .btn{display:inline-flex;align-items:center;gap:10px;padding:10px 14px;border-radius:12px;background:var(--glass);backdrop-filter: blur(6px);border:1px solid rgba(255,255,255,0.03);color:#eaf3ff;text-decoration:none;font-weight:600}
    .btn .dot{width:10px;height:10px;border-radius:50%;background:var(--accent);box-shadow:0 4px 12px rgba(124,58,237,0.2)}

    /* grid */
    .grid{display:grid;grid-template-columns:1fr 420px;gap:20px;margin-top:20px}

    /* card */
    .card{background:linear-gradient(180deg,var(--card), rgba(8,12,18,0.6));border-radius:14px;padding:18px;border:1px solid var(--glass-2)}
    .card h3{margin:0 0 12px}

    /* stats */
    .stats{display:flex;gap:10px}
    .stat{flex:1;padding:12px;border-radius:10px;background:linear-gradient(180deg, rgba(255,255,255,0.01), rgba(255,255,255,0.00));text-align:center}
    .stat .num{font-weight:700;font-size:18px}
    .muted{color:var(--muted);font-size:13px}

    /* graphs */
    .graph-wrap{height:220px}
    canvas{width:100%;height:100%}

    /* activity */
    .activity img{width:100%;border-radius:8px}

    /* footer */
    .footer{display:flex;justify-content:space-between;align-items:center;margin-top:18px;color:var(--muted);font-size:13px}

    /* animations */
    .sparkles{position:absolute;left:0;top:0;right:0;bottom:0;pointer-events:none;overflow:hidden;border-radius:16px}
    .sparkles i{position:absolute;width:6px;height:6px;border-radius:50%;background:linear-gradient(90deg,#fff,#7c3aed);opacity:0.9;animation:float 6s linear infinite}
    @keyframes float{0%{transform:translateY(0) scale(0.6)}50%{transform:translateY(-80px) scale(1)}100%{transform:translateY(0) scale(0.6)}}

    /* responsive */
    @media (max-width:980px){.grid{grid-template-columns:1fr}.intro p.lead{max-width:100%}}
  </style>
</head>
<body>
  <div class="container">
    <div class="header">
      <div class="avatar card" style="min-width:120px;">
        <img src="https://avatars.githubusercontent.com/052-Usman?s=400&u=1c2b4f2a4d0b8ef5b1a6c8b9d9f4b2e7f9a6c3d1&v=4" alt="Usman Virk">
        <div class="sparkles" aria-hidden>
          <i style="left:10%;top:20%;animation-duration:7s"></i>
          <i style="left:60%;top:10%;animation-duration:6s"></i>
          <i style="left:80%;top:50%;animation-duration:8s"></i>
          <i style="left:30%;top:70%;animation-duration:9s"></i>
        </div>
      </div>

      <div class="intro">
        <h1>Usman Arshad Virk <span style="color:var(--accent);font-weight:700">(Usman Virk)</span></h1>
        <h2>Full-Stack Developer · Cloud Practitioner · AI & Automation</h2>
        <p class="lead">I build scalable web applications, developer tools, and AI-driven marketing solutions. Focused on clean architecture, performance, and delightful user experiences.</p>

        <div class="links">
          <a class="btn" href="https://github.com/052-Usman" target="_blank"><span class="dot"></span> View GitHub</a>
          <a class="btn" href="https://www.linkedin.com/in/usman-arshad-virk" target="_blank">🔗 LinkedIn</a>
          <a class="btn" href="https://usmanarshadvirk.vercel.app" target="_blank">🌐 Portfolio</a>
          <a class="btn" href="https://x.com/usmanvirk052" target="_blank">🐦 X / Twitter</a>
        </div>
      </div>
    </div>

    <div class="grid">
      <div>
        <div class="card">
          <h3>About</h3>
          <p class="muted">Software Engineer with expertise in React, Next.js, Node.js, Angular, AWS, and modern DevOps practices. I enjoy turning ideas into products and optimizing engineering workflows with automation and AI.</p>

          <div style="margin-top:16px" class="stats">
            <div class="stat">
              <div class="num" id="reposCount">—</div>
              <div class="muted">Public Repos</div>
            </div>
            <div class="stat">
              <div class="num" id="followersCount">—</div>
              <div class="muted">Followers</div>
            </div>
            <div class="stat">
              <div class="num" id="starsCount">—</div>
              <div class="muted">Total Stars</div>
            </div>
          </div>
        </div>

        <div class="card" style="margin-top:16px">
          <h3>Graphs</h3>
          <div class="graph-wrap">
            <canvas id="langChart"></canvas>
          </div>
          <p class="muted" style="margin-top:8px">Language distribution (computed from public repos' primary language).</p>
        </div>

        <div class="card" style="margin-top:16px">
          <h3>Commits & Activity</h3>
          <div style="display:flex;gap:12px;align-items:flex-start;flex-wrap:wrap">
            <div style="flex:1;min-width:280px">
              <div class="activity card" style="padding:10px">
                <h4 style="margin:6px 0">Contribution Heatmap</h4>
                <img id="contribSvg" src="https://github-readme-activity-graph.vercel.app/graph?username=052-Usman&theme=tokyo-night&hide_border=true" alt="contributions" />
              </div>
            </div>

            <div style="width:200px">
              <div class="card" style="padding:12px;text-align:center">
                <h4 style="margin:6px 0">Recent Events</h4>
                <div id="recentEvents" class="muted" style="font-size:13px;max-height:220px;overflow:auto;text-align:left"></div>
              </div>
            </div>
          </div>
        </div>

      </div>

      <aside>
        <div class="card">
          <h3>Highlights</h3>
          <ul style="padding-left:18px;color:var(--muted);margin:8px 0">
            <li>AWS Cloud Practitioner certified</li>
            <li>Chrome Extension: Meeting Flow Pro (testing)</li>
            <li>Projects: Marketing Platform, Transcribe & Analyze, Search Sphere</li>
          </ul>

          <h3 style="margin-top:12px">Contact</h3>
          <p class="muted" style="margin:6px 0">Email: <a href="mailto:usman@example.com">usman@example.com</a> (replace with your email)</p>

          <div style="display:flex;gap:8px;flex-wrap:wrap;margin-top:12px">
            <a class="btn" href="https://www.linkedin.com/in/usman-arshad-virk" target="_blank">LinkedIn</a>
            <a class="btn" href="https://www.instagram.com/usmanvirk052" target="_blank">Instagram</a>
            <a class="btn" href="https://www.facebook.com/usmanarshadvirk/" target="_blank">Facebook</a>
          </div>
        </div>

        <div class="card" style="margin-top:16px">
          <h3>GitHub Stats</h3>
          <img src="https://github-readme-stats.vercel.app/api?username=052-Usman&show_icons=true&theme=tokyonight&hide_title=true&hide_border=true" alt="stats" style="width:100%;border-radius:8px"/>
        </div>

        <div class="card" style="margin-top:16px">
          <h3>Quick Links</h3>
          <div style="display:flex;flex-direction:column;gap:8px;margin-top:8px">
            <a class="btn" href="https://usmanarshadvirk.vercel.app" target="_blank">Portfolio</a>
            <a class="btn" href="https://github.com/052-Usman" target="_blank">GitHub</a>
            <a class="btn" href="https://x.com/usmanvirk052" target="_blank">X / Twitter</a>
          </div>
        </div>
      </aside>
    </div>

    <div class="footer">
      <div>Made with ❤️ • Usman Arshad Virk</div>
      <div class="muted">Last updated: <span id="lastUpdated">—</span></div>
    </div>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>
  <script>
    // small animated entrance
    document.querySelectorAll('.card').forEach((c,i)=>{c.style.opacity=0;setTimeout(()=>{c.style.transition='opacity 700ms ease-out,transform 700ms';c.style.opacity=1;c.style.transform='translateY(0)';},120*i)});

    const username = '052-Usman';
    document.getElementById('lastUpdated').innerText = new Date().toLocaleString();

    // Fetch basic user info
    async function fetchUser(){
      try{
        const res = await fetch(`https://api.github.com/users/${username}`);
        if(!res.ok) throw new Error('rate or network');
        const data = await res.json();
        document.getElementById('reposCount').innerText = data.public_repos;
        document.getElementById('followersCount').innerText = data.followers;
      }catch(e){console.warn(e);document.getElementById('reposCount').innerText='—';document.getElementById('followersCount').innerText='—'}
    }

    // Fetch repos and compute language distribution + stars
    async function fetchReposAndDraw(){
      try{
        let page=1, per=100, repos=[];
        while(true){
          const r = await fetch(`https://api.github.com/users/${username}/repos?per_page=${per}&page=${page}`);
          if(!r.ok) break;
          const chunk = await r.json();
          if(chunk.length===0) break;
          repos = repos.concat(chunk); page++; if(chunk.length<per) break;
        }
        // summarize
        const langMap = {};
        let totalStars=0;
        for(const repo of repos){
          if(repo.language) langMap[repo.language] = (langMap[repo.language]||0) + 1;
          totalStars += repo.stargazers_count || 0;
        }
        document.getElementById('starsCount').innerText = totalStars;

        // prepare chart
        const labels = Object.keys(langMap).slice(0,8);
        const values = labels.map(l=>langMap[l]);
        if(labels.length===0){labels.push('No data'); values.push(1)}

        const ctx = document.getElementById('langChart').getContext('2d');
        new Chart(ctx, {
          type:'doughnut',
          data:{labels, datasets:[{data:values, hoverOffset:8}]},
          options:{plugins:{legend:{labels:{color:'#cfe8ff'}}}, maintainAspectRatio:false}
        });

      }catch(e){console.warn('repos fail',e)}
    }

    // Fetch recent events
    async function fetchEvents(){
      try{
        const r = await fetch(`https://api.github.com/users/${username}/events/public?per_page=10`);
        if(!r.ok) return;
        const events = await r.json();
        const el = document.getElementById('recentEvents');
        el.innerHTML = events.map(ev=>{
          const date = new Date(ev.created_at).toLocaleString();
          let action = ev.type.replace(/Event$/,'');
          const repo = ev.repo ? `<strong>${ev.repo.name}</strong>` : '';
          return `<div style="margin-bottom:10px"><div style=\"font-weight:600;color:#eaf3ff\">${action}</div><div class=\"muted\">${repo} • ${date}</div></div>`;
        }).join('');
      }catch(e){console.warn(e)}
    }

    fetchUser(); fetchReposAndDraw(); fetchEvents();

    // little floating sparkle creation (adds variation)
    (function randomSparkles(){
      const parent = document.querySelector('.sparkles');
      if(!parent) return;
      for(let i=0;i<8;i++){const el=document.createElement('i');el.style.left=Math.random()*100+'%';el.style.top=Math.random()*100+'%';el.style.animationDuration=(6+Math.random()*6)+'s';parent.appendChild(el)}
    })();
  </script>
</body>
</html>
