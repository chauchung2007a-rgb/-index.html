<!DOCTYPE html>
<html lang="km">
<head>
<meta charset="UTF-8">

<meta name="viewport"
      content="width=device-width,
      initial-scale=1.0,
      maximum-scale=1.0,
      user-scalable=no">

<title> 𝑪𝒉𝒂𝒕𝒔 </title>

<style>

/* =====================================================
                   01. GLOBAL
===================================================== */

*{
  box-sizing:border-box;
  -webkit-tap-highlight-color:transparent;
}

:root{
  /* Premium Blue Frosted Glass Palette */
  --sky:#B7E8F5;
  --sky2:#DDF7FF;
  --card:rgba(255,255,255,0.65);
  --text:#173944;
  --muted:#5A7A85;
  --primary:#38B6E8;
  --soft:rgba(255,255,255,0.45);
  --border:rgba(255,255,255,0.70);
  --danger:#e35d6a;

  --chatGreen:rgba(180,230,245,0.55);
  --chatGreen2:rgba(200,240,250,0.45);
  --chatBubble:rgba(255,255,255,0.75);
  
  /* Glass Effect Variables */
  --glass-bg: rgba(255,255,255,0.65);
  --glass-border: rgba(255,255,255,0.75);
  --glass-shadow: 0 8px 30px rgba(50,130,160,0.15);
  --glass-blur: blur(18px);
}

body.dark{
  --sky:#0F2D3C;
  --sky2:#1A3E4D;
  --card:rgba(20,45,60,0.75);
  --text:#eefcff;
  --muted:#a9c1c9;
  --primary:#32b3ee;
  --soft:rgba(30,60,75,0.55);
  --border:rgba(255,255,255,0.30);

  --chatGreen:rgba(25,55,70,0.65);
  --chatGreen2:rgba(20,45,58,0.55);
  --chatBubble:rgba(35,65,80,0.75);
  
  /* Dark Glass Effect */
  --glass-bg: rgba(15,45,60,0.70);
  --glass-border: rgba(255,255,255,0.35);
  --glass-shadow: 0 8px 30px rgba(0,20,30,0.35);
  --glass-blur: blur(18px);
}

html,
body{
  width:100%;
  height:100%;
  margin:0;
  overflow:hidden;

  font-family:
    Arial,
    "Noto Sans Khmer",
    sans-serif;
}

body{
  background:var(--sky);
  color:var(--text);
}

button,
input,
textarea,
select{
  font:inherit;
}

button{
  cursor:pointer;
}

.app{
  position:relative;

  width:100%;
  max-width:520px;
  height:100dvh;

  margin:auto;
  overflow:hidden;

  background:
    radial-gradient(
      circle at 12% 7%,
      rgba(255,255,255,0.85),
      transparent 35%
    ),
    radial-gradient(
      circle at 90% 15%,
      rgba(180,230,245,0.75),
      transparent 35%
    ),
    radial-gradient(
      circle at 50% 85%,
      rgba(140,210,235,0.60),
      transparent 40%
    ),
    linear-gradient(
      160deg,
      #B7E8F5 0%,
      #DDF7FF 50%,
      #C9F0FA 100%
    );
}

body.dark .app{
  background:
    radial-gradient(
      circle at 12% 7%,
      rgba(50,90,110,0.65),
      transparent 35%
    ),
    radial-gradient(
      circle at 90% 15%,
      rgba(30,60,80,0.55),
      transparent 35%
    ),
    radial-gradient(
      circle at 50% 85%,
      rgba(20,50,65,0.65),
      transparent 40%
    ),
    linear-gradient(
      160deg,
      #0F2D3C 0%,
      #1A3E4D 50%,
      #153544 100%
    );
}

/* =====================================================
                   02. SCREENS
===================================================== */

.screen{
  position:absolute;
  inset:0;

  display:none;

  overflow-y:auto;

  padding:14px 14px 105px;
}

.screen.active{
  display:block;
}

/* =====================================================
                   03. COMMON
===================================================== */

.topbar{
  min-height:52px;

  display:flex;
  align-items:center;
  gap:10px;

  margin-bottom:10px;
}

.topbar h1{
  flex:1;
  margin:0;
  font-size:25px;
}

.icon{
  width:44px;
  height:44px;

  border:0;
  border-radius:14px;

  background:var(--glass-bg);
  color:var(--text);

  font-size:20px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  border:1px solid var(--glass-border);

  box-shadow:var(--glass-shadow);
}

.card{
  background:var(--glass-bg);

  border:1px solid var(--glass-border);

  border-radius:20px;

  padding:14px;
  margin-bottom:11px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  box-shadow:var(--glass-shadow);
}

.input,
.select,
.textarea{
  width:100%;

  border:1px solid var(--border);

  border-radius:14px;

  background:var(--glass-bg);
  color:var(--text);

  outline:none;

  padding:12px 14px;
  margin-bottom:9px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.input{
  height:48px;
}

.textarea{
  min-height:110px;
  resize:none;
}

.primary{
  width:100%;
  height:49px;

  border:0;
  border-radius:14px;

  background:linear-gradient(135deg, #38B6E8, #5CC8F0);
  color:white;

  font-weight:bold;

  box-shadow:0 4px 15px rgba(56,182,232,0.35);

  transition:all 0.3s ease;
}

.primary:active{
  transform:scale(0.97);
  box-shadow:0 2px 8px rgba(56,182,232,0.25);
}

.secondary{
  width:100%;
  height:47px;

  border:1px solid var(--glass-border);
  border-radius:14px;

  background:var(--glass-bg);
  color:var(--text);

  margin-top:8px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.muted{
  color:var(--muted);
}

.hidden{
  display:none!important;
}

/* =====================================================
                   04. BRAND
===================================================== */

.brand{
  text-align:center;
  padding:10px 0 20px;
}

.brandIcon{
  width:80px;
  height:80px;
  object-fit:cover;
  border-radius:50%;
  border:2px solid rgba(255,255,255,0.80);
  box-shadow:0 8px 25px rgba(50,130,160,0.25);
}

.brand h1{
  margin:8px 0 4px;
  font-size:28px;
}

.brand p{
  margin:0;
}

.signupField{
  display:flex;
  align-items:center;

  gap:10px;

  height:55px;

  margin-bottom:12px;

  border:1px solid var(--glass-border);
  border-radius:999px;

  background:var(--glass-bg);

  padding:0 16px 0 6px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  box-shadow:var(--glass-shadow);
}

.signupFieldIcon{
  flex-shrink:0;

  width:40px;
  height:40px;

  border-radius:50%;

  display:flex;
  align-items:center;
  justify-content:center;

  line-height:1;

  font-size:18px;

  background:linear-gradient(135deg, #B7E8F5, #DDF7FF);

  box-shadow:0 3px 10px rgba(50,130,160,0.25);
}

.signupInput{
  flex:1;

  min-width:0;

  height:100%;

  margin-bottom:0;

  border:0;

  border-radius:0;

  background:transparent;

  padding:0;
}

/* =====================================================
                   05. HOME
===================================================== */

.googleSearchBar{
  display:flex;
  align-items:center;
  gap:8px;

  width:100%;
  height:48px;

  border:1px solid var(--glass-border);
  border-radius:24px;

  background:var(--glass-bg);

  padding:0 8px 0 16px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  box-shadow:var(--glass-shadow);
}

.googleSearchBar .searchIcon{
  font-size:17px;
  color:var(--muted);
  flex-shrink:0;
}

.googleSearchInput{
  flex:1;
  min-width:0;

  height:100%;

  border:0;
  outline:none;
  background:transparent;

  color:var(--text);
  font-size:16px;
}

.googleSearchInput::placeholder{
  color:var(--muted);
}

.searchClearBtn{
  width:30px;
  height:30px;

  flex-shrink:0;

  border:0;
  border-radius:50%;

  background:var(--soft);
  color:var(--text);

  font-size:14px;

  display:flex;
  align-items:center;
  justify-content:center;
}

.newsHeading{
  font-size:19px;
  font-weight:bold;
  margin:12px 3px 9px;
}

.newsCard{
  padding:0;
  overflow:hidden;
}

.newsImage{
  height:185px;

  display:flex;
  justify-content:center;
  align-items:center;

  font-size:72px;

  background:linear-gradient(135deg, #C9F0FA, #8FD8EE);
}

.newsBody{
  padding:14px;
}

.newsTitle{
  font-size:18px;
  line-height:1.4;
  font-weight:bold;
}

.newsMeta{
  color:var(--muted);
  font-size:13px;
  margin-top:6px;
}

.newsText{
  color:var(--muted);
  font-size:14px;
  line-height:1.6;
  margin-top:8px;
}

.article{
  display:none;
}

.article.show{
  display:block;
}

.articleBack{
  margin-bottom:14px;
}

.articleImage{
  height:235px;

  border-radius:21px;

  display:flex;
  align-items:center;
  justify-content:center;

  font-size:85px;

  background:var(--soft);

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.article h1{
  font-size:24px;
  line-height:1.4;
}

.articleContent{
  line-height:1.85;
  font-size:16px;
}

/* =====================================================
                   06. CHATS
===================================================== */

.chat{
  display:flex;
  align-items:center;
  gap:12px;
}

.chatAvatar{
  width:56px;
  height:56px;

  flex-shrink:0;

  border-radius:50%;

  display:flex;
  align-items:center;
  justify-content:center;

  background:linear-gradient(135deg, #729af6, #625de0);

  color:white;

  font-weight:bold;
  font-size:20px;

  border:2px solid rgba(255,255,255,0.75);

  box-shadow:0 3px 10px rgba(50,70,150,0.25);
}

.chatInfo{
  flex:1;
  min-width:0;
}

.chatInfo b,
.chatInfo small{
  display:block;
}

.chatInfo small{
  color:var(--muted);
  margin-top:5px;
}

/* =====================================================
                07. CHAT DETAIL
===================================================== */

#chatDetail{
  padding:0;

  overflow:hidden;

  background:linear-gradient(135deg, #B7E8F5 0%, #DDF7FF 50%, #C9F0FA 100%);
}

body.dark #chatDetail{
  background:linear-gradient(135deg, #0F2D3C 0%, #1A3E4D 50%, #153544 100%);
}

.chatWindow{
  position:relative;

  width:100%;
  height:100%;

  overflow:hidden;

  background:
    radial-gradient(
      circle at 10% 15%,
      rgba(140,210,235,0.50),
      transparent 35%
    ),
    radial-gradient(
      circle at 88% 20%,
      rgba(255,255,255,0.60),
      transparent 35%
    ),
    radial-gradient(
      circle at 40% 60%,
      rgba(180,230,245,0.55),
      transparent 40%
    ),
    linear-gradient(
      135deg,
      var(--chatGreen),
      var(--chatGreen2)
    );
}

.chatWindow:before{
  content:"";

  position:absolute;
  inset:0;

  opacity:0.06;

  background-image:
    radial-gradient(
      circle,
      rgba(255,255,255,0.50) 1px,
      transparent 1.5px
    );

  background-size:25px 25px;

  pointer-events:none;
}

/* =====================================================
                08. CHAT HEADER
===================================================== */

.chatHeader{
  position:absolute;

  z-index:20;

  top:0;
  left:0;
  right:0;

  height:82px;

  display:flex;
  align-items:center;

  padding:11px 14px 8px;

  gap:9px;

  background:rgba(255,255,255,0.35);

  backdrop-filter:blur(18px);
  -webkit-backdrop-filter:blur(18px);

  border-bottom:1px solid rgba(255,255,255,0.50);
}

.chatBack{
  width:53px;
  height:53px;

  flex-shrink:0;

  border:0;
  border-radius:50%;

  background:rgba(255,255,255,0.65);

  color:#173944;

  font-size:34px;

  display:flex;
  align-items:center;
  justify-content:center;

  backdrop-filter:blur(12px);
  -webkit-backdrop-filter:blur(12px);

  border:1px solid rgba(255,255,255,0.75);

  box-shadow:0 4px 15px rgba(50,130,160,0.15);
}

.chatHeaderName{
  flex:1;

  min-width:0;

  height:57px;

  display:flex;
  align-items:center;
  justify-content:center;

  flex-direction:column;

  background:rgba(255,255,255,0.55);

  border-radius:32px;

  padding:4px 15px;

  color:#173944;

  backdrop-filter:blur(15px);
  -webkit-backdrop-filter:blur(15px);

  border:1px solid rgba(255,255,255,0.70);

  box-shadow:0 4px 18px rgba(50,130,160,0.15);

  cursor:pointer;
}

.chatHeaderName strong{
  font-size:22px;

  line-height:1.1;

  white-space:nowrap;
  overflow:hidden;
  text-overflow:ellipsis;

  max-width:100%;
}

.chatHeaderName small{
  font-size:14px;

  color:#5A7A85;

  margin-top:3px;
}

.chatProfile{
  width:58px;
  height:58px;

  flex-shrink:0;

  border:3px solid rgba(255,255,255,0.80);

  border-radius:50%;

  background:linear-gradient(135deg, #7da8fa, #655ce5);

  color:white;

  display:flex;
  align-items:center;
  justify-content:center;

  font-size:24px;
  font-weight:bold;

  box-shadow:0 3px 13px rgba(50,70,150,0.30);

  cursor:pointer;
}

/* =====================================================
                  09. CHAT MESSAGES
===================================================== */

.messages{
  position:absolute;

  z-index:3;

  top:82px;
  left:0;
  right:0;
  bottom:83px;

  overflow-y:auto;

  padding:18px 13px 20px;

  display:flex;
  flex-direction:column;

  justify-content:flex-end;

  gap:7px;
}

.chatDate{
  align-self:center;

  background:rgba(56,182,232,0.70);

  color:white;

  padding:6px 13px;

  border-radius:15px;

  font-weight:bold;

  font-size:13px;

  margin-bottom:5px;

  backdrop-filter:blur(10px);
  -webkit-backdrop-filter:blur(10px);

  border:1px solid rgba(255,255,255,0.50);
}

.joined{
  align-self:center;

  background:rgba(56,182,232,0.65);

  color:white;

  padding:7px 13px;

  border-radius:16px;

  font-weight:bold;

  font-size:14px;

  text-align:center;

  backdrop-filter:blur(10px);
  -webkit-backdrop-filter:blur(10px);

  border:1px solid rgba(255,255,255,0.50);
}

.messageRow{
  display:flex;
  width:100%;
}

.messageRow.mine{
  justify-content:flex-end;
}

.messageBubble{
  max-width:78%;

  padding:9px 12px;

  border-radius:17px;

  background:var(--chatBubble);

  color:#173944;

  box-shadow:0 2px 10px rgba(50,130,160,0.12);

  font-size:15px;

  line-height:1.45;

  backdrop-filter:blur(12px);
  -webkit-backdrop-filter:blur(12px);

  border:1px solid rgba(255,255,255,0.60);
}

.messageRow.mine .messageBubble{
  background:rgba(180,230,245,0.70);

  border:1px solid rgba(150,215,240,0.70);
}

/* =====================================================
                  10. CHAT INPUT
===================================================== */

.chatInputBar{
  position:absolute;

  z-index:30;

  left:0;
  right:0;
  bottom:0;

  height:82px;

  display:flex;
  align-items:center;

  padding:10px 12px;

  background:rgba(255,255,255,0.30);

  backdrop-filter:blur(18px);
  -webkit-backdrop-filter:blur(18px);

  border-top:1px solid rgba(255,255,255,0.50);
}

.messageBarPill{
  flex:1;

  min-width:0;

  height:55px;

  display:flex;
  align-items:center;

  gap:2px;

  border-radius:28px;

  background:rgba(255,255,255,0.55);

  padding:0 6px 0 14px;

  backdrop-filter:blur(15px);
  -webkit-backdrop-filter:blur(15px);

  border:1px solid rgba(255,255,255,0.70);

  box-shadow:0 3px 12px rgba(50,130,160,0.12);
}

.msgIconBtn{
  width:36px;
  height:36px;

  flex-shrink:0;

  border:0;
  border-radius:50%;

  background:transparent;

  color:#3f5054;

  font-size:21px;

  display:flex;
  align-items:center;
  justify-content:center;
}

.messageField{
  flex:1;

  min-width:0;

  height:100%;

  border:0;

  outline:none;

  background:transparent;

  color:#173944;

  font-size:17px;

  padding:0 4px;
}

.messageField::placeholder{
  color:#8d9694;
}

.sendButton{
  display:none;

  width:42px;
  height:42px;

  flex-shrink:0;

  align-items:center;
  justify-content:center;

  border:0;
  border-radius:14px;

  background:linear-gradient(135deg, #38B6E8, #5CC8F0);

  color:white;

  font-size:19px;

  box-shadow:0 3px 12px rgba(56,182,232,0.40);
}

/* =====================================================
            11. FRIEND PROFILE / CALL PANEL
===================================================== */

.friendPanel{
  position:absolute;

  z-index:100;

  inset:0;

  display:none;

  align-items:flex-end;

  background:rgba(0,0,0,0.30);

  backdrop-filter:blur(5px);
  -webkit-backdrop-filter:blur(5px);
}

.friendPanel.show{
  display:flex;
}

.friendSheet{
  width:100%;

  max-height:88%;

  overflow-y:auto;

  padding:18px 16px 25px;

  background:linear-gradient(135deg, #DDF7FF, #C9F0FA);

  border-radius:28px 28px 0 0;

  color:var(--text);

  animation:sheetUp .22s ease;

  box-shadow:0 -8px 30px rgba(50,130,160,0.20);
}

body.dark .friendSheet{
  background:linear-gradient(135deg, #1A3E4D, #153544);
}

@keyframes sheetUp{
  from{
    transform:translateY(100%);
  }

  to{
    transform:translateY(0);
  }
}

.friendHandle{
  width:45px;
  height:5px;

  border-radius:10px;

  background:rgba(255,255,255,0.60);

  margin:0 auto 16px;
}

.friendLargeAvatar{
  width:105px;
  height:105px;

  margin:auto;

  border-radius:50%;

  display:flex;
  align-items:center;
  justify-content:center;

  background:linear-gradient(135deg, #7da8fa, #655ce5);

  color:white;

  font-size:43px;
  font-weight:bold;

  border:4px solid rgba(255,255,255,0.80);

  box-shadow:0 7px 25px rgba(30,50,120,0.30);
}

.friendName{
  text-align:center;

  font-size:25px;

  margin:11px 0 3px;
}

.friendStatus{
  text-align:center;

  color:var(--muted);

  margin-bottom:17px;
}

.callActions{
  display:flex;

  gap:10px;

  margin-bottom:12px;
}

.callButton{
  flex:1;

  min-height:70px;

  border:1px solid var(--glass-border);
  border-radius:18px;

  background:var(--glass-bg);

  color:var(--text);

  font-weight:bold;

  font-size:16px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.callButton .callIcon{
  display:block;

  font-size:28px;

  margin-bottom:3px;
}

.callButton.call{
  background:rgba(180,230,245,0.60);
  color:#1d8b9a;
}

.callButton.video{
  background:rgba(200,225,255,0.60);
  color:#3567cf;
}

.closeFriend{
  width:100%;

  height:48px;

  border:1px solid var(--glass-border);
  border-radius:15px;

  background:var(--glass-bg);

  color:var(--text);

  font-weight:bold;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

/* =====================================================
                     12. MUSIC
===================================================== */

.musicHeader{
  height:52px;

  display:flex;
  align-items:center;

  margin-bottom:8px;
}

.musicHeader h1{
  flex:1;

  margin:0;

  font-size:25px;
}

.searchMusic{
  width:44px;
  height:44px;

  border:1px solid var(--glass-border);
  border-radius:14px;

  background:var(--glass-bg);
  color:var(--text);

  font-size:20px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  box-shadow:var(--glass-shadow);
}

.musicSearchPanel{
  display:none;
  margin-bottom:10px;
}

.musicSearchPanel.show{
  display:block;
}

.sectionTitle{
  font-size:18px;
  font-weight:bold;

  margin:14px 3px 9px;
}

.song{
  display:flex;
  align-items:center;

  gap:11px;
}

.cover{
  width:65px;
  height:65px;

  flex-shrink:0;

  border-radius:17px;

  display:flex;
  align-items:center;
  justify-content:center;

  font-size:30px;

  background:rgba(255,255,255,0.45);

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.songInfo{
  flex:1;
  min-width:0;
}

.songInfo b,
.songInfo small{
  display:block;
}

.songInfo b{
  white-space:nowrap;

  overflow:hidden;

  text-overflow:ellipsis;
}

.songInfo small{
  color:var(--muted);

  margin-top:5px;
}

.roundButton{
  width:42px;
  height:42px;

  border:0;
  border-radius:50%;

  background:linear-gradient(135deg, #38B6E8, #5CC8F0);

  color:white;

  box-shadow:0 3px 12px rgba(56,182,232,0.35);
}

/* =====================================================
                 13. ARTIST / MEDIA
===================================================== */

.artistCard{
  display:flex;

  gap:12px;

  align-items:center;
}

.artistPhoto{
  width:72px;
  height:72px;

  border-radius:18px;

  display:flex;

  justify-content:center;
  align-items:center;

  background:rgba(255,255,255,0.45);

  font-size:35px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  border:1px solid var(--glass-border);
}

.artistInfo{
  flex:1;
}

.artistInfo b,
.artistInfo small{
  display:block;
}

.artistInfo small{
  color:var(--muted);
  margin-top:5px;
}

.videoBox{
  height:190px;

  border-radius:18px;

  background:rgba(15,45,60,0.70);

  color:white;

  display:flex;

  align-items:center;
  justify-content:center;

  font-size:60px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  border:1px solid rgba(255,255,255,0.30);
}

/* =========================
   14. MINI PLAYER
========================= */

.mini{
  position:absolute;
  z-index:40;
  left:9px;
  right:9px;
  bottom:82px;
  height:67px;
  display:none;
  flex-direction:column;
  background:var(--glass-bg);
  border-radius:18px;
  box-shadow:var(--glass-shadow);
  overflow:hidden;
  transition:height .3s cubic-bezier(0.4, 0, 0.2, 1),
             opacity .3s ease,
             transform .3s cubic-bezier(0.4, 0, 0.2, 1);
  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
  border:1px solid var(--glass-border);
  touch-action:none;
  user-select:none;
  -webkit-user-select:none;
}

.mini.open{
  height:calc(100vh - 105px);
}

.mini.closing{
  opacity:0;
  transform:translateY(100px);
  pointer-events:none;
}

.miniHandle{
  position:absolute;
  top:0;
  left:0;
  right:0;
  height:20px;
  z-index:5;
  cursor:grab;
  touch-action:none;
  display:flex;
  align-items:center;
  justify-content:center;
}

.miniHandle:active{
  cursor:grabbing;
}

.miniHandle span{
  display:block;
  width:42px;
  height:5px;
  border-radius:10px;
  background:rgba(255,255,255,0.70);
  opacity:1;
}

.miniCloseBtn{
  display:none;
}

.mini.open .miniCloseBtn{
  display:flex;
  position:absolute;
  z-index:6;
  top:12px;
  right:12px;
  width:34px;
  height:34px;
  align-items:center;
  justify-content:center;
  border:0;
  border-radius:50%;
  background:rgba(255,255,255,0.45);
  color:inherit;
  font-size:16px;
  cursor:pointer;
  backdrop-filter:blur(10px);
  -webkit-backdrop-filter:blur(10px);
  transition:background .2s ease;
}

.mini.open .miniCloseBtn:hover{
  background:rgba(255,255,255,0.65);
}

.miniMain{
  position:relative;
  min-height:67px;
  display:flex;
  align-items:center;
  gap:11px;
  padding:7px 12px;
  padding-top:20px;
  box-sizing:border-box;
  cursor:pointer;
  touch-action:none;
}

.mini.open .miniMain{
  min-height:auto;
  flex-direction:column;
  justify-content:flex-start;
  padding:42px 18px 10px;
  gap:10px;
}

.miniCover{
  width:52px;
  height:52px;
  flex:0 0 52px;
  border-radius:14px;
  display:flex;
  align-items:center;
  justify-content:center;
  overflow:hidden;
  font-size:30px;
  background:rgba(255,255,255,0.35);
  border:1px solid rgba(255,255,255,0.50);
  transition:all .3s cubic-bezier(0.4, 0, 0.2, 1);
}

.mini.open .miniCover{
  width:min(72vw,310px);
  height:min(72vw,310px);
  flex-basis:auto;
  border-radius:18px;
  font-size:70px;
  margin-top:5px;
  box-shadow:0 8px 25px rgba(50,130,160,0.25);
}

.miniInfo{
  min-width:0;
  flex:1;
  overflow:hidden;
}

.mini.open .miniInfo{
  width:100%;
  flex:none;
  text-align:left;
}

.miniInfo b,
.miniInfo small{
  display:block;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
}

.miniInfo b{
  font-size:14px;
}

.miniInfo small{
  margin-top:3px;
  font-size:12px;
  opacity:.65;
}

.miniControls{
  display:none;
}

.mini.open .miniControls{
  width:100%;
  display:flex;
  align-items:center;
  justify-content:center;
  gap:12px;
  margin-top:4px;
}

.miniIconBtn{
  width:44px;
  height:44px;
  border:0;
  border-radius:50%;
  background:transparent;
  color:inherit;
  display:flex;
  align-items:center;
  justify-content:center;
  cursor:pointer;
  padding:0;
  transition:background .2s ease;
}

.miniIconBtn svg{
  width:22px;
  height:22px;
  stroke:currentColor;
  fill:none;
  stroke-width:2;
  stroke-linecap:round;
  stroke-linejoin:round;
}

.miniIconBtn:hover{
  background:rgba(255,255,255,0.30);
}

.miniIconBtn.active{
  background:rgba(56,182,232,0.30);
  color:#38B6E8;
}

.miniPlay{
  width:50px;
  height:50px;
  flex:0 0 50px;
  border:0;
  border-radius:50%;
  background:linear-gradient(135deg, #38B6E8, #5CC8F0);
  color:white;
  display:flex;
  align-items:center;
  justify-content:center;
  cursor:pointer;
  padding:0;
  box-shadow:0 3px 12px rgba(56,182,232,0.40);
}

.miniPlay svg{
  width:23px;
  height:23px;
  stroke:currentColor;
  fill:none;
  stroke-width:2.4;
  stroke-linecap:round;
  stroke-linejoin:round;
}

.miniProgressWrap{
  display:none;
}

.mini.open .miniProgressWrap{
  width:100%;
  display:block;
  margin-top:4px;
}

.miniProgress{
  width:100%;
  height:4px;
  accent-color:#38B6E8;
  cursor:pointer;
}

.miniTime{
  display:flex;
  justify-content:space-between;
  margin-top:4px;
  font-size:10px;
  opacity:.70;
}

.miniActions{
  display:none;
}

.mini.open .miniActions{
  width:100%;
  display:flex;
  justify-content:space-around;
  align-items:center;
  margin-top:2px;
  padding:2px 0;
}

.miniAction{
  width:46px;
  height:42px;
  border:0;
  background:transparent;
  color:inherit;
  border-radius:12px;
  display:flex;
  align-items:center;
  justify-content:center;
  cursor:pointer;
}

.miniAction svg{
  width:21px;
  height:21px;
  stroke:currentColor;
  fill:none;
  stroke-width:2;
  stroke-linecap:round;
  stroke-linejoin:round;
}

.miniAction.active{
  background:rgba(56,182,232,0.30);
  color:#38B6E8;
}

.miniDownloads{
  display:none;
}

.mini.open .miniDownloads{
  display:block;
  width:100%;
  flex:1;
  min-height:0;
  overflow:hidden;
  border-top:1px solid rgba(255,255,255,0.40);
}

.miniDownloadsTitle{
  padding:12px 15px 8px;
  font-size:14px;
  font-weight:700;
}

.miniDownloadList{
  height:calc(100% - 42px);
  overflow-y:auto;
  padding:0 10px 15px;
}

.miniDownloadItem{
  width:100%;
  display:flex;
  align-items:center;
  gap:10px;
  padding:8px;
  margin-bottom:5px;
  border:0;
  border-radius:12px;
  background:transparent;
  color:inherit;
  text-align:left;
  cursor:pointer;
}

.miniDownloadItem:hover{
  background:rgba(255,255,255,0.25);
}

.miniDownloadItem.selected{
  background:rgba(56,182,232,0.25);
}

.miniDownloadCover{
  width:45px;
  height:45px;
  flex:0 0 45px;
  border-radius:10px;
  display:flex;
  align-items:center;
  justify-content:center;
  overflow:hidden;
  font-size:24px;
  background:rgba(255,255,255,0.35);
  border:1px solid rgba(255,255,255,0.50);
}

.miniDownloadInfo{
  min-width:0;
  flex:1;
}

.miniDownloadInfo b,
.miniDownloadInfo small{
  display:block;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
}

.miniDownloadInfo b{
  font-size:13px;
}

.miniDownloadInfo small{
  margin-top:3px;
  font-size:11px;
  opacity:.6;
}

.miniSelectMark{
  width:20px;
  height:20px;
  border:1.5px solid currentColor;
  border-radius:6px;
  display:flex;
  align-items:center;
  justify-content:center;
  opacity:.55;
}

.miniDownloadItem.selected .miniSelectMark{
  opacity:1;
}

.miniSelectMark svg{
  width:13px;
  height:13px;
  stroke:currentColor;
  fill:none;
  stroke-width:2.5;
}

.miniEmpty{
  padding:25px 15px;
  text-align:center;
  opacity:.55;
  font-size:13px;
}

.miniSelectPanel{
  display:none;
  position:absolute;
  inset:0;
  z-index:10;
  background:var(--glass-bg);
  overflow:hidden;
  flex-direction:column;
  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.mini.selecting .miniSelectPanel{
  display:flex;
}

.miniSelectHeader{
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:18px 15px 12px;
  border-bottom:1px solid rgba(255,255,255,0.40);
}

.miniSelectHeader b{
  font-size:16px;
}

.miniSelectClose{
  width:36px;
  height:36px;
  border:0;
  border-radius:50%;
  background:transparent;
  color:inherit;
  display:flex;
  align-items:center;
  justify-content:center;
}

.miniSelectList{
  flex:1;
  overflow-y:auto;
  padding:8px 10px;
}

/* =====================================================
                    15. FULL PLAYER
===================================================== */

.player{
  position:absolute;

  z-index:90;

  inset:0;

  display:none;

  background:rgba(50,130,160,0.35);

  backdrop-filter:blur(8px);
  -webkit-backdrop-filter:blur(8px);
}

.player.show{
  display:block;
}

.playerSheet{
  position:absolute;

  left:0;
  right:0;
  bottom:0;

  height:89%;

  padding:15px;

  background:linear-gradient(135deg, #DDF7FF, #C9F0FA);

  border-radius:28px 28px 0 0;

  transform:translateY(100%);

  transition:.3s;

  box-shadow:0 -8px 30px rgba(50,130,160,0.25);
}

body.dark .playerSheet{
  background:linear-gradient(135deg, #1A3E4D, #153544);
}

.player.show .playerSheet{
  transform:translateY(0);
}

.handle{
  width:45px;
  height:5px;

  border-radius:10px;

  background:rgba(255,255,255,0.60);

  margin:0 auto 13px;
}

.closePlayer{
  position:absolute;

  right:14px;
  top:11px;

  width:42px;
  height:42px;

  border:1px solid var(--glass-border);

  border-radius:13px;

  background:var(--glass-bg);

  color:var(--text);

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.bigCover{
  width:100%;
  height:285px;

  border-radius:24px;

  background:rgba(255,255,255,0.45);

  display:flex;

  align-items:center;
  justify-content:center;

  font-size:88px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  border:1px solid var(--glass-border);
}

.playerTitle{
  text-align:center;

  margin:14px 0 4px;
}

.playerArtist{
  text-align:center;

  color:var(--muted);
}

.actions{
  display:flex;

  gap:9px;

  margin-top:18px;
}

.actions button{
  flex:1;

  height:45px;

  border:1px solid var(--glass-border);

  border-radius:14px;

  background:var(--glass-bg);

  color:var(--text);

  font-size:18px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.controls{
  display:flex;

  justify-content:center;
  align-items:center;

  gap:20px;

  margin-top:20px;
}

.controls button{
  width:51px;
  height:51px;

  border:1px solid var(--glass-border);

  border-radius:50%;

  background:var(--glass-bg);

  color:var(--text);

  font-size:18px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.controls .play{
  width:64px;
  height:64px;

  background:linear-gradient(135deg, #38B6E8, #5CC8F0);

  color:white;

  border:0;

  box-shadow:0 4px 15px rgba(56,182,232,0.45);
}

/* =====================================================
                   16. SETTINGS
===================================================== */

.profile{
  text-align:center;
}

.profileAvatar{
  width:90px;
  height:90px;

  margin:auto;

  border-radius:50%;

  background:linear-gradient(135deg, #38B6E8, #5CC8F0);

  color:white;

  display:flex;

  align-items:center;
  justify-content:center;

  font-size:38px;

  border:3px solid rgba(255,255,255,0.80);

  box-shadow:0 5px 20px rgba(56,182,232,0.35);
}

.setting{
  display:flex;

  align-items:center;

  gap:10px;
}

.settingIcon{
  width:40px;

  text-align:center;

  font-size:22px;
}

.settingText{
  flex:1;
}

.settingText b,
.settingText small{
  display:block;
}

.settingText small{
  color:var(--muted);

  margin-top:4px;
}

.arrow{
  border:0;

  background:transparent;

  color:var(--text);

  font-size:21px;
}

/* =====================================================
                 17. OWNER / ADMIN
===================================================== */

.ownerBadge{
  border:1px solid rgba(228,189,85,0.70);

  background:linear-gradient(135deg, rgba(255,235,145,0.55), rgba(255,255,255,0.65));

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.ownerTitle{
  font-weight:bold;
  font-size:18px;
}

.ownerOnly{
  display:none;
}

.ownerOnly.show{
  display:block;
}

.adminGrid{
  display:grid;

  grid-template-columns:1fr 1fr;

  gap:9px;
}

.adminButton{
  min-height:75px;

  border:1px solid var(--glass-border);

  border-radius:17px;

  background:var(--glass-bg);

  color:var(--text);

  font-weight:bold;

  padding:10px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

/* =====================================================
                  18. BOTTOM NAV
===================================================== */

.bottomNav{
  position:absolute;

  z-index:45;

  left:9px;
  right:9px;
  bottom:8px;

  height:68px;

  display:none;

  background:var(--glass-bg);

  border-radius:22px;

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  border:1px solid var(--glass-border);

  box-shadow:var(--glass-shadow);
}

.nav{
  flex:1;

  border:0;

  background:transparent;

  color:var(--muted);

  font-size:11px;

  font-weight:bold;
}

.nav span{
  display:block;

  font-size:23px;

  margin-bottom:2px;
}

.nav.active{
  color:var(--primary);
}

.nav.active span{
  text-shadow:0 0 15px rgba(56,182,232,0.60);
}

/* =====================================================
                     19. MODAL
===================================================== */

.modal{
  position:absolute;

  z-index:120;

  inset:0;

  display:none;

  align-items:flex-end;

  background:rgba(50,130,160,0.30);

  backdrop-filter:blur(5px);
  -webkit-backdrop-filter:blur(5px);
}

.modal.show{
  display:flex;
}

.modalBox{
  width:100%;

  max-height:90%;

  overflow-y:auto;

  padding:20px;

  background:linear-gradient(135deg, #DDF7FF, #C9F0FA);

  border-radius:25px 25px 0 0;

  box-shadow:0 -8px 30px rgba(50,130,160,0.25);
}

body.dark .modalBox{
  background:linear-gradient(135deg, #1A3E4D, #153544);
}

.modalBox h2{
  margin-top:0;
}

/* =====================================================
                     20. TOAST
===================================================== */

.toast{
  position:absolute;

  z-index:200;

  left:50%;

  bottom:160px;

  transform:translateX(-50%);

  display:none;

  padding:10px 16px;

  border-radius:13px;

  background:rgba(15,45,60,0.80);

  color:white;

  white-space:nowrap;

  backdrop-filter:blur(12px);
  -webkit-backdrop-filter:blur(12px);

  border:1px solid rgba(255,255,255,0.30);
}

/* =====================================================
                     21. UPLOAD
===================================================== */

.uploadBox{
  border:2px dashed rgba(56,182,232,0.50);

  border-radius:18px;

  padding:18px;

  text-align:center;

  margin-bottom:10px;

  background:rgba(255,255,255,0.30);

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);
}

.uploadBox input{
  width:100%;
}

/* =====================================================
                     22. SWITCH
===================================================== */

.switch{
  position:relative;

  width:51px;
  height:29px;
}

.switch input{
  opacity:0;

  width:0;
  height:0;
}

.slider{
  position:absolute;

  inset:0;

  border-radius:30px;

  background:rgba(182,203,210,0.60);

  backdrop-filter:var(--glass-blur);
  -webkit-backdrop-filter:var(--glass-blur);

  border:1px solid rgba(255,255,255,0.50);
}

.slider:before{
  content:"";

  position:absolute;

  width:21px;
  height:21px;

  left:4px;
  top:4px;

  border-radius:50%;

  background:white;

  transition:.2s;
}

.switch input:checked + .slider{
  background:linear-gradient(135deg, #38B6E8, #5CC8F0);
}

.switch input:checked + .slider:before{
  transform:translateX(22px);
}

/* =====================================================
                   23. CALL SCREEN
===================================================== */

.callOverlay{
  position:absolute;

  z-index:180;

  inset:0;

  display:none;

  flex-direction:column;

  align-items:center;
  justify-content:center;

  background:linear-gradient(180deg, #0F2D3C, #08191e);

  color:white;

  text-align:center;

  backdrop-filter:blur(20px);
  -webkit-backdrop-filter:blur(20px);
}

.callOverlay.show{
  display:flex;
}

.callAvatar{
  width:120px;
  height:120px;

  border-radius:50%;

  display:flex;
  align-items:center;
  justify-content:center;

  background:linear-gradient(135deg, #7da8fa, #655ce5);

  border:4px solid rgba(255,255,255,0.80);

  font-size:48px;
  font-weight:bold;

  margin-bottom:18px;

  box-shadow:0 10px 35px rgba(56,182,232,0.40);
}

.callName{
  font-size:26px;
  font-weight:bold;
}

.callType{
  color:#b7c8ce;

  margin-top:6px;
}

.callButtons{
  display:flex;

  gap:18px;

  margin-top:45px;
}

.callControl{
  width:62px;
  height:62px;

  border:1px solid rgba(255,255,255,0.40);

  border-radius:50%;

  background:rgba(255,255,255,0.15);

  color:white;

  font-size:25px;

  backdrop-filter:blur(12px);
  -webkit-backdrop-filter:blur(12px);
}

.endCall{
  background:linear-gradient(135deg, #e4515e, #f06b78);

  border:0;

  box-shadow:0 4px 18px rgba(228,81,94,0.50);
}

/* =====================================================
                   24. RESPONSIVE
===================================================== */

@media(max-width:390px){

  .chatHeader{
    padding-left:9px;
    padding-right:9px;
  }

  .chatBack{
    width:49px;
    height:49px;
  }

  .chatProfile{
    width:53px;
    height:53px;
  }

  .chatHeaderName strong{
    font-size:19px;
  }

  .chatHeaderName small{
    font-size:12px;
  }

}

</style>
</head>

<body>

<div class="app">

<!-- =====================================================
                         01. HOME
===================================================== -->

<section id="home" class="screen active">

  <div class="topbar">

    <div class="googleSearchBar">

      <span class="searchIcon">🔍</span>

      <input id="newsSearch" class="googleSearchInput" placeholder="Search news..." autocomplete="off" oninput="renderNews(); updateNewsClearButton();">

      <button id="newsClearBtn" class="searchClearBtn hidden" type="button" onclick="clearNewsSearch()">✕</button>

    </div>

  </div>

  <div id="newsList"></div>

  <div id="article" class="article">

    <button class="icon articleBack" onclick="closeArticle()">←</button>

    <div id="articleImage" class="articleImage">📰</div>

    <h1 id="articleTitle"></h1>

    <div id="articleMeta" class="newsMeta"></div>

    <div id="articleContent" class="articleContent"></div>

  </div>

</section>


<!-- =====================================================
                         02. CHATS
===================================================== -->

<section id="chats" class="screen">

  <div class="topbar">
    <h1>✉️ Chats</h1>
  </div>

  <input id="chatSearch" class="input" placeholder="Search chats..." oninput="renderChats()">

  <div id="chatList"></div>

</section>


<!-- =====================================================
                    03. CHAT DETAIL
===================================================== -->

<section id="chatDetail" class="screen">

  <div class="chatWindow">

    <div class="chatHeader">

      <button class="chatBack" onclick="closeChatDetail()">‹</button>

      <div class="chatHeaderName" onclick="openFriendPanel()">
        <strong id="detailName">Chau Cheo</strong>
        <small id="detailStatus">last seen 28/08/26</small>
      </div>

      <button id="detailAvatar" class="chatProfile" onclick="openFriendPanel()">C</button>

    </div>

    <div id="messages" class="messages">
      <div class="chatDate">April 3</div>
      <div class="joined">Chau Cheo joined Chat</div>
    </div>

    <div class="chatInputBar">

      <div class="messageBarPill">

        <button class="msgIconBtn" onclick="showToast('📎 Attachment')">📎</button>

        <input id="messageInput" class="messageField" placeholder="Message" autocomplete="off">

        <button id="micButton" class="msgIconBtn" onclick="showToast('🎙️ Voice message')">🎙️</button>

        <button id="sendButton" class="sendButton" onclick="sendMessage()">➤</button>

      </div>

    </div>

  </div>

</section>


<!-- =====================================================
               04. FRIEND PROFILE / CALL PANEL
===================================================== -->

<div id="friendPanel" class="friendPanel">

  <div class="friendSheet">

    <div class="friendHandle"></div>

    <div id="friendLargeAvatar" class="friendLargeAvatar">C</div>

    <h2 id="friendName" class="friendName">Chau Cheo</h2>

    <div id="friendStatus" class="friendStatus">last seen 28/08/26</div>

    <div class="callActions">

      <button class="callButton call" onclick="startCall(false)">
        <span class="callIcon">📞</span>
        Call
      </button>

      <button class="callButton video" onclick="startCall(true)">
        <span class="callIcon">📹</span>
        Video Call
      </button>

    </div>

    <button class="closeFriend" onclick="closeFriendPanel()">Close</button>

  </div>

</div>


<!-- =====================================================
                         05. MUSIC
===================================================== -->

<section id="music" class="screen">

  <div class="musicHeader">
    <h1>💿 Music</h1>
    <button class="searchMusic" onclick="toggleMusicSearch()">🔍</button>
  </div>

  <div id="musicSearchPanel" class="musicSearchPanel">
    <input id="musicSearch" class="input" placeholder="Search music..." oninput="renderMusic()">
  </div>

  <div class="sectionTitle">🎤 Artists & New Songs</div>

  <div id="artistList"></div>

  <div class="sectionTitle">💿 Songs</div>

  <div id="musicList"></div>

  <div class="sectionTitle">⬇️ Downloads</div>

  <div id="downloadList"></div>

</section>


<!-- =====================================================
                         06. SETTINGS
===================================================== -->

<section id="settings" class="screen">

  <div class="topbar">
    <h1>⚙️ Settings</h1>
  </div>

  <div class="card profile">

    <div class="profileAvatar">👤</div>

    <h2 id="profileName">User</h2>

    <p id="profileEmail" class="muted"></p>

    <button class="primary" onclick="openProfile()">Edit Profile</button>

  </div>

  <div class="card setting" onclick="showToast('Notifications')">
    <div class="settingIcon">🔔</div>
    <div class="settingText">
      <b>Notifications</b>
      <small>Notification settings</small>
    </div>
    <button class="arrow">›</button>
  </div>

  <div class="card setting" onclick="toggleDarkMode()">
    <div class="settingIcon">🌙</div>
    <div class="settingText">
      <b>Dark Mode</b>
      <small>Light / Dark</small>
    </div>
    <button id="darkSwitch" class="arrow">›</button>
  </div>

  <div class="card setting" onclick="showToast('Privacy & Security')">
    <div class="settingIcon">🔒</div>
    <div class="settingText">
      <b>Privacy & Security</b>
      <small>Privacy settings</small>
    </div>
    <button class="arrow">›</button>
  </div>

  <div class="card setting" onclick="openFontSettings()">
    <div class="settingIcon">🔤</div>
    <div class="settingText">
      <b>Font</b>
      <small>Font & size</small>
    </div>
    <button class="arrow">›</button>
  </div>

  <div class="card setting" onclick="openLanguageSettings()">
    <div class="settingIcon">🌐</div>
    <div class="settingText">
      <b>Language</b>
      <small id="languageLabel">English</small>
    </div>
    <button class="arrow">›</button>
  </div>

  <div class="card setting" onclick="openStorageSettings()">
    <div class="settingIcon">📶</div>
    <div class="settingText">
      <b>Data & Storage</b>
      <small>Downloads & Storage</small>
    </div>
    <button class="arrow">›</button>
  </div>

  <div class="card setting" onclick="clearCache()">
    <div class="settingIcon">🗑️</div>
    <div class="settingText">
      <b>Clear Cache</b>
      <small>Clear temporary data</small>
    </div>
    <button class="arrow">›</button>
  </div>

  <div id="ownerArea" class="ownerOnly">

    <div class="card ownerBadge">
      <div class="ownerTitle">👑 Owner / Admin</div>
      <small>Owner only</small>
    </div>

    <div class="card setting" onclick="openAppCustomization()">
      <div class="settingIcon">🎨</div>
      <div class="settingText">
        <b>App Customization</b>
        <small>Logo, Name, Color, Size</small>
      </div>
      <button class="arrow">›</button>
    </div>

    <div class="card">
      <div class="sectionTitle">👑 Owner Control</div>
      <div class="adminGrid">
        <button class="adminButton" onclick="openAdmin('users')">👥<br>Users</button>
        <button class="adminButton" onclick="openAdmin('music')">💿<br>Music</button>
        <button class="adminButton" onclick="openAdmin('artists')">🎤<br>Artists</button>
        <button class="adminButton" onclick="openAdmin('news')">📰<br>News</button>
        <button class="adminButton" onclick="openAdmin('media')">🖼️<br>Media</button>
        <button class="adminButton" onclick="openAdmin('reports')">🚨<br>Reports</button>
        <button class="adminButton" onclick="openAdmin('statistics')">📊<br>Statistics</button>
        <button class="adminButton" onclick="openAdmin('age')">🎂<br>Age</button>
        <button class="adminButton" onclick="openAdmin('fonts')">🔤<br>Fonts</button>
        <button class="adminButton" onclick="openAdmin('notifications')">🔔<br>Notifications</button>
      </div>
    </div>

  </div>

  <div class="card setting" onclick="logout()">
    <div class="settingIcon">🚪</div>
    <div class="settingText">
      <b>Logout</b>
      <small>Sign out</small>
    </div>
    <button class="arrow">›</button>
  </div>

</section>


<!-- =====================================================
                      07. MINI PLAYER
===================================================== -->

<div id="mini" class="mini">

  <div id="miniHandle" class="miniHandle"><span></span></div>

  <button id="miniCloseBtn" class="miniCloseBtn" type="button" title="Close" onclick="closeMiniPlayer()">✕</button>

  <div class="miniMain" id="miniMain">

    <div id="miniCover" class="miniCover">🌆</div>

    <div class="miniInfo">
      <b id="miniTitle">Phành phố sương mờ</b>
      <small id="miniArtist">Young Quá, NhoxJet</small>
    </div>

    <div class="miniProgressWrap">
      <input id="miniProgress" class="miniProgress" type="range" min="0" max="100" value="0">
      <div class="miniTime">
        <span id="miniCurrentTime">0:00</span>
        <span id="miniDuration">0:00</span>
      </div>
    </div>

    <div class="miniControls">

      <button class="miniIconBtn" id="miniSelectBtn" title="Select songs" onclick="event.stopPropagation();toggleMiniSelect()">
        <svg viewBox="0 0 24 24"><path d="M8 6h13"/><path d="M8 12h13"/><path d="M8 18h13"/><path d="M3 6h.01"/><path d="M3 12h.01"/><path d="M3 18h.01"/></svg>
      </button>

      <button class="miniIconBtn" title="Previous" onclick="event.stopPropagation();miniPreviousSong()">
        <svg viewBox="0 0 24 24"><path d="M19 20L9 12l10-8v16z"/><path d="M5 19V5"/></svg>
      </button>

      <button id="miniPlay" class="miniPlay" title="Play / Pause" onclick="event.stopPropagation();togglePlay()">
        <svg id="miniPlayIcon" viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
      </button>

      <button class="miniIconBtn" title="Next" onclick="event.stopPropagation();miniNextSong()">
        <svg viewBox="0 0 24 24"><path d="M5 4l10 8-10 8V4z"/><path d="M19 5v14"/></svg>
      </button>

      <button id="miniRepeat" class="miniIconBtn" title="Repeat" onclick="event.stopPropagation();toggleMiniRepeat()">
        <svg viewBox="0 0 24 24"><path d="M17 2l4 4-4 4"/><path d="M3 11V9a3 3 0 0 1 3-3h15"/><path d="M7 22l-4-4 4-4"/><path d="M21 13v2a3 3 0 0 1-3 3H3"/></svg>
      </button>

    </div>

    <div class="miniActions">

      <button class="miniAction" title="Like" onclick="event.stopPropagation();toggleMiniAction(this)">
        <svg viewBox="0 0 24 24"><path d="M7 10v11H4a2 2 0 0 1-2-2v-7a2 2 0 0 1 2-2h3z"/><path d="M7 21h9.5a2 2 0 0 0 1.9-1.4l2.2-7A2 2 0 0 0 18.7 10H14l.7-4.2A3 3 0 0 0 11.8 2L7 10"/></svg>
      </button>

      <button class="miniAction" title="Dislike" onclick="event.stopPropagation();toggleMiniAction(this)">
        <svg viewBox="0 0 24 24"><path d="M7 14V3H4a2 2 0 0 0-2 2v7a2 2 0 0 0 2 2h3z"/><path d="M7 3h9.5a2 2 0 0 1 1.9 1.4l2.2 7A2 2 0 0 1 18.7 14H14l.7 4.2a3 3 0 0 1-2.9 3.8L7 14"/></svg>
      </button>

      <button class="miniAction" title="Comment" onclick="event.stopPropagation();miniComment()">
        <svg viewBox="0 0 24 24"><path d="M20 11.5a8 8 0 0 1-8 8H7l-4 3v-5.2a8 8 0 1 1 17-5.8z"/></svg>
      </button>

    </div>

  </div>

  <div id="miniSelectPanel" class="miniSelectPanel">
    <div class="miniSelectHeader">
      <b>Select songs</b>
      <button class="miniSelectClose" onclick="toggleMiniSelect()" title="Close">
        <svg viewBox="0 0 24 24" width="21" height="21"><path d="M6 6l12 12"/><path d="M18 6L6 18"/></svg>
      </button>
    </div>
    <div id="miniSelectList" class="miniSelectList"></div>
  </div>

  <div id="miniDownloads" class="miniDownloads">
    <div class="miniDownloadsTitle">Download</div>
    <div id="miniDownloadList" class="miniDownloadList"></div>
  </div>

</div>


<!-- =====================================================
                       08. FULL PLAYER
===================================================== -->

<div id="player" class="player">

  <div class="playerSheet">

    <div class="handle"></div>

    <button class="closePlayer" onclick="closePlayer()">✕</button>

    <div id="bigCover" class="bigCover">🌆</div>

    <h2 id="playerTitle" class="playerTitle">Phành phố sương mờ</h2>

    <div id="playerArtist" class="playerArtist">Young Quá, NhoxJet</div>

    <div class="actions">
      <button onclick="showToast('👎🏻 Dislike')">👎🏻</button>
      <button onclick="showToast('👍🏻 Like')">👍🏻</button>
      <button onclick="shareSong()">✉️</button>
    </div>

    <div class="controls">
      <button onclick="previousSong()">⏮</button>
      <button id="mainPlay" class="play" onclick="togglePlay()">▶️</button>
      <button onclick="nextSong()">⏭</button>
    </div>

  </div>

</div>


<!-- =====================================================
                    09. PROFILE MODAL
===================================================== -->

<div id="profileModal" class="modal">
  <div class="modalBox">
    <h2>👤 Profile</h2>
    <input id="editName" class="input" placeholder="Name">
    <input id="editEmail" class="input" placeholder="Gmail">
    <button class="primary" onclick="saveProfile()">Save</button>
    <button class="secondary" onclick="closeModal('profileModal')">Close</button>
  </div>
</div>


<!-- =====================================================
                       10. FONT MODAL
===================================================== -->

<div id="fontModal" class="modal">
  <div class="modalBox">
    <h2>🔤 Font</h2>
    <p class="muted">Select font</p>
    <select id="fontSelect" class="select" onchange="applyFont()">
      <option value="Arial">Arial</option>
      <option value="Georgia">Georgia</option>
      <option value="Verdana">Verdana</option>
      <option value="Tahoma">Tahoma</option>
      <option value="Times New Roman">Times New Roman</option>
      <option value="monospace">Monospace</option>
    </select>
    <label>Font size</label>
    <input id="fontSize" type="range" min="13" max="24" value="16" style="width:100%" oninput="applyFont()">
    <div class="uploadBox">
      <b>📁 Upload your font</b>
      <p class="muted">Select font file</p>
      <input type="file" accept=".ttf,.otf,.woff,.woff2" onchange="loadCustomFont(event)">
    </div>
    <button class="primary" onclick="saveFont(); closeModal('fontModal');">Save</button>
  </div>
</div>


<!-- =====================================================
                    11. LANGUAGE MODAL
===================================================== -->

<div id="languageModal" class="modal">
  <div class="modalBox">
    <h2>🌐 Language</h2>
    <button class="secondary" onclick="setLanguage('ខ្មែរ')">🇰🇭 ខ្មែរ</button>
    <button class="secondary" onclick="setLanguage('English')">🇺🇸 English</button>
    <button class="secondary" onclick="setLanguage('Tiếng Việt')">🇻🇳 Tiếng Việt</button>
    <button class="secondary" onclick="closeModal('languageModal')">Close</button>
  </div>
</div>


<!-- =====================================================
                    12. STORAGE MODAL
===================================================== -->

<div id="storageModal" class="modal">
  <div class="modalBox">
    <h2>📶 Data & Storage</h2>
    <div class="card">
      <b>Downloads</b>
      <p id="storageInfo" class="muted">0 songs</p>
    </div>
    <button class="primary" onclick="clearDownloads()">🗑️ Clear Downloads</button>
    <button class="secondary" onclick="closeModal('storageModal')">Close</button>
  </div>
</div>


<!-- =====================================================
                     13. ADMIN MODAL
===================================================== -->

<div id="adminModal" class="modal">
  <div class="modalBox">
    <h2 id="adminTitle">👑 Owner</h2>
    <div id="adminContent"></div>
    <button class="secondary" onclick="closeModal('adminModal')">Close</button>
  </div>
</div>


<!-- =====================================================
                     14. CALL OVERLAY
===================================================== -->

<div id="callOverlay" class="callOverlay">
  <div id="callAvatar" class="callAvatar">C</div>
  <div id="callName" class="callName">Chau Cheo</div>
  <div id="callType" class="callType">Calling...</div>
  <div class="callButtons">
    <button class="callControl" onclick="showToast('🔇 Microphone')">🎙️</button>
    <button class="callControl endCall" onclick="endCall()">📞</button>
    <button class="callControl" onclick="showToast('🔊 Speaker')">🔊</button>
  </div>
</div>


<!-- =====================================================
                    15. BOTTOM NAVIGATION
===================================================== -->

<nav id="bottomNav" class="bottomNav">
  <button class="nav active" data-page="home" onclick="go('home')">
    <span>🏠</span>
    Home
  </button>
  <button class="nav" data-page="chats" onclick="go('chats')">
    <span>✉️</span>
    Chats
  </button>
  <button class="nav" data-page="music" onclick="go('music')">
    <span>💿</span>
    Music
  </button>
  <button class="nav" data-page="settings" onclick="go('settings')">
    <span>⚙️</span>
    Settings
  </button>
</nav>


<!-- =====================================================
                         16. TOAST
===================================================== -->

<div id="toast" class="toast"></div>


<!-- =====================================================
                   17. SIGN UP MODAL
===================================================== -->

<div id="signupModal" class="modal show" style="align-items:center; background:rgba(50,130,160,0.50); backdrop-filter:blur(10px); -webkit-backdrop-filter:blur(10px);">

  <div class="modalBox" style="border-radius:25px; max-width:420px; margin:0 auto; background:linear-gradient(135deg, #DDF7FF, #C9F0FA);">

    <div class="brand">

      <img src="data:image/png;base64,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" class="brandIcon" alt="Chats Logo">

      <h1>𝑪𝒉𝒂𝒕𝒔</h1>

      <p class="muted">Create your account</p>

    </div>

    <div id="signupContent"></div>

  </div>

</div>

</div>


<script>

/* =====================================================
                     01. CONFIG
===================================================== */

const OWNER_EMAIL = "chauchung2007a@gmail.com";

let user = null;
let currentSong = 0;
let playing = false;
let minimumAge = 13;
let ageRestrictionEnabled = false;
let currentChat = null;
let currentLanguage = "English";


/* =====================================================
                       03. DATA
===================================================== */

const songs = [
  { title:"Phành phố sương mờ", artist:"Young Quá, NhoxJet", cover:"🌆" },
  { title:"Tránh Duyên", artist:"Đình Dũng", cover:"🎤" },
  { title:"Y Que Fue?", artist:"Don Miguelo", cover:"🎧" },
  { title:"Girl In My Dream", artist:"Louch Sokchea", cover:"💜" },
  { title:"New Song", artist:"New Artist", cover:"🎙️" }
];

const artists = [
  { name:"Young Quá", description:"Artist", photo:"🎤", video:"🎬" },
  { name:"NhoxJet", description:"Artist", photo:"🎧", video:"🎬" },
  { name:"Louch Sokchea", description:"New Artist", photo:"🎙️", video:"🎬" }
];

const news = [
  { title:"Daily News", source:"Chat News", time:"10 minutes ago", image:"📰", text:"This is a place to display daily news and articles you can read." },
  { title:"Technology News", source:"Technology", time:"30 minutes ago", image:"💻", text:"Read the latest technology news about mobile apps and innovations." },
  { title:"Music & Artist News", source:"Music News", time:"1 hour ago", image:"🎤", text:"Latest news about artists, new songs, and recently posted videos." },
  { title:"Sports News", source:"Sport", time:"2 hours ago", image:"⚽", text:"Latest sports news and results that are getting attention." }
];

const chats = [
  { name:"Chau Cheo", message:"Hello 👋", avatar:"C", status:"last seen 28/08/26" },
  { name:"BEEP", message:"New message", avatar:"B", status:"online" },
  { name:"Group krang chai", message:"3 messages", avatar:"G", status:"last seen recently" },
  { name:"Volunteer Support", message:"Choose an option", avatar:"V", status:"online" }
];


/* =====================================================
                    04. SIGN UP
===================================================== */

function renderSignup(){
  document.getElementById("signupContent").innerHTML = `
    <div class="signupField">
      <span class="signupFieldIcon">👤</span>
      <input id="signupName" class="input signupInput" placeholder="Name" autocomplete="off">
    </div>
    <div class="signupField">
      <span class="signupFieldIcon">🔒</span>
      <input id="signupPassword" class="input signupInput" type="password" placeholder="Password" autocomplete="off">
    </div>
    <button class="primary" onclick="finishSignup()">Enter Chat</button>
  `;
}


/* =====================================================
                  05. PASSWORD RULES
===================================================== */

const PASSWORD_SPECIAL_CHARS = /[\[\]\{\}#%\^\*\+=_\\|~<>$€£·\.,\?!'\-\/:;\(\)៛&@"]/;

function validatePassword(password){
  if(!password) return "Please enter Password";
  if(!/[A-Z]/.test(password)) return "Password must have at least 1 uppercase letter";
  if(!/[a-z]/.test(password)) return "Password must have at least 1 lowercase letter";
  if(!/[0-9]/.test(password)) return "Password must have at least 1 number";
  if(!PASSWORD_SPECIAL_CHARS.test(password)) return "Password must have at least 1 special character";
  return null;
}


/* =====================================================
                    06. FINISH SIGNUP
===================================================== */

function finishSignup(){
  const name = document.getElementById("signupName").value.trim();
  const password = document.getElementById("signupPassword").value;

  if(!name){
    showToast("Please enter name");
    return;
  }

  const passwordError = validatePassword(password);
  if(passwordError){
    showToast(passwordError);
    return;
  }

  user = { name:name, username:name, password:password };
  localStorage.setItem("chat_user", JSON.stringify(user));
  enterApp();
}


/* =====================================================
                     09. ENTER APP
===================================================== */

function enterApp(){
  const saved = localStorage.getItem("chat_user");
  if(saved){
    user = JSON.parse(saved);
  }

  document.querySelectorAll(".screen").forEach(screen=>{
    screen.classList.remove("active");
  });

  document.getElementById("home").classList.add("active");
  document.getElementById("bottomNav").style.display = "flex";

  const signupModal = document.getElementById("signupModal");
  if(signupModal){
    signupModal.classList.remove("show");
    signupModal.style.display = "none";
  }

  updateProfile();
  renderNews();
  renderChats();
  renderMusic();
  selectSong(0);

  document.getElementById("mini").style.display = "none";
  checkOwner();
}


/* =====================================================
                    10. NAVIGATION
===================================================== */

function go(page){
  if(page === "chatDetail") return;

  document.querySelectorAll(".screen").forEach(screen=>{
    screen.classList.remove("active");
  });

  document.getElementById(page).classList.add("active");

  document.querySelectorAll(".nav").forEach(nav=>{
    nav.classList.toggle("active", nav.dataset.page === page);
  });

  const mini = document.getElementById("mini");

  if(page === "music"){
    mini.style.display = "flex";
  }else{
    mini.style.display = "none";
    mini.classList.remove("open");
    closePlayer();
  }

  closeArticle();
}


/* =====================================================
                       11. HOME
===================================================== */

function clearNewsSearch(){
  const input = document.getElementById("newsSearch");
  if(!input) return;
  input.value = "";
  renderNews();
  updateNewsClearButton();
  input.focus();
}

function updateNewsClearButton(){
  const input = document.getElementById("newsSearch");
  const clearBtn = document.getElementById("newsClearBtn");
  if(!input || !clearBtn) return;
  clearBtn.classList.toggle("hidden", !input.value);
}

function renderNews(){
  const search = (document.getElementById("newsSearch")?.value || "").toLowerCase();
  const list = news.filter(item =>
    (item.title + item.source + item.text).toLowerCase().includes(search)
  );

  document.getElementById("newsList").innerHTML = `
    <div class="newsHeading">📰 Latest News</div>
    ${list.length ? list.map(item => {
      const index = news.indexOf(item);
      return `
        <article class="card newsCard" onclick="openArticle(${index})">
          <div class="newsImage">${item.image}</div>
          <div class="newsBody">
            <div class="newsTitle">${item.title}</div>
            <div class="newsMeta">${item.source} • ${item.time}</div>
            <div class="newsText">${item.text}</div>
          </div>
        </article>
      `;
    }).join("") : `<div class="card muted">No news available.</div>`}
  `;
}

function openArticle(index){
  const item = news[index];
  if(!item) return;

  document.getElementById("newsList").style.display = "none";
  document.getElementById("article").classList.add("show");
  document.getElementById("articleImage").textContent = item.image;
  document.getElementById("articleTitle").textContent = item.title;
  document.getElementById("articleMeta").textContent = item.source + " • " + item.time;
  document.getElementById("articleContent").textContent = item.text + " " + item.text + " " + item.text;
}

function closeArticle(){
  const article = document.getElementById("article");
  article.classList.remove("show");
  document.getElementById("newsList").style.display = "block";
}


/* =====================================================
                       12. CHATS
===================================================== */

function renderChats(){
  const search = (document.getElementById("chatSearch")?.value || "").toLowerCase();
  const list = chats.filter(item =>
    (item.name + item.message).toLowerCase().includes(search)
  );

  document.getElementById("chatList").innerHTML = list.map((item, index) => `
    <div class="card chat" onclick="openChatDetail(${index})">
      <div class="chatAvatar">${item.avatar}</div>
      <div class="chatInfo">
        <b>${item.name}</b>
        <small>${item.message}</small>
      </div>
    </div>
  `).join("");
}


/* =====================================================
                 13. OPEN CHAT DETAIL
===================================================== */

function openChatDetail(index){
  const chat = chats[index];
  if(!chat) return;

  currentChat = chat;

  document.getElementById("detailName").textContent = chat.name;
  document.getElementById("detailStatus").textContent = chat.status;
  document.getElementById("detailAvatar").textContent = chat.avatar;
  document.getElementById("friendLargeAvatar").textContent = chat.avatar;
  document.getElementById("friendName").textContent = chat.name;
  document.getElementById("friendStatus").textContent = chat.status;
  document.getElementById("callAvatar").textContent = chat.avatar;
  document.getElementById("callName").textContent = chat.name;

  document.querySelectorAll(".screen").forEach(screen=>{
    screen.classList.remove("active");
  });

  document.getElementById("chatDetail").classList.add("active");
  document.getElementById("bottomNav").style.display = "none";
  document.getElementById("mini").style.display = "none";

  closePlayer();
  closeFriendPanel();
  renderChatMessages();
}


/* =====================================================
                14. CLOSE CHAT DETAIL
===================================================== */

function closeChatDetail(){
  document.getElementById("chatDetail").classList.remove("active");
  document.getElementById("chats").classList.add("active");

  document.querySelectorAll(".nav").forEach(nav=>{
    nav.classList.toggle("active", nav.dataset.page === "chats");
  });

  document.getElementById("bottomNav").style.display = "flex";
  closeFriendPanel();
}


/* =====================================================
               15. CHAT MESSAGE STORAGE
===================================================== */

function renderChatMessages(){
  const messages = document.getElementById("messages");
  messages.innerHTML = `
    <div class="chatDate">April 3</div>
    <div class="joined">${currentChat?.name || "Chau Cheo"} joined Chat</div>
  `;

  const saved = JSON.parse(localStorage.getItem("chat_messages") || "{}");
  const key = currentChat?.name || "Chau Cheo";
  const list = saved[key] || [];

  list.forEach(message => {
    addMessageBubble(message.text, message.mine, false);
  });

  setTimeout(() => {
    messages.scrollTop = messages.scrollHeight;
  }, 50);
}

function addMessageBubble(text, mine = true, scroll = true){
  const messages = document.getElementById("messages");
  const row = document.createElement("div");
  row.className = "messageRow" + (mine ? " mine" : "");

  const bubble = document.createElement("div");
  bubble.className = "messageBubble";
  bubble.textContent = text;

  row.appendChild(bubble);
  messages.appendChild(row);

  if(scroll){
    messages.scrollTop = messages.scrollHeight;
  }
}

function sendMessage(){
  const input = document.getElementById("messageInput");
  const text = input.value.trim();
  if(!text) return;

  addMessageBubble(text, true, true);

  const saved = JSON.parse(localStorage.getItem("chat_messages") || "{}");
  const key = currentChat?.name || "Chau Cheo";

  if(!saved[key]){
    saved[key] = [];
  }

  saved[key].push({ text:text, mine:true });
  localStorage.setItem("chat_messages", JSON.stringify(saved));

  input.value = "";
  updateMessageButtons();
}

function updateMessageButtons(){
  const input = document.getElementById("messageInput");
  const mic = document.getElementById("micButton");
  const send = document.getElementById("sendButton");

  if(!input) return;

  if(input.value.trim()){
    mic.style.display = "none";
    send.style.display = "flex";
    send.style.alignItems = "center";
    send.style.justifyContent = "center";
  }else{
    mic.style.display = "flex";
    send.style.display = "none";
  }
}


/* =====================================================
              16. FRIEND PROFILE / CALL
===================================================== */

function openFriendPanel(){
  if(!currentChat) return;
  document.getElementById("friendPanel").classList.add("show");
}

function closeFriendPanel(){
  document.getElementById("friendPanel").classList.remove("show");
}

function startCall(video = false){
  if(!currentChat) return;

  document.getElementById("callAvatar").textContent = currentChat.avatar;
  document.getElementById("callName").textContent = currentChat.name;
  document.getElementById("callType").textContent = video ? "📹 Video Calling..." : "📞 Calling...";

  closeFriendPanel();
  document.getElementById("callOverlay").classList.add("show");
}

function endCall(){
  document.getElementById("callOverlay").classList.remove("show");
  showToast("Call ended");
}


/* =====================================================
                       17. MUSIC
===================================================== */

function toggleMusicSearch(){
  document.getElementById("musicSearchPanel").classList.toggle("show");
  if(document.getElementById("musicSearchPanel").classList.contains("show")){
    document.getElementById("musicSearch").focus();
  }
}

function renderMusic(){
  const search = (document.getElementById("musicSearch")?.value || "").toLowerCase();

  const filteredSongs = songs.filter(song =>
    (song.title + song.artist).toLowerCase().includes(search)
  );

  const filteredArtists = artists.filter(artist =>
    (artist.name + artist.description).toLowerCase().includes(search)
  );

  document.getElementById("artistList").innerHTML = filteredArtists.map(artist => `
    <div class="card artistCard">
      <div class="artistPhoto">${artist.photo}</div>
      <div class="artistInfo">
        <b>${artist.name}</b>
        <small>${artist.description}</small>
      </div>
      <button class="roundButton" onclick="showToast('Video of ${artist.name}')">▶</button>
    </div>
  `).join("");

  document.getElementById("musicList").innerHTML = filteredSongs.map(song => {
    const index = songs.indexOf(song);
    return `
      <div class="card song" onclick="selectSong(${index})">
        <div class="cover">${song.cover}</div>
        <div class="songInfo">
          <b>${song.title}</b>
          <small>${song.artist}</small>
        </div>
        <button class="roundButton" onclick="event.stopPropagation(); downloadSong(${index});">⬇️</button>
      </div>
    `;
  }).join("");

  renderDownloads();
}

function renderDownloads(){
  const saved = JSON.parse(localStorage.getItem("chat_downloads") || "[]");
  const list = saved.map(index => songs[index]).filter(Boolean);

  document.getElementById("downloadList").innerHTML = list.length ? list.map(song => {
    const index = songs.indexOf(song);
    return `
      <div class="card song" onclick="selectSong(${index})">
        <div class="cover">${song.cover}</div>
        <div class="songInfo">
          <b>${song.title}</b>
          <small>${song.artist}</small>
        </div>
        ▶️
      </div>
    `;
  }).join("") : `<div class="card muted">No downloads yet.</div>`;

  updateStorageInfo();
}


/* =====================================================
                    18. MUSIC PLAYER
===================================================== */

var miniRepeat = false;
var miniSelectedSongs = [];

function toggleMiniPlayer(){
  const mini = document.getElementById("mini");
  if(!mini) return;
  if(mini.classList.contains("selecting")) return;
  mini.classList.toggle("open");
}

function closeMiniPlayer(){
  const mini = document.getElementById("mini");
  if(!mini) return;
  mini.style.display = "none";
  mini.classList.remove("open");
}

function isMiniInteractiveTarget(target){
  return !!(target.closest("button") || target.closest("input"));
}

function attachMiniDrag(el){
  if(!el) return;

  let startY = null;
  let startHeight = null;
  let dragging = false;
  let moved = false;

  function getClosedHeight(){ return 67; }
  function getOpenHeight(){ return window.innerHeight - 105; }

  el.addEventListener("pointerdown", function(event){
    if(isMiniInteractiveTarget(event.target)) return;

    const mini = document.getElementById("mini");
    if(!mini || mini.classList.contains("selecting")) return;

    dragging = true;
    moved = false;
    startY = event.clientY;
    startHeight = mini.classList.contains("open") ? getOpenHeight() : getClosedHeight();
    mini.style.transition = "none";

    if(el.setPointerCapture){
      try{ el.setPointerCapture(event.pointerId); }catch(error){}
    }
  });

  el.addEventListener("pointermove", function(event){
    if(!dragging) return;

    const mini = document.getElementById("mini");
    if(!mini) return;

    const delta = startY - event.clientY;
    if(Math.abs(delta) > 4){ moved = true; }

    const closed = getClosedHeight();
    const open = getOpenHeight();
    let newHeight = startHeight + delta;

    if(newHeight < closed) newHeight = closed;
    if(newHeight > open) newHeight = open;

    mini.style.height = newHeight + "px";
    mini.classList.toggle("open", newHeight > closed + (open - closed) * 0.35);
  });

  function finishDrag(event){
    if(!dragging) return;
    dragging = false;

    const mini = document.getElementById("mini");
    if(!mini){
      startY = null;
      startHeight = null;
      return;
    }

    mini.style.transition = "";

    if(!moved){
      mini.classList.toggle("open");
    }else{
      const closed = getClosedHeight();
      const open = getOpenHeight();
      const currentHeight = parseFloat(mini.style.height) || closed;
      const shouldOpen = currentHeight > closed + (open - closed) * 0.35;
      mini.classList.toggle("open", shouldOpen);

      // បើអូសចុះក្រោមខ្លាំង បិទ Mini Player
      if(!shouldOpen && currentHeight <= closed + 20){
        mini.style.display = "none";
        mini.classList.remove("open");
      }
    }

    mini.style.height = "";

    if(el.releasePointerCapture && event && event.pointerId !== undefined){
      try{ el.releasePointerCapture(event.pointerId); }catch(error){}
    }

    startY = null;
    startHeight = null;
    moved = false;
  }

  el.addEventListener("pointerup", finishDrag);
  el.addEventListener("pointercancel", finishDrag);
}

function selectSong(index){
  const song = songs[index];
  if(!song) return;

  currentSong = index;

  document.getElementById("miniCover").textContent = song.cover;
  document.getElementById("miniTitle").textContent = song.title;
  document.getElementById("miniArtist").textContent = song.artist;
  document.getElementById("bigCover").textContent = song.cover;
  document.getElementById("playerTitle").textContent = song.title;
  document.getElementById("playerArtist").textContent = song.artist;

  renderMiniDownloads();
  updateMiniRepeatButton();
}

function toggleMiniSelect(){
  const mini = document.getElementById("mini");
  if(!mini) return;
  mini.classList.toggle("selecting");
  if(mini.classList.contains("selecting")){
    renderMiniSelectList();
  }
}

function renderMiniSelectList(){
  const list = document.getElementById("miniSelectList");
  if(!list) return;
  list.innerHTML = "";

  songs.forEach(function(song, index){
    const selected = miniSelectedSongs.includes(index);
    const item = document.createElement("button");
    item.type = "button";
    item.className = "miniDownloadItem" + (selected ? " selected" : "");
    item.innerHTML = `
      <div class="miniDownloadCover">${song.cover}</div>
      <div class="miniDownloadInfo">
        <b>${index + 1}. ${song.title}</b>
        <small>${song.artist}</small>
      </div>
      <div class="miniSelectMark">
        ${selected ? `<svg viewBox="0 0 24 24"><path d="M5 12l4 4L19 6"></path></svg>` : ""}
      </div>
    `;
    item.onclick = function(event){
      event.stopPropagation();
      toggleMiniSong(index);
    };
    list.appendChild(item);
  });
}

function toggleMiniSong(index){
  const position = miniSelectedSongs.indexOf(index);
  if(position === -1){
    miniSelectedSongs.push(index);
  }else{
    miniSelectedSongs.splice(position, 1);
  }
  renderMiniSelectList();
  renderMiniDownloads();
}

function miniPreviousSong(){
  const list = miniSelectedSongs.length ? miniSelectedSongs : songs.map(function(_, index){ return index; });
  if(!list.length) return;

  let position = list.indexOf(currentSong);
  if(position === -1){ position = 0; } else { position--; }
  if(position < 0){ position = list.length - 1; }

  selectSong(list[position]);
}

function miniNextSong(){
  const list = miniSelectedSongs.length ? miniSelectedSongs : songs.map(function(_, index){ return index; });
  if(!list.length) return;

  let position = list.indexOf(currentSong);
  if(position === -1){ position = 0; } else { position++; }
  if(position >= list.length){ position = 0; }

  selectSong(list[position]);
}

function previousSong(){ miniPreviousSong(); }
function nextSong(){ miniNextSong(); }

function togglePlay(){
  playing = !playing;
  updateMiniPlayIcon();
  updateMainPlay();
}

function updateMiniPlayIcon(){
  const icon = document.getElementById("miniPlayIcon");
  if(!icon) return;

  if(playing){
    icon.innerHTML = `<path d="M7 5v14"></path><path d="M17 5v14"></path>`;
  }else{
    icon.innerHTML = `<path d="M8 5v14l11-7z"></path>`;
  }
}

function updateMainPlay(){
  const button = document.getElementById("mainPlay");
  if(!button) return;
  button.textContent = playing ? "⏸️" : "▶️";
}

function toggleMiniRepeat(){
  miniRepeat = !miniRepeat;
  updateMiniRepeatButton();
}

function updateMiniRepeatButton(){
  const button = document.getElementById("miniRepeat");
  if(!button) return;
  button.classList.toggle("active", miniRepeat);
}

function toggleMiniAction(button){
  if(!button) return;
  button.classList.toggle("active");
}

function miniComment(){
  showToast("Comment");
}

function renderMiniDownloads(){
  const list = document.getElementById("miniDownloadList");
  if(!list) return;
  list.innerHTML = "";

  songs.forEach(function(song, index){
    const item = document.createElement("button");
    item.type = "button";
    item.className = "miniDownloadItem" + (miniSelectedSongs.includes(index) ? " selected" : "");
    item.innerHTML = `
      <div class="miniDownloadCover">${song.cover}</div>
      <div class="miniDownloadInfo">
        <b>${index + 1}. ${song.title}</b>
        <small>${song.artist}</small>
      </div>
      <div class="miniSelectMark">
        ${miniSelectedSongs.includes(index) ? `<svg viewBox="0 0 24 24"><path d="M5 12l4 4L19 6"></path></svg>` : ""}
      </div>
    `;
    item.onclick = function(event){
      event.stopPropagation();
      selectSong(index);
    };
    list.appendChild(item);
  });
}

function downloadSong(index){
  let saved = JSON.parse(localStorage.getItem("chat_downloads") || "[]");
  if(!saved.includes(index)){
    saved.push(index);
  }
  localStorage.setItem("chat_downloads", JSON.stringify(saved));
  renderDownloads();
  renderMiniDownloads();
  showToast("Downloaded ⬇️");
}

function shareSong(){
  const song = songs[currentSong];
  if(!song) return;

  if(navigator.share){
    navigator.share({
      title: song.title,
      text: song.title + " - " + song.artist
    }).catch(function(){});
  }else{
    showToast("Share");
  }
}

function openPlayer(){
  const music = document.getElementById("music");
  if(!music || !music.classList.contains("active")) return;

  const player = document.getElementById("player");
  if(player){
    player.classList.add("show");
  }
}

function closePlayer(){
  const player = document.getElementById("player");
  if(player){
    player.classList.remove("show");
  }
}


/* =====================================================
                       19. PROFILE
===================================================== */

function updateProfile(){
  document.getElementById("profileName").textContent = user?.name || "User";
  document.getElementById("profileEmail").textContent = user?.email || "";
}

function openProfile(){
  document.getElementById("editName").value = user?.name || "";
  document.getElementById("editEmail").value = user?.email || "";
  document.getElementById("profileModal").classList.add("show");
}

function saveProfile(){
  user.name = document.getElementById("editName").value.trim() || "User";
  user.email = document.getElementById("editEmail").value.trim();
  localStorage.setItem("chat_user", JSON.stringify(user));
  updateProfile();
  closeModal("profileModal");
  checkOwner();
  showToast("Profile saved");
}


/* =====================================================
                       20. FONT
===================================================== */

function openFontSettings(){
  document.getElementById("fontModal").classList.add("show");
}

function applyFont(){
  const font = document.getElementById("fontSelect").value;
  const size = document.getElementById("fontSize").value;
  document.body.style.fontFamily = font;
  document.body.style.fontSize = size + "px";
}

function saveFont(){
  localStorage.setItem("chat_font", document.getElementById("fontSelect").value);
  localStorage.setItem("chat_font_size", document.getElementById("fontSize").value);
  showToast("Font saved");
}

function loadCustomFont(event){
  const file = event.target.files[0];
  if(!file) return;

  const url = URL.createObjectURL(file);
  const fontName = "UserCustomFont";
  const face = new FontFace(fontName, `url(${url})`);

  face.load()
    .then(loaded => {
      document.fonts.add(loaded);
      document.body.style.fontFamily = fontName;
      showToast("Font uploaded");
    })
    .catch(() => {
      showToast("Cannot upload font");
    });
}


/* =====================================================
                     21. LANGUAGE
===================================================== */

function openLanguageSettings(){
  document.getElementById("languageModal").classList.add("show");
}

function setLanguage(language){
  currentLanguage = language;
  localStorage.setItem("chat_language", language);
  document.getElementById("languageLabel").textContent = language;
  closeModal("languageModal");
  showToast("Language: " + language);
  
  // នៅទីនេះអាចបន្ថែមការបកប្រែពេញ App បាន
  applyLanguage(language);
}

function applyLanguage(language){
  // ការបកប្រែអាចត្រូវបានបន្ថែមនៅទីនេះ
  // ឧទាហរណ៍: ផ្លាស់ប្តូរ text ទាំងអស់នៅក្នុង App
  if(language === "ខ្មែរ"){
    // បកប្រែទៅជាភាសាខ្មែរ
  } else if(language === "English"){
    // បកប្រែទៅជាភាសាអង់គ្លេស
  } else if(language === "Tiếng Việt"){
    // បកប្រែទៅជាភាសាវៀតណាម
  }
}


/* =====================================================
                    22. DARK MODE
===================================================== */

function toggleDarkMode(){
  document.body.classList.toggle("dark");
  localStorage.setItem("chat_dark", document.body.classList.contains("dark"));
}


/* =====================================================
                      23. STORAGE
===================================================== */

function openStorageSettings(){
  updateStorageInfo();
  document.getElementById("storageModal").classList.add("show");
}

function updateStorageInfo(){
  const saved = JSON.parse(localStorage.getItem("chat_downloads") || "[]");
  const el = document.getElementById("storageInfo");
  if(el){
    el.textContent = saved.length + " songs";
  }
}

function clearDownloads(){
  localStorage.removeItem("chat_downloads");
  renderDownloads();
  closeModal("storageModal");
  showToast("Downloads cleared");
}

function clearCache(){
  showToast("Cache cleared");
}


/* =====================================================
                   24. OWNER / ADMIN
===================================================== */

function checkOwner(){
  const area = document.getElementById("ownerArea");
  if(user && user.email && user.email.toLowerCase() === OWNER_EMAIL.toLowerCase()){
    area.classList.add("show");
  }else{
    area.classList.remove("show");
  }
}

function openAppCustomization(){
  if(!user || !user.email || user.email.toLowerCase() !== OWNER_EMAIL.toLowerCase()){
    showToast("Owner only");
    return;
  }
  showToast("🎨 App Customization");
}

function openAdmin(section){
  if(!user || user.email.toLowerCase() !== OWNER_EMAIL.toLowerCase()){
    showToast("Owner only");
    return;
  }

  const titles = {
    users:"👥 User Management",
    music:"🎵 Music Management",
    artists:"🎤 Artist Management",
    news:"📰 News Management",
    media:"🖼️ Image / Video Management",
    reports:"🚨 Reports",
    statistics:"📊 Statistics",
    age:"🎂 Age Restriction",
    fonts:"🔤 Font Management",
    notifications:"🔔 Notification Management"
  };

  document.getElementById("adminTitle").textContent = titles[section] || "👑 Owner";

  let content = "";

  if(section === "users"){
    content = `<div class="card"><b>👥 Users</b><p class="muted">Manage user accounts.</p></div><button class="primary" onclick="showToast('User Management')">Manage Users</button>`;
  }

  if(section === "music"){
    content = `<div class="card"><b>🎵 Music</b><p class="muted">Add, edit, or delete songs.</p></div><div class="uploadBox"><b>🎵 Upload song</b><input type="file" accept="audio/*"></div>`;
  }

  if(section === "artists"){
    content = `<div class="card"><b>🎤 Artist Management</b><p class="muted">Manage artist images and information.</p></div><div class="uploadBox">🖼️ Artist image<input type="file" accept="image/*"></div><div class="uploadBox">🎬 Artist video<input type="file" accept="video/*"></div>`;
  }

  if(section === "news"){
    content = `<input class="input" placeholder="News title"><textarea class="textarea" placeholder="Write news..."></textarea><button class="primary" onclick="showToast('News published')">📰 Publish News</button>`;
  }

  if(section === "media"){
    content = `<div class="uploadBox">🖼️ Upload Image<input type="file" accept="image/*"></div><div class="uploadBox">🎬 Upload Video<input type="file" accept="video/*"></div>`;
  }

  if(section === "reports"){
    content = `<div class="card">🚨 Reports<p class="muted">Owner can review reported content.</p></div>`;
  }

  if(section === "statistics"){
    content = `<div class="card">👥 Users<h2>0</h2></div><div class="card">🎵 Music<h2>${songs.length}</h2></div><div class="card">📰 News<h2>${news.length}</h2></div>`;
  }

  if(section === "age"){
    content = `<div class="card"><div style="display:flex;align-items:center;justify-content:space-between;"><b>🎂 Age Restriction</b><label class="switch"><input id="ageToggle" type="checkbox" ${ageRestrictionEnabled ? "checked" : ""} onchange="updateAgeSetting()"><span class="slider"></span></label></div></div><div class="card"><label>Minimum age</label><input id="minimumAge" class="input" type="number" min="1" max="100" value="${minimumAge}"><button class="primary" onclick="saveAgeSetting()">💾 Save</button></div>`;
  }

  if(section === "fonts"){
    content = `<div class="card"><b>🔤 Font Management</b><p class="muted">Owner can configure fonts.</p></div><div class="uploadBox">📁 Upload new font<input type="file" accept=".ttf,.otf,.woff,.woff2"></div>`;
  }

  if(section === "notifications"){
    content = `<textarea class="textarea" placeholder="Write notification..."></textarea><button class="primary" onclick="showToast('Notification sent')">🔔 Send Notification</button>`;
  }

  document.getElementById("adminContent").innerHTML = content;
  document.getElementById("adminModal").classList.add("show");
}


/* =====================================================
                    25. AGE SETTINGS
===================================================== */

function updateAgeSetting(){
  const checkbox = document.getElementById("ageToggle");
  if(checkbox){
    ageRestrictionEnabled = checkbox.checked;
  }
}

function saveAgeSetting(){
  const input = document.getElementById("minimumAge");
  const age = parseInt(input.value);

  if(!age || age < 1 || age > 100){
    showToast("Invalid age");
    return;
  }

  minimumAge = age;
  ageRestrictionEnabled = document.getElementById("ageToggle").checked;

  localStorage.setItem("chat_age_enabled", ageRestrictionEnabled);
  localStorage.setItem("chat_min_age", minimumAge);

  showToast("Age Restriction saved");
}


/* =====================================================
                      26. MODAL
===================================================== */

function closeModal(id){
  document.getElementById(id).classList.remove("show");
}


/* =====================================================
                      27. TOAST
===================================================== */

function showToast(message){
  const toast = document.getElementById("toast");
  toast.textContent = message;
  toast.style.display = "block";

  clearTimeout(window.toastTimer);
  window.toastTimer = setTimeout(() => {
    toast.style.display = "none";
  }, 1800);
}


/* =====================================================
                      28. LOGOUT
===================================================== */

function logout(){
  localStorage.removeItem("chat_user");
  location.reload();
}


/* =====================================================
                   29. LOAD SETTINGS
===================================================== */

function loadSettings(){
  const dark = localStorage.getItem("chat_dark") === "true";
  if(dark){
    document.body.classList.add("dark");
  }

  const font = localStorage.getItem("chat_font");
  const fontSize = localStorage.getItem("chat_font_size");

  if(font){
    document.body.style.fontFamily = font;
    const select = document.getElementById("fontSelect");
    if(select){ select.value = font; }
  }

  if(fontSize){
    document.body.style.fontSize = fontSize + "px";
    const range = document.getElementById("fontSize");
    if(range){ range.value = fontSize; }
  }

  const language = localStorage.getItem("chat_language");
  if(language){
    document.getElementById("languageLabel").textContent = language;
  }

  const savedAge = localStorage.getItem("chat_min_age");
  const savedAgeEnabled = localStorage.getItem("chat_age_enabled");

  if(savedAge){
    minimumAge = parseInt(savedAge);
  }

  if(savedAgeEnabled !== null){
    ageRestrictionEnabled = savedAgeEnabled === "true";
  }
}


/* =====================================================
                 30. EVENT LISTENERS
===================================================== */

document.addEventListener("DOMContentLoaded", () => {
  const input = document.getElementById("messageInput");

  if(input){
    input.addEventListener("input", updateMessageButtons);
    input.addEventListener("keydown", event => {
      if(event.key === "Enter" && !event.shiftKey){
        event.preventDefault();
        sendMessage();
      }
    });
  }

  const panel = document.getElementById("friendPanel");
  panel.addEventListener("click", event => {
    if(event.target === panel){
      closeFriendPanel();
    }
  });

  attachMiniDrag(document.getElementById("miniHandle"));
  attachMiniDrag(document.getElementById("miniMain"));
});


/* =====================================================
                         31. START
===================================================== */

loadSettings();
renderSignup();

if(localStorage.getItem("chat_user")){
  enterApp();
}

</script>

</body>
</html>
