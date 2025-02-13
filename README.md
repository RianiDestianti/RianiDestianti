<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Riani Destianti - Interactive Profile</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/particles.js/2.0.0/particles.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/vanilla-tilt/1.7.0/vanilla-tilt.min.js"></script>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #0a192f;
      color: #fff;
      line-height: 1.6;
      overflow-x: hidden;
    }

    #particles-js {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 2rem;
      position: relative;
      z-index: 2;
    }

    h1, h2 {
      text-align: center;
      margin: 2rem 0;
      background: linear-gradient(45deg, #00ADB5, #FF2D20);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 0.6s ease forwards;
    }

    .typing-text {
      min-height: 72px;
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 2rem 0;
    }

    .card {
      background: rgba(255, 255, 255, 0.05);
      backdrop-filter: blur(10px);
      border-radius: 15px;
      padding: 2rem;
      margin: 2rem 0;
      transform-style: preserve-3d;
      transform: perspective(1000px);
      transition: all 0.3s ease;
      opacity: 0;
      animation: fadeIn 0.6s ease forwards;
    }

    .code-block {
      background: #1a1a1a;
      padding: 1.5rem;
      border-radius: 10px;
      overflow-x: auto;
      position: relative;
    }

    .code-block::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, #00ADB5, #FF2D20);
      opacity: 0.1;
      pointer-events: none;
    }

    .tech-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 1rem;
      margin: 2rem 0;
    }

    .tech-item {
      background: rgba(255, 255, 255, 0.1);
      padding: 1rem;
      border-radius: 10px;
      text-align: center;
      transition: all 0.3s ease;
      cursor: pointer;
    }

    .tech-item:hover {
      transform: translateY(-5px);
      background: rgba(255, 255, 255, 0.2);
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 1rem;
      margin: 2rem 0;
    }

    .social-links a {
      padding: 0.5rem 1rem;
      border-radius: 5px;
      transition: all 0.3s ease;
      text-decoration: none;
      color: #fff;
    }

    .social-links a:hover {
      transform: translateY(-3px);
    }

    @keyframes fadeInUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes fadeIn {
      to {
        opacity: 1;
      }
    }

    .progress-bar {
      width: 100%;
      height: 8px;
      background: rgba(255, 255, 255, 0.1);
      border-radius: 4px;
      margin: 1rem 0;
      position: relative;
      overflow: hidden;
    }

    .progress-bar::after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 0;
      background: linear-gradient(45deg, #00ADB5, #FF2D20);
      animation: progressAnimation 1.5s ease forwards;
    }

    @keyframes progressAnimation {
      to {
        width: var(--progress);
      }
    }
  </style>
</head>
<body>
  <div id="particles-js"></div>
  <div class="container">
    <h1>Hi there, I'm Riani Destianti! 👋</h1>

    <div class="typing-text">
      <img src="https://readme-typing-svg.herokuapp.com?font=Montserrat&weight=600&size=24&pause=1000&color=00ADB5&center=true&vCenter=true&random=false&width=500&lines=Mobile+App+Development+Enthusiast;Flutter+Developer;Learning+Full+Stack+Development" alt="Typing SVG" />
    </div>

    <div class="card" data-tilt data-tilt-max="5">
      <h2>👩‍💻 About Me</h2>
      <div class="code-block">
        <pre><code>fun main() {
    val dev = Developer()
}

class Developer {
    val name = "Riani Destianti"
    val education = "Software Engineering Student"
    val location = "Bandung, Indonesia"

    val interests = listOf(
        "Mobile Development",
        "Machine Learning",
        "Web Development"
    )

    val skills = mapOf(
        "Mobile" to listOf("Flutter", "Kotlin", "React Native"),
        "Backend" to listOf("PHP", "Laravel", "MySQL"),
        "Frontend" to listOf("HTML5", "CSS3", "JavaScript", "Bootstrap"),
        "Other" to listOf("Python", "C#", "Arduino")
    )

    val primaryFocus = mapOf(
        "Mobile" to "Flutter, Kotlin & React Native Development",
        "Web" to "Full Stack Development",
        "Learning" to "Machine Learning & AI"
    )
}</code></pre>
      </div>
    </div>

    <div class="card" data-tilt data-tilt-max="5">
      <h2>🛠️ Technologies & Tools</h2>
      <div class="tech-grid">
        <div class="tech-item" style="--progress: 90%">
          Flutter
          <div class="progress-bar"></div>
        </div>
        <div class="tech-item" style="--progress: 85%">
          Kotlin
          <div class="progress-bar"></div>
        </div>
        <div class="tech-item" style="--progress: 80%">
          React Native
          <div class="progress-bar"></div>
        </div>
        <div class="tech-item" style="--progress: 75%">
          Laravel
          <div class="progress-bar"></div>
        </div>
        <div class="tech-item" style="--progress: 85%">
          MySQL
          <div class="progress-bar"></div>
        </div>
        <div class="tech-item" style="--progress: 70%">
          Python
          <div class="progress-bar"></div>
        </div>
      </div>
    </div>

    <div class="card" data-tilt data-tilt-max="5">
      <h2>🌟 Currently</h2>
      <ul>
        <li>🤖 Machine Learning: Fascinated by AI's ability to solve complex problems</li>
        <li>💡 Emerging Tech Trends: Staying ahead of the curve in technological innovations</li>
        <li>🧠 Adaptive Learning: Rapidly integrating new technological paradigms</li>
        <li>🚀 Future-Focused: Committed to understanding and leveraging next-generation technologies</li>
      </ul>
    </div>

    <div class="social-links">
      <a href="https://www.instagram.com/rianidstiantii/" style="background: #E4405F">Instagram</a>
      <a href="https://www.linkedin.com/in/riani-destianti-70504a323/" style="background: #0077B5">LinkedIn</a>
    </div>
  </div>

  <script>
    particlesJS('particles-js', {
      particles: {
        number: { value: 80 },
        color: { value: '#00ADB5' },
        shape: { type: 'circle' },
        opacity: { value: 0.5 },
        size: { value: 3 },
        line_linked: {
          enable: true,
          distance: 150,
          color: '#00ADB5',
          opacity: 0.4,
          width: 1
        },
        move: {
          enable: true,
          speed: 2,
          direction: 'none',
          random: false,
          straight: false,
          out_mode: 'out',
          bounce: false,
        }
      },
      interactivity: {
        detect_on: 'canvas',
        events: {
          onhover: { enable: true, mode: 'repulse' },
          onclick: { enable: true, mode: 'push' },
          resize: true
        }
      },
      retina_detect: true
    });

    VanillaTilt.init(document.querySelectorAll('.card'), {
      max: 5,
      speed: 400,
      glare: true,
      'max-glare': 0.2,
    });

    // Animate cards on scroll
    const cards = document.querySelectorAll('.card');
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.style.opacity = '1';
            entry.target.style.transform = 'translateY(0)';
          }
        });
      },
      { threshold: 0.1 }
    );

    cards.forEach(card => {
      observer.observe(card);
    });
  </script>
</body>
</html>
