// script.js
const openBtn = document.querySelector('.open-btn');
const cover = document.querySelector('.cover');
const page = document.querySelector('.page');
const sparkleContainer = document.getElementById('sparkleContainer');

openBtn.addEventListener('click', () => {
  cover.style.transform = 'rotateY(-180deg)';
  page.style.transform = 'rotateY(0deg)';
  triggerSparkles();
});

function triggerSparkles() {
  for (let i = 0; i < 50; i++) {
    const sparkle = document.createElement('div');
    sparkle.classList.add('sparkle');
    sparkle.style.left = `${50 + Math.random() * 10 - 5}vw`; // near center
    sparkle.style.top = `${50 + Math.random() * 10 - 5}vh`; // near center
    sparkleContainer.appendChild(sparkle);

    setTimeout(() => sparkle.remove(), 800);
  }
}
