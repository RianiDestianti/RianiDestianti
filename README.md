<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 800 500">
  <!-- Definitions -->
  <defs>
    <!-- Background gradient -->
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#00ADB5;stop-opacity:0.05"/>
      <stop offset="100%" style="stop-color:#00ADB5;stop-opacity:0.15"/>
    </linearGradient>
    
    <!-- Connection lines -->
    <pattern id="connectPattern" x="0" y="0" width="50" height="50" patternUnits="userSpaceOnUse">
      <path d="M0 25h50" stroke="#00ADB5" stroke-width="0.5" stroke-opacity="0.1"/>
      <path d="M25 0v50" stroke="#00ADB5" stroke-width="0.5" stroke-opacity="0.1"/>
    </pattern>
  </defs>

  <!-- Background -->
  <rect width="800" height="500" fill="url(#bgGrad)"/>
  <rect width="800" height="500" fill="url(#connectPattern)"/>

  <!-- Programming Languages -->
  <g transform="translate(50, 50)">
    <!-- HTML5 Logo -->
    <path d="M0,0 L50,0 L45.5,45 L25,50 L4.5,45 Z" fill="#E34F26"/>
    <path d="M25,5 L25,45 L41,41 L45,5 Z" fill="#F06529"/>
    <path d="M25,25 L15,25 L14,15 L25,15 Z M25,35 L15,35 L14,30 L25,30 Z" fill="white"/>
    
    <!-- CSS3 Logo -->
    <g transform="translate(80, 0)">
      <path d="M0,0 L50,0 L45.5,45 L25,50 L4.5,45 Z" fill="#1572B6"/>
      <path d="M25,5 L25,45 L41,41 L45,5 Z" fill="#33A9DC"/>
      <path d="M25,25 L35,25 L34,35 L25,38 L16,35 L15.5,30 Z" fill="white"/>
    </g>

    <!-- JavaScript Logo -->
    <g transform="translate(160, 0)">
      <rect x="0" y="0" width="50" height="50" fill="#F7DF1E"/>
      <path d="M15,35 C15,42 30,42 30,35 L30,25 L15,25 L15,30 L25,30 L25,35" fill="black"/>
      <path d="M35,25 L35,35 C35,42 20,42 20,35" fill="black"/>
    </g>

    <!-- Python Logo -->
    <g transform="translate(240, 0)">
      <path d="M25,0 C11,0 12,10 12,10 L12,20 L38,20 L38,25 L5,25 C5,25 0,23 0,35 C0,47 5,45 5,45 L15,45 L15,35 C15,35 14,25 25,25 C36,25 35,35 35,35 L35,45 L45,45 C45,45 50,47 50,35 C50,23 45,25 45,25 L35,25 L35,10 C35,10 36,0 25,0 Z" fill="#3776AB"/>
    </g>
  </g>

  <!-- Frameworks -->
  <g transform="translate(50, 150)">
    <!-- Flutter Logo -->
    <path d="M0,25 L25,0 L50,25 L25,50 Z" fill="#02569B"/>
    <path d="M12.5,25 L25,37.5 L37.5,25 L25,12.5 Z" fill="#45D1FD"/>
    
    <!-- React Logo -->
    <g transform="translate(80, 0)">
      <circle cx="25" cy="25" r="5" fill="#61DAFB"/>
      <ellipse cx="25" cy="25" rx="20" ry="7" stroke="#61DAFB" fill="none" stroke-width="2"/>
      <ellipse cx="25" cy="25" rx="20" ry="7" stroke="#61DAFB" fill="none" stroke-width="2" transform="rotate(60 25 25)"/>
      <ellipse cx="25" cy="25" rx="20" ry="7" stroke="#61DAFB" fill="none" stroke-width="2" transform="rotate(-60 25 25)"/>
    </g>

    <!-- Laravel Logo -->
    <g transform="translate(160, 0)">
      <path d="M25,0 L50,45 L0,45 Z" fill="#FF2D20"/>
      <path d="M15,15 L35,15 L25,35 Z" fill="white"/>
    </g>

    <!-- Node.js Logo -->
    <g transform="translate(240, 0)">
      <path d="M25,0 L50,15 L50,35 L25,50 L0,35 L0,15 Z" fill="#339933"/>
      <path d="M25,10 L37,18 L37,32 L25,40 L13,32 L13,18 Z" fill="white"/>
    </g>
  </g>

  <!-- Development Tools -->
  <g transform="translate(50, 250)">
    <!-- VS Code Logo -->
    <path d="M0,25 L10,5 L40,25 L10,45 Z" fill="#007ACC"/>
    
    <!-- Git Logo -->
    <g transform="translate(80, 0)">
      <path d="M45,25 L25,5 L5,25 L25,45 Z" fill="#F05032"/>
      <circle cx="25" cy="25" r="5" fill="white"/>
    </g>

    <!-- Firebase Logo -->
    <g transform="translate(160, 0)">
      <path d="M10,40 L25,5 L35,20 L40,10 L45,40 Z" fill="#FFCA28"/>
    </g>

    <!-- MySQL Logo -->
    <g transform="translate(240, 0)">
      <path d="M0,25 C0,11 11,0 25,0 C39,0 50,11 50,25 C50,39 39,50 25,50 C11,50 0,39 0,25" fill="#4479A1"/>
      <path d="M15,15 L35,35 M35,15 L15,35" stroke="white" stroke-width="3"/>
    </g>
  </g>

  <!-- Decorative elements -->
  <circle cx="700" cy="100" r="30" fill="#00ADB5" opacity="0.1"/>
  <circle cx="750" cy="400" r="40" fill="#00ADB5" opacity="0.1"/>
  <path d="M680 250 L720 250 L700 290 Z" fill="#00ADB5" opacity="0.1"/>
</svg>
