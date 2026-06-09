<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>👑 King Kayseur - Signalement WhatsApp</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:url('272408.jpg') center center/cover no-repeat fixed;
min-height:100vh;
color:white;
}

.overlay{
background:rgba(0,0,0,.75);
min-height:100vh;
padding:30px 15px;
}

h1{
text-align:center;
font-size:40px;
color:#ffd700;
text-shadow:0 0 15px #ffd700, 0 0 30px #ff8c00;
margin-top:30px;
}

.subtitle{
text-align:center;
font-size:18px;
margin-top:10px;
margin-bottom:40px;
color:#ffd700;
}

.form-box{
max-width:700px;
margin:auto;
background:rgba(0,0,0,.7);
border:1px solid rgba(255,215,0,.4);
border-radius:25px;
padding:25px;
backdrop-filter:blur(10px);
}

label{
display:block;
margin-top:20px;
margin-bottom:8px;
font-size:18px;
}

input, textarea{
width:100%;
padding:15px;
border:none;
border-radius:15px;
background:#111;
color:white;
font-size:16px;
}

textarea{
height:180px;
resize:none;
}

button{
width:100%;
margin-top:25px;
padding:18px;
border:none;
border-radius:20px;
font-size:20px;
font-weight:bold;
cursor:pointer;
background:linear-gradient(45deg, #ffd700, #ff8c00);
color:black;
box-shadow:0 0 20px #ffd700;
}

button:hover{
transform:scale(1.02);
}

.info-msg{
text-align:center;
margin-top:20px;
font-size:13px;
color:#ffd700;
}

.crown{
font-size:30px;
text-align:center;
margin-bottom:10px;
}

.toast{
position:fixed;
bottom:30px;
left:50%;
transform:translateX(-50%);
background:#ffd700;
color:black;
padding:12px 25px;
border-radius:30px;
font-weight:bold;
z-index:1000;
animation:fadeout 3s forwards;
}

@keyframes fadeout{
0%{opacity:1;bottom:30px;}
70%{opacity:1;}
100%{opacity:0;bottom:-50px;display:none;}
}
</style>
</head>

<body>

<div class="overlay">

<div class="crown">👑</div>

<h1>𝑲𝒊𝒏𝒈 𝑲𝒂𝒚𝒔𝒆𝒖𝒓</h1>

<div class="subtitle">
Le Roi du Signalement WhatsApp
</div>

<div class="form-box">

<label>📱 Numéro à signaler</label>
<input id="numero" placeholder="+509xxxxxxx">

<label>⚠️ Raison du signalement</label>
<input id="raison" placeholder="Spam, scam, bots, harcèlement...">

<label>📝 Description détaillée</label>
<textarea id="description" placeholder="Décrivez le problème précisément..."></textarea>

<button onclick="envoyerSignalement()">
👑 Signaler comme King Kayseur 👑
</button>

<div class="info-msg">
⚡ Envoi direct - TOUS les supports WhatsApp ⚡
</div>

</div>
</div>

<script>
// Liste complète des destinataires
const TOUS_DESTINATAIRES = [
"smb_web@support.whatsapp.com",
"business@support.whatsapp.com",
"enterprise@support.whatsapp.com",
"android@support.whatsapp.com",
"android-support@whatsapp.com",
"iphone@support.whatsapp.com",
"android_web@support.whatsapp.com",
"iphone_web@support.whatsapp.com",
"web@support.whatsapp.com",
"webclient_web@support.whatsapp.com",
"windowsphone@support.whatsapp.com",
"wp_web@support.whatsapp.com",
"kaios@support.whatsapp.com",
"account@support.whatsapp.com",
"support@whatsapp.com"
];

function showToast(message){
const toast = document.createElement('div');
toast.className = 'toast';
toast.textContent = message;
document.body.appendChild(toast);
setTimeout(() => toast.remove(), 3000);
}

function envoyerSignalement(){
const numero = document.getElementById("numero").value;
const raison = document.getElementById("raison").value;
const description = document.getElementById("description").value;

if(!numero){
showToast("❌ Veuillez entrer un numéro !");
return;
}

const destinatairesStr = TOUS_DESTINATAIRES.join(",");
const sujet = encodeURIComponent("URGENT - Signalement WhatsApp - King Kayseur");
const corps = encodeURIComponent(
`👑 SIGNALEMENT KING KAYSEUR 👑

Numéro suspect : ${numero}

Raison : ${raison}

Description détaillée :
${description}

---
Signalement officiel - King Kayseur
`
);

// Créer un lien temporaire et cliquer dessus
const mailtoLink = document.createElement('a');
mailtoLink.href = `mailto:${destinatairesStr}?subject=${sujet}&body=${corps}`;
mailtoLink.style.display = 'none';
document.body.appendChild(mailtoLink);
mailtoLink.click();
document.body.removeChild(mailtoLink);

showToast("👑 Ouverture de votre messagerie...");

// Fallback si ça ne marche pas
setTimeout(() => {
    showToast("📧 Si rien ne s'ouvre, vérifiez votre appli email");
}, 1000);
}
</script>

</body>
</html>
