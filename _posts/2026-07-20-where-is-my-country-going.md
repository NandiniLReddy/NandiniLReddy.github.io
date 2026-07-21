---
layout: default
title: "Where Is My Country Going"
date: 2026-07-20
author: Nandini Lokesh Reddy
---

<div style="display:flex;align-items:center;gap:12px;background:#1a1a1a;border:1px solid #333;border-radius:6px;padding:10px 14px;margin-bottom:2rem;">
  <img src="https://img.youtube.com/vi/V6PVZP7zLkU/mqdefault.jpg" style="width:44px;height:44px;object-fit:cover;border-radius:3px;flex-shrink:0;">
  <div style="flex-shrink:0;min-width:130px;">
    <div style="font-size:0.8rem;color:#ddd;font-style:italic;">read it with this song</div>
    <div style="font-size:0.72rem;color:#888;margin-top:2px;">hum honge kamyab, instrumental</div>
  </div>
  <button id="play-btn" onclick="togglePlay()" style="background:none;border:none;color:#ddd;cursor:pointer;font-size:1.1rem;flex-shrink:0;padding:0 4px;">▶</button>
  <span id="cur-time" style="font-size:0.75rem;color:#888;flex-shrink:0;">0:00</span>
  <div id="prog-bar" onclick="seekTo(event)" style="flex:1;height:3px;background:#444;border-radius:2px;cursor:pointer;position:relative;">
    <div id="prog-fill" style="height:100%;width:0%;background:#ccc;border-radius:2px;position:relative;">
      <div style="width:10px;height:10px;background:#fff;border-radius:50%;position:absolute;right:-5px;top:-3.5px;"></div>
    </div>
  </div>
  <span id="rem-time" style="font-size:0.75rem;color:#888;flex-shrink:0;">-0:00</span>
</div>
<div id="yt-player" style="position:absolute;left:-9999px;width:1px;height:1px;"></div>

<script>
var tag = document.createElement('script');
tag.src = "https://www.youtube.com/iframe_api";
document.head.appendChild(tag);
var player, playing = false, ticker;
function onYouTubeIframeAPIReady() {
  player = new YT.Player('yt-player', {
    height:'1', width:'1', videoId:'V6PVZP7zLkU',
    playerVars:{autoplay:0, playsinline:1},
    events:{onStateChange:function(e){
      if(e.data===0){playing=false;document.getElementById('play-btn').innerHTML='▶';clearInterval(ticker);}
    }}
  });
}
function togglePlay() {
  if (!player) return;
  if (playing) { player.pauseVideo(); document.getElementById('play-btn').innerHTML='▶'; clearInterval(ticker); }
  else { player.playVideo(); document.getElementById('play-btn').innerHTML='⏸'; ticker=setInterval(tick,500); }
  playing=!playing;
}
function tick() {
  if(!player.getDuration) return;
  var c=player.getCurrentTime(), d=player.getDuration();
  document.getElementById('cur-time').textContent=fmt(c);
  document.getElementById('rem-time').textContent='-'+fmt(d-c);
  document.getElementById('prog-fill').style.width=(c/d*100)+'%';
}
function seekTo(e) {
  if(!player.getDuration) return;
  var r=e.currentTarget.getBoundingClientRect();
  player.seekTo(((e.clientX-r.left)/r.width)*player.getDuration(),true);
}
function fmt(s){s=Math.floor(s);return Math.floor(s/60)+':'+(('0'+s%60).slice(-2));}
</script>

India. My beautiful India. A country that has lived through its values, its *tathvas*, for thousands of years. And today, I watched it do something I never thought I'd have to witness.

Why do we call a country democratic? Why do we call it a people's country? Isn't it because a government is elected *by* the people, to protect them, to listen to their problems, to solve them? So tell me, what did we do today?

They are kids. Fucking kids. Sixteen, seventeen, eighteen years old. Fighting for their educational rights, for their future. I have never in my life seen a protest this peaceful. And the audacity it takes, to give an order to beat our own children. To throw tear gas at them. At *kids*. At our own kids.

There are parents in this country who have already lost their children to suicide over this exam. Over the pressure of it, the unfairness of it. And knowing that knowing exactly what a student gives up, how much stress and time and hope goes into clearing something like NEET  how does anyone in a position of power raise a hand against them?

And instead of sitting with these students, instead of asking them what's wrong, the response was to question their nationality. Their religion. Whether some opposition party had "put them up to it." Where was this scrutiny when the exam paper was leaked? Where was it when the results came back inconsistent, contradictory, impossible to trust? If the government had solved this the first time, would any opposition have had a chance to stand beside these students at all?

And yes I know papers leaked under the last government too. That is exactly *why* they were voted out. So don't sit there and act like history started the day you took power.

Two months. Two months since this began, and there has been no sitting down, no listening, no accountability. Nothing. Just silence, and then force. Police. Army personnel. Sent in against a protest that hurt no one.

If this is what happens when we speak, where is my freedom of speech? Where is my basic human right to ask a question of the people I elected?

And now you question *my* nationality. *My* religion. Let me be clear: I am more Hindu than you will ever measure, and my blood is more Indian than you will ever get to question. Patriotism is not obedience. Faith is not silence.

Students are this country's future, and you are letting them bleed on the streets. Why does any government deserve to hold power while it destroys its own future like that?

We already don't have the economy to raise kids. Not the nutrition, not the food to give them. Not land with values left in it. Not a peaceful world for them to grow up in. And now you want to take their education and their future rights too? Then why the hell should the next generation even have kids? Just to bring them into a world to die without a future?

How is it that this barely made the news? How is it that the second an opposition member stood up in parliament to ask about it, the session got adjourned in one minute? Kids are dying. Kids are injured. Where the hell is my country going?

This was never about religion. Never about nationality. Never about my integrity toward my nation, my nation *is* these students. Question the corrupt ones who let this happen. Question the silence, the adjournment, the absence of press, the absence of accountability. Do your fucking job. Not to us, for us.

---

I don't know where this goes from here. I don't know if the ones responsible will ever answer for it. But I know this: a country is not its government. A country is the sixteen-year-old standing in the street, tear gas in her eyes, still asking to be heard. That is India. That is what I will keep believing in, even on a day like today.
