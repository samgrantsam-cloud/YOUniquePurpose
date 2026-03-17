<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>YOUnique Purpose Assessment</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;800;900&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
:root {
  --blue: #263F6A;
  --red: #F7403A;
  --gold: #EFBD47;
  --grey: #E0DED8;
  --blue-light: rgba(38,63,106,0.08);
  --red-light: rgba(247,64,58,0.08);
  --text: #1a1a1a;
  --text-muted: #999;
  --bg: #ffffff;
  --border: #ebebeb;
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body { font-family: 'DM Sans', sans-serif; background: var(--bg); color: var(--text); min-height: 100vh; }

/* ── PROGRESS BAR ── */
.progress-strip {
  position: fixed; top: 0; left: 0; right: 0; z-index: 200;
  height: 4px; background: var(--grey);
}
.progress-fill {
  height: 4px; background: var(--blue); transition: width 0.5s ease;
  position: relative;
}
.progress-fill::after {
  content: ''; position: absolute; right: 0; top: -2px;
  width: 8px; height: 8px; background: var(--blue); border-radius: 50%;
}

/* ── NAV ── */
.nav {
  position: fixed; top: 4px; left: 0; right: 0; z-index: 100;
  display: flex; align-items: center; justify-content: space-between;
  padding: 14px 40px; background: white;
  border-bottom: 1px solid var(--border);
}
.nav-logo {
  font-family: 'Playfair Display', serif; font-weight: 900; font-size: 18px;
  color: var(--blue); letter-spacing: -0.3px;
}
.nav-logo span { color: var(--red); }
.nav-progress-text { font-size: 12px; color: var(--text-muted); font-weight: 500; letter-spacing: 0.05em; }
.nav-section { font-size: 12px; color: var(--blue); font-weight: 600; letter-spacing: 0.05em; }

/* ── SCREENS ── */
.screen { display: none; min-height: 100vh; }
.screen.active { display: block; }

/* ── WELCOME ── */
.welcome-wrap {
  min-height: 100vh; display: flex; align-items: center; justify-content: center;
  padding: 80px 24px 40px;
}
.welcome-inner { max-width: 620px; width: 100%; }
.welcome-tag {
  display: inline-block; font-size: 11px; font-weight: 600; letter-spacing: 0.12em;
  text-transform: uppercase; color: var(--red); border: 1px solid var(--red);
  padding: 4px 12px; border-radius: 20px; margin-bottom: 20px;
}
.welcome-h1 {
  font-family: 'Playfair Display', serif; font-size: clamp(36px,5vw,56px);
  font-weight: 900; line-height: 1.1; color: var(--blue); margin-bottom: 20px;
}
.welcome-h1 em { color: var(--red); font-style: normal; }
.welcome-p {
  font-size: 17px; line-height: 1.7; color: #555; margin-bottom: 36px; max-width: 500px;
}
.welcome-stats {
  display: flex; gap: 32px; margin-bottom: 40px; flex-wrap: wrap;
}
.ws-item { }
.ws-num {
  font-family: 'Playfair Display', serif; font-size: 32px; font-weight: 900;
  color: var(--blue); line-height: 1;
}
.ws-label { font-size: 12px; color: var(--text-muted); margin-top: 2px; }
.form-group { margin-bottom: 16px; }
.form-label { font-size: 13px; font-weight: 500; color: var(--text); margin-bottom: 6px; display: block; }
.form-input {
  width: 100%; padding: 14px 18px; border: 1.5px solid var(--border); border-radius: 12px;
  font-size: 15px; font-family: 'DM Sans', sans-serif; outline: none; transition: border 0.2s;
  background: white; color: var(--text);
}
.form-input:focus { border-color: var(--blue); }
.btn-start {
  display: inline-flex; align-items: center; gap: 10px;
  background: var(--blue); color: white; border: none; border-radius: 50px;
  padding: 16px 36px; font-size: 15px; font-weight: 600; font-family: 'DM Sans', sans-serif;
  cursor: pointer; transition: all 0.2s; margin-top: 8px;
}
.btn-start:hover { background: #1a2f52; transform: translateY(-1px); }
.btn-start svg { transition: transform 0.2s; }
.btn-start:hover svg { transform: translateX(3px); }
.welcome-verse {
  margin-top: 40px; padding: 20px 24px; background: var(--blue-light);
  border-left: 3px solid var(--blue); border-radius: 0 10px 10px 0;
  font-size: 14px; color: var(--blue); line-height: 1.6; font-style: italic;
}
.welcome-verse cite { font-style: normal; font-size: 12px; font-weight: 600; opacity: 0.7; display: block; margin-top: 6px; }

/* ── SECTION INTRO ── */
.section-intro-wrap {
  min-height: 100vh; display: flex; align-items: center; justify-content: center;
  padding: 80px 24px;
}
.section-intro-inner { max-width: 560px; width: 100%; text-align: center; }
.si-number {
  font-family: 'Playfair Display', serif; font-size: 80px; font-weight: 900;
  color: var(--grey); line-height: 1; margin-bottom: 16px;
}
.si-title {
  font-family: 'Playfair Display', serif; font-size: 36px; font-weight: 900;
  color: var(--blue); margin-bottom: 16px;
}
.si-desc { font-size: 16px; line-height: 1.7; color: #555; margin-bottom: 12px; }
.si-count {
  font-size: 13px; color: var(--text-muted); font-weight: 500; margin-bottom: 36px;
}
.scale-demo {
  background: #f8f8f8; border-radius: 16px; padding: 20px 24px; margin-bottom: 36px;
  display: flex; align-items: center; justify-content: space-between;
}
.scale-demo-label { font-size: 13px; color: var(--text-muted); font-weight: 500; }
.scale-demo-circles { display: flex; gap: 10px; align-items: center; }
.sdc { border-radius: 50%; border: 2px solid; }
.btn-begin {
  display: inline-flex; align-items: center; gap: 10px;
  background: var(--red); color: white; border: none; border-radius: 50px;
  padding: 15px 32px; font-size: 15px; font-weight: 600;
  font-family: 'DM Sans', sans-serif; cursor: pointer; transition: all 0.2s;
}
.btn-begin:hover { background: #d62f29; transform: translateY(-1px); }

/* ── QUESTIONS ── */
.questions-wrap { padding: 80px 24px 120px; max-width: 760px; margin: 0 auto; }
.q-block {
  padding: 40px 0; border-bottom: 1px solid var(--border);
  transition: opacity 0.3s;
}
.q-block.faded { opacity: 0.25; pointer-events: none; }
.q-block.active { opacity: 1; pointer-events: all; }
.q-block:last-child { border-bottom: none; }
.q-statement {
  font-size: clamp(16px,2.2vw,20px); font-weight: 400; color: var(--text);
  line-height: 1.5; margin-bottom: 28px; letter-spacing: -0.2px;
}
.q-scale-row {
  display: flex; align-items: center; gap: clamp(6px,1.5vw,14px);
}
.q-scale-label {
  font-size: 13px; font-weight: 500; min-width: 40px; white-space: nowrap;
}
.q-scale-label.never { color: var(--text-muted); }
.q-scale-label.always { color: var(--blue); }
.q-circles { display: flex; gap: clamp(8px,1.5vw,16px); align-items: center; flex: 1; justify-content: center; }
.q-circle {
  border-radius: 50%; border: 2.5px solid; cursor: pointer;
  transition: all 0.2s; flex-shrink: 0;
  display: flex; align-items: center; justify-content: center;
}
/* Sizes: value 0=smallest(neutral-ish), value 5=largest */
.q-circle[data-val="0"] { width: 32px; height: 32px; border-color: #ccc; background: transparent; }
.q-circle[data-val="1"] { width: 38px; height: 38px; border-color: #bbb; background: transparent; }
.q-circle[data-val="2"] { width: 42px; height: 42px; border-color: #aaa; background: transparent; }
.q-circle[data-val="3"] { width: 42px; height: 42px; border-color: #6a9fd8; background: transparent; }
.q-circle[data-val="4"] { width: 48px; height: 48px; border-color: var(--blue); background: transparent; }
.q-circle[data-val="5"] { width: 54px; height: 54px; border-color: var(--blue); background: transparent; }
.q-circle[data-val="0"]:hover { border-color: #999; background: rgba(150,150,150,0.1); }
.q-circle[data-val="1"]:hover { border-color: #888; background: rgba(100,100,100,0.08); }
.q-circle[data-val="2"]:hover { border-color: #777; background: rgba(80,80,80,0.06); }
.q-circle[data-val="3"]:hover { border-color: #6a9fd8; background: rgba(106,159,216,0.1); }
.q-circle[data-val="4"]:hover { border-color: var(--blue); background: var(--blue-light); }
.q-circle[data-val="5"]:hover { border-color: var(--blue); background: var(--blue-light); }
.q-circle.selected[data-val="0"] { background: #bbb; border-color: #bbb; }
.q-circle.selected[data-val="1"] { background: #999; border-color: #999; }
.q-circle.selected[data-val="2"] { background: #7a9fc0; border-color: #7a9fc0; }
.q-circle.selected[data-val="3"] { background: #5080b0; border-color: #5080b0; }
.q-circle.selected[data-val="4"] { background: var(--blue); border-color: var(--blue); }
.q-circle.selected[data-val="5"] { background: var(--blue); border-color: var(--blue); box-shadow: 0 0 0 4px rgba(38,63,106,0.15); }

/* ── PAGE NAV ── */
.page-nav {
  position: fixed; bottom: 0; left: 0; right: 0; background: white;
  border-top: 1px solid var(--border); padding: 16px 40px;
  display: flex; align-items: center; justify-content: space-between;
  z-index: 100;
}
.btn-next {
  display: inline-flex; align-items: center; gap: 10px;
  background: var(--blue); color: white; border: none; border-radius: 50px;
  padding: 14px 32px; font-size: 15px; font-weight: 600;
  font-family: 'DM Sans', sans-serif; cursor: pointer; transition: all 0.2s;
}
.btn-next:hover { background: #1a2f52; }
.btn-next:disabled { background: var(--grey); color: #aaa; cursor: not-allowed; }
.btn-back {
  display: inline-flex; align-items: center; gap: 8px;
  background: transparent; color: var(--text-muted); border: none;
  padding: 14px 20px; font-size: 14px; font-weight: 500;
  font-family: 'DM Sans', sans-serif; cursor: pointer; transition: all 0.2s;
}
.btn-back:hover { color: var(--text); }
.page-counter { font-size: 13px; color: var(--text-muted); font-weight: 500; }
.unanswered-warning {
  font-size: 12px; color: var(--red); font-weight: 500; display: none;
}

/* ── SECTION COMPLETE ── */
.section-complete-wrap {
  min-height: 100vh; display: flex; align-items: center; justify-content: center;
  padding: 80px 24px;
}
.sc-inner { max-width: 480px; width: 100%; text-align: center; }
.sc-check {
  width: 72px; height: 72px; background: #e8f5e9; border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  margin: 0 auto 24px; font-size: 32px;
}
.sc-title {
  font-family: 'Playfair Display', serif; font-size: 28px; font-weight: 900;
  color: var(--blue); margin-bottom: 12px;
}
.sc-desc { font-size: 15px; color: #555; line-height: 1.6; margin-bottom: 28px; }
.sc-result-preview {
  background: var(--blue-light); border-radius: 14px; padding: 20px 24px;
  margin-bottom: 28px; text-align: left;
}
.sc-result-label { font-size: 11px; font-weight: 600; color: var(--blue); text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 4px; }
.sc-result-value { font-family: 'Playfair Display', serif; font-size: 22px; font-weight: 900; color: var(--blue); }
.sc-result-sub { font-size: 13px; color: #666; margin-top: 4px; }

/* ── REPORT ── */
.report-wrap { padding-top: 68px; }
.report-cover {
  min-height: 60vh; background: var(--blue); display: flex; align-items: flex-end;
  padding: 60px; position: relative; overflow: hidden;
}
.report-cover::before {
  content: ''; position: absolute; top: -100px; right: -100px;
  width: 500px; height: 500px; border-radius: 50%;
  background: rgba(239,189,71,0.12);
}
.report-cover::after {
  content: ''; position: absolute; bottom: -80px; left: 40%;
  width: 300px; height: 300px; border-radius: 50%;
  background: rgba(247,64,58,0.1);
}
.rc-inner { position: relative; z-index: 1; }
.rc-tag {
  font-size: 11px; font-weight: 600; letter-spacing: 0.15em; text-transform: uppercase;
  color: var(--gold); margin-bottom: 16px; opacity: 0.9;
}
.rc-name {
  font-family: 'Playfair Display', serif; font-size: clamp(42px,6vw,72px);
  font-weight: 900; color: white; line-height: 1; margin-bottom: 12px;
}
.rc-subtitle { font-size: 16px; color: rgba(255,255,255,0.65); margin-bottom: 6px; }
.rc-date { font-size: 13px; color: rgba(255,255,255,0.45); }
.rc-verse {
  position: absolute; top: 60px; right: 60px; max-width: 280px;
  text-align: right; color: rgba(255,255,255,0.4); font-size: 13px;
  line-height: 1.6; font-style: italic;
}
.rc-verse cite { font-style: normal; font-size: 11px; display: block; margin-top: 6px; opacity: 0.6; }

/* ── REPORT SECTIONS ── */
.report-section { padding: 60px; border-bottom: 1px solid var(--border); max-width: 100%; }
.report-section:last-child { border-bottom: none; }
.rs-label {
  font-size: 11px; font-weight: 700; letter-spacing: 0.15em; text-transform: uppercase;
  color: var(--red); margin-bottom: 6px;
}
.rs-title {
  font-family: 'Playfair Display', serif; font-size: clamp(28px,4vw,42px);
  font-weight: 900; color: var(--blue); margin-bottom: 8px; line-height: 1.1;
}
.rs-desc { font-size: 15px; color: #666; line-height: 1.7; max-width: 680px; margin-bottom: 36px; }

/* ── SUMMARY GRID ── */
.summary-grid {
  display: grid; grid-template-columns: repeat(auto-fit, minmax(200px,1fr));
  gap: 2px; background: var(--border); border-radius: 16px; overflow: hidden;
  margin-bottom: 40px;
}
.sg-card {
  background: white; padding: 28px 24px;
}
.sg-label { font-size: 10px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.12em; color: var(--text-muted); margin-bottom: 8px; }
.sg-value { font-family: 'Playfair Display', serif; font-size: 20px; font-weight: 900; color: var(--blue); margin-bottom: 4px; line-height: 1.1; }
.sg-sub { font-size: 12px; color: var(--text-muted); line-height: 1.4; }

/* ── BARS ── */
.bar-group { margin-bottom: 12px; }
.bar-label { display: flex; justify-content: space-between; font-size: 13px; margin-bottom: 5px; font-weight: 500; }
.bar-pct { color: var(--text-muted); font-size: 12px; }
.bar-track { background: var(--grey); border-radius: 6px; height: 8px; overflow: hidden; }
.bar-fill { height: 8px; border-radius: 6px; transition: width 1.2s cubic-bezier(0.4,0,0.2,1); }
.bar-fill.primary { background: var(--blue); }
.bar-fill.secondary { background: var(--red); }
.bar-fill.tertiary { background: var(--gold); }
.bar-fill.grey { background: #bbb; }

/* ── GIFT DETAIL ── */
.gift-detail-block {
  background: #f9f9f9; border-radius: 16px; padding: 32px; margin-bottom: 20px;
  border-left: 4px solid var(--blue);
}
.gift-detail-block.secondary { border-left-color: var(--red); }
.gift-detail-block.tertiary { border-left-color: var(--gold); }
.gdb-rank { font-size: 11px; font-weight: 700; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 6px; }
.gdb-name { font-family: 'Playfair Display', serif; font-size: 28px; font-weight: 900; color: var(--blue); margin-bottom: 4px; }
.gift-detail-block.secondary .gdb-name { color: var(--red); }
.gdb-thrust {
  display: inline-block; background: var(--blue); color: white;
  font-size: 11px; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase;
  padding: 4px 12px; border-radius: 20px; margin-bottom: 14px;
}
.gift-detail-block.secondary .gdb-thrust { background: var(--red); }
.gdb-desc { font-size: 14px; color: #555; line-height: 1.7; margin-bottom: 16px; }
.gdb-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
.gdb-item { }
.gdb-item-label { font-size: 10px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em; color: var(--text-muted); margin-bottom: 3px; }
.gdb-item-val { font-size: 13px; color: var(--text); line-height: 1.5; }

/* ── PASSION CHIPS ── */
.passion-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-bottom: 28px; }
.passion-chip {
  border-radius: 14px; padding: 20px;
}
.passion-chip.p1 { background: var(--blue); }
.passion-chip.p2 { background: var(--red); }
.passion-chip.p3 { background: var(--gold); }
.passion-chip.p4 { background: #2d6a4f; }
.pc-cat { font-size: 10px; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; color: rgba(255,255,255,0.65); margin-bottom: 6px; }
.pc-val { font-family: 'Playfair Display', serif; font-size: 22px; font-weight: 900; color: white; line-height: 1.1; }
.pc-desc { font-size: 12px; color: rgba(255,255,255,0.75); margin-top: 6px; line-height: 1.4; }

/* ── VIA STRENGTHS ── */
.via-grid { display: grid; grid-template-columns: repeat(auto-fit,minmax(160px,1fr)); gap: 10px; margin-bottom: 28px; }
.via-card {
  background: #f4f4f4; border-radius: 12px; padding: 16px;
  border-top: 3px solid var(--blue); text-align: center;
}
.via-card:nth-child(2) { border-top-color: var(--red); }
.via-card:nth-child(3) { border-top-color: var(--gold); }
.via-card:nth-child(4) { border-top-color: #5080b0; }
.via-card:nth-child(5) { border-top-color: #2d6a4f; }
.via-rank { font-size: 10px; font-weight: 700; color: var(--text-muted); text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 4px; }
.via-name { font-family: 'Playfair Display', serif; font-size: 16px; font-weight: 900; color: var(--blue); margin-bottom: 3px; }
.via-virtue { font-size: 11px; color: var(--text-muted); }
.via-score { font-size: 22px; font-weight: 700; color: var(--blue); margin-top: 8px; }

/* ── RIASEC ── */
.riasec-code-display {
  display: flex; gap: 8px; margin-bottom: 28px;
}
.riasec-letter {
  width: 64px; height: 64px; border-radius: 14px; display: flex; align-items: center;
  justify-content: center; font-family: 'Playfair Display', serif;
  font-size: 32px; font-weight: 900; color: white;
}
.rl-R { background: #1a5c3a; }
.rl-I { background: var(--blue); }
.rl-A { background: var(--red); }
.rl-S { background: #2d6a4f; }
.rl-E { background: #9a3412; }
.rl-C { background: #555; }

/* ── PERSONALITY ── */
.type-display {
  display: flex; gap: 8px; margin-bottom: 16px;
}
.type-letter-block {
  width: 56px; height: 56px; border-radius: 12px; background: var(--blue);
  display: flex; align-items: center; justify-content: center;
  font-family: 'Playfair Display', serif; font-size: 28px; font-weight: 900; color: white;
}
.dimension-bars { display: grid; grid-template-columns: 1fr 1fr; gap: 10px 24px; margin-top: 20px; }
.dim-row { }
.dim-labels { display: flex; justify-content: space-between; font-size: 12px; margin-bottom: 4px; font-weight: 500; }
.dim-track {
  height: 10px; border-radius: 6px; overflow: hidden;
  display: flex; background: var(--grey);
}
.dim-left { background: var(--blue); height: 10px; transition: width 1s ease; }
.dim-right { background: var(--red); height: 10px; transition: width 1s ease; }

/* ── PATHWAYS ── */
.pathways-bars { display: flex; flex-direction: column; gap: 20px; margin-bottom: 28px; }
.pw-item { }
.pw-header { display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px; }
.pw-name { font-size: 15px; font-weight: 600; }
.pw-stage {
  font-size: 12px; font-weight: 700; padding: 3px 12px; border-radius: 20px;
}
.pw-stage.striving { background: #fef2f2; color: var(--red); }
.pw-stage.surviving { background: #fffbeb; color: #92400e; }
.pw-stage.thriving { background: #f0fdf4; color: #166534; }
.pw-track { background: var(--grey); border-radius: 8px; height: 14px; overflow: hidden; }
.pw-fill { height: 14px; border-radius: 8px; transition: width 1.2s ease; }
.pw-fill.striving { background: var(--red); }
.pw-fill.surviving { background: var(--gold); }
.pw-fill.thriving { background: #22c55e; }
.pathway-overall-card {
  background: var(--blue); border-radius: 16px; padding: 28px 32px;
  color: white; margin-top: 28px;
}
.poc-stage { font-size: 11px; font-weight: 700; letter-spacing: 0.12em; text-transform: uppercase; color: var(--gold); margin-bottom: 8px; }
.poc-score { font-family: 'Playfair Display', serif; font-size: 48px; font-weight: 900; color: white; line-height: 1; margin-bottom: 12px; }
.poc-desc { font-size: 14px; color: rgba(255,255,255,0.75); line-height: 1.7; }

/* ── CALLING CANVAS ── */
.calling-canvas {
  background: linear-gradient(135deg, #0f1c30, #1a2f52);
  border-radius: 20px; padding: 40px; margin-top: 20px;
}
.cc-title { font-family: 'Playfair Display', serif; font-size: 22px; font-weight: 900; color: var(--gold); margin-bottom: 24px; }
.cc-grid { display: grid; grid-template-columns: repeat(auto-fit,minmax(180px,1fr)); gap: 2px; background: rgba(255,255,255,0.06); border-radius: 12px; overflow: hidden; }
.cc-item { padding: 20px; background: rgba(255,255,255,0.04); }
.cc-item-label { font-size: 10px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.12em; color: rgba(255,255,255,0.4); margin-bottom: 6px; }
.cc-item-val { font-family: 'Playfair Display', serif; font-size: 16px; font-weight: 900; color: var(--gold); line-height: 1.2; }

/* ── NEXT STEPS ── */
.next-steps-card { background: #f8f8f8; border-radius: 16px; padding: 32px; margin-bottom: 16px; }
.ns-num { font-family: 'Playfair Display', serif; font-size: 48px; font-weight: 900; color: var(--grey); line-height: 1; margin-bottom: 8px; }
.ns-title { font-size: 17px; font-weight: 600; color: var(--text); margin-bottom: 8px; }
.ns-desc { font-size: 14px; color: #666; line-height: 1.7; }
.coaching-cta {
  background: var(--red); border-radius: 20px; padding: 48px 40px;
  text-align: center; margin-top: 32px;
}
.cta-title { font-family: 'Playfair Display', serif; font-size: 32px; font-weight: 900; color: white; margin-bottom: 12px; }
.cta-desc { font-size: 15px; color: rgba(255,255,255,0.8); line-height: 1.6; margin-bottom: 28px; max-width: 480px; margin-left: auto; margin-right: auto; }
.btn-cta {
  display: inline-flex; align-items: center; gap: 10px;
  background: white; color: var(--red); border: none; border-radius: 50px;
  padding: 16px 36px; font-size: 15px; font-weight: 700;
  font-family: 'DM Sans', sans-serif; cursor: pointer; transition: all 0.2s;
  text-decoration: none;
}
.btn-cta:hover { background: var(--gold); color: white; transform: translateY(-2px); }
.btn-print {
  display: inline-flex; align-items: center; gap: 8px;
  background: transparent; color: rgba(255,255,255,0.7); border: 1.5px solid rgba(255,255,255,0.3);
  border-radius: 50px; padding: 12px 24px; font-size: 13px; font-weight: 600;
  font-family: 'DM Sans', sans-serif; cursor: pointer; transition: all 0.2s; margin-top: 12px;
}
.btn-print:hover { background: rgba(255,255,255,0.1); color: white; }

@media print {
  .nav, .page-nav, .progress-strip { display: none !important; }
  .report-wrap { padding-top: 0; }
  .report-section { page-break-inside: avoid; }
}
@media (max-width: 600px) {
  .nav { padding: 12px 20px; }
  .report-section { padding: 36px 24px; }
  .report-cover { padding: 40px 24px; }
  .rc-verse { display: none; }
  .questions-wrap { padding: 60px 20px 100px; }
  .gdb-grid { grid-template-columns: 1fr; }
  .page-nav { padding: 12px 20px; }
  .passion-grid { grid-template-columns: 1fr; }
}
</style>
</head>
<body>

<div class="progress-strip"><div class="progress-fill" id="progressFill" style="width:0%"></div></div>

<nav class="nav">
  <div class="nav-logo">YOU<span>nique</span> Purpose</div>
  <div style="text-align:center">
    <div class="nav-section" id="navSection">Assessment</div>
  </div>
  <div class="nav-progress-text" id="navProgress">0 of 177</div>
</nav>

<!-- ══════════════ WELCOME ══════════════ -->
<div class="screen active" id="screen-welcome">
  <div class="welcome-wrap">
    <div class="welcome-inner">
      <div class="welcome-tag">Fifteen25 · YOUnique Purpose</div>
      <h1 class="welcome-h1">Discover your<br><em>YOUnique</em> Purpose</h1>
      <p class="welcome-p">Are you ready to discover the life God created for you? Your purpose is unique — shaped by your gifts, passions, and experiences. Discover how it all comes together to guide your life and make an impact.</p>
      <div class="welcome-stats">
        <div class="ws-item"><div class="ws-num">177</div><div class="ws-label">Questions</div></div>
        <div class="ws-item"><div class="ws-num">6</div><div class="ws-label">Frameworks</div></div>
        <div class="ws-item"><div class="ws-num">~30</div><div class="ws-label">Minutes</div></div>
        <div class="ws-item"><div class="ws-num">1</div><div class="ws-label">Full Report</div></div>
      </div>
      <div class="form-group">
        <label class="form-label">Your Name</label>
        <input class="form-input" type="text" id="userName" placeholder="Enter your name..." />
      </div>
      <div class="form-group">
        <label class="form-label">Email Address</label>
        <input class="form-input" type="email" id="userEmail" placeholder="your@email.com" />
      </div>
      <button class="btn-start" onclick="startAssessment()">
        Begin My Assessment
        <svg width="16" height="16" viewBox="0 0 16 16" fill="none"><path d="M3 8H13M13 8L9 4M13 8L9 12" stroke="white" stroke-width="2" stroke-linecap="round"/></svg>
      </button>
      <div class="welcome-verse">
        "For we are God's masterpiece. He has created us anew in Christ Jesus, so we can do the good things he planned for us long ago."
        <cite>Ephesians 2:10</cite>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════ QUESTIONS ══════════════ -->
<div class="screen" id="screen-questions">
  <div class="questions-wrap" id="questionsWrap"></div>
</div>

<!-- ══════════════ REPORT ══════════════ -->
<div class="screen" id="screen-report">
  <div class="report-wrap" id="reportContent"></div>
</div>

<!-- ══════════════ PAGE NAV ══════════════ -->
<div class="page-nav" id="pageNav" style="display:none">
  <button class="btn-back" id="btnBack" onclick="prevPage()">
    <svg width="14" height="14" viewBox="0 0 14 14" fill="none"><path d="M11 7H3M3 7L7 3M3 7L7 11" stroke="currentColor" stroke-width="1.8" stroke-linecap="round"/></svg>
    Back
  </button>
  <div style="display:flex;flex-direction:column;align-items:center;gap:4px">
    <div class="page-counter" id="pageCounter">Page 1</div>
    <div class="unanswered-warning" id="unansweredWarning">Please answer all questions to continue</div>
  </div>
  <button class="btn-next" id="btnNext" onclick="nextPage()">
    Continue
    <svg width="14" height="14" viewBox="0 0 14 14" fill="none"><path d="M3 7H11M11 7L7 3M11 7L7 11" stroke="white" stroke-width="1.8" stroke-linecap="round"/></svg>
  </button>
</div>

<script>
// ════════════════════════════════════════════════════════════
// DATA — All 177 questions with scoring keys
// ════════════════════════════════════════════════════════════

const SECTIONS = [
  { id:'gifts', name:'Spiritual Gifts', count:48 },
  { id:'passion', name:'Passion', count:22 },
  { id:'via', name:'Potential', count:24 },
  { id:'riasec', name:'Career Interests', count:18 },
  { id:'personality', name:'Personality', count:40 },
  { id:'pathways', name:'Pathways', count:25 }
];

// All questions flat — each has: text, section, key
const ALL_QUESTIONS = [
  // ─── SPIRITUAL GIFTS (48) ───
  {t:"I am good at setting goals and can motivate others to work toward a shared vision.",s:"gifts",k:"A"},
  {t:"I enjoy organizing people, tasks, or events so that everything runs smoothly.",s:"gifts",k:"B"},
  {t:"I believe God can do the impossible, and I trust Him even when I cannot see how things will work out.",s:"gifts",k:"C"},
  {t:"I know the Bible well and often find myself explaining or correcting misunderstandings about it.",s:"gifts",k:"D"},
  {t:"When I know someone is in financial need, I am happy to give money or resources to help them.",s:"gifts",k:"E"},
  {t:"I can usually sense when something feels spiritually wrong in a situation, even before I know why.",s:"gifts",k:"F"},
  {t:"I love telling people about Jesus. I find it easy and natural to share my faith with others.",s:"gifts",k:"G"},
  {t:"I prefer to work behind the scenes and support others rather than being in front.",s:"gifts",k:"H"},
  {t:"Sometimes I seem to understand things about a person or situation that I could not have known on my own.",s:"gifts",k:"I"},
  {t:"I feel a strong sense of responsibility to look out for and protect the people I care about.",s:"gifts",k:"J"},
  {t:"I enjoy welcoming people into my home and making them feel comfortable and at ease.",s:"gifts",k:"K"},
  {t:"People often come to me for advice, and I give them wise, practical, and godly guidance.",s:"gifts",k:"L"},
  {t:"I find it easy to explain what the Bible means in a simple and clear way that others understand.",s:"gifts",k:"M"},
  {t:"I feel drawn to help people who are sick, struggling, or going through a difficult time.",s:"gifts",k:"N"},
  {t:"I naturally encourage people and help them feel better about themselves and their situation.",s:"gifts",k:"O"},
  {t:"When I see a need, my first instinct is to step in and help in a practical way.",s:"gifts",k:"P"},
  {t:"I can cast a clear vision, set goals, and help a group of people move forward to achieve them.",s:"gifts",k:"A"},
  {t:"When things are disorganized, I feel uncomfortable and want to step in to bring order.",s:"gifts",k:"B"},
  {t:"I often feel God calling me to trust Him and act on His Word, even when there is no visible proof yet.",s:"gifts",k:"C"},
  {t:"I enjoy explaining what the Bible says and helping people understand its meaning for daily life.",s:"gifts",k:"D"},
  {t:"I enjoy giving money or resources to support God's work — whether to a ministry or someone in need.",s:"gifts",k:"E"},
  {t:"I can usually tell whether a person's intentions are genuine or not, even if they seem fine on the surface.",s:"gifts",k:"F"},
  {t:"I think about sharing the message of Jesus with people who do not know Him almost every day.",s:"gifts",k:"G"},
  {t:"I find it deeply fulfilling to support and assist others as they carry out their calling or role.",s:"gifts",k:"H"},
  {t:"I love to study the Bible deeply and often discover truths or insights that others have not noticed.",s:"gifts",k:"I"},
  {t:"I notice when someone in my group is struggling, absent, or feeling left out, even if they have not said anything.",s:"gifts",k:"J"},
  {t:"I enjoy making newcomers, guests, and strangers feel welcomed, included, and at home.",s:"gifts",k:"K"},
  {t:"I can look at a complicated situation and help others find the wisest and most godly way forward.",s:"gifts",k:"L"},
  {t:"I love to teach others what I know about God and help them understand the Bible for themselves.",s:"gifts",k:"M"},
  {t:"I feel compassion for people that others might give up on, and I want to help them anyway.",s:"gifts",k:"N"},
  {t:"People around me would say that I am someone who always builds them up and gives them hope.",s:"gifts",k:"O"},
  {t:"I love to serve and contribute — whether in big or small ways — whenever there is a need.",s:"gifts",k:"P"},
  {t:"People naturally look to me for direction, and I feel confident leading and guiding a group.",s:"gifts",k:"A"},
  {t:"I naturally bring structure and order to situations that feel messy or unclear.",s:"gifts",k:"B"},
  {t:"When I or others face an impossible situation, I am the one who prays and believes God for a miracle.",s:"gifts",k:"C"},
  {t:"I enjoy speaking in front of people and communicating God's message clearly and powerfully.",s:"gifts",k:"D"},
  {t:"Giving generously comes naturally to me. I do not hesitate to give money when someone truly needs it.",s:"gifts",k:"E"},
  {t:"I often have a strong inner sense about whether a decision is right or wrong, before the evidence is clear.",s:"gifts",k:"F"},
  {t:"People around me know that I regularly talk to others about Jesus and share my faith.",s:"gifts",k:"G"},
  {t:"I love helping others grow and succeed, even if I get no credit for the role I played.",s:"gifts",k:"H"},
  {t:"I have a strong desire to understand spiritual truth deeply, and I believe God reveals things to me for others.",s:"gifts",k:"I"},
  {t:"When someone I know is hurting, I feel a strong pull to be with them and support them.",s:"gifts",k:"J"},
  {t:"I have a gift for making people feel instantly welcome, comfortable, and valued when they enter a space.",s:"gifts",k:"K"},
  {t:"The people around me would say that my advice is wise, balanced, and reflects more than just common sense.",s:"gifts",k:"L"},
  {t:"I am passionate about teaching people the Bible and helping them understand and apply God's Word.",s:"gifts",k:"M"},
  {t:"I feel motivated to do practical acts of service for people who are poor, marginalized, or overlooked.",s:"gifts",k:"N"},
  {t:"It bothers me deeply when I see someone feeling discouraged or defeated. I want to lift them back up.",s:"gifts",k:"O"},
  {t:"I am happy to take on any task — big or small — if it contributes to something meaningful.",s:"gifts",k:"P"},
  // ─── PASSION (22) ───
  {t:"I love spending time with and helping children between the ages of 4 and 12.",s:"passion",k:"people_kids"},
  {t:"I enjoy mentoring and being around teenagers between the ages of 13 and 17.",s:"passion",k:"people_teens"},
  {t:"I feel most alive when I am working with young people between the ages of 18 and 21.",s:"passion",k:"people_youth"},
  {t:"I enjoy supporting young adults between 22 and 25 as they navigate life decisions.",s:"passion",k:"people_youngadults"},
  {t:"I like working alongside and serving adults between the ages of 25 and 65.",s:"passion",k:"people_adults"},
  {t:"I enjoy spending time with and caring for elderly people who are 65 years and above.",s:"passion",k:"people_elderly"},
  {t:"I care deeply about helping people grow in their faith and relationship with God.",s:"passion",k:"issues_spiritual"},
  {t:"I want to help people with their practical and physical needs — food, health, shelter, and basic resources.",s:"passion",k:"issues_physical"},
  {t:"I am moved to help people with their emotions, relationships, and mental wellbeing.",s:"passion",k:"issues_relational"},
  {t:"I enjoy helping people learn, think clearly, and grow in knowledge and understanding.",s:"passion",k:"issues_intellectual"},
  {t:"I feel comfortable taking risks even when the outcome is uncertain.",s:"passion",k:"roles_risk"},
  {t:"I prefer to think things through carefully before making any move, even when others want to act fast.",s:"passion",k:"roles_cautious"},
  {t:"I enjoy finding new and creative ways of doing things rather than following set procedures.",s:"passion",k:"roles_change"},
  {t:"I prefer doing things in a proven, reliable way rather than trying new approaches.",s:"passion",k:"roles_stability"},
  {t:"I can move forward on tasks even when I do not have all the information or clarity I need.",s:"passion",k:"roles_ambiguity"},
  {t:"I work best with clear instructions and a step-by-step structure to follow.",s:"passion",k:"roles_clarity"},
  {t:"How strongly do you feel called to share the good news of Jesus and help others know Him?",s:"passion",k:"ministry_evangelism"},
  {t:"How passionate are you about walking alongside someone and helping them grow deeper in their faith?",s:"passion",k:"ministry_discipleship"},
  {t:"How much do you feel moved to serve and care for people who are suffering or in need?",s:"passion",k:"ministry_compassion"},
  {t:"How strongly do you feel called to guide, inspire, and bring out the best in others?",s:"passion",k:"ministry_leadership"},
  {t:"How excited are you about reaching people from different cultures, languages, or nations with God's love?",s:"passion",k:"ministry_missions"},
  {t:"How passionate are you about creating content, art, music, or media that spreads God's message?",s:"passion",k:"ministry_creative"},
  // ─── VIA (24) ───
  {t:"I come up with new and original ideas — people would describe me as a creative person.",s:"via",k:"Creativity"},
  {t:"I am always asking questions and wanting to learn more about the world around me.",s:"via",k:"Curiosity"},
  {t:"I think things through carefully and look at a situation from multiple angles before deciding.",s:"via",k:"Judgment"},
  {t:"I love to learn new things — whether in school, from books, from people, or from life experience.",s:"via",k:"Love of Learning"},
  {t:"People often come to me for advice because I see the bigger picture and offer balanced perspectives.",s:"via",k:"Perspective"},
  {t:"I speak up for what I believe in, even when others disagree or it is not popular.",s:"via",k:"Bravery"},
  {t:"When I start something important, I keep going even when it gets hard or takes a long time.",s:"via",k:"Perseverance"},
  {t:"I always try to tell the truth and be genuine — I do not pretend to be someone I am not.",s:"via",k:"Honesty"},
  {t:"I approach life with energy and enthusiasm — I feel alive and excited about what I do.",s:"via",k:"Zest"},
  {t:"I value my close relationships deeply and care genuinely for the people I love.",s:"via",k:"Love"},
  {t:"I enjoy doing kind things for others, even when there is nothing in it for me.",s:"via",k:"Kindness"},
  {t:"I can easily read people's feelings and adapt how I interact with different kinds of people.",s:"via",k:"Social Intelligence"},
  {t:"I work well as part of a group — I contribute my part and support others to contribute theirs.",s:"via",k:"Teamwork"},
  {t:"I believe strongly in treating every person fairly, regardless of who they are or where they come from.",s:"via",k:"Fairness"},
  {t:"I naturally step into a leadership role in a group and help organise people toward a goal.",s:"via",k:"Leadership"},
  {t:"I find it easy to let go of grudges and forgive people who have hurt or wronged me.",s:"via",k:"Forgiveness"},
  {t:"I do not need to be the centre of attention — I am happy to let others take the praise.",s:"via",k:"Humility"},
  {t:"I think carefully before acting — I avoid impulsive decisions that I might regret later.",s:"via",k:"Prudence"},
  {t:"I am disciplined — when I set a goal for myself, I can control my actions to achieve it.",s:"via",k:"Self-Regulation"},
  {t:"I notice and appreciate beauty in things around me — in nature, art, music, or in people.",s:"via",k:"Appreciation of Beauty"},
  {t:"I regularly feel thankful for the good things in my life — big and small.",s:"via",k:"Gratitude"},
  {t:"Even in difficult times, I believe things will get better — I hold on to hope for the future.",s:"via",k:"Hope"},
  {t:"I use humour and laughter to bring joy to others and to get through difficult moments.",s:"via",k:"Humour"},
  {t:"My faith and relationship with God is a central and meaningful part of who I am and how I live.",s:"via",k:"Spirituality"},
  // ─── RIASEC (18) ───
  {t:"I enjoy working with my hands — building, fixing, making, or operating things.",s:"riasec",k:"R"},
  {t:"I am interested in practical skills like farming, construction, technology repair, or engineering.",s:"riasec",k:"R"},
  {t:"I prefer doing physical, hands-on work over sitting at a desk thinking about ideas.",s:"riasec",k:"R"},
  {t:"I enjoy researching, analysing information, and trying to understand how and why things work.",s:"riasec",k:"I"},
  {t:"I like solving complex problems by thinking deeply and logically rather than by trial and error.",s:"riasec",k:"I"},
  {t:"I am drawn to subjects like science, maths, medicine, law, or technology that require deep thinking.",s:"riasec",k:"I"},
  {t:"I enjoy expressing myself through art, music, writing, design, photography, or performance.",s:"riasec",k:"A"},
  {t:"I like to create things that are original and unique — I get bored doing things the same way every time.",s:"riasec",k:"A"},
  {t:"I am drawn to music, media, storytelling, graphic design, or creative ministry.",s:"riasec",k:"A"},
  {t:"I find it deeply rewarding to help, teach, mentor, or support other people.",s:"riasec",k:"S"},
  {t:"I prefer work that involves being with and serving people rather than working alone with tasks or machines.",s:"riasec",k:"S"},
  {t:"I am drawn to teaching, counselling, social work, healthcare, or community and ministry work.",s:"riasec",k:"S"},
  {t:"I enjoy persuading people, selling ideas, and leading others toward a goal or vision.",s:"riasec",k:"E"},
  {t:"I am excited by the idea of starting something new — a business, a project, a ministry, or a movement.",s:"riasec",k:"E"},
  {t:"I am drawn to leadership, entrepreneurship, business, law, or roles where I make decisions and drive change.",s:"riasec",k:"E"},
  {t:"I enjoy working with data, numbers, records, or detailed processes that require accuracy and order.",s:"riasec",k:"C"},
  {t:"I work best when there are clear rules, set procedures, and a structured system to follow.",s:"riasec",k:"C"},
  {t:"I am drawn to finance, accounting, administration, data management, or church/organisational operations.",s:"riasec",k:"C"},
  // ─── PERSONALITY (40) ───
  {t:"I feel most energized and alive when I am around other people.",s:"personality",k:"E"},
  {t:"I like to share my thoughts and feelings openly with others.",s:"personality",k:"E"},
  {t:"I prefer having a large circle of friends and acquaintances.",s:"personality",k:"E"},
  {t:"I enjoy being the centre of conversations and social gatherings.",s:"personality",k:"E"},
  {t:"I think better when I can talk things through with others rather than processing alone.",s:"personality",k:"E"},
  {t:"I feel most energized and restored when I have quiet time alone.",s:"personality",k:"I"},
  {t:"I prefer to keep my thoughts and feelings to myself rather than sharing openly.",s:"personality",k:"I"},
  {t:"I prefer having a small number of close, deep friendships.",s:"personality",k:"I"},
  {t:"I prefer to listen more than I speak in most conversations.",s:"personality",k:"I"},
  {t:"I process my thoughts best when I have time alone to think before responding.",s:"personality",k:"I"},
  {t:"I trust facts, details, and things I can see or touch more than gut feelings.",s:"personality",k:"S"},
  {t:"I prefer to focus on what is real and happening now rather than imagining possibilities.",s:"personality",k:"S"},
  {t:"I like step-by-step instructions with all the details laid out clearly.",s:"personality",k:"S"},
  {t:"I prefer doing things in a proven, reliable way that I know works.",s:"personality",k:"S"},
  {t:"I focus on practical, measurable outcomes rather than abstract ideas.",s:"personality",k:"S"},
  {t:"I trust my gut feelings and imagination more than facts and concrete details.",s:"personality",k:"N"},
  {t:"I prefer to imagine what could be possible in the future rather than focusing on now.",s:"personality",k:"N"},
  {t:"I like to understand the big picture first before worrying about the details.",s:"personality",k:"N"},
  {t:"I enjoy finding new and creative ways of doing things rather than sticking to what works.",s:"personality",k:"N"},
  {t:"I enjoy exploring ideas even without a clear or immediate practical outcome.",s:"personality",k:"N"},
  {t:"I make decisions based on logic and objective facts rather than feelings.",s:"personality",k:"T"},
  {t:"I can stay calm and detached when handling emotionally charged situations.",s:"personality",k:"T"},
  {t:"I value truth and directness, even if it means someone's feelings might be affected.",s:"personality",k:"T"},
  {t:"I am a fair and objective person — I try not to let emotions cloud my judgement.",s:"personality",k:"T"},
  {t:"I give feedback directly, even if it is hard for the other person to hear.",s:"personality",k:"T"},
  {t:"I make decisions based on how I feel and how they will affect the people around me.",s:"personality",k:"F"},
  {t:"I take things personally and feel them deeply, even when I know I probably shouldn't.",s:"personality",k:"F"},
  {t:"I value kindness and harmony more than being exactly right or technically correct.",s:"personality",k:"F"},
  {t:"I am a compassionate and empathetic person — I feel what others feel very deeply.",s:"personality",k:"F"},
  {t:"I encourage and build people up even when they make mistakes, rather than pointing out what went wrong.",s:"personality",k:"F"},
  {t:"I like to make plans and stick to them — I feel unsettled when plans change unexpectedly.",s:"personality",k:"J"},
  {t:"I feel most comfortable when things are decided and settled rather than open-ended.",s:"personality",k:"J"},
  {t:"I like having a regular schedule and routine to structure my days.",s:"personality",k:"J"},
  {t:"I tend to finish tasks well before deadlines rather than working best under last-minute pressure.",s:"personality",k:"J"},
  {t:"I am very organised and like my environment and plans to be in order.",s:"personality",k:"J"},
  {t:"I prefer to stay flexible and see how things unfold rather than committing to a plan.",s:"personality",k:"P"},
  {t:"I like to keep my options open for as long as possible before making a final decision.",s:"personality",k:"P"},
  {t:"I enjoy spontaneous and unplanned experiences rather than following a fixed schedule.",s:"personality",k:"P"},
  {t:"I work best when the deadline is close — pressure helps me focus and perform.",s:"personality",k:"P"},
  {t:"I am flexible and adapt easily to new or changing situations.",s:"personality",k:"P"},
  // ─── PATHWAYS (25) ───
  {t:"I regularly spend time reading the Bible and praying — this is a consistent habit in my life.",s:"pathways",k:"Faith"},
  {t:"I have a clear sense of what God is calling me to do with my life right now.",s:"pathways",k:"Faith"},
  {t:"I am actively part of a faith community, church group, or youth ministry.",s:"pathways",k:"Faith"},
  {t:"I feel equipped and ready to serve God in the area He is calling me to.",s:"pathways",k:"Faith"},
  {t:"I have identified a specific ministry, mission, or area of service that God has placed on my heart.",s:"pathways",k:"Faith"},
  {t:"My relationships with my family members are generally healthy, respectful, and loving.",s:"pathways",k:"Family"},
  {t:"When there is conflict in my family, I handle it in a calm and constructive way.",s:"pathways",k:"Family"},
  {t:"I feel emotionally close and connected to the people who matter most to me.",s:"pathways",k:"Family"},
  {t:"I invest regular, meaningful time into building strong relationships with my family.",s:"pathways",k:"Family"},
  {t:"I have a clear understanding of my role and responsibilities within my family.",s:"pathways",k:"Family"},
  {t:"I am learning to manage money wisely and I avoid spending more than I have.",s:"pathways",k:"Finances"},
  {t:"I give generously to God and others as a regular habit, not just when it is convenient.",s:"pathways",k:"Finances"},
  {t:"I have a basic plan for how I want to manage or save money for my future.",s:"pathways",k:"Finances"},
  {t:"I do not feel constantly stressed or anxious about money.",s:"pathways",k:"Finances"},
  {t:"I see whatever resources I have as a gift from God that I am responsible to use well.",s:"pathways",k:"Finances"},
  {t:"I am physically active and I take regular care of my body.",s:"pathways",k:"Fitness"},
  {t:"I get enough sleep and rest to feel energized for the next day.",s:"pathways",k:"Fitness"},
  {t:"I try to eat in a way that keeps me healthy and gives me energy.",s:"pathways",k:"Fitness"},
  {t:"I feel physically strong and healthy enough to pursue what God has called me to do.",s:"pathways",k:"Fitness"},
  {t:"I take care of my emotional and mental health — I know when I need rest, help, or support.",s:"pathways",k:"Fitness"},
  {t:"I have at least one trusted friend I can be completely honest with about my life.",s:"pathways",k:"Friends"},
  {t:"I have a group of people around me who encourage my faith and help me grow.",s:"pathways",k:"Friends"},
  {t:"I regularly put time and effort into building and maintaining meaningful friendships.",s:"pathways",k:"Friends"},
  {t:"I have people in my life who challenge me, hold me accountable, and help me become better.",s:"pathways",k:"Friends"},
  {t:"I feel that I truly belong somewhere — in a community where people know and care about me.",s:"pathways",k:"Friends"}
];

const GIFT_META = {
  A:{name:"Leadership",thrust:"Influencing others toward vision",cat:"Motivational",pct:"2%",desc:"Confidence to step forward, give direction, and provide motivation to fulfil a dream or vision. The capacity to exercise influence over a group so as to lead it toward a goal or purpose.",bible:"Romans 12:8 · John 21:15-17",ministry:"Pastor, ministry team lead, fellowship coordinator, pastoral staff",careers:"CEO, Business Manager, Project Manager, Startup Founder, Operations Director, Nonprofit Manager, Team Coach",blindspot:"Dominance: Task focused, demanding, insensitive, controlling"},
  B:{name:"Administration",thrust:"Supportive organizational abilities",cat:"Ministry",pct:"18%",desc:"The gift that enables a believer to formulate, direct, and carry out plans necessary to fulfil a purpose.",bible:"1 Corinthians 12:28 · Acts 14:23",ministry:"Finance coordinator, ministry administrator, event coordinator",careers:"Project Manager, Operations Manager, Event Planner, Logistics Coordinator, Executive Assistant",blindspot:"Over-control: perfectionism, rigidity, losing people in pursuit of order"},
  C:{name:"Faith",thrust:"Trusting God for the impossible",cat:"Manifestation",pct:"~5%",desc:"Extraordinary confidence that God will intervene and act on His promises, even when circumstances seem impossible.",bible:"1 Corinthians 12:9 · Hebrews 11:1",ministry:"Intercession team, church planting, mission fields",careers:"Chaplain, Missionary, Ministry Leader, Prayer Coordinator",blindspot:"Presumption: confusing personal desire with God's will"},
  D:{name:"Preaching",thrust:"To provide correction or perspective",cat:"Motivational",pct:"3%",desc:"The supernatural ability to effectively proclaim and communicate the Word of God providing insight, warning, correction and encouragement.",bible:"1 Timothy 4:12-16 · 2 Timothy 4:1-5",ministry:"Pastor, conference speaker, Sunday teacher, small group leader",careers:"Motivational Speaker, Corporate Trainer, Lawyer, News Anchor, Author",blindspot:"Harshness: delivering truth without grace or sensitivity"},
  E:{name:"Giving",thrust:"Channelling God's resources to others",cat:"Ministry",pct:"7%",desc:"Enables a believer to recognize God's blessings and respond by generously and sacrificially giving of one's resources — time, talent, and treasure.",bible:"2 Corinthians 9:6-15 · Romans 12:8",ministry:"Stewardship ministry, missions funding, community relief",careers:"Financial Advisor, Philanthropy Manager, Social Entrepreneur, Stewardship Consultant",blindspot:"Control: attaching strings to giving, using generosity for influence"},
  F:{name:"Discernment",thrust:"Distinguishing truth from deception",cat:"Manifestation",pct:"~4%",desc:"The ability to distinguish between the spirit of truth and the spirit of error — to recognize what is truly of God.",bible:"1 Corinthians 12:10 · 1 John 4:1",ministry:"Counselling ministry, leadership advisory, intercessory team",careers:"Counselor, Advisor, Spiritual Director, Investigator",blindspot:"Suspicion: seeing threats everywhere, damaging relationships"},
  G:{name:"Evangelism",thrust:"Introducing others to the Gospel",cat:"Motivational",pct:"4%",desc:"Moves believers to reach non-believers in such a way that they are baptized and become active members of the Christian community.",bible:"Matthew 28:16-20 · Ephesians 4:11-16",ministry:"Outreach team, evangelism programs, advertising and marketing",careers:"Sales Executive, Marketing Strategist, Brand Ambassador, Community Organizer",blindspot:"Pushiness: making people feel pressured rather than loved"},
  H:{name:"Helps",thrust:"Aiding others in practical ways",cat:"Ministry",pct:"5%",desc:"God-given special ability to serve and strengthen the body of Christ by offering assistance in reaching goals that glorify God.",bible:"Mark 15:40-41 · Romans 16:1-2",ministry:"Support staff, behind-the-scenes ministry, setup and operations",careers:"Social Worker, Caregiver, Ministry Support Staff, Volunteer Coordinator",blindspot:"People-pleasing: difficulty saying no, burning out in service"},
  I:{name:"Knowledge",thrust:"Supernatural revelation of truth",cat:"Manifestation",pct:"~4%",desc:"The supernatural ability to receive specific insights and understanding that could not be acquired through natural means.",bible:"1 Corinthians 12:8 · Daniel 1:17",ministry:"Bible study leader, teaching team, theological research",careers:"Researcher, Teacher, Theologian, Author, Investigative Journalist",blindspot:"Pride: using knowledge to impress rather than serve"},
  J:{name:"Shepherding",thrust:"Caring for the growth of followers",cat:"Motivational",pct:"1%",desc:"The gift that gives a believer confidence, capability, and compassion to provide spiritual leadership and direction for individuals or groups.",bible:"John 10:1-18 · 1 Peter 5:1-3",ministry:"Small group leader, discipleship leader, pastoral care",careers:"Social Worker, Life Coach, Human Resources Specialist, Counselor",blindspot:"Enmeshment: over-involvement, difficulty releasing people to grow independently"},
  K:{name:"Hospitality",thrust:"Making others feel welcomed",cat:"Ministry",pct:"8%",desc:"The gift that enables a believer to joyfully welcome and receive guests and those in need of food and lodging.",bible:"Romans 12:13 · Hebrews 13:1-2",ministry:"Greeters, welcome team, small group host",careers:"Hotel Manager, Guest Relations Officer, Event Host, Restaurant Manager",blindspot:"Superficiality: mistaking social warmth for genuine spiritual care"},
  L:{name:"Wisdom",thrust:"Application of divine understanding",cat:"Manifestation",pct:"~4%",desc:"The ability to apply spiritual knowledge practically — to see situations from God's perspective and give godly direction.",bible:"1 Corinthians 12:8 · James 1:5",ministry:"Counselling, elder team, mentoring ministry",careers:"Life Coach, Counselor, Mediator, Strategic Advisor",blindspot:"Passivity: withholding wisdom when it is needed, fear of being wrong"},
  M:{name:"Teaching",thrust:"To clarify truth",cat:"Motivational",pct:"2%",desc:"This gift enables a believer to communicate a personal understanding of the Bible and faith in such a way that it becomes clear and understood by others.",bible:"Romans 12:7 · 1 Corinthians 12:28",ministry:"Sunday school teacher, discipleship leader, Bible study facilitator",careers:"School Teacher, Corporate Trainer, Educational Consultant, Professor",blindspot:"Ivory tower: valuing knowledge over people, becoming detached from practical needs"},
  N:{name:"Mercy",thrust:"Empathetic care for those who hurt",cat:"Ministry",pct:"17%",desc:"Feel genuine empathy and compassion for individuals who suffer distressing physical, mental, or emotional problems and to translate that compassion into action.",bible:"Luke 7:12-15 · Romans 12:6-8",ministry:"Home/hospital visitation, social ministry, support groups",careers:"Counselor, Nurse, Chaplain, Social Worker, Therapist",blindspot:"Rescuing: enabling others, blurring boundaries, absorbing others' pain"},
  O:{name:"Encouragement",thrust:"Lifting others through biblical truth",cat:"Ministry",pct:"10%",desc:"The gift that moves the believer to minister words of encouragement, consolation, and comfort from God's word to help others complete their tasks.",bible:"John 14:1 · Romans 12:8",ministry:"Hospital visitation, peer counselling, discipleship",careers:"Life Coach, Counselor, Motivational Speaker, Youth Worker",blindspot:"Flattery: encouraging without honesty, avoiding necessary truth"},
  P:{name:"Service",thrust:"Serving the body behind the scenes",cat:"Ministry",pct:"1%",desc:"The gift to invest the talents one has in the life and ministry of other members of the body, thus enabling those others to increase the effectiveness of their own gifts.",bible:"Luke 23:50-54 · Romans 16:1-16",ministry:"Operations, logistics, maintenance, behind-the-scenes support",careers:"Administrative Assistant, Facilities Manager, IT Support, Logistics Coordinator",blindspot:"Busyness: so focused on tasks that relationships and vision are missed"}
};

const VIA_VIRTUES = {
  "Creativity":"Wisdom","Curiosity":"Wisdom","Judgment":"Wisdom","Love of Learning":"Wisdom","Perspective":"Wisdom",
  "Bravery":"Courage","Perseverance":"Courage","Honesty":"Courage","Zest":"Courage",
  "Love":"Humanity","Kindness":"Humanity","Social Intelligence":"Humanity",
  "Teamwork":"Justice","Fairness":"Justice","Leadership":"Justice",
  "Forgiveness":"Temperance","Humility":"Temperance","Prudence":"Temperance","Self-Regulation":"Temperance",
  "Appreciation of Beauty":"Transcendence","Gratitude":"Transcendence","Hope":"Transcendence","Humour":"Transcendence","Spirituality":"Transcendence"
};

const RIASEC_META = {
  R:{name:"Realistic",label:"The Builder",desc:"Hands-on, practical, works with tools, nature, or machines. You thrive when you can see, touch, and create tangible results.",careers:"Engineering · Agriculture · IT · Construction · Healthcare · Mechanics"},
  I:{name:"Investigative",label:"The Thinker",desc:"Analytical, curious, loves research and solving complex problems. You are energised by questions and ideas.",careers:"Science · Research · Technology · Law · Medicine · Academia"},
  A:{name:"Artistic",label:"The Creator",desc:"Creative, expressive, original — works best without rigid rules. You bring beauty and meaning to everything you do.",careers:"Music · Design · Writing · Media · Creative Ministry · Film"},
  S:{name:"Social",label:"The Helper",desc:"People-focused, teaches, counsels, and cares for others. You are most fulfilled when you can make a direct difference in someone's life.",careers:"Teaching · Counselling · Ministry · Social Work · Healthcare · Community Development"},
  E:{name:"Enterprising",label:"The Leader",desc:"Persuasive, ambitious, leads and influences others. You are energised by vision, momentum, and taking initiative.",careers:"Business · Entrepreneurship · Law · Ministry Leadership · Sales · Politics"},
  C:{name:"Conventional",label:"The Organiser",desc:"Detail-oriented, systematic, follows structure and order. You make organisations run with precision and reliability.",careers:"Finance · Administration · Data · Church Admin · Accounting · Research Management"}
};

const MBTI_META = {
  INTJ:{name:"Mastermind",role:"Strategist",pct:"2.1%",desc:"INTJs are quiet, reserved, and highly strategic. They develop plans and strategies with ruthless clarity, and don't like uncertainty. Visionary, independent, and relentlessly purposeful.",strengths:"High self-confidence · Independent · Strategic · Hard-working · Decisive · Honest",weaknesses:"Can be arrogant · Perfectionist · Judgemental · Overly analytical · Insensitive"},
  INTP:{name:"Thinker",role:"Strategist",pct:"3.3%",desc:"INTPs are known for their brilliant theories and unrelenting logic. They love patterns and are natural problem-solvers — though they can lose themselves in ideas.",strengths:"Abstract thinker · Honest · Objective · Imaginative · Open-minded · Versatile",weaknesses:"Absent-minded · Insensitive · Very private · Condescending · Loathes rules"},
  ENTJ:{name:"Commander",role:"Strategist",pct:"1.8%",desc:"ENTJs are natural-born leaders. They live in a world of possibilities and see every challenge as an opportunity. Decisive, energetic, and always moving toward a goal.",strengths:"High confidence · Strategic · Energetic · Charismatic · Honest · Very efficient",weaknesses:"Stubborn · Arrogant · Cold · Poor with emotions · Impatient · Intolerant"},
  ENTP:{name:"Visionary",role:"Strategist",pct:"3.2%",desc:"ENTPs are highly intelligent and need constant mental stimulation. They discuss theories and ideas with passion, always questioning the status quo.",strengths:"Quick thinker · Excellent brainstormer · Original · Charismatic · Energetic · Open-minded",weaknesses:"Argumentative · Insensitive · Easily bored · Absent-minded · Loathes routine"},
  INFJ:{name:"Counselor",role:"Diplomat",pct:"1.5%",desc:"INFJs are visionaries and idealists with creative imagination and brilliant ideas. They have a deeper way of looking at the world — always searching for deeper meaning.",strengths:"Creative · Insightful · Inspiring · Decisive · Determined · Altruistic",weaknesses:"Sensitive · Extremely private · Perfectionistic · Easily burned out · Preoccupied"},
  INFP:{name:"Idealist",role:"Diplomat",pct:"4.4%",desc:"INFPs are quiet, reflective, and deeply idealistic. They love analyzing symbols and meaning, and are driven by a deep desire to make the world more in line with their values.",strengths:"Passionate · Altruistic · Very creative · Open-minded · Idealistic · Seek harmony",weaknesses:"Too altruistic · Dislikes data · Takes things personally · May be impractical"},
  ENFJ:{name:"Giver",role:"Diplomat",pct:"2.5%",desc:"ENFJs are people-focused individuals — extroverted, idealistic, charismatic, and highly principled. They know how to connect with others no matter their background.",strengths:"Very charismatic · Altruistic · Natural leader · Decisive · Creative · Reliable",weaknesses:"Too selfless · Overly idealistic · Too sensitive · Vulnerable to criticism"},
  ENFP:{name:"Champion",role:"Diplomat",pct:"8.1%",desc:"ENFPs are highly individualistic champions who strive toward creating their own methods and ideas. They have strong intuition and operate from the heart.",strengths:"Observant · Popular · Energetic · Creative · Open-minded · Excellent communicator",weaknesses:"Highly emotional · Poor practical skills · Overthinks · Gets stressed easily"},
  ISTJ:{name:"Inspector",role:"Guardian",pct:"11.6%",desc:"ISTJs appear serious and formal. They love traditions and old-school values that uphold patience, hard work, and social responsibility. Reliable and thorough.",strengths:"Strong-willed · Very responsible · Good at creating order · Calm and practical · Honest",weaknesses:"Stubborn · Insensitive · Judgmental · Always by the book · Blames themselves"},
  ISFJ:{name:"Nurturer",role:"Guardian",pct:"13.8%",desc:"ISFJs are warm philanthropists, always ready to give back. They value harmony and cooperation and are likely to be sensitive to other people's feelings.",strengths:"Very supportive · Loyal · Reliable · Imaginative · Patient · Good practical skills",weaknesses:"Humble to a fault · Overloads themselves · Takes things too personally · Stubborn"},
  ESTJ:{name:"Supervisor",role:"Guardian",pct:"8.7%",desc:"ESTJs are organised, honest, dedicated, and traditional. Great believers in doing what is right and socially acceptable, they are glad to take their place as leaders.",strengths:"Dedicated · Excellent organizer · Loyal · Strong-willed · Direct · Very responsible",weaknesses:"Inflexible · Judgmental · Struggles to express emotions · Overly status-conscious"},
  ESFJ:{name:"Provider",role:"Guardian",pct:"12.0%",desc:"ESFJs are social butterflies. Their need to interact and make people happy makes them popular and well-loved. They excel at organising communities.",strengths:"Looks for win-win · Very loyal · Warm · Connects easily with people · Reliable",weaknesses:"Status-obsessed · Unwilling to improvise · Vulnerable to criticism · Too selfless"},
  ISTP:{name:"Craftsman",role:"Pioneer",pct:"5.4%",desc:"ISTPs are rational and logical but also quite spontaneous. They are mysterious in appearance but utterly practical in action — masters of tools and technique.",strengths:"Optimistic · Creative and practical · Relaxed · Spontaneous yet rational · Bold",weaknesses:"Stubborn · Private · Gets bored quickly · Insensitive · Dislikes commitment"},
  ISFP:{name:"Composer",role:"Pioneer",pct:"8.8%",desc:"ISFPs are quiet but warm, approachable, and friendly once you know them. They live fully in the present and love exploring new experiences and sensations.",strengths:"Sensitive · Charming · Open-minded · Artistic · Imaginative · Curious",weaknesses:"Low self-esteem · Stress easily · Very competitive · Fiercely independent"},
  ESTP:{name:"Doer",role:"Pioneer",pct:"4.3%",desc:"ESTPs leap before they look. They are governed by a need for social interaction, logic, and freedom. They fix mistakes as they go rather than planning ahead.",strengths:"Bold · Honest · Perceptive · Rational · Practical · Great people skills",weaknesses:"Dislikes rules · Takes big risks · Can be insensitive · Impatient · Misses big picture"},
  ESFP:{name:"Performer",role:"Pioneer",pct:"8.5%",desc:"ESFPs love the spotlight. Born to be in front of others, they are warm, generous, enthusiastic learners who bring energy and joy to every room they enter.",strengths:"Bold · Excellent people skills · Great aesthetics · Practical · Very observant",weaknesses:"Struggles to focus · Very sensitive · Poor planner · Always seeks excitement"}
};

// ════════════════════════════════════════════════════════════
// STATE
// ════════════════════════════════════════════════════════════
let state = {
  name: '', email: '',
  answers: {}, // index -> value (0-5)
  currentPage: 0,
  pages: [], // array of arrays of question indices
  totalAnswered: 0
};

const PER_PAGE = 10;

// ════════════════════════════════════════════════════════════
// SHUFFLE within section boundaries
// ════════════════════════════════════════════════════════════
function shuffleSectionInPlace(arr) {
  // Shuffle within each section, keep sections ordered
  let result = [];
  let sectionStart = 0;
  SECTIONS.forEach(sec => {
    let slice = arr.slice(sectionStart, sectionStart + sec.count);
    for (let i = slice.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      [slice[i], slice[j]] = [slice[j], slice[i]];
    }
    result = result.concat(slice);
    sectionStart += sec.count;
  });
  return result;
}

function buildPages() {
  const indices = ALL_QUESTIONS.map((_,i) => i);
  const shuffled = shuffleSectionInPlace(indices);
  const pages = [];
  for (let i = 0; i < shuffled.length; i += PER_PAGE) {
    pages.push(shuffled.slice(i, i + PER_PAGE));
  }
  state.pages = pages;
}

// ════════════════════════════════════════════════════════════
// NAVIGATION
// ════════════════════════════════════════════════════════════
function showScreen(id) {
  document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
  document.getElementById('screen-' + id).classList.add('active');
}

function updateProgress() {
  const total = ALL_QUESTIONS.length;
  const answered = Object.keys(state.answers).length;
  const pct = Math.round((answered / total) * 100);
  document.getElementById('progressFill').style.width = pct + '%';
  document.getElementById('navProgress').textContent = answered + ' of ' + total;
  // Section name
  const firstQ = state.pages[state.currentPage]?.[0] ?? 0;
  const sec = ALL_QUESTIONS[firstQ]?.s;
  const secName = SECTIONS.find(s => s.id === sec)?.name || 'Assessment';
  document.getElementById('navSection').textContent = secName;
}

function startAssessment() {
  const name = document.getElementById('userName').value.trim();
  const email = document.getElementById('userEmail').value.trim();
  if (!name) { alert('Please enter your name to begin.'); return; }
  state.name = name;
  state.email = email;
  buildPages();
  showScreen('questions');
  document.getElementById('pageNav').style.display = 'flex';
  renderPage(0);
  updateProgress();
}

function renderPage(pageIndex) {
  state.currentPage = pageIndex;
  const wrap = document.getElementById('questionsWrap');
  const qIndices = state.pages[pageIndex];
  wrap.innerHTML = '';

  qIndices.forEach((qIdx, localIdx) => {
    const q = ALL_QUESTIONS[qIdx];
    const answered = state.answers[qIdx] !== undefined;
    const block = document.createElement('div');
    block.className = 'q-block' + (!answered && localIdx > 0 ? ' faded' : ' active');
    block.id = 'qblock-' + qIdx;

    const sizes = [32, 38, 42, 42, 48, 54];
    let circlesHtml = '';
    for (let v = 0; v <= 5; v++) {
      const sel = state.answers[qIdx] === v ? ' selected' : '';
      circlesHtml += `<div class="q-circle${sel}" data-val="${v}" data-qidx="${qIdx}" onclick="selectAnswer(${qIdx}, ${v})" title="${['Never','Rarely','Sometimes','Often','Usually','Always'][v]}"></div>`;
    }

    block.innerHTML = `
      <div class="q-statement">${q.t}</div>
      <div class="q-scale-row">
        <span class="q-scale-label never">Never</span>
        <div class="q-circles">${circlesHtml}</div>
        <span class="q-scale-label always">Always</span>
      </div>
    `;
    wrap.appendChild(block);
  });

  // Page counter
  document.getElementById('pageCounter').textContent = `Page ${pageIndex + 1} of ${state.pages.length}`;
  document.getElementById('unansweredWarning').style.display = 'none';

  // Back button
  document.getElementById('btnBack').style.visibility = pageIndex === 0 ? 'hidden' : 'visible';

  // Next button text
  const isLast = pageIndex === state.pages.length - 1;
  document.getElementById('btnNext').textContent = isLast ? 'See My Results →' : 'Continue →';

  window.scrollTo({ top: 0, behavior: 'smooth' });
  updateFading(pageIndex);
  updateProgress();
}

function selectAnswer(qIdx, value) {
  state.answers[qIdx] = value;
  // Update circles for this question
  const block = document.getElementById('qblock-' + qIdx);
  block.querySelectorAll('.q-circle').forEach(c => {
    c.classList.remove('selected');
    if (parseInt(c.dataset.val) === value) c.classList.add('selected');
  });
  block.classList.remove('faded');
  block.classList.add('active');
  updateFading(state.currentPage);
  updateProgress();
  // Auto-advance to next unanswered question on page
  const pageQs = state.pages[state.currentPage];
  const nextUnanswered = pageQs.find(qi => state.answers[qi] === undefined);
  if (nextUnanswered !== undefined) {
    const nextBlock = document.getElementById('qblock-' + nextUnanswered);
    if (nextBlock) {
      setTimeout(() => nextBlock.scrollIntoView({ behavior: 'smooth', block: 'center' }), 150);
    }
  }
}

function updateFading(pageIndex) {
  const qIndices = state.pages[pageIndex];
  let foundUnanswered = false;
  qIndices.forEach(qIdx => {
    const block = document.getElementById('qblock-' + qIdx);
    if (!block) return;
    if (state.answers[qIdx] !== undefined) {
      block.classList.remove('faded');
      block.classList.add('active');
    } else if (!foundUnanswered) {
      foundUnanswered = true;
      block.classList.remove('faded');
      block.classList.add('active');
    } else {
      block.classList.add('faded');
      block.classList.remove('active');
    }
  });
}

function nextPage() {
  const pageQs = state.pages[state.currentPage];
  const unanswered = pageQs.filter(qi => state.answers[qi] === undefined);
  if (unanswered.length > 0) {
    document.getElementById('unansweredWarning').style.display = 'block';
    const firstUnanswered = document.getElementById('qblock-' + unanswered[0]);
    if (firstUnanswered) firstUnanswered.scrollIntoView({ behavior: 'smooth', block: 'center' });
    return;
  }
  document.getElementById('unansweredWarning').style.display = 'none';
  const isLast = state.currentPage === state.pages.length - 1;
  if (isLast) {
    generateReport();
  } else {
    renderPage(state.currentPage + 1);
  }
}

function prevPage() {
  if (state.currentPage > 0) renderPage(state.currentPage - 1);
}

// ════════════════════════════════════════════════════════════
// SCORING
// ════════════════════════════════════════════════════════════
function score() {
  // GIFTS
  const gifts = {A:0,B:0,C:0,D:0,E:0,F:0,G:0,H:0,I:0,J:0,K:0,L:0,M:0,N:0,O:0,P:0};
  // PASSION
  const people = {kids:0,teens:0,youth:0,youngadults:0,adults:0,elderly:0};
  const issues = {spiritual:0,physical:0,relational:0,intellectual:0};
  const roles = {risk:0,cautious:0,change:0,stability:0,ambiguity:0,clarity:0};
  const ministry = {evangelism:0,discipleship:0,compassion:0,leadership:0,missions:0,creative:0};
  // VIA
  const via = {};
  VIA_QUESTIONS_LIST = ALL_QUESTIONS.filter(q=>q.s==='via');
  // RIASEC
  const riasec = {R:0,I:0,A:0,S:0,E:0,C:0};
  const riasecCount = {R:0,I:0,A:0,S:0,E:0,C:0};
  // PERSONALITY
  const pers = {E:0,I:0,S:0,N:0,T:0,F:0,J:0,P:0};
  // PATHWAYS
  const paths = {Faith:0,Family:0,Finances:0,Fitness:0,Friends:0};
  const pathsCount = {Faith:0,Family:0,Finances:0,Fitness:0,Friends:0};

  ALL_QUESTIONS.forEach((q, idx) => {
    const val = state.answers[idx] ?? 0;
    if (q.s === 'gifts') gifts[q.k] += val;
    if (q.s === 'passion') {
      const [cat, sub] = q.k.split('_');
      if (cat === 'people') people[sub] = (people[sub]||0) + val;
      if (cat === 'issues') issues[sub] = (issues[sub]||0) + val;
      if (cat === 'roles') roles[sub] = (roles[sub]||0) + val;
      if (cat === 'ministry') ministry[sub] = (ministry[sub]||0) + val;
    }
    if (q.s === 'via') via[q.k] = (via[q.k]||0) + val;
    if (q.s === 'riasec') { riasec[q.k] += val; riasecCount[q.k]++; }
    if (q.s === 'personality') pers[q.k] += val;
    if (q.s === 'pathways') { paths[q.k] += val; pathsCount[q.k]++; }
  });

  // Sort gifts
  const giftsSorted = Object.entries(gifts).sort((a,b)=>b[1]-a[1]);
  const giftsMax = giftsSorted[0][1] || 1;

  // Top people
  const peopleSorted = Object.entries(people).sort((a,b)=>b[1]-a[1]);
  const issuesSorted = Object.entries(issues).sort((a,b)=>b[1]-a[1]);
  const ministrySorted = Object.entries(ministry).sort((a,b)=>b[1]-a[1]);

  // Role score
  const roleScore = (roles.risk||0)*2 + (roles.change||0)*2 + (roles.ambiguity||0)*2 - (roles.cautious||0) - (roles.stability||0) - (roles.clarity||0);
  let roleLabel = 'Doer', roleDesc = 'Action-oriented, reliable, hands-on — you make things happen.';
  if (roleScore >= 15) { roleLabel = 'Thinker / Pioneer'; roleDesc = 'You love thinking deeply, exploring new ideas, and challenging the status quo.'; }
  else if (roleScore >= 10) { roleLabel = 'Innovator'; roleDesc = 'You are energized by new ideas, fresh thinking, and creative problem-solving.'; }
  else if (roleScore >= 5) { roleLabel = 'Manager'; roleDesc = 'You bring structure, systems, and strategy to turn vision into reality.'; }
  else if (roleScore >= 0) { roleLabel = 'Supervisor'; roleDesc = 'You guide and support teams, bridging plans and day-to-day action.'; }

  // VIA top 5
  const viaSorted = Object.entries(via).sort((a,b)=>b[1]-a[1]);

  // RIASEC
  const riasecSorted = Object.entries(riasec).sort((a,b)=>b[1]-a[1]);
  const riasecMax = riasecSorted[0][1] || 1;
  const hollandCode = riasecSorted.slice(0,3).map(([k])=>k).join('');

  // Personality type
  const EI = pers.E >= pers.I ? 'E' : 'I';
  const SN = pers.S >= pers.N ? 'S' : 'N';
  const TF = pers.T >= pers.F ? 'T' : 'F';
  const JP = pers.J >= pers.P ? 'J' : 'P';
  const mbtiType = EI+SN+TF+JP;
  const eiMax = Math.max(pers.E,pers.I)||1;
  const snMax = Math.max(pers.S,pers.N)||1;
  const tfMax = Math.max(pers.T,pers.F)||1;
  const jpMax = Math.max(pers.J,pers.P)||1;

  // Pathways
  const pathResults = {};
  Object.keys(paths).forEach(f => {
    const maxScore = 5 * 5;
    const pct = Math.round((paths[f] / maxScore) * 100);
    let stage = 'Striving';
    if (pct >= 81) stage = 'Thriving';
    else if (pct >= 41) stage = 'Surviving';
    pathResults[f] = { score: pct, stage };
  });
  const overallPath = Math.round(Object.values(pathResults).reduce((a,b)=>a+b.score,0)/5);
  let overallStage = 'Striving';
  if (overallPath >= 81) overallStage = 'Thriving';
  else if (overallPath >= 41) overallStage = 'Surviving';

  const overallDesc = {
    Striving: "Your pathway reveals an area needing intentional investment and support. This is not a place of shame — it is an invitation to build. Every foundation starts somewhere, and knowing where to build is the first step toward living your calling fully.",
    Surviving: "Your pathway reveals a life of resilience amid challenges. You have managed to persevere through real difficulties. This journey reflects determination — and with the right support and next steps, you are positioned to move from survival to flourishing.",
    Thriving: "Your pathway reveals a life of strength and flourishing. You are walking in alignment with God's design across the key areas of your life. Keep investing, keep growing — and use this strong foundation to launch fully into your calling."
  }[overallStage];

  const peopleLabels = {kids:'Kids (4–12)',teens:'Teens (13–17)',youth:'Youth (18–21)',youngadults:'Young Adults (22–25)',adults:'Adults (25–65)',elderly:'Elderly (65+)'};
  const issueLabels = {spiritual:'Spiritual',physical:'Physical',relational:'Relational & Emotional',intellectual:'Intellectual'};
  const ministryLabels = {evangelism:'Evangelism',discipleship:'Discipleship',compassion:'Compassion',leadership:'Leadership',missions:'Missions',creative:'Creative'};

  return {
    gifts, giftsSorted, giftsMax,
    primaryGift: giftsSorted[0][0],
    secondaryGift: giftsSorted[1][0],
    supportingGift: giftsSorted[2][0],
    people, peopleSorted, peopleLabels,
    issues, issuesSorted, issueLabels,
    ministry, ministrySorted, ministryLabels,
    roleLabel, roleDesc,
    viaSorted,
    riasecSorted, riasecMax, hollandCode,
    pers, mbtiType, EI, SN, TF, JP,
    eiPcts:[Math.round((pers.E/eiMax)*100),Math.round((pers.I/eiMax)*100)],
    snPcts:[Math.round((pers.S/snMax)*100),Math.round((pers.N/snMax)*100)],
    tfPcts:[Math.round((pers.T/tfMax)*100),Math.round((pers.F/tfMax)*100)],
    jpPcts:[Math.round((pers.J/jpMax)*100),Math.round((pers.P/jpMax)*100)],
    pathResults, overallPath, overallStage, overallDesc
  };
}

// ════════════════════════════════════════════════════════════
// REPORT GENERATOR
// ════════════════════════════════════════════════════════════
function generateReport() {
  document.getElementById('pageNav').style.display = 'none';
  document.getElementById('progressFill').style.width = '100%';
  document.getElementById('navSection').textContent = 'Your Report';
  document.getElementById('navProgress').textContent = '177 of 177';

  const R = score();
  const date = new Date().toLocaleDateString('en-GB', {day:'numeric',month:'long',year:'numeric'});
  const gm1 = GIFT_META[R.primaryGift];
  const gm2 = GIFT_META[R.secondaryGift];
  const gm3 = GIFT_META[R.supportingGift];
  const pm = MBTI_META[R.mbtiType] || MBTI_META['INFP'];
  const rm1 = RIASEC_META[R.riasecSorted[0][0]];
  const rm2 = RIASEC_META[R.riasecSorted[1][0]];

  const pplTop = R.peopleSorted[0][0];
  const issTop = R.issuesSorted[0][0];
  const minTop = R.ministrySorted[0][0];

  // Build bars for gifts
  const topGifts5 = R.giftsSorted.slice(0,5);
  const giftBars = topGifts5.map(([k,v],i) => {
    const pct = Math.round((v/R.giftsMax)*100);
    const cls = i===0?'primary':i===1?'secondary':i===2?'tertiary':'grey';
    return `<div class="bar-group"><div class="bar-label"><span>${GIFT_META[k].name}</span><span class="bar-pct">${pct}%</span></div><div class="bar-track"><div class="bar-fill ${cls}" style="width:${pct}%"></div></div></div>`;
  }).join('');

  const riasecBars = R.riasecSorted.map(([k,v],i) => {
    const pct = Math.round((v/R.riasecMax)*100);
    return `<div class="bar-group"><div class="bar-label"><span>${RIASEC_META[k].name} — ${RIASEC_META[k].label}</span><span class="bar-pct">${pct}%</span></div><div class="bar-track"><div class="bar-fill ${i===0?'primary':i===1?'secondary':'tertiary'}" style="width:${pct}%"></div></div></div>`;
  }).join('');

  const viaBars = R.viaSorted.map(([k,v],i) => {
    const pct = Math.round((v/5)*100);
    return `<div class="bar-group"><div class="bar-label"><span>${k}</span><span class="bar-pct">${pct}%</span></div><div class="bar-track"><div class="bar-fill ${i===0?'primary':i===1?'secondary':i===2?'tertiary':'grey'}" style="width:${pct}%"></div></div></div>`;
  }).join('');

  const via5Cards = R.viaSorted.slice(0,5).map(([k,v],i) => `
    <div class="via-card">
      <div class="via-rank">#${i+1}</div>
      <div class="via-name">${k}</div>
      <div class="via-virtue">${VIA_VIRTUES[k]||''}</div>
      <div class="via-score">${Math.round((v/5)*100)}%</div>
    </div>`).join('');

  const hollandLetters = R.hollandCode.split('').map(l =>
    `<div class="riasec-letter rl-${l}">${l}</div>`).join('');

  const typeLetters = R.mbtiType.split('').map(l =>
    `<div class="type-letter-block">${l}</div>`).join('');

  const pathBars = Object.entries(R.pathResults).map(([f,r]) => `
    <div class="pw-item">
      <div class="pw-header">
        <div class="pw-name">${f}</div>
        <div class="pw-stage ${r.stage.toLowerCase()}">${r.stage} — ${r.score}%</div>
      </div>
      <div class="pw-track"><div class="pw-fill ${r.stage.toLowerCase()}" style="width:${r.score}%"></div></div>
    </div>`).join('');

  const actionSteps = [
    { num:'01', title:`Develop your gift of ${gm1.name}`, desc:`Your primary gift is ${gm1.name}. This week, identify one specific opportunity to use this gift intentionally — in your community, your church, or your workplace. Find a mentor who operates in this gift and ask them for one piece of guidance.` },
    { num:'02', title:`Serve your passion: ${R.peopleLabels[pplTop]} through ${R.ministryLabels[minTop]}`, desc:`You are called to ${R.peopleLabels[pplTop]} through ${R.ministryLabels[minTop]}. This month, take one concrete step toward that — attend an event, volunteer with a group, or have a conversation with someone already doing this work.` },
    { num:'03', title:`Invest in your lowest Pathway: ${Object.entries(R.pathResults).sort((a,b)=>a[1].score-b[1].score)[0][0]}`, desc:`Your ${Object.entries(R.pathResults).sort((a,b)=>a[1].score-b[1].score)[0][0]} Pathway is where the greatest opportunity for growth lies. A strong foundation in every area of your life is what sustains your calling long-term. Identify one person who can support you and one step you can take this week.` }
  ];
  const stepsHtml = actionSteps.map(s => `
    <div class="next-steps-card">
      <div class="ns-num">${s.num}</div>
      <div class="ns-title">${s.title}</div>
      <div class="ns-desc">${s.desc}</div>
    </div>`).join('');

  const html = `
    <!-- COVER -->
    <div class="report-cover">
      <div class="rc-verse">
        "For I know the plans I have for you, declares the Lord, plans to prosper you and not to harm you, plans to give you hope and a future."
        <cite>Jeremiah 29:11</cite>
      </div>
      <div class="rc-inner">
        <div class="rc-tag">YOUnique Purpose · Fifteen25 · ${date}</div>
        <div class="rc-name">${state.name}</div>
        <div class="rc-subtitle">YOUnique Purpose Detailed Report</div>
        <div class="rc-date">${date}</div>
      </div>
    </div>

    <!-- SUMMARY -->
    <div class="report-section">
      <div class="rs-label">Summary</div>
      <div class="rs-title">Your Purpose Profile</div>
      <div class="rs-desc">This report brings together six globally validated frameworks to reveal the unique purpose God has placed inside you. Each section answers a different question about who you are and what you are called to do.</div>
      <div class="summary-grid">
        <div class="sg-card">
          <div class="sg-label">Primary Spiritual Gift</div>
          <div class="sg-value">${gm1.name}</div>
          <div class="sg-sub">${gm1.thrust}</div>
        </div>
        <div class="sg-card">
          <div class="sg-label">Passion — People</div>
          <div class="sg-value">${R.peopleLabels[pplTop]}</div>
          <div class="sg-sub">Calling: ${R.ministryLabels[minTop]}</div>
        </div>
        <div class="sg-card">
          <div class="sg-label">Top Character Strength</div>
          <div class="sg-value">${R.viaSorted[0][0]}</div>
          <div class="sg-sub">${VIA_VIRTUES[R.viaSorted[0][0]]||''} virtue</div>
        </div>
        <div class="sg-card">
          <div class="sg-label">Holland Code</div>
          <div class="sg-value">${R.hollandCode}</div>
          <div class="sg-sub">${R.riasecSorted.slice(0,3).map(([k])=>RIASEC_META[k].name).join(' · ')}</div>
        </div>
        <div class="sg-card">
          <div class="sg-label">Personality Type</div>
          <div class="sg-value">${R.mbtiType}</div>
          <div class="sg-sub">${pm.name} · ${pm.role}</div>
        </div>
        <div class="sg-card">
          <div class="sg-label">Overall Pathway</div>
          <div class="sg-value">${R.overallStage}</div>
          <div class="sg-sub">${R.overallPath}% — ${R.overallStage} Pathway</div>
        </div>
      </div>
    </div>

    <!-- SPIRITUAL GIFTS -->
    <div class="report-section">
      <div class="rs-label">Section 1 — Spiritual Gifts</div>
      <div class="rs-title">What God has equipped you to do</div>
      <div class="rs-desc">Your spiritual gifts are the supernatural endowments God placed in you at the moment of your new birth. They are not natural talents — they are divine equipment for kingdom impact.</div>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:24px;margin-bottom:32px">
        <div>${giftBars}</div>
        <div>
          <div class="gift-detail-block">
            <div class="gdb-rank">Primary Gift · ${gm1.pct} of Christians</div>
            <div class="gdb-name">${gm1.name}</div>
            <div class="gdb-thrust">${gm1.thrust}</div>
            <div class="gdb-desc">${gm1.desc}</div>
            <div class="gdb-grid">
              <div class="gdb-item"><div class="gdb-item-label">Biblical Reference</div><div class="gdb-item-val">${gm1.bible}</div></div>
              <div class="gdb-item"><div class="gdb-item-label">Category</div><div class="gdb-item-val">${gm1.cat} Gift</div></div>
              <div class="gdb-item"><div class="gdb-item-label">Ministry Areas</div><div class="gdb-item-val">${gm1.ministry}</div></div>
              <div class="gdb-item"><div class="gdb-item-label">Blind Spot</div><div class="gdb-item-val">${gm1.blindspot}</div></div>
            </div>
          </div>
        </div>
      </div>
      <div class="gift-detail-block secondary">
        <div class="gdb-rank">Secondary Gift · ${gm2.pct} of Christians</div>
        <div class="gdb-name">${gm2.name}</div>
        <div class="gdb-thrust">${gm2.thrust}</div>
        <div class="gdb-desc">${gm2.desc}</div>
        <div class="gdb-grid">
          <div class="gdb-item"><div class="gdb-item-label">Possible Careers</div><div class="gdb-item-val">${gm2.careers}</div></div>
          <div class="gdb-item"><div class="gdb-item-label">Ministry Areas</div><div class="gdb-item-val">${gm2.ministry}</div></div>
        </div>
      </div>
      <div class="gift-detail-block tertiary">
        <div class="gdb-rank">Supporting Gift</div>
        <div class="gdb-name">${gm3.name}</div>
        <div class="gdb-thrust">${gm3.thrust}</div>
        <div class="gdb-desc">${gm3.desc}</div>
      </div>
    </div>

    <!-- PASSION -->
    <div class="report-section">
      <div class="rs-label">Section 2 — Passion</div>
      <div class="rs-title">Where your heart is most alive</div>
      <div class="rs-desc">Passion is the fuel of purpose. It reveals who you are called to serve, what breaks your heart, how you prefer to operate, and which form of kingdom work energises you most.</div>
      <div class="passion-grid">
        <div class="passion-chip p1">
          <div class="pc-cat">Passion for People</div>
          <div class="pc-val">${R.peopleLabels[pplTop]}</div>
          <div class="pc-desc">The age group your heart is most drawn to serve</div>
        </div>
        <div class="passion-chip p2">
          <div class="pc-cat">Passion for Issues</div>
          <div class="pc-val">${R.issueLabels[issTop]}</div>
          <div class="pc-desc">The type of need that moves you to action</div>
        </div>
        <div class="passion-chip p3">
          <div class="pc-cat">Passion for Roles</div>
          <div class="pc-val">${R.roleLabel}</div>
          <div class="pc-desc">${R.roleDesc}</div>
        </div>
        <div class="passion-chip p4">
          <div class="pc-cat">Passion for Ministry</div>
          <div class="pc-val">${R.ministryLabels[minTop]}</div>
          <div class="pc-desc">The kingdom function that energises you most</div>
        </div>
      </div>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:20px">
        <div>
          <div style="font-size:12px;font-weight:700;color:var(--text-muted);text-transform:uppercase;letter-spacing:.1em;margin-bottom:12px">People Passion</div>
          ${R.peopleSorted.map(([k,v])=>{const pct=Math.round((v/5)*100);return `<div class="bar-group"><div class="bar-label"><span>${R.peopleLabels[k]}</span><span class="bar-pct">${pct}%</span></div><div class="bar-track"><div class="bar-fill ${k===pplTop?'primary':'grey'}" style="width:${pct}%"></div></div></div>`;}).join('')}
        </div>
        <div>
          <div style="font-size:12px;font-weight:700;color:var(--text-muted);text-transform:uppercase;letter-spacing:.1em;margin-bottom:12px">Ministry Passion</div>
          ${R.ministrySorted.map(([k,v])=>{const pct=Math.round((v/5)*100);return `<div class="bar-group"><div class="bar-label"><span>${R.ministryLabels[k]}</span><span class="bar-pct">${pct}%</span></div><div class="bar-track"><div class="bar-fill ${k===minTop?'secondary':'grey'}" style="width:${pct}%"></div></div></div>`;}).join('')}
        </div>
      </div>
    </div>

    <!-- VIA -->
    <div class="report-section">
      <div class="rs-label">Section 3A — VIA Character Strengths</div>
      <div class="rs-title">Who you are at your best</div>
      <div class="rs-desc">VIA Character Strengths are scientifically validated positive traits — present across all cultures, ages, and backgrounds — that represent what is best about your personality. These are your virtues in action.</div>
      <div class="via-grid">${via5Cards}</div>
      ${viaBars}
    </div>

    <!-- RIASEC -->
    <div class="report-section">
      <div class="rs-label">Section 3B — Holland RIASEC</div>
      <div class="rs-title">What kind of work energises you</div>
      <div class="rs-desc">Your Holland Code reveals the work environments, activities, and vocational contexts where you will be most engaged, effective, and fulfilled — both in ministry and career.</div>
      <div class="riasec-code-display">${hollandLetters}</div>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-bottom:24px">
        <div class="gift-detail-block" style="margin-bottom:0">
          <div class="gdb-rank">Primary Interest Type</div>
          <div class="gdb-name">${rm1.name}</div>
          <div class="gdb-thrust">${rm1.label}</div>
          <div class="gdb-desc">${rm1.desc}</div>
          <div class="gdb-item"><div class="gdb-item-label">Career Directions</div><div class="gdb-item-val">${rm1.careers}</div></div>
        </div>
        <div class="gift-detail-block secondary" style="margin-bottom:0">
          <div class="gdb-rank">Secondary Interest Type</div>
          <div class="gdb-name">${rm2.name}</div>
          <div class="gdb-thrust">${rm2.label}</div>
          <div class="gdb-desc">${rm2.desc}</div>
          <div class="gdb-item"><div class="gdb-item-label">Career Directions</div><div class="gdb-item-val">${rm2.careers}</div></div>
        </div>
      </div>
      ${riasecBars}
    </div>

    <!-- PERSONALITY -->
    <div class="report-section">
      <div class="rs-label">Section 4 — Personality</div>
      <div class="rs-title">How you are wired to engage the world</div>
      <div class="rs-desc">Your personality type reveals how your mind naturally takes in information, makes decisions, relates to people, and organises your life. This is the delivery mechanism through which all your gifts flow.</div>
      <div class="type-display">${typeLetters}</div>
      <div style="margin-bottom:8px">
        <div style="font-family:'Playfair Display',serif;font-size:28px;font-weight:900;color:var(--blue)">${pm.name}</div>
        <div style="font-size:14px;color:var(--text-muted);margin-bottom:4px">Role: ${pm.role} · ${pm.pct} of the world's population</div>
      </div>
      <div class="rs-desc" style="margin-bottom:20px">${pm.desc}</div>
      <div class="dimension-bars">
        <div class="dim-row">
          <div class="dim-labels"><span>Extraversion ${R.eiPcts[0]}%</span><span>Introversion ${R.eiPcts[1]}%</span></div>
          <div class="dim-track"><div class="dim-left" style="width:${R.eiPcts[0]}%"></div><div class="dim-right" style="width:${R.eiPcts[1]}%"></div></div>
        </div>
        <div class="dim-row">
          <div class="dim-labels"><span>Sensing ${R.snPcts[0]}%</span><span>iNtuitive ${R.snPcts[1]}%</span></div>
          <div class="dim-track"><div class="dim-left" style="width:${R.snPcts[0]}%"></div><div class="dim-right" style="width:${R.snPcts[1]}%"></div></div>
        </div>
        <div class="dim-row">
          <div class="dim-labels"><span>Thinking ${R.tfPcts[0]}%</span><span>Feeling ${R.tfPcts[1]}%</span></div>
          <div class="dim-track"><div class="dim-left" style="width:${R.tfPcts[0]}%"></div><div class="dim-right" style="width:${R.tfPcts[1]}%"></div></div>
        </div>
        <div class="dim-row">
          <div class="dim-labels"><span>Judging ${R.jpPcts[0]}%</span><span>Perceiving ${R.jpPcts[1]}%</span></div>
          <div class="dim-track"><div class="dim-left" style="width:${R.jpPcts[0]}%"></div><div class="dim-right" style="width:${R.jpPcts[1]}%"></div></div>
        </div>
      </div>
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:24px">
        <div class="gift-detail-block" style="margin-bottom:0">
          <div class="gdb-rank">Strengths</div>
          <div class="gdb-desc">${pm.strengths}</div>
        </div>
        <div class="gift-detail-block secondary" style="margin-bottom:0">
          <div class="gdb-rank">Watch out for</div>
          <div class="gdb-desc">${pm.weaknesses}</div>
        </div>
      </div>
    </div>

    <!-- PATHWAYS -->
    <div class="report-section">
      <div class="rs-label">Section 5 — Pathways</div>
      <div class="rs-title">The 5 F's of your life foundation</div>
      <div class="rs-desc">Purpose without a strong foundation collapses. The Pathways section reveals how each area of your life is currently positioned to support and sustain your calling.</div>
      <div class="pathways-bars">${pathBars}</div>
      <div class="pathway-overall-card">
        <div class="poc-stage">${R.overallStage} Pathway · ${R.overallPath}%</div>
        <div class="poc-score">${R.overallPath}%</div>
        <div class="poc-desc">${R.overallDesc}</div>
      </div>
    </div>

    <!-- CALLING CANVAS -->
    <div class="report-section">
      <div class="rs-label">Calling Intersection</div>
      <div class="rs-title">Where it all comes together</div>
      <div class="rs-desc">Your calling is not one thing — it is the intersection of everything God has placed in you. Below is your unique calling profile: the convergence of your gifts, passion, potential, personality, and pathway.</div>
      <div class="calling-canvas">
        <div class="cc-title">Your Calling Canvas</div>
        <div class="cc-grid">
          <div class="cc-item"><div class="cc-item-label">Primary Gift</div><div class="cc-item-val">${gm1.name}</div></div>
          <div class="cc-item"><div class="cc-item-label">Secondary Gift</div><div class="cc-item-val">${gm2.name}</div></div>
          <div class="cc-item"><div class="cc-item-label">People</div><div class="cc-item-val">${R.peopleLabels[pplTop]}</div></div>
          <div class="cc-item"><div class="cc-item-label">Issues</div><div class="cc-item-val">${R.issueLabels[issTop]}</div></div>
          <div class="cc-item"><div class="cc-item-label">Ministry</div><div class="cc-item-val">${R.ministryLabels[minTop]}</div></div>
          <div class="cc-item"><div class="cc-item-label">Role</div><div class="cc-item-val">${R.roleLabel}</div></div>
          <div class="cc-item"><div class="cc-item-label">Top Strength</div><div class="cc-item-val">${R.viaSorted[0][0]}</div></div>
          <div class="cc-item"><div class="cc-item-label">Holland Code</div><div class="cc-item-val">${R.hollandCode}</div></div>
          <div class="cc-item"><div class="cc-item-label">Personality</div><div class="cc-item-val">${R.mbtiType} — ${pm.name}</div></div>
          <div class="cc-item"><div class="cc-item-label">Overall Pathway</div><div class="cc-item-val">${R.overallStage} · ${R.overallPath}%</div></div>
        </div>
      </div>
    </div>

    <!-- NEXT STEPS -->
    <div class="report-section">
      <div class="rs-label">Next Steps</div>
      <div class="rs-title">What you do with this</div>
      <div class="rs-desc">Discovery is only the beginning. Here are three personalised action steps drawn directly from your results — and one clear invitation to go deeper.</div>
      ${stepsHtml}
      <div class="coaching-cta">
        <div class="cta-title">Book Your Purpose Coaching Call</div>
        <div class="cta-desc">Your report reveals who you are. A coaching call helps you understand what to do with it. Connect with a certified YOUnique Purpose Coach to walk through your results, ask your questions, and build your action plan.</div>
        <a class="btn-cta" href="https://youniquepurpose.com/coaching" target="_blank">
          Connect with a Purpose Coach →
        </a>
        <br>
        <button class="btn-print" onclick="window.print()">
          <svg width="14" height="14" viewBox="0 0 14 14" fill="none"><rect x="2" y="4" width="10" height="7" rx="1.5" stroke="currentColor" stroke-width="1.5"/><path d="M4 4V2.5A.5.5 0 014.5 2h5a.5.5 0 01.5.5V4" stroke="currentColor" stroke-width="1.5"/><rect x="4" y="8" width="6" height="3" rx=".5" fill="currentColor" opacity=".3"/></svg>
          Download / Print Report
        </button>
      </div>
    </div>
  `;

  document.getElementById('reportContent').innerHTML = html;
  showScreen('report');
  window.scrollTo({ top: 0, behavior: 'smooth' });
}
</script>
</body>
</html>
