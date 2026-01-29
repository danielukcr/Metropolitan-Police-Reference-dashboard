<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>MET Officer Handbook</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #0f172a;
  color: #e2e8f0;
  line-height: 1.6;
}

header {
  background: #111827;
  padding: 16px;
  border-bottom: 1px solid rgba(255,255,255,0.08);
}

nav button {
  background: none;
  border: none;
  color: #e2e8f0;
  font-weight: bold;
  margin-right: 12px;
  cursor: pointer;
}

nav button:hover {
  text-decoration: underline;
}

.container {
  max-width: 1200px;
  margin: auto;
  padding: 20px;
}

.section {
  display: none;
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 14px;
  padding: 18px;
  margin-bottom: 18px;
}

.section.active {
  display: block;
}

h1, h2, h3 {
  margin-top: 0;
}

ul {
  margin-left: 20px;
}

pre {
  background: #0b1022;
  border: 1px solid rgba(255,255,255,0.08);
  padding: 14px;
  border-radius: 12px;
  white-space: pre-wrap;
  font-family: monospace;
}

input {
  padding: 8px;
  border-radius: 8px;
  border: none;
  margin-right: 8px;
  margin-bottom: 10px;
}
</style>
</head>

<body>

<header>
  <nav>
    <button onclick="showSection('home')">Home</button>
    <button onclick="showSection('procedures')">Procedures</button>
    <button onclick="showSection('acts')">Acts</button>
    <button onclick="showSection('articles')">Articles</button>
  </nav>
</header>

<div class="container">

<!-- HOME -->
<div id="home" class="section active">
  <h1>MET Officer Handbook</h1>
  <p>
    A complete reference for MET officers covering mindset, procedures,
    UK legislation, and Human Rights guidance.
  </p>
</div>

<!-- PROCEDURES -->
<div id="procedures" class="section">

<h2>Professional standards</h2>

<h3>1) Professional mindset</h3>
<ul>
<li>Remain calm and composed in all situations.</li>
<li>Speak clearly, respectfully, and with authority.</li>
<li>Follow policy, law, and lawful orders.</li>
<li>Maintain a professional appearance and attitude.</li>
</ul>

<h3>2) Safety & discipline</h3>
<ul>
<li>Always assess risk before acting.</li>
<li>Communicate effectively with your team.</li>
<li>Use force proportionately and lawfully.</li>
<li>Keep situational awareness at all times.</li>
</ul>

<h3>3) Teamwork</h3>
<ul>
<li>Support colleagues and share information.</li>
<li>Understand your role within the unit.</li>
<li>If possible, crew with someone.</li>
</ul>

<h3>4) Public trust</h3>
<ul>
<li>Act fairly and without bias.</li>
<li>Explain actions when safe and appropriate.</li>
<li>Document incidents accurately.</li>
<li>Take accountability and improve continuously.</li>
</ul>

<h2>Quick checklist</h2>
<pre>
✅ Briefing completed
✅ Equipment checked (TASER, PAVA, CUFFS, VEHICLE CHECKS)
✅ Clear communication (Wait for radio to clear)
✅ Team roles understood (Do not overstep)
✅ Risk assessed (Complete a DRA)
✅ Professional conduct at all times
</pre>

<h2>Officer introduction (EDITABLE)</h2>

<input id="nameInput" placeholder="Officer Name">
<input id="callInput" placeholder="Call-sign">

<pre id="introText">
Hello, I am [NAME] [CALL-SIGN].
I am a police officer with the Metropolitan Police.
My body-cam is recording audio and video.
</pre>

<h2>Traffic stop</h2>
<pre>
Can I see your roleplay ID. This is required for the traffic stop.

I am going to run your identification through our system.
Remain in park and do not leave the vehicle.
Failure to comply may result in arrest.
</pre>

<h2>Police caution</h2>
<pre>
You do not have to say anything, but it may harm your defence
if you do not mention when questioned something which you later rely on in court.

Anything you say may be given in evidence.
</pre>

<h2>Initial pursuit radio call</h2>
<pre>
BREAK BREAK, MP MP, ACTIVE MESSAGE.
Vehicle failing to stop.

Location & Direction:
ROAD, BOROUGH, NESW, LANDMARKS

Vehicle:
MAKE, MODEL, VRM

Speed:
CURRENT SPEED

Vehicle Density:
LOW | MEDIUM | HIGH

Pedestrian Density:
LOW | MEDIUM | HIGH

Road Conditions:
WET | DRY | DIRT

Weather:
CLEAR | LIGHT | DARK

Visibility:
POOR | MODERATE | GOOD

DRA:
LOW | MEDIUM | HIGH

Driver:
IPP | ADVANCED | TPAC

Police Vehicle:
MARKED | UNMARKED
</pre>

</div>

<!-- Legislation -->
<div id="acts" class="section">
<h2>UK Legislation</h2>
<p>
<a href="https://danielukcr.github.io/Legislation/">Click here</a>
</p>
<p>
</p>
</div>

<!-- ARTICLES -->
<div id="articles" class="section">
<h2>Human Rights Articles</h2>
<p>
<a href="https://danielukcr.github.io/Articles/">Click here</a>
</p>
</div>

</div>

<script>
function showSection(id) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}

const nameInput = document.getElementById("nameInput");
const callInput = document.getElementById("callInput");
const introText = document.getElementById("introText");

function updateIntro() {
  const name = nameInput.value || "[NAME]";
  const call = callInput.value || "[CALL-SIGN]";

  introText.textContent =
`Hello, I am ${name} ${call}.
I am a police officer with the Metropolitan Police.
My body-cam is recording audio and video.`;
}

nameInput.addEventListener("input", updateIntro);
callInput.addEventListener("input", updateIntro);
</script>

</body>
</html>
