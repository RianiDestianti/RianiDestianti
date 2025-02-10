<!DOCTYPE html>
<html>
<head>
  <style>
    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-10px); }
      100% { transform: translateY(0px); }
    }

    @keyframes glow {
      0% { box-shadow: 0 0 5px #00ADB5; }
      50% { box-shadow: 0 0 20px #00ADB5; }
      100% { box-shadow: 0 0 5px #00ADB5; }
    }

    .container {
      background: linear-gradient(135deg, #1a1a1a, #2d2d2d);
      color: white;
      padding: 2rem;
      border-radius: 1rem;
      font-family: 'Montserrat', sans-serif;
    }

    .tech-badge {
      background: rgba(255, 255, 255, 0.1);
      padding: 0.5rem 1rem;
      border-radius: 0.5rem;
      margin: 0.25rem;
      display: inline-block;
      transition: all 0.3s ease;
      animation: glow 3s infinite;
    }

    .tech-badge:hover {
      transform: translateY(-5px);
      box-shadow: 0 0 20px #00ADB5;
    }

    .profile-section {
      background: rgba(0, 173, 181, 0.1);
      border-radius: 1rem;
      padding: 1.5rem;
      margin: 1rem 0;
      animation: float 6s ease-in-out infinite;
    }

    .code-block {
      background: #2d2d2d;
      padding: 1rem;
      border-radius: 0.5rem;
      border-left: 4px solid #00ADB5;
      font-family: 'Fira Code', monospace;
      position: relative;
      overflow: hidden;
    }

    .code-block::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(
        90deg,
        transparent,
        rgba(0, 173, 181, 0.2),
        transparent
      );
      animation: shine 3s infinite;
    }

    @keyframes shine {
      to {
        left: 100%;
      }
    }

    .social-links a {
      margin: 0 1rem;
      transition: transform 0.3s ease;
    }

    .social-links a:hover {
      transform: scale(1.2);
    }

    .currently-section li {
      transition: all 0.3s ease;
      padding: 0.5rem;
      border-radius: 0.5rem;
    }

    .currently-section li:hover {
      background: rgba(0, 173, 181, 0.1);
      transform: translateX(10px);
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- Your existing content structure remains, but with added animations -->
    <div class="profile-section">
      <div class="code-block">
        <pre><code>
class Developer {
    val name = "Riani Destianti"
    val education = "Software Engineering Student"
    val location = "Bandung, Indonesia"
    
    val interests = listOf(
        "Mobile Development",
        "Machine Learning",
        "Web Development"
    )
}
        </code></pre>
      </div>
    </div>

    <div class="tech-stack">
      <!-- Mobile Development -->
      <div class="tech-badge">Flutter</div>
      <div class="tech-badge">Kotlin</div>
      <div class="tech-badge">React Native</div>
      
      <!-- Web Development -->
      <div class="tech-badge">Laravel</div>
      <div class="tech-badge">PHP</div>
      <div class="tech-badge">MySQL</div>
      
      <!-- Frontend -->
      <div class="tech-badge">HTML5</div>
      <div class="tech-badge">CSS3</div>
      <div class="tech-badge">JavaScript</div>
      <div class="tech-badge">Bootstrap</div>
    </div>

    <div class="currently-section">
      <h2>🌟 Currently</h2>
      <ul>
        <li>🤖 Machine Learning Explorer</li>
        <li>💡 Tech Trend Watcher</li>
        <li>🧠 Continuous Learner</li>
        <li>🚀 Future Builder</li>
      </ul>
    </div>
  </div>
</body>
</html>
