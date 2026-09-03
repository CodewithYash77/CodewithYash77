<svg width="1200" height="420" viewBox="0 0 1200 420" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#050914"/>
      <stop offset="55%" stop-color="#0a1628"/>
      <stop offset="100%" stop-color="#050810"/>
    </linearGradient>
    <linearGradient id="deskGlow" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0%" stop-color="#00e5ff" stop-opacity="0.35"/>
      <stop offset="100%" stop-color="#00e5ff" stop-opacity="0"/>
    </linearGradient>
    <radialGradient id="hubGlow" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#00e5ff" stop-opacity="0.55"/>
      <stop offset="100%" stop-color="#00e5ff" stop-opacity="0"/>
    </radialGradient>
    <filter id="softGlow" x="-60%" y="-60%" width="220%" height="220%">
      <feGaussianBlur stdDeviation="4.2" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
    <filter id="bigGlow" x="-100%" y="-100%" width="300%" height="300%">
      <feGaussianBlur stdDeviation="10" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>

  <!-- background -->
  <rect x="0" y="0" width="1200" height="420" fill="url(#bg)"/>

  <!-- faint pipeline grid -->
  <g stroke="#0f3550" stroke-width="1" opacity="0.55">
    <line x1="0" y1="60" x2="1200" y2="60"/>
    <line x1="0" y1="140" x2="1200" y2="140"/>
    <line x1="0" y1="300" x2="1200" y2="300"/>
    <line x1="0" y1="380" x2="1200" y2="380"/>
    <line x1="150" y1="0" x2="150" y2="420"/>
    <line x1="450" y1="0" x2="450" y2="420"/>
    <line x1="750" y1="0" x2="750" y2="420"/>
    <line x1="1050" y1="0" x2="1050" y2="420"/>
  </g>

  <!-- central hub glow behind the engineer -->
  <ellipse cx="600" cy="230" rx="330" ry="190" fill="url(#hubGlow)"/>

  <!-- glowing pipeline connectors -->
  <g fill="none" stroke="#00e5ff" stroke-width="1.4" opacity="0.55" filter="url(#softGlow)">
    <path d="M170,90 C320,110 420,150 520,190"/>
    <path d="M1030,90 C880,110 780,150 690,190"/>
    <path d="M150,230 C260,230 340,225 470,222"/>
    <path d="M1050,230 C940,230 860,225 730,222"/>
    <path d="M190,340 C320,300 420,270 520,240"/>
    <path d="M1010,340 C880,300 780,270 690,240"/>
    <path d="M600,60 C600,110 600,140 600,185"/>
  </g>
  <!-- pulse dots along pipelines -->
  <g fill="#7cf3ff">
    <circle cx="340" cy="118" r="3"/>
    <circle cx="860" cy="118" r="3"/>
    <circle cx="300" cy="228" r="3"/>
    <circle cx="900" cy="228" r="3"/>
    <circle cx="360" cy="290" r="3"/>
    <circle cx="840" cy="290" r="3"/>
    <circle cx="600" cy="120" r="3"/>
  </g>

  <!-- command desk -->
  <rect x="440" y="330" width="320" height="14" rx="4" fill="#0c1b2b" stroke="#123047" stroke-width="1"/>
  <rect x="460" y="344" width="14" height="46" fill="#0c1b2b"/>
  <rect x="726" y="344" width="14" height="46" fill="#0c1b2b"/>
  <rect x="470" y="230" width="260" height="100" fill="url(#deskGlow)"/>

  <!-- dual monitors -->
  <g filter="url(#softGlow)">
    <rect x="470" y="205" width="150" height="100" rx="6" fill="#061420" stroke="#1c4a63" stroke-width="1.5"/>
    <rect x="580" y="200" width="150" height="105" rx="6" fill="#061420" stroke="#1c4a63" stroke-width="1.5"/>
  </g>
  <!-- monitor 1: terminal lines -->
  <g stroke="#25e0c0" stroke-width="2" stroke-linecap="round" opacity="0.9">
    <line x1="482" y1="222" x2="560" y2="222"/>
    <line x1="482" y1="236" x2="540" y2="236"/>
    <line x1="482" y1="250" x2="600" y2="250"/>
    <line x1="482" y1="264" x2="520" y2="264"/>
    <line x1="482" y1="278" x2="580" y2="278"/>
  </g>
  <!-- monitor 2: cluster nodes -->
  <g>
    <circle cx="610" cy="230" r="10" fill="none" stroke="#00e5ff" stroke-width="1.5"/>
    <circle cx="650" cy="250" r="10" fill="none" stroke="#00e5ff" stroke-width="1.5"/>
    <circle cx="690" cy="228" r="10" fill="none" stroke="#00e5ff" stroke-width="1.5"/>
    <path d="M618,235 L642,247 M660,248 L682,232" stroke="#00e5ff" stroke-width="1.2" fill="none"/>
    <line x1="600" y1="285" x2="710" y2="285" stroke="#25e0c0" stroke-width="2" stroke-linecap="round"/>
    <line x1="600" y1="272" x2="670" y2="272" stroke="#25e0c0" stroke-width="2" stroke-linecap="round" opacity="0.7"/>
  </g>

  <!-- engineer silhouette -->
  <g fill="#0a0f18" stroke="#0d2436" stroke-width="1">
    <rect x="565" y="330" width="70" height="10" rx="4" fill="#0c1b2b"/>
    <rect x="575" y="300" width="50" height="34" rx="10" fill="#0c1b2b"/>
    <path d="M572,300 C572,255 628,255 628,300 L628,330 L572,330 Z" fill="#0b1220"/>
    <circle cx="600" cy="238" r="24" fill="#12233a"/>
    <path d="M578,290 C585,275 615,275 622,290 L618,312 L582,312 Z" fill="#0b1220"/>
  </g>
  <path d="M576,238 A24,24 0 0 1 600,214" fill="none" stroke="#00e5ff" stroke-width="1.5" opacity="0.6" filter="url(#softGlow)"/>
  <path d="M572,300 C572,255 600,254 600,254" fill="none" stroke="#00e5ff" stroke-width="1.2" opacity="0.4" filter="url(#softGlow)"/>
  <rect x="560" y="325" width="80" height="6" rx="3" fill="#00e5ff" opacity="0.5" filter="url(#softGlow)"/>

  <!-- floating neon tech nodes -->
  <g filter="url(#bigGlow)"><circle cx="150" cy="70" r="34" fill="#0a1a2c" stroke="#f2a33c" stroke-width="1.6"/></g>
  <text x="150" y="76" text-anchor="middle" font-family="Verdana, Arial, sans-serif" font-size="13" font-weight="bold" fill="#ffcf8f">AWS</text>

  <g filter="url(#bigGlow)"><circle cx="1050" cy="70" r="34" fill="#0a1a2c" stroke="#3fd1ff" stroke-width="1.6"/></g>
  <text x="1050" y="76" text-anchor="middle" font-family="Verdana, Arial, sans-serif" font-size="12" font-weight="bold" fill="#aeeaff">Docker</text>

  <g filter="url(#bigGlow)"><circle cx="130" cy="230" r="34" fill="#0a1a2c" stroke="#4f7bff" stroke-width="1.6"/></g>
  <text x="130" y="234" text-anchor="middle" font-family="Verdana, Arial, sans-serif" font-size="10.5" font-weight="bold" fill="#c1cfff">K8s</text>

  <g filter="url(#bigGlow)"><circle cx="1070" cy="230" r="34" fill="#0a1a2c" stroke="#a855f7" stroke-width="1.6"/></g>
  <text x="1070" y="234" text-anchor="middle" font-family="Verdana, Arial, sans-serif" font-size="10" font-weight="bold" fill="#e3c9ff">Terraform</text>

  <g filter="url(#bigGlow)"><circle cx="170" cy="360" r="34" fill="#0a1a2c" stroke="#ff4b4b" stroke-width="1.6"/></g>
  <text x="170" y="365" text-anchor="middle" font-family="Verdana, Arial, sans-serif" font-size="10.5" font-weight="bold" fill="#ffc2c2">Ansible</text>

  <g filter="url(#bigGlow)"><circle cx="1030" cy="360" r="34" fill="#0a1a2c" stroke="#ff8a4c" stroke-width="1.6"/></g>
  <text x="1030" y="358" text-anchor="middle" font-family="Verdana, Arial, sans-serif" font-size="9.5" font-weight="bold" fill="#ffd6b8">GitLab</text>
  <text x="1030" y="370" text-anchor="middle" font-family="Verdana, Arial, sans-serif" font-size="9.5" font-weight="bold" fill="#ffd6b8">CI/CD</text>

  <g filter="url(#bigGlow)"><circle cx="600" cy="40" r="30" fill="#0a1a2c" stroke="#2ee6a6" stroke-width="1.6"/></g>
  <text x="600" y="45" text-anchor="middle" font-family="Verdana, Arial, sans-serif" font-size="11" font-weight="bold" fill="#b6ffe4">Python</text>

  <!-- title text -->
  <text x="600" y="405" text-anchor="middle" font-family="Consolas, 'Courier New', monospace" font-size="20" letter-spacing="3" fill="#7fe9ff" filter="url(#softGlow)">DEVOPS &amp; CLOUD ENGINEERING</text>
</svg>
