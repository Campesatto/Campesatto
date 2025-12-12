<?xml version="1.0" encoding="UTF-8"?>
<svg xmlns="http://www.w3.org/2000/svg" width="720" height="220" viewBox="0 0 720 220" role="img" aria-label="Animated robot">
  <style>
    /* layout */
    .bg { fill: #0f1724; }
    .card { fill: #071126; rx: 12; }
    .accent { fill: #06b6d4; }
    .metal { fill: #cbd5e1; }
    .dark { fill: #94a3b8; }
    .eye { fill: #071126; }
    .screen { fill: #021827; }

    /* robot motion */
    .robot { transform-origin: center; animation: float 4s ease-in-out infinite; }
    @keyframes float {
      0% { transform: translateY(0px) }
      50% { transform: translateY(-6px) }
      100% { transform: translateY(0px) }
    }

    /* arm wave */
    .arm-right { transform-origin: 520px 110px; animation: wave 1.6s ease-in-out infinite; }
    @keyframes wave {
      0% { transform: rotate(0deg) }
      20% { transform: rotate(-24deg) }
      40% { transform: rotate(8deg) }
      60% { transform: rotate(-18deg) }
      100% { transform: rotate(0deg) }
    }

    /* eye blink */
    .eye-lid { animation: blink 4.2s step-end infinite; transform-origin: center; }
    @keyframes blink {
      0%, 92% { transform: scaleY(0); opacity: 0 }
      94% { transform: scaleY(1); opacity: 1 }
      100% { transform: scaleY(0); opacity: 0 }
    }

    /* pupil shimmer */
    .pupil { animation: look 6s ease-in-out infinite; }
    @keyframes look {
      0% { transform: translateX(0) }
      50% { transform: translateX(2px) }
      100% { transform: translateX(0) }
    }

    /* subtle slide in from left on load */
    .slide-in { transform: translateX(-16px); animation: slide 0.9s cubic-bezier(.2,.9,.3,1) forwards; opacity: 0; }
    @keyframes slide {
      to { transform: translateX(0); opacity: 1; }
    }

    /* text style */
    .name { fill: #e6f6f9; font-family: Inter, Roboto, Arial, sans-serif; font-weight:700; font-size:16px; }
    .title { fill: #9fb7bf; font-family: Inter, Roboto, Arial, sans-serif; font-size:12px; }
  </style>

  <!-- background card -->
  <rect class="bg" x="0" y="0" width="720" height="220" rx="0" />
  <g class="slide-in">
    <rect class="card" x="16" y="16" width="688" height="188" rx="10" />
    <!-- left info -->
    <g transform="translate(36,36)">
      <text class="name">Vitor Henrique Campesatto Lopes</text>
      <text class="title" y="22">QA Automation • Cypress • JavaScript • API Testing</text>
      <text class="title" y="42">Orlando, FL • vitoorcamp@hotmail.com • github.com/Campesatto</text>
    </g>

    <!-- robot group -->
    <g class="robot" transform="translate(420,54)">
      <!-- shadow -->
      <ellipse cx="160" cy="110" rx="64" ry="12" fill="#031020" opacity="0.28"/>

      <!-- body -->
      <g transform="translate(96,24)">
        <rect x="40" y="24" width="160" height="120" rx="14" class="metal" />
        <rect x="56" y="40" width="128" height="88" rx="8" class="screen" />

        <!-- chest accent -->
        <rect x="64" y="46" width="30" height="12" rx="3" class="accent" />
        <rect x="102" y="46" width="46" height="12" rx="3" class="dark" />

        <!-- eyes -->
        <g transform="translate(84,72)">
          <circle cx="0" cy="0" r="10" class="eye" />
          <circle cx="0" cy="0" r="4" class="pupil" />
          <rect x="-10" y="-10" width="20" height="20" rx="10" fill="none" />
          <!-- left lid -->
          <rect class="eye-lid" x="-10" y="-12" width="20" height="12" rx="6" fill="#071126"/>
        </g>
        <g transform="translate(148,72)">
          <circle cx="0" cy="0" r="10" class="eye" />
          <circle cx="0" cy="0" r="4" class="pupil" />
          <!-- right lid -->
          <rect class="eye-lid" x="-10" y="-12" width="20" height="12" rx="6" fill="#071126"/>
        </g>

        <!-- mouth -->
        <rect x="104" y="96" width="24" height="6" rx="3" class="dark" />

        <!-- left arm (static) -->
        <g transform="translate(-18,56)">
          <rect x="0" y="0" width="20" height="12" rx="4" class="metal" />
          <rect x="-8" y="10" width="8" height="34" rx="4" class="metal" />
          <circle cx="-4" cy="42" r="6" class="accent" />
        </g>

        <!-- right arm (waving) -->
        <g class="arm-right" transform="translate(198,40)">
          <rect x="-8" y="0" width="20" height="12" rx="4" class="metal" />
          <rect x="-8" y="10" width="8" height="34" rx="4" class="metal" />
          <circle cx="-4" cy="44" r="6" class="accent" />
        </g>

        <!-- antenna -->
        <g transform="translate(120,6)">
          <rect x="-2" y="0" width="4" height="10" rx="2" class="dark" />
          <circle cx="0" cy="-4" r="6" class="accent" />
        </g>
      </g>

      <!-- laptop -->
      <g transform="translate(-6,140)">
        <rect x="0" y="0" width="232" height="12" rx="3" class="dark"/>
        <rect x="6" y="-18" width="220" height="14" rx="3" class="metal"/>
        <rect x="14" y="-16" width="204" height="10" rx="2" class="screen"/>
        <!-- small screen content: lines -->
        <g transform="translate(22,-12)">
          <rect x="0" y="0" width="120" height="2" rx="1" fill="#98d8df" opacity="0.9"/>
          <rect x="0" y="6" width="80" height="2" rx="1" fill="#7fc6cc" opacity="0.8"/>
          <rect x="0" y="12" width="140" height="2" rx="1" fill="#6eb6bd" opacity="0.7"/>
        </g>
      </g>

    </g> <!-- end robot -->

    <!-- footer badges -->
    <g transform="translate(36,160)">
      <rect x="0" y="0" rx="6" width="120" height="28" fill="#062b33" />
      <text x="12" y="18" class="title">Cypress • JavaScript</text>
      <rect x="136" y="0" rx="6" width="140" height="28" fill="#051e2b" />
      <text x="152" y="18" class="title">API Testing • Postman</text>
      <rect x="288" y="0" rx="6" width="120" height="28" fill="#04202a" />
      <text x="304" y="18" class="title">Azure DevOps</text>
    </g>
  </g>
</svg>

# *Vitor Campesatto*
### *Software QA*


<br>

### *Sobre Mim*

<p align="left" margin-left="10px"> 
 
Graduated in IT Management, I currently work as Software QA

Passionate about the world of QAs and technology.

Hard Skills

- Web/Mobile Test Automation with NTX
- Web Test Automation with Cypress/JS
- Postman/Endpoints
- Azure DevOps
- Jmeter
- SQL for queries
- Jira
- Agile methodology
- Trello

 
  
  
 

<br>



### *Contato*

- Perfil : www.linkedin.com/in/vitor-campesatto-9bb6b1193
- Email : vitoorcamp@hotmail.com

