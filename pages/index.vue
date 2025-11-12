<template>
  <div class="landing-page">
    <header>
      <h1><span class="glitch">S0FTS0RR0W's blog</span></h1>
    </header>
    <main>
      <section class="welcome card">
        <h2><span class="neon-text">Welcome</span></h2>
        <p>This is a place for thoughts, code, and everything in between.</p>
      </section>
      <section class="posts card">
        <h3><span class="neon-text">Latest Posts</span></h3>
        <p>Coming soon...</p>
      </section>
    </main>
    <footer>
      <p>&copy; 2025 s0fts0rr0w</p>
    </footer>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Roboto+Mono:wght@400;700&display=swap');

body {
  background-color: #0a0a0a; /* Very dark background */
  color: #c0c0c0; /* Desaturated text */
  font-family: 'Roboto Mono', monospace; /* Techy font */
  margin: 0;
  padding: 0;
  overflow-x: hidden; /* Prevent horizontal scroll */
}

.landing-page {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  align-items: center;
  text-align: center;
  padding: 20px;
  box-sizing: border-box;
}

header {
  padding: 3rem 0 2rem;
}

header h1 {
  font-family: 'Press Start 2P', cursive; /* Retro gaming font for title */
  font-size: 2.5rem;
  color: #00ffcc; /* Neon green */
  text-shadow: 0 0 10px #00ffcc, 0 0 20px #00ffcc, 0 0 30px #00ffcc;
  margin-bottom: 1rem;
}

.glitch {
  animation: glitch 1.5s infinite;
}

@keyframes glitch {
  0% {
    text-shadow: 0 0 10px #00ffcc, 0 0 20px #00ffcc, 0 0 30px #00ffcc;
    transform: translate(0);
  }
  20% {
    text-shadow: 0 0 10px #ff00ff, 0 0 20px #ff00ff, 0 0 30px #ff00ff;
    transform: translate(-2px, 2px);
  }
  40% {
    text-shadow: 0 0 10px #00ffff, 0 0 20px #00ffff, 0 0 30px #00ffff;
    transform: translate(-2px, -2px);
  }
  60% {
    text-shadow: 0 0 10px #00ffcc, 0 0 20px #00ffcc, 0 0 30px #00ffcc;
    transform: translate(2px, 2px);
  }
  80% {
    text-shadow: 0 0 10px #ff00ff, 0 0 20px #ff00ff, 0 0 30px #ff00ff;
    transform: translate(2px, -2px);
  }
  100% {
    text-shadow: 0 0 10px #00ffcc, 0 0 20px #00ffcc, 0 0 30px #00ffcc;
    transform: translate(0);
  }
}

main {
  flex-grow: 1;
  width: 90%;
  max-width: 900px;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.card {
  background-color: #1a1a1a;
  border: 1px solid #333;
  border-radius: 8px;
  padding: 2rem;
  box-shadow: 0 0 15px rgba(0, 255, 204, 0.2); /* Subtle neon glow */
  transition: all 0.3s ease;
}

.card:hover {
  box-shadow: 0 0 25px rgba(0, 255, 204, 0.4);
  transform: translateY(-5px);
}

.neon-text {
  color: #00ffff; /* Neon blue */
  text-shadow: 0 0 8px #00ffff, 0 0 15px #00ffff;
}

h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
}

h3 {
  font-size: 1.5rem;
  border-bottom: 1px solid #333;
  padding-bottom: 0.5rem;
  margin-bottom: 1.5rem;
}

p {
  line-height: 1.6;
  font-size: 1.1rem;
}

footer {
  padding: 1.5rem 0;
  font-size: 0.9rem;
  color: #666;
  margin-top: 2rem;
  border-top: 1px dashed #333;
  width: 100%;
}
</style>
