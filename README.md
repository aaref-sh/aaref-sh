### Hi there 👋



<div class="container">
    <p>
	Muhammad Aaref Al-Shami 
	<span class="typed-text">
	</span><span class="cursor"> </span>
    </p>
</div>


<style>


  .container {
  background-position: center;
	background-size: cover;
  height: 650px;
  display: flex;
  justify-content: center;
  align-items: center;
}


.container p {
  font-size: 3rem;
  padding: 0.5rem;
  font-weight: bold;
  letter-spacing: 0.1rem;
  text-align: center;
  overflow: hidden;
}


.container p span.typed-text {
  font-weight: normal;
  color: #dd7732;
}


.container p span.cursor {
  display: inline-block;
  background-color: #ccc;
  margin-left: 0.1rem;
  width: 3px;
  animation: blink 1s infinite;
}


.container p span.cursor.typing {
  animation: none;
}


@keyframes blink {
  0%  { background-color: #ccc; }
  49% { background-color: #ccc; }
  50% { background-color: transparent; }
  99% { background-color: transparent; }
  100%  { background-color: #ccc; }
}


</style>
<script>
	
	
  const typedTextSpan = document.querySelector(".typed-text");
const cursorSpan = document.querySelector(".cursor");

const textArray = ["Software Engineer", "Problem Solver", "Backend Developer", ".NET ❤️"];
const typingDelay = 200;
const erasingDelay = 100;
const newTextDelay = 200; // Delay between current and next text
	
	
let textArrayIndex = 0;
let charIndex = 0;

function type() {
  if (charIndex < textArray[textArrayIndex].length) {
    if(!cursorSpan.classList.contains("typing")) cursorSpan.classList.add("typing");
    typedTextSpan.textContent += textArray[textArrayIndex].charAt(charIndex);
    charIndex++;
    setTimeout(type, typingDelay);
  } 
  else {
    cursorSpan.classList.remove("typing");
  	setTimeout(erase, newTextDelay);
  }
}

function erase() {
	if (charIndex > 0) {
    if(!cursorSpan.classList.contains("typing")) cursorSpan.classList.add("typing");
    typedTextSpan.textContent = textArray[textArrayIndex].substring(0, charIndex-1);
    charIndex--;
    setTimeout(erase, erasingDelay);
  } 
  else {
    cursorSpan.classList.remove("typing");
    textArrayIndex++;
    if(textArrayIndex>=textArray.length) textArrayIndex=0;
    setTimeout(type, typingDelay + 1100);
  }
}

document.addEventListener("DOMContentLoaded", function() { // On DOM Load initiate the effect
  if(textArray.length) setTimeout(type, newTextDelay + 100);
});
	
	
</script>
<!--
**aaref-sh/aaref-sh** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
