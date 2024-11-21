<template>
  <main
    class="mt-10 md:mt-1 flex flex-col-reverse gap-8 items-center md:flex-row md:gap-16 md:justify-center min-h-[65vh] md:min-h-[80vh] bg-black"
  >
    <div class="space-y-2 text-center md:text-left px-10">
      <p class="text-green-200 green-text blink">Hello World, I'm</p>
      <h1 class="text-4xl font-bold md:text-5xl text-green-200 fadein-up">
        Muhammad Kafaby
      </h1>
      <div class="py-2">
        <h1
          class="typewrite text-xl font-semibold text-transparent bg-clip-text bg-gradient-to-r from-green-100 to-green-500 md:text-2xl fadein-up"
          ref="typewriter"
        >
          <span class="wrap">{{ txt }}</span>
        </h1>
      </div>
      <p class="text-green-200 pr-4 fade-in-from-left">
        Welcome to My personal website. <span class="wave">👋🏼</span>
      </p>
      <br />
      <a href="https://drive.usercontent.google.com/download?id=1XcUN4NMzv3-6nPErp6QoxbtnaugUxYpq&export=download&authuser=1&confirm=t&uuid=86accf5c-e44a-4eb8-8620-39bb9954cbbe&at=AENtkXYLKqNIGyexClL0lLDQhJ5E:1732173017665" target="_blank" rel="noopener noreferrer">
      <button
        class="fadein-bot fade-500 flex items-center py-2 px-4 mx-auto text-sm font-medium rounded-lg border transition duration-300 md:py-2.5 md:px-5 md:mx-0 text-green-200 border-green-200 hover:bg-green-200 hover:bg-opacity-10 bg-transparent focus:outline-none w-fit"><svg
          xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="mr-2 w-4 h-4">
          <path fill-rule="evenodd"
            d="M5.625 1.5H9a3.75 3.75 0 013.75 3.75v1.875c0 1.036.84 1.875 1.875 1.875H16.5a3.75 3.75 0 013.75 3.75v7.875c0 1.035-.84 1.875-1.875 1.875H5.625a1.875 1.875 0 01-1.875-1.875V3.375c0-1.036.84-1.875 1.875-1.875zm5.845 17.03a.75.75 0 001.06 0l3-3a.75.75 0 10-1.06-1.06l-1.72 1.72V12a.75.75 0 00-1.5 0v4.19l-1.72-1.72a.75.75 0 00-1.06 1.06l3 3z"
            clip-rule="evenodd"></path>
          <path
            d="M14.25 5.25a5.23 5.23 0 00-1.279-3.434 9.768 9.768 0 016.963 6.963A5.23 5.23 0 0016.5 7.5h-1.875a.375.375 0 01-.375-.375V5.25z">
          </path>
        </svg>Download Resume</button>
      </a>
    </div>
    <div class="flex justify-center md:justify-start fadein-right">
      <img
        alt="avatar"
        fetchpriority="high"
        width="300"
        height="300"
        decoding="async"
        data-nimg="1"
        class="w-10/12 md:h-auto rounded-full border-4 border-green-200 pict"
        src="https://i1.sndcdn.com/avatars-000214125831-5q6tdw-t500x500.jpg"
      />
    </div>
  </main>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      toRotate: [
        "DevOps Engineer",
        "Cyber Security Enthusiast",
        "Web Developer | Full-stack",
        "Diploma Informatics Student | Telkom University",
        "Tech Enthusiast",
      ],
      period: 2000,
      txt: "",
      loopNum: 0,
      isDeleting: false,
    };
  },
  mounted() {
    this.$nextTick(() => {
      this.tick();
    });
  },
  methods: {
    tick() {
      let typewriter = this.$refs.typewriter;

      if (!typewriter) {
        return;
      }

      let i = this.loopNum % this.toRotate.length;
      let fullTxt = this.toRotate[i];

      this.txt = this.isDeleting
        ? fullTxt.substring(0, this.txt.length - 1)
        : fullTxt.substring(0, this.txt.length + 1);
      typewriter.innerHTML = `<span class="wrap">${this.txt}</span>`;

      let that = this;
      let delta = 200 - Math.random() * 100;

      if (this.isDeleting) {
        delta /= 2;
      }

      if (!this.isDeleting && this.txt === fullTxt) {
        delta = this.period;
        this.isDeleting = true;
      } else if (this.isDeleting && this.txt === "") {
        this.isDeleting = false;
        this.loopNum++;
        delta = 500;
      }

      setTimeout(() => {
        that.tick();
      }, delta);
    },
  },
};
</script>

<style>
body {
  overflow-y: scroll;
  overflow-x: hidden;
  background-color: black;
  color: #00ff00; /* Warna hijau hacker */
}

.green-text, .text-green-200, .border-green-200 {
  color: #00ff00 !important;
  border-color: #00ff00 !important;
}

.typewrite > .wrap {
  border-right: 0.08em solid #00ff00;
}

.wave {
  animation-name: wave-animation;
  animation-duration: 2.5s;
  animation-iteration-count: infinite;
  transform-origin: 70% 70%;
  display: inline-block;
}

a {
  color: #00ff00;
  transition: color 0.3s ease;
}

a:hover {
  color: #00cc00;
}

button {
  background-color: black;
  color: #00ff00;
  transition: background-color 0.3s ease, color 0.3s ease, transform 0.3s ease;
}

button:hover {
  background-color: #00ff00;
  color: black;
  transform: scale(1.05);
}

input, textarea {
  background-color: black;
  color: #00ff00;
  border: 1px solid #00ff00;
  transition: border-color 0.3s ease, box-shadow 0.3s ease;
}

input:focus, textarea:focus {
  border-color: #00cc00;
  box-shadow: 0 0 10px #00cc00;
}

@keyframes wave-animation {
  0% {
    transform: rotate(0deg);
  }

  10% {
    transform: rotate(14deg);
  }

  20% {
    transform: rotate(-8deg);
  }

  30% {
    transform: rotate(14deg);
  }

  40% {
    transform: rotate(-4deg);
  }

  50% {
    transform: rotate(10deg);
  }

  60% {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(0deg);
  }
}

.pict {
  box-shadow: 0px 0px 73px -9px rgba(0, 255, 0, 0.44); /* Green color */
  -webkit-box-shadow: 0px 0px 73px -9px rgba(0, 255, 0, 0.44); /* Green color */
  -moz-box-shadow: 0px 0px 73px -9px rgba(0, 255, 0, 0.44); /* Green color */
}

.fadein-up, .fade-in-from-left, .fadein-right, .fadein-bot {
  color: #00ff00;
}

.fadein-up {
  opacity: 0;
  animation-name: fadeInUp;
  animation-duration: 0.5s;
  animation-fill-mode: forwards;
  animation-delay: 500ms;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translate3d(0, 100%, 0);
  }

  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}

.fade-in-from-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
  animation-delay: 500ms;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadein-right {
  opacity: 0;
  animation: fadeInRight 0.5s ease-out forwards;
  animation-delay: 500ms;
}

@keyframes fadeInRight {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadein-bot {
  opacity: 0;
  animation: fadeInBot 0.5s forwards;
}

@keyframes fadeInBot {
  from {
    opacity: 0;
    transform: translate3d(0, -100%, 0);
  }

  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}

.fadein-1 {
  animation-delay: 200ms;
}
.fadein-2 {
  animation-delay: 400ms;
}
.fadein-3 {
  animation-delay: 600ms;
}
.fade-500 {
  animation-delay: 500ms;
}

/* Animasi berkedip */
.blink {
  animation: blink-animation 1s steps(5, start) infinite;
  -webkit-animation: blink-animation 1s steps(5, start) infinite;
}

@keyframes blink-animation {
  to {
    visibility: hidden;
  }
}

/* Animasi glitch */
.glitch {
  position: relative;
  color: #00ff00;
  font-size: 2em;
  animation: glitch-animation 1s infinite;
}

.glitch::before,
.glitch::after {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: black;
  overflow: hidden;
}

.glitch::before {
  left: 2px;
  text-shadow: -2px 0 red;
  clip: rect(24px, 550px, 90px, 0);
  animation: glitch-animation 2s infinite linear alternate-reverse;
}

.glitch::after {
  left: -2px;
  text-shadow: -2px 0 blue;
  clip: rect(85px, 550px, 140px, 0);
  animation: glitch-animation 3s infinite linear alternate-reverse;
}

@keyframes glitch-animation {
  0% {
    clip: rect(42px, 9999px, 44px, 0);
    transform: skew(0.3deg);
  }
  5% {
    clip: rect(12px, 9999px, 74px, 0);
    transform: skew(0.3deg);
  }
  10% {
    clip: rect(82px, 9999px, 14px, 0);
    transform: skew(0.3deg);
  }
  15% {
    clip: rect(12px, 9999px, 64px, 0);
    transform: skew(0.3deg);
  }
  20% {
    clip: rect(32px, 9999px, 84px, 0);
    transform: skew(0.3deg);
  }
  25% {
    clip: rect(22px, 9999px, 54px, 0);
    transform: skew(0.3deg);
  }
  30% {
    clip: rect(12px, 9999px, 94px, 0);
    transform: skew(0.3deg);
  }
  35% {
    clip: rect(42px, 9999px, 24px, 0);
    transform: skew(0.3deg);
  }
  40% {
    clip: rect(72px, 9999px, 34px, 0);
    transform: skew(0.3deg);
  }
  45% {
    clip: rect(52px, 9999px, 44px, 0);
    transform: skew(0.3deg);
  }
  50% {
    clip: rect(32px, 9999px, 54px, 0);
    transform: skew(0.3deg);
  }
  55% {
    clip: rect(12px, 9999px, 64px, 0);
    transform: skew(0.3deg);
  }
  60% {
    clip: rect(42px, 9999px, 74px, 0);
    transform: skew(0.3deg);
  }
  65% {
    clip: rect(22px, 9999px, 84px, 0);
    transform: skew(0.3deg);
  }
  70% {
    clip: rect(32px, 9999px, 94px, 0);
    transform: skew(0.3deg);
  }
  75% {
    clip: rect(12px, 9999px, 104px, 0);
    transform: skew(0.3deg);
  }
  80% {
    clip: rect(42px, 9999px, 114px, 0);
    transform: skew(0.3deg);
  }
  85% {
    clip: rect(72px, 9999px, 124px, 0);
    transform: skew(0.3deg);
  }
  90% {
    clip: rect(52px, 9999px, 134px, 0);
    transform: skew(0.3deg);
  }
  95% {
    clip: rect(32px, 9999px, 144px, 0);
    transform: skew(0.3deg);
  }
  100% {
    clip: rect(12px, 9999px, 154px, 0);
    transform: skew(0.3deg);
  }
}
</style>