const nav = document.getElementById('nav');
function updateNav() {
  nav.classList.toggle('solid', window.scrollY > 80);
}
updateNav();
window.addEventListener('scroll', updateNav);

document.querySelectorAll('.menu-tab').forEach(tab => {
  tab.addEventListener('click', () => {
    const key = tab.dataset.tab;
    document.querySelectorAll('.menu-tab').forEach(t => t.classList.remove('active'));
    document.querySelectorAll('.menu-panel').forEach(p => p.classList.remove('active'));
    tab.classList.add('active');
    document.querySelector(`[data-panel="${key}"]`).classList.add('active');
  });
});

function openMob() { document.getElementById('mobMenu').classList.add('open'); }
function closeMob() { document.getElementById('mobMenu').classList.remove('open'); }

function submitBooking() {
  const btn = document.querySelector('.form-submit');
  btn.textContent = '✓ Заявка отправлена';
  btn.style.background = '#4a7c59';
  btn.style.color = 'white';
  setTimeout(() => {
    btn.textContent = 'Подтвердить бронирование';
    btn.style.background = '';
    btn.style.color = '';
  }, 4000);
}

const observer = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.style.opacity = '1';
      e.target.style.transform = 'translateY(0)';
    }
  });
}, { threshold: .08 });

document.querySelectorAll('.event-card, .menu-card, .contact-block').forEach(el => {
  el.style.opacity = '0';
  el.style.transform = 'translateY(16px)';
  el.style.transition = 'opacity .5s, transform .5s';
  observer.observe(el);
});
