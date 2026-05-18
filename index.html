<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Atendente IA WhatsApp</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', sans-serif; }
  body { background: #050505; color: #fff; min-height: 100vh; }
  .page { display: flex; justify-content: center; padding: 20px 16px; min-height: 100vh; }
  .wrap { width: 100%; max-width: 420px; display: flex; flex-direction: column; gap: 14px; }
  .btn-green { background: #25D366; border: none; border-radius: 14px; color: #fff; padding: 16px; font-size: 16px; font-weight: 800; cursor: pointer; width: 100%; }
  .btn-green:disabled { opacity: 0.4; }
  .btn-back { background: none; border: none; color: #555; font-size: 16px; cursor: pointer; padding: 0; align-self: flex-start; margin-bottom: 4px; }
  .card { background: #0e0e0e; border: 1px solid #1a1a1a; border-radius: 16px; padding: 20px; display: flex; flex-direction: column; gap: 12px; }
  .lbl { color: #777; font-size: 12px; font-weight: 600; }
  .inp { background: #141414; border: 1px solid #222; border-radius: 10px; color: #fff; padding: 12px 14px; font-size: 15px; outline: none; width: 100%; font-family: inherit; }
  textarea.inp { resize: vertical; height: 65px; }
  .grid4 { display: grid; grid-template-columns: repeat(4,1fr); gap: 8px; }
  .seg-btn { background: #141414; border: 1px solid #222; border-radius: 10px; padding: 10px 4px; cursor: pointer; display: flex; flex-direction: column; align-items: center; gap: 4px; color: #777; font-size: 10px; line-height: 1.2; }
  .seg-btn.on { background: rgba(37,211,102,0.12); border-color: #25D366; color: #25D366; }
  .hidden { display: none !important; }
  #screen-loading { display: flex; align-items: center; justify-content: center; min-height: 100vh; }
  .spinner { width: 36px; height: 36px; border: 3px solid #1a1a1a; border-top: 3px solid #25D366; border-radius: 50%; animation: spin 0.8s linear infinite; }
  @keyframes spin { to { transform: rotate(360deg); } }
  .hero { background: linear-gradient(160deg,#0a1a0a,#111); border: 1px solid #1a2a1a; border-radius: 20px; padding: 28px; text-align: center; display: flex; flex-direction: column; align-items: center; gap: 10px; }
  .hero-emoji { font-size: 52px; }
  .hero-title { font-size: 26px; font-weight: 900; line-height: 1.2; }
  .hero-sub { color: #777; font-size: 15px; line-height: 1.6; }
  .hero-badge { background: rgba(37,211,102,0.12); border: 1px solid rgba(37,211,102,0.3); border-radius: 20px; padding: 6px 16px; color: #25D366; font-size: 13px; font-weight: 600; }
  .feat { background: #0e0e0e; border: 1px solid #1a1a1a; border-radius: 14px; padding: 16px; display: flex; gap: 14px; align-items: flex-start; }
  .feat-icon { font-size: 24px; background: #141414; border-radius: 10px; width: 44px; height: 44px; display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
  .feat-t { font-size: 15px; font-weight: 700; margin-bottom: 3px; }
  .feat-s { color: #666; font-size: 13px; }
  .btn-note { color: #333; font-size: 12px; text-align: center; }
  #screen-chat { display: flex; flex-direction: column; height: 100vh; max-width: 480px; margin: 0 auto; background: #ECE5DD; }
  .chat-head { background: #075E54; padding: 12px 16px; display: flex; align-items: center; gap: 12px; flex-shrink: 0; }
  .chat-av { width: 42px; height: 42px; border-radius: 50%; background: #25D366; display: flex; align-items: center; justify-content: center; font-weight: 800; font-size: 18px; color: #fff; flex-shrink: 0; }
  .chat-name { color: #fff; font-weight: 700; font-size: 15px; }
  .chat-status { color: #a8d8b9; font-size: 12px; }
  .chat-badge { border-radius: 20px; padding: 4px 10px; font-size: 12px; font-weight: 700; }
  .chat-banner { background: #FEF3C7; border-bottom: 1px solid #FCD34D; padding: 10px 16px; font-size: 13px; color: #92400E; text-align: center; }
  .chat-msgs { flex: 1; overflow-y: auto; padding: 12px; display: flex; flex-direction: column; gap: 4px; }
  .msg-row { display: flex; }
  .msg-row.user { justify-content: flex-end; }
  .msg-row.bot { justify-content: flex-start; }
  .bubble { max-width: 75%; border-radius: 12px; padding: 8px 12px; font-size: 14px; line-height: 1.5; box-shadow: 0 1px 2px rgba(0,0,0,0.15); color: #111; white-space: pre-wrap; }
  .bubble.bot { background: #fff; border-top-left-radius: 2px; }
  .bubble.user { background: #DCF8C6; border-top-right-radius: 2px; }
  .typing-dots { display: flex; gap: 4px; padding: 4px; align-items: center; }
  .dot { width: 7px; height: 7px; border-radius: 50%; background: #999; display: inline-block; animation: bounce 1.2s infinite; }
  .dot:nth-child(2) { animation-delay: 0.2s; }
  .dot:nth-child(3) { animation-delay: 0.4s; }
  @keyframes bounce { 0%,80%,100%{transform:translateY(0)} 40%{transform:translateY(-5px)} }
  .chat-input-bar { background: #F0F0F0; padding: 8px 12px; display: flex; gap: 8px; border-top: 1px solid #ddd; flex-shrink: 0; }
  .chat-inp { flex: 1; background: #fff; border: none; border-radius: 24px; padding: 10px 16px; font-size: 14px; outline: none; }
  .send-btn { background: #25D366; border: none; border-radius: 50%; width: 42px; height: 42px; color: #fff; font-size: 16px; cursor: pointer; flex-shrink: 0; display: flex; align-items: center; justify-content: center; }
  .send-btn:disabled { opacity: 0.4; }
  .admin-bar { background: #f5f5f5; border-top: 1px solid #e0e0e0; padding: 7px 16px; display: flex; justify-content: space-between; align-items: center; flex-shrink: 0; }
  .admin-bar span { color: #aaa; font-size: 11px; }
  .admin-bar button { background: none; border: 1px solid #ddd; border-radius: 8px; padding: 4px 10px; font-size: 11px; color: #888; cursor: pointer; }
  .pw-card { background: #0e0e0e; border: 1px solid #1a1a1a; border-radius: 20px; padding: 24px; display: flex; flex-direction: column; gap: 14px; align-items: center; text-align: center; }
  .pw-title { font-size: 22px; font-weight: 800; }
  .pw-sub { color: #666; font-size: 14px; line-height: 1.6; max-width: 320px; }
  .pw-contact { background: rgba(37,211,102,0.06); border: 1px solid rgba(37,211,102,0.2); border-radius: 12px; padding: 14px; text-align: left; width: 100%; }
  .pw-contact-title { color: #25D366; font-size: 13px; font-weight: 700; margin-bottom: 6px; }
  .pw-contact-text { color: #888; font-size: 13px; line-height: 1.6; }
  .code-inp { background: #141414; border: 2px solid #222; border-radius: 10px; color: #fff; padding: 14px; font-size: 22px; font-weight: 800; letter-spacing: 6px; outline: none; width: 100%; text-align: center; font-family: monospace; transition: border-color 0.2s; }
  .code-inp.error { border-color: #EF4444; color: #EF4444; }
  .code-inp.success { border-color: #25D366; color: #25D366; }
  .code-msg { font-size: 13px; }
  .code-msg.error { color: #EF4444; }
  .code-msg.success { color: #25D366; }
  .reset-btn { background: none; border: none; color: #333; font-size: 12px; cursor: pointer; }
  #screen-admin { display: flex; align-items: flex-start; justify-content: center; min-height: 100vh; padding: 20px 16px; }
  .admin-card { background: #0e0e0e; border: 1px solid #1a1a1a; border-radius: 20px; padding: 28px; width: 100%; max-width: 380px; display: flex; flex-direction: column; gap: 16px; }
  .code-result { background: rgba(37,211,102,0.1); border: 1px solid rgba(37,211,102,0.3); border-radius: 14px; padding: 20px; text-align: center; }
  .code-month { color: #555; font-size: 12px; margin-bottom: 8px; }
  .code-value { color: #25D366; font-size: 32px; font-weight: 900; letter-spacing: 4px; margin-bottom: 14px; font-family: monospace; }
  .copy-msg-btn { background: #1a1a1a; border: 1px solid #252525; border-radius: 8px; color: #888; padding: 8px 16px; font-size: 13px; cursor: pointer; }
  .how-it-works { background: #141414; border-radius: 12px; padding: 14px; }
  .how-title { color: #F59E0B; font-size: 12px; font-weight: 700; margin-bottom: 8px; }
  .how-text { color: #666; font-size: 12px; line-height: 1.8; }
</style>
</head>
<body>
<div id="screen-loading"><div class="spinner"></div></div>
<div id="screen-landing" class="page hidden">
  <div class="wrap">
    <div class="hero">
      <div class="hero-emoji">🤖</div>
      <div class="hero-title">Seu atendente no WhatsApp</div>
      <div class="hero-sub">Responde clientes 24h por dia, automático.</div>
      <div class="hero-badge">✨ 7 dias grátis — sem cartão</div>
    </div>
    <div class="feat"><div class="feat-icon">⚡</div><div><div class="feat-t">Responde na hora</div><div class="feat-s">Nenhum cliente fica sem resposta</div></div></div>
    <div class="feat"><div class="feat-icon">📅</div><div><div class="feat-t">Agenda sozinho</div><div class="feat-s">Marca horários automaticamente</div></div></div>
    <div class="feat"><div class="feat-icon">🧠</div><div><div class="feat-t">Fala do seu negócio</div><div class="feat-s">Configurado com seus serviços e preços</div></div></div>
    <button class="btn-green" onclick="showScreen('setup')">Testar grátis 7 dias →</button>
    <div class="btn-note">Configura em 2 minutos. Sem cartão.</div>
  </div>
</div>
<div id="screen-setup" class="page hidden">
  <div class="wrap">
    <button class="btn-back" onclick="showScreen('landing')">← Voltar</button>
    <div style="font-size:22px;font-weight:800;text-align:center;">Configure seu atendente</div>
    <div style="color:#555;font-size:13px;text-align:center;">Preencha com os dados do seu negócio</div>
    <div class="card">
      <div class="lbl">📛 Nome do negócio *</div>
      <div style="color:#555;font-size:11px;margin-top:-8px;margin-bottom:4px">Como seu negócio se chama</div>
      <input class="inp" id="inp-name" placeholder="Ex: Salão da Ana, Clínica Saúde Total...">
      <div class="lbl">📱 Seu WhatsApp * (com DDD, só números)</div>
      <div style="color:#555;font-size:11px;margin-top:-8px;margin-bottom:4px">Necessário para gerar seu código de acesso</div>
      <input class="inp" id="inp-phone" placeholder="Ex: 85986897912" type="tel">
      <div class="lbl">🏢 Tipo de negócio *</div>
      <div style="color:#555;font-size:11px;margin-top:-8px;margin-bottom:4px">Toque para selecionar o seu</div>
      <div class="grid4" id="seg-grid"></div>
      <div class="lbl">🕐 Horário de funcionamento</div>
      <div style="color:#555;font-size:11px;margin-top:-8px;margin-bottom:4px">Quando você atende os clientes</div>
      <input class="inp" id="inp-hours" placeholder="Ex: Seg a Sex das 8h às 18h, Sáb das 8h às 12h">
      <div class="lbl">📍 Endereço do negócio</div>
      <div style="color:#555;font-size:11px;margin-top:-8px;margin-bottom:4px">Rua, número, bairro e cidade</div>
      <input class="inp" id="inp-address" placeholder="Ex: Rua das Flores, 123 - Centro, Fortaleza-CE">
      <div class="lbl">💰 Serviços e preços</div>
      <div style="color:#555;font-size:11px;margin-top:-8px;margin-bottom:4px">Liste o que você oferece com os valores</div>
      <textarea class="inp" id="inp-services" placeholder="Ex: Corte R$60, Escova R$50, Coloração R$150, Manicure R$35..."></textarea>
      <div class="lbl">ℹ️ Outras informações</div>
      <div style="color:#555;font-size:11px;margin-top:-8px;margin-bottom:4px">Formas de pagamento, estacionamento, regras...</div>
      <textarea class="inp" id="inp-extra" placeholder="Ex: Aceitamos PIX, cartão e dinheiro. Agendamento obrigatório. Estacionamento gratuito."></textarea>
    </div>
    <button class="btn-green" id="btn-setup" onclick="handleSetup()">Ativar grátis por 7 dias 🚀</button>
    <div class="btn-note">Sem cartão de crédito. Cancele quando quiser.</div>
  </div>
</div>
<div id="screen-chat" class="hidden">
  <div class="chat-head">
    <div class="chat-av" id="chat-avatar">B</div>
    <div style="flex:1"><div class="chat-name" id="chat-name">Negócio</div><div class="chat-status">🟢 Online</div></div>
    <div class="chat-badge" id="chat-badge"></div>
  </div>
  <div class="chat-banner hidden" id="chat-banner"></div>
  <div class="chat-msgs" id="chat-msgs"></div>
  <div class="chat-input-bar">
    <input class="chat-inp" id="chat-inp" placeholder="Digite uma mensagem..." onkeydown="handleKey(event)">
    <button class="send-btn" id="send-btn" onclick="sendMessage()">➤</button>
  </div>
  <div class="admin-bar"><span>Preview do atendente</span><button onclick="resetApp()">⚙️ Reconfigurar</button></div>
</div>
<div id="screen-paywall" class="page hidden">
  <div class="wrap">
    <div class="pw-card">
      <div style="font-size:48px">🔒</div>
      <div class="pw-title">Período grátis encerrado</div>
      <div class="pw-sub">Seu atendente ficou ativo por 7 dias. Para continuar, renove seu acesso.</div>
      <div class="pw-contact" style="width:100%">
        <div class="pw-contact-title">💸 Pague via PIX e receba seu código</div>
        <div class="pw-contact-text">
          <strong style="color:#fff">Chave PIX (celular):</strong><br>
          <span style="font-size:20px;font-weight:900;color:#25D366;letter-spacing:1px">(85) 98689-7912</span><br><br>
          Após o pagamento, envie o comprovante para esse mesmo número no WhatsApp. Você receberá seu código em minutos. ✅
        </div>
        <a href="https://wa.me/5585986897912?text=Olá!%20Quero%20renovar%20meu%20acesso.%20Segue%20o%20comprovante%20do%20PIX%20em%20anexo." style="display:block;background:#25D366;color:#fff;text-align:center;padding:12px;border-radius:10px;font-weight:700;font-size:14px;text-decoration:none;margin-top:12px">
          📲 Enviar comprovante no WhatsApp
        </a>
      </div>
      <div class="lbl" style="align-self:flex-start">Seu código de acesso</div>
      <input class="code-inp" id="code-inp" placeholder="XXXXXXXX" maxlength="8" oninput="this.value=this.value.toUpperCase()">
      <div class="code-msg hidden" id="code-msg"></div>
      <button class="btn-green" onclick="handleUnlock()">Liberar acesso por 30 dias →</button>
    </div>
    <button class="reset-btn" onclick="resetApp()">Usar conta diferente</button>
  </div>
</div>
<div id="screen-admin" class="hidden">
  <div class="admin-card">
    <div style="font-size:32px;text-align:center">🔑</div>
    <div style="font-size:20px;font-weight:800;text-align:center">Painel do Dono</div>
    <div style="color:#555;font-size:13px;text-align:center">Gere o código após o pagamento</div>
    <div><div class="lbl" style="margin-bottom:6px">WHATSAPP DO CLIENTE</div>
    <input class="inp" id="admin-phone" placeholder="Ex: 85986897912" type="tel"></div>
    <button class="btn-green" onclick="generateCode()">Gerar código →</button>
    <div class="code-result hidden" id="code-result">
      <div class="code-month" id="code-month"></div>
      <div class="code-value" id="code-value"></div>
      <button class="copy-msg-btn" onclick="copyCodeMsg()">📋 Copiar mensagem pro cliente</button>
    </div>
    <div class="how-it-works">
      <div class="how-title">⚙️ Como funciona</div>
      <div class="how-text">1. Cliente usa 7 dias grátis<br>2. Acesso bloqueia<br>3. Cliente paga e te chama<br>4. Você gera o código aqui<br>5. Ele digita → 30 dias liberados<br>6. Mês seguinte bloqueia de novo</div>
    </div>
  </div>
</div>
<script>
const SECRET_KEY="minhachavesecreta123";
const TRIAL_DAYS=7;
const PAID_DAYS=30;
const SEGMENTS=[{emoji:"🦷",label:"Clínica"},{emoji:"💇",label:"Salão"},{emoji:"🍕",label:"Restaurante"},{emoji:"🏠",label:"Imobiliária"},{emoji:"🛍️",label:"Loja"},{emoji:"💪",label:"Academia"},{emoji:"🐾",label:"Pet Shop"},{emoji:"🔧",label:"Serviços"}];
const PROMPTS={"Clínica":"Você é atendente virtual de uma clínica. Agende consultas, informe horários. Seja simpático. Colete nome, serviço e data. Mensagens curtas estilo WhatsApp.","Salão":"Você é atendente de um salão. Agende horários, informe serviços. Colete nome, serviço e data.","Restaurante":"Você é atendente de restaurante. Receba pedidos, informe cardápio. Colete pedido, endereço e pagamento.","Imobiliária":"Você é assistente de imobiliária. Ajude a encontrar imóveis, agende visitas.","Loja":"Você é atendente de loja. Informe produtos e preços. Ajude a fechar compras.","Academia":"Você é atendente de academia. Informe planos e aulas.","Pet Shop":"Você é atendente de pet shop. Agende banho e tosa, informe preços.","Serviços":"Você é atendente. Agende visitas, passe orçamentos."};
let selectedSegment="",chatHistory=[],currentData=null;
function makeCode(p,s){const m=new Date().toISOString().slice(0,7);const r=p+"-"+m+"-"+s;let h=0;for(let i=0;i<r.length;i++){h=((h<<5)-h)+r.charCodeAt(i);h|=0;}return Math.abs(h).toString(36).toUpperCase().slice(0,8);}
function validateCode(i,p,s){return i.toUpperCase()===makeCode(p,s);}
const screens=["loading","landing","setup","chat","paywall","admin"];
function showScreen(n){screens.forEach(s=>{const e=document.getElementById("screen-"+s);if(e){e.classList.add("hidden");e.style.display="";}});const t=document.getElementById("screen-"+n);if(t){t.classList.remove("hidden");if(n==="chat")t.style.display="flex";if(n==="admin")t.style.display="flex";}}
window.onload=function(){
if(window.location.search.includes("admin")){showScreen("admin");return;}
const grid=document.getElementById("seg-grid");
SEGMENTS.forEach(seg=>{const btn=document.createElement("button");btn.className="seg-btn";btn.innerHTML='<span style="font-size:20px">'+seg.emoji+'</span><span>'+seg.label+'</span>';btn.onclick=()=>{document.querySelectorAll(".seg-btn").forEach(b=>b.classList.remove("on"));btn.classList.add("on");selectedSegment=seg.label;};grid.appendChild(btn);});
const saved=localStorage.getItem("saas_data");
if(!saved){showScreen("landing");return;}
const d=JSON.parse(saved);currentData=d;const now=new Date();
if(d.paidUntil){const pl=Math.ceil((new Date(d.paidUntil)-now)/86400000);if(pl>0){startChat(d,pl,false);return;}}
const tl=TRIAL_DAYS-Math.floor((now-new Date(d.startDate))/86400000);
if(tl>0)startChat(d,tl,true);else showScreen("paywall");
};
function handleSetup(){const name=document.getElementById("inp-name").value.trim();const phone=document.getElementById("inp-phone").value.replace(/\D/g,"");const hours=document.getElementById("inp-hours").value.trim();const address=document.getElementById("inp-address").value.trim();const services=document.getElementById("inp-services").value.trim();const extra=document.getElementById("inp-extra").value.trim();if(!name||!selectedSegment||!phone)return;const fullExtra=[hours?"Horário: "+hours:"",address?"Endereço: "+address:"",services?"Serviços/Preços: "+services:"",extra].filter(Boolean).join(". ");const d={businessName:name,segment:selectedSegment,phone,extra:fullExtra,startDate:new Date().toISOString()};localStorage.setItem("saas_data",JSON.stringify(d));currentData=d;startChat(d,TRIAL_DAYS,true);}
function startChat(d,daysLeft,isTrial){document.getElementById("chat-avatar").textContent=d.businessName[0].toUpperCase();document.getElementById("chat-name").textContent=d.businessName;const badge=document.getElementById("chat-badge");const color=daysLeft<=3?"#EF4444":"#25D366";badge.textContent=isTrial?daysLeft+"d grátis":daysLeft+"d restantes";badge.style.background=color+"22";badge.style.color=color;badge.style.border="1px solid "+color+"44";const banner=document.getElementById("chat-banner");if(daysLeft<=3){banner.classList.remove("hidden");banner.innerHTML="⚠️ Acesso expira em <strong>"+daysLeft+" dia"+(daysLeft!==1?"s":"")+"</strong>. Entre em contato para renovar.";}chatHistory=[];document.getElementById("chat-msgs").innerHTML="";addBotMsg("Olá! 👋 Bem-vindo ao atendimento do *"+d.businessName+"*. Como posso te ajudar?");showScreen("chat");document.getElementById("screen-chat").style.display="flex";document.getElementById("screen-chat").style.flexDirection="column";}
function addBotMsg(text){const div=document.createElement("div");div.className="msg-row bot";div.innerHTML='<div class="bubble bot">'+text.replace(/\*(.*?