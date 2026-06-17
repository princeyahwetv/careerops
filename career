<!doctype html>
<html style="height: 100%;">
 <head><script src="/_sdk/telemetry_sdk.js"></script>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Career Opportunities</title>
  <script src="https://cdn.tailwindcss.com/3.4.17"></script>
  <script src="https://cdn.jsdelivr.net/npm/lucide@0.263.0/dist/umd/lucide.min.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;700&amp;display=swap" rel="stylesheet">
  <script src="/_sdk/element_sdk.js"></script>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    html, body { height: 100%; width: 100%; }
    body { font-family: 'DM Sans', -apple-system, sans-serif; }
    #app { height: 100%; width: 100%; }
    .drop-zone { min-height: 80px; transition: all 0.2s; }
    .answer-tag { cursor: grab; user-select: none; }
    .answer-tag:active { cursor: grabbing; }
    .answer-tag.dragging { opacity: 0.4; }
    .timer-warning { animation: pulse 1s infinite; }
    @keyframes pulse { 0%,100%{ opacity:1; } 50%{ opacity:0.5; } }
  </style>
  <style>body { box-sizing: border-box; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
 </head>
 <body style="background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #78350f 100%);">
  <div id="app" class="w-full overflow-auto" style="height: 100%; background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #78350f 100%);">
   <!-- NAME ENTRY SCREEN -->
   <div id="entry-screen" style="display: flex; align-items: center; justify-content: center; height: 100%; padding: 20px;">
    <div style="background: rgba(30, 41, 59, 0.9); border: 2px solid #475569; border-radius: 16px; padding: 48px; max-width: 500px; width: 100%;">
     <h1 style="font-size: 36px; font-weight: bold; color: #fef3c7; text-align: center; margin-bottom: 8px;">CSS Career Opportunities</h1>
     <p style="color: #94a3b8; text-align: center; margin-bottom: 32px; font-size: 16px;">Enter your details to begin the quiz</p>
     <div style="display: flex; flex-direction: column; gap: 20px;">
      <div>
       <label for="student-name" style="color: #cbd5e1; font-size: 14px; font-weight: 600; display: block; margin-bottom: 6px;">Full Name</label> <input id="student-name" type="text" placeholder="Enter your full name" style="width: 100%; padding: 14px 16px; border-radius: 8px; border: 2px solid #475569; background: rgba(15, 23, 42, 0.8); color: #f1f5f9; font-size: 16px; outline: none;" onfocus="this.style.borderColor='#f59e0b'" onblur="this.style.borderColor='#475569'">
      </div>
      <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 16px;">
       <div>
        <label for="student-grade" style="color: #cbd5e1; font-size: 14px; font-weight: 600; display: block; margin-bottom: 6px;">Grade Level</label> <select id="student-grade" style="width: 100%; padding: 14px 16px; border-radius: 8px; border: 2px solid #475569; background: rgba(15, 23, 42, 0.8); color: #f1f5f9; font-size: 16px; outline: none;" onfocus="this.style.borderColor='#f59e0b'" onblur="this.style.borderColor='#475569'"> <option value="">Select Grade</option> <option value="7">Grade 7</option> <option value="8">Grade 8</option> <option value="9">Grade 9</option> <option value="10">Grade 10</option> <option value="11">Grade 11</option> <option value="12">Grade 12</option> </select>
       </div>
       <div>
        <label for="student-section" style="color: #cbd5e1; font-size: 14px; font-weight: 600; display: block; margin-bottom: 6px;">Section</label> <input id="student-section" type="text" placeholder="e.g. Section A" style="width: 100%; padding: 14px 16px; border-radius: 8px; border: 2px solid #475569; background: rgba(15, 23, 42, 0.8); color: #f1f5f9; font-size: 16px; outline: none;" onfocus="this.style.borderColor='#f59e0b'" onblur="this.style.borderColor='#475569'">
       </div>
      </div>
      <div id="entry-error" style="display: none; color: #fca5a5; font-size: 14px; text-align: center;"></div><button onclick="startQuiz()" style="background: #f59e0b; color: #1f2937; font-weight: bold; padding: 16px; border-radius: 8px; border: none; font-size: 18px; cursor: pointer; margin-top: 8px; transition: background 0.2s;" onmouseover="this.style.background='#d97706'" onmouseout="this.style.background='#f59e0b'"> Start Quiz → </button>
     </div>
    </div>
   </div><!-- QUIZ SCREEN -->
   <div id="quiz-screen" style="display: none; padding: 40px 20px; max-width: 1400px; margin: 0 auto;">
    <!-- HEADER -->
    <div style="text-align: center; margin-bottom: 40px;">
     <h1 id="quiz-title" style="font-size: 48px; font-weight: bold; color: #fef3c7; margin-bottom: 12px;">CSS Career Opportunities</h1>
     <p id="student-info-display" style="font-size: 16px; color: #94a3b8; margin-bottom: 16px;"></p>
     <p style="font-size: 24px; color: #cbd5e1; margin-bottom: 20px;">Drag the correct career category to each job description</p>
     <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
      <div style="background: rgba(71, 85, 105, 0.6); padding: 16px 24px; border-radius: 50px; border: 2px solid #64748b;">
       <span style="font-size: 24px; color: #fef3c7; font-weight: bold;">Score: <span id="score">0</span>/20</span>
      </div>
      <div id="timer-display" style="background: rgba(71, 85, 105, 0.6); padding: 16px 24px; border-radius: 50px; border: 2px solid #64748b;">
       <span style="font-size: 24px; color: #fef3c7; font-weight: bold;">⏱ <span id="timer">30:00</span></span>
      </div>
     </div>
    </div><!-- MAIN CONTENT -->
    <div style="display: grid; grid-template-columns: 2fr 1fr; gap: 32px; margin-bottom: 40px;">
     <div id="situations" style="display: flex; flex-direction: column; gap: 20px;"></div>
     <div style="display: flex; flex-direction: column; gap: 24px; position: sticky; top: 20px; height: fit-content;">
      <div style="background: rgba(30, 41, 59, 0.7); border: 2px solid #475569; border-radius: 12px; padding: 24px;">
       <p style="font-size: 16px; color: #cbd5e1; margin-bottom: 16px; font-weight: bold; text-align: center; text-transform: uppercase;">Drag answers from here:</p>
       <div id="answer-bank" style="display: flex; flex-direction: column; gap: 12px;"></div>
      </div><button onclick="checkAnswers()" style="background: #f59e0b; color: #1f2937; font-weight: bold; padding: 20px 24px; border-radius: 8px; border: none; font-size: 18px; cursor: pointer; transition: all 0.2s;">✓ Check Answers</button> <button onclick="resetActivity()" style="background: #64748b; color: #f1f5f9; font-weight: bold; padding: 20px 24px; border-radius: 8px; border: none; font-size: 18px; cursor: pointer; transition: all 0.2s;">↻ Reset</button>
      <div id="feedback" style="display: none; padding: 20px; border-radius: 8px; text-align: center; font-size: 18px; color: #fef3c7;"></div>
     </div>
    </div>
   </div><!-- TIME'S UP SCREEN -->
   <div id="timesup-screen" style="display: none; align-items: center; justify-content: center; height: 100%; padding: 20px;">
    <div style="background: rgba(30, 41, 59, 0.9); border: 2px solid #ef4444; border-radius: 16px; padding: 48px; max-width: 500px; width: 100%; text-align: center;">
     <div style="font-size: 64px; margin-bottom: 16px;">
      ⏰
     </div>
     <h2 style="font-size: 32px; font-weight: bold; color: #fca5a5; margin-bottom: 12px;">Time's Up!</h2>
     <p id="timesup-score" style="font-size: 20px; color: #cbd5e1; margin-bottom: 24px;"></p><button onclick="resetActivity()" style="background: #f59e0b; color: #1f2937; font-weight: bold; padding: 16px 32px; border-radius: 8px; border: none; font-size: 18px; cursor: pointer;">Try Again</button>
    </div>
   </div>
  </div>
  <script>
const data = [
  { situation: "Diagnoses and repairs computer hardware and software problems.", answer: "Computer Technician" },
  { situation: "Assists users with computer and network issues via phone, chat, or in person.", answer: "Technical Support Specialist" },
  { situation: "Maintains computers, printers, and other IT equipment.", answer: "IT Support Staff" },
  { situation: "Installs, configures, and maintains desktop computers and laptops.", answer: "Desktop Support Technician" },
  { situation: "Builds and upgrades computer systems and tests hardware components.", answer: "Computer Assembler" },
  { situation: "Installs and maintains local area networks (LANs).", answer: "Network Technician" },
  { situation: "Helps monitor and troubleshoot network connectivity problems.", answer: "Network Support Assistant" },
  { situation: "Travels to customer locations to repair and maintain computer systems.", answer: "Field Service Technician" },
  { situation: "Installs and repairs printers, scanners, and other peripherals.", answer: "Printer and Peripheral Technician" },
  { situation: "Provides technical assistance and customer support for IT issues.", answer: "IT Help Desk Analyst" },
  { situation: "Manages and secures computer networks and network operations.", answer: "Network Administrator" },
  { situation: "Maintains servers and IT infrastructure for organizations.", answer: "Systems Administrator" },
  { situation: "Installs operating systems and software applications on computers.", answer: "Computer Technician" },
  { situation: "Provides troubleshooting support via multiple communication channels.", answer: "Technical Support Specialist" },
  { situation: "Supports daily IT operations in offices and educational institutions.", answer: "IT Support Staff" },
  { situation: "Handles user account management and resolves software issues.", answer: "Desktop Support Technician" },
  { situation: "Configures routers, switches, and other network devices.", answer: "Network Technician" },
  { situation: "Monitors network performance and resolves connectivity issues.", answer: "Network Support Assistant" },
  { situation: "Delivers on-site computer repair and maintenance services.", answer: "Field Service Technician" },
  { situation: "Sets up and repairs printing devices and peripheral equipment.", answer: "Printer and Peripheral Technician" }
];

let userAnswers = new Array(20).fill(null);
let draggedEl = null;
let timerInterval = null;
let timeRemaining = 30 * 60; // 30 minutes in seconds
let studentName = '';
let studentGrade = '';
let studentSection = '';

// Timer
function startTimer() {
  timeRemaining = 30 * 60;
  updateTimerDisplay();
  timerInterval = setInterval(() => {
    timeRemaining--;
    updateTimerDisplay();
    if (timeRemaining <= 0) {
      clearInterval(timerInterval);
      timesUp();
    }
  }, 1000);
}

function updateTimerDisplay() {
  const mins = Math.floor(timeRemaining / 60);
  const secs = timeRemaining % 60;
  const timerEl = document.getElementById('timer');
  timerEl.textContent = `${String(mins).padStart(2,'0')}:${String(secs).padStart(2,'0')}`;
  const timerBox = document.getElementById('timer-display');
  if (timeRemaining <= 300) {
    timerBox.style.borderColor = '#ef4444';
    timerEl.parentElement.style.color = '#fca5a5';
    if (timeRemaining <= 60) timerBox.className = 'timer-warning';
  } else {
    timerBox.style.borderColor = '#64748b';
    timerEl.parentElement.style.color = '#fef3c7';
    timerBox.className = '';
  }
}

function timesUp() {
  playLoserSound();
  let score = 0;
  userAnswers.forEach((ans, idx) => { if (ans === data[idx].answer) score++; });
  document.getElementById('quiz-screen').style.display = 'none';
  const ts = document.getElementById('timesup-screen');
  ts.style.display = 'flex';
  document.getElementById('timesup-score').textContent = `You scored ${score}/20. Better luck next time, ${studentName}!`;
}

function startQuiz() {
  studentName = document.getElementById('student-name').value.trim();
  studentGrade = document.getElementById('student-grade').value;
  studentSection = document.getElementById('student-section').value.trim();
  const errEl = document.getElementById('entry-error');

  if (!studentName || !studentGrade || !studentSection) {
    errEl.style.display = 'block';
    errEl.textContent = 'Please fill in all fields to continue.';
    return;
  }
  errEl.style.display = 'none';

  document.getElementById('student-info-display').textContent = `${studentName} • Grade ${studentGrade} • ${studentSection}`;
  document.getElementById('entry-screen').style.display = 'none';
  document.getElementById('quiz-screen').style.display = 'block';
  buildUI();
  startTimer();
}

// Audio
let audioCtx;
function initAudio() { if (!audioCtx) audioCtx = new (window.AudioContext || window.webkitAudioContext)(); }

function playDragSound() {
  initAudio();
  const now = audioCtx.currentTime;
  const osc = audioCtx.createOscillator(); const gain = audioCtx.createGain();
  osc.connect(gain); gain.connect(audioCtx.destination);
  osc.frequency.setValueAtTime(400, now); osc.frequency.exponentialRampToValueAtTime(200, now + 0.1);
  gain.gain.setValueAtTime(0.1, now); gain.gain.exponentialRampToValueAtTime(0.01, now + 0.1);
  osc.start(now); osc.stop(now + 0.1);
}

function playDropSound() {
  initAudio();
  const now = audioCtx.currentTime;
  const osc = audioCtx.createOscillator(); const gain = audioCtx.createGain();
  osc.connect(gain); gain.connect(audioCtx.destination);
  osc.frequency.setValueAtTime(800, now); osc.frequency.exponentialRampToValueAtTime(400, now + 0.15);
  gain.gain.setValueAtTime(0.15, now); gain.gain.exponentialRampToValueAtTime(0.01, now + 0.15);
  osc.start(now); osc.stop(now + 0.15);
}

function playCorrectSound() {
  initAudio();
  const now = audioCtx.currentTime;
  for (let i = 0; i < 2; i++) {
    const osc = audioCtx.createOscillator(); const gain = audioCtx.createGain();
    osc.connect(gain); gain.connect(audioCtx.destination);
    osc.frequency.value = 600 + (i * 200);
    gain.gain.setValueAtTime(0.1, now + (i * 0.1)); gain.gain.exponentialRampToValueAtTime(0.01, now + (i * 0.1) + 0.15);
    osc.start(now + (i * 0.1)); osc.stop(now + (i * 0.1) + 0.15);
  }
}

function playIncorrectSound() {
  initAudio();
  const now = audioCtx.currentTime;
  const osc = audioCtx.createOscillator(); const gain = audioCtx.createGain();
  osc.connect(gain); gain.connect(audioCtx.destination);
  osc.frequency.setValueAtTime(300, now); osc.frequency.exponentialRampToValueAtTime(150, now + 0.2);
  gain.gain.setValueAtTime(0.12, now); gain.gain.exponentialRampToValueAtTime(0.01, now + 0.2);
  osc.start(now); osc.stop(now + 0.2);
}

function playDiscoMusic() {
  initAudio();
  const now = audioCtx.currentTime;
  [100,150,100,150].forEach((freq, i) => {
    const osc = audioCtx.createOscillator(); const gain = audioCtx.createGain();
    osc.connect(gain); gain.connect(audioCtx.destination);
    osc.frequency.value = freq;
    const t = now + (i * 0.15);
    gain.gain.setValueAtTime(0.2, t); gain.gain.exponentialRampToValueAtTime(0.05, t + 0.1);
    osc.start(t); osc.stop(t + 0.1);
  });
  [523,659,784,659,523,659,784,879].forEach((freq, i) => {
    const osc = audioCtx.createOscillator(); const gain = audioCtx.createGain();
    osc.connect(gain); gain.connect(audioCtx.destination);
    osc.frequency.value = freq;
    const t = now + (i * 0.1) + 0.2;
    gain.gain.setValueAtTime(0.12, t); gain.gain.exponentialRampToValueAtTime(0.02, t + 0.15);
    osc.start(t); osc.stop(t + 0.15);
  });
}

function playLoserSound() {
  initAudio();
  const now = audioCtx.currentTime;
  const osc = audioCtx.createOscillator(); const gain = audioCtx.createGain();
  osc.connect(gain); gain.connect(audioCtx.destination);
  osc.frequency.setValueAtTime(400, now); osc.frequency.exponentialRampToValueAtTime(100, now + 0.5);
  gain.gain.setValueAtTime(0.15, now); gain.gain.exponentialRampToValueAtTime(0.01, now + 0.5);
  osc.start(now); osc.stop(now + 0.5);
}

function getColorStyle(ans) {
  const colors = {
    'Computer Technician': 'background: rgba(30, 58, 138, 0.7); border: 2px solid #60a5fa; color: #e0f2fe;',
    'Technical Support Specialist': 'background: rgba(5, 100, 88, 0.7); border: 2px solid #34d399; color: #d1fae5;',
    'IT Support Staff': 'background: rgba(88, 28, 135, 0.7); border: 2px solid #c084fc; color: #f3e8ff;',
    'Desktop Support Technician': 'background: rgba(120, 53, 15, 0.7); border: 2px solid #fb923c; color: #fed7aa;',
    'Computer Assembler': 'background: rgba(30, 58, 138, 0.7); border: 2px solid #60a5fa; color: #e0f2fe;',
    'Network Technician': 'background: rgba(5, 100, 88, 0.7); border: 2px solid #34d399; color: #d1fae5;',
    'Network Support Assistant': 'background: rgba(88, 28, 135, 0.7); border: 2px solid #c084fc; color: #f3e8ff;',
    'Field Service Technician': 'background: rgba(120, 53, 15, 0.7); border: 2px solid #fb923c; color: #fed7aa;',
    'Printer and Peripheral Technician': 'background: rgba(30, 58, 138, 0.7); border: 2px solid #60a5fa; color: #e0f2fe;',
    'IT Help Desk Analyst': 'background: rgba(5, 100, 88, 0.7); border: 2px solid #34d399; color: #d1fae5;',
    'Network Administrator': 'background: rgba(88, 28, 135, 0.7); border: 2px solid #c084fc; color: #f3e8ff;',
    'Systems Administrator': 'background: rgba(120, 53, 15, 0.7); border: 2px solid #fb923c; color: #fed7aa;'
  };
  return colors[ans] || 'background: rgba(30, 41, 59, 0.7); border: 2px solid #475569; color: #cbd5e1;';
}

function buildUI() {
  const bank = document.getElementById('answer-bank');
  const sitDiv = document.getElementById('situations');
  let allAnswers = ['Computer Technician','Technical Support Specialist','IT Support Staff','Desktop Support Technician','Computer Assembler','Network Technician','Network Support Assistant','Field Service Technician','Printer and Peripheral Technician','IT Help Desk Analyst','Network Administrator','Systems Administrator'];
  allAnswers = shuffleArray([...allAnswers]);

  bank.innerHTML = '';
  allAnswers.forEach((ans) => {
    const tag = document.createElement('div');
    tag.style.cssText = 'padding: 16px 20px; border-radius: 8px; font-size: 16px; font-weight: 600; cursor: grab; user-select: none; ' + getColorStyle(ans);
    tag.textContent = ans;
    tag.draggable = true;
    tag.dataset.answer = ans;
    tag.className = 'answer-tag';
    tag.addEventListener('dragstart', () => { draggedEl = tag; playDragSound(); });
    tag.addEventListener('dragend', () => { draggedEl = null; });
    bank.appendChild(tag);
  });

  sitDiv.innerHTML = '';
  data.forEach((item, idx) => {
    const card = document.createElement('div');
    card.style.cssText = 'background: rgba(30, 41, 59, 0.8); border: 2px solid rgba(71, 85, 105, 0.6); border-radius: 12px; padding: 24px;';

    const headerDiv = document.createElement('div');
    headerDiv.style.cssText = 'display: flex; gap: 20px; margin-bottom: 20px;';

    const numCircle = document.createElement('div');
    numCircle.style.cssText = 'width: 48px; height: 48px; border-radius: 50%; background: rgba(217, 119, 6, 0.3); display: flex; align-items: center; justify-content: center; font-size: 24px; font-weight: bold; color: #fbbf24; flex-shrink: 0;';
    numCircle.textContent = idx + 1;

    const textDiv = document.createElement('p');
    textDiv.style.cssText = 'color: #e2e8f0; font-size: 18px; line-height: 1.6; margin: 0;';
    textDiv.textContent = item.situation;

    headerDiv.appendChild(numCircle);
    headerDiv.appendChild(textDiv);

    const dropZone = document.createElement('div');
    dropZone.className = 'drop-zone';
    dropZone.dataset.index = idx;
    dropZone.style.cssText = 'margin-left: 68px; margin-top: 16px; min-height: 80px; border: 2px dashed rgba(71, 85, 105, 0.8); border-radius: 8px; padding: 16px; display: flex; align-items: center; justify-content: center; color: #94a3b8; font-size: 16px; transition: all 0.2s;';
    dropZone.textContent = 'Drop answer here';

    dropZone.addEventListener('dragover', (e) => { e.preventDefault(); dropZone.style.background = '#fef3c7'; dropZone.style.borderColor = '#f59e0b'; });
    dropZone.addEventListener('dragleave', () => { dropZone.style.background = ''; dropZone.style.borderColor = 'rgba(71, 85, 105, 0.8)'; });
    dropZone.addEventListener('drop', (e) => {
      e.preventDefault();
      dropZone.style.background = '';
      dropZone.style.borderColor = 'rgba(71, 85, 105, 0.8)';
      if (!draggedEl) return;
      playDropSound();
      placeAnswer(dropZone, draggedEl);
    });

    card.appendChild(headerDiv);
    card.appendChild(dropZone);
    sitDiv.appendChild(card);
  });
}

function placeAnswer(zone, tag) {
  const idx = parseInt(zone.dataset.index);
  const clone = tag.cloneNode(true);
  clone.draggable = true;
  clone.addEventListener('dragstart', () => { draggedEl = clone; });
  zone.innerHTML = '';
  zone.appendChild(clone);
  userAnswers[idx] = tag.dataset.answer;
  zone.style.borderStyle = 'solid';
  draggedEl = null;
}

function checkAnswers() {
  let score = 0;
  document.querySelectorAll('.drop-zone').forEach((zone, idx) => {
    zone.style.background = '';
    zone.style.borderColor = 'rgba(71, 85, 105, 0.8)';
    if (userAnswers[idx] === data[idx].answer) {
      zone.style.background = '#d1fae5';
      zone.style.borderColor = '#10b981';
      score++;
    } else if (userAnswers[idx]) {
      zone.style.background = '#fee2e2';
      zone.style.borderColor = '#ef4444';
    }
  });
  if (score > 0) playCorrectSound(); else if (userAnswers.some(a => a)) playIncorrectSound();

  document.getElementById('score').textContent = score;
  const fb = document.getElementById('feedback');
  fb.style.display = 'block';

  if (score === 20) {
    clearInterval(timerInterval);
    setTimeout(() => playDiscoMusic(), 300);
    fb.style.background = 'rgba(16, 185, 129, 0.2)';
    fb.style.border = '2px solid #10b981';
    fb.style.color = '#d1fae5';
    fb.innerHTML = '🎉🚀💼 PERFECT SCORE! You\'re a career expert! 🚀🎉';
  } else {
    fb.style.background = 'rgba(217, 119, 6, 0.2)';
    fb.style.border = '2px solid #f59e0b';
    fb.style.color = '#fef3c7';
    fb.innerHTML = `${score}/20 correct. Incorrect answers are highlighted in red.`;
  }
}

function shuffleArray(arr) {
  return arr.sort(() => Math.random() - 0.5);
}

function resetActivity() {
  clearInterval(timerInterval);
  userAnswers = new Array(20).fill(null);
  document.getElementById('score').textContent = '0';
  document.getElementById('feedback').style.display = 'none';
  document.getElementById('timesup-screen').style.display = 'none';
  document.getElementById('quiz-screen').style.display = 'block';

  const shuffled = shuffleArray([...data]);
  data.length = 0;
  data.push(...shuffled);

  buildUI();
  startTimer();
}

// Element SDK init
const defaultConfig = {
  quiz_title: 'CSS Career Opportunities',
  background_color: '#0f172a',
  surface_color: '#1e293b',
  text_color: '#fef3c7',
  primary_action_color: '#f59e0b',
  secondary_action_color: '#64748b',
  font_family: 'DM Sans',
  font_size: 16
};

window.elementSdk.init({
  defaultConfig,
  onConfigChange: async (config) => {
    const title = config.quiz_title || defaultConfig.quiz_title;
    const el = document.getElementById('quiz-title');
    if (el) el.textContent = title;
  },
  mapToCapabilities: (config) => ({
    recolorables: [
      { get: () => config.background_color || defaultConfig.background_color, set: (v) => { config.background_color = v; window.elementSdk.setConfig({ background_color: v }); } },
      { get: () => config.surface_color || defaultConfig.surface_color, set: (v) => { config.surface_color = v; window.elementSdk.setConfig({ surface_color: v }); } },
      { get: () => config.text_color || defaultConfig.text_color, set: (v) => { config.text_color = v; window.elementSdk.setConfig({ text_color: v }); } },
      { get: () => config.primary_action_color || defaultConfig.primary_action_color, set: (v) => { config.primary_action_color = v; window.elementSdk.setConfig({ primary_action_color: v }); } },
      { get: () => config.secondary_action_color || defaultConfig.secondary_action_color, set: (v) => { config.secondary_action_color = v; window.elementSdk.setConfig({ secondary_action_color: v }); } }
    ],
    borderables: [],
    fontEditable: { get: () => config.font_family || defaultConfig.font_family, set: (v) => { config.font_family = v; window.elementSdk.setConfig({ font_family: v }); } },
    fontSizeable: { get: () => config.font_size || defaultConfig.font_size, set: (v) => { config.font_size = v; window.elementSdk.setConfig({ font_size: v }); } }
  }),
  mapToEditPanelValues: (config) => new Map([
    ["quiz_title", config.quiz_title || defaultConfig.quiz_title]
  ])
});

lucide.createIcons();
  </script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'a0ce63c6f7644669',t:'MTc4MTY2MDg4My4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
