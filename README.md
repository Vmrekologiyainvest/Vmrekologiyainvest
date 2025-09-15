</form>
        <div id="toast" class="toast" role="status" aria-live="polite">Заявка отправлена. Мы свяжемся с вами в ближайшее время.</div>
      </div>
    </section>
    <section id="contact">
      <div class="wrap">
        <h2 class="section-title">Контакты</h2>
        <div class="contacts">
          <div class="contact-card card">
            <h4>ООО «ВМРЭКОЛОГИЯИНВЕСТ»</h4>
            <div class="contact-line">Республика Беларусь, Минский район</div>
            <div class="contact-line">Тел.: <a href="tel:+375293509218">+375 29 350 92 18</a></div>
            <div class="contact-line">Режим работы: Пн–Пт 9:00–18:00</div>
          </div>
          <div class="contact-card card">
            <h4>Документы и приёмка</h4>
            <div class="contact-line">Договор поставки, УПД/акты</div>
            <div class="contact-line">Весовой контроль, акт качества, фотофиксация</div>
            <div class="contact-line">Самовывоз 1–3 дня по заявке</div>
          </div>
        </div>
        <div class="kp">
          <a class="btn" href="#materials">Требования к сырью</a>
          <a class="btn primary" href="#request">Оставить заявку</a>
        </div>
        <p class="notice">Если у вас есть прайс или спецификация сырья — отправьте при звонке или укажите в комментарии формы.</p>
      </div>
    </section>
  </main>
  <footer>
    <div class="wrap">
      <div>© <span id="year"></span> ООО «ВМРЭКОЛОГИЯИНВЕСТ». Все права защищены.</div>
      <div class="notice">Информация на сайте не является публичной офертой. Цены и условия уточняются индивидуально по заявке.</div>
    </div>
  </footer>
  <div class="float-call">
    <a class="btn call" href="tel:+375293509218">Связаться: +375 29 350 92 18</a>
  </div>vmrekologiyainvest@mail.ru
  <script>
    // Year
    document.getElementById('year').textContent = new Date().getFullYear();
    // Fake submit handler (replace with real endpoint/fetch)
    function submitForm(){
      const toast = document.getElementById('toast');
      toast.classList.add('show');
      setTimeout(()=> toast.classList.remove('show'), 2600);
      // Example to collect data:
      const data = {
        name: document.getElementById('name').value.trim(),
        phone: document.getElementById('phone').value.trim(),
        material: document.getElementById('material').value.trim(),
        volume: document.getElementById('volume').value.trim(),
        address: document.getElementById('address').value.trim(),
        notes: document.getElementById('notes').value.trim()
      };
      console.log('Lead:', data);
      // To integrate: send to email/Telegram/CRM via fetch(...)
      // fetch('/api/lead', {method:'POST', headers:{'Content-Type':'application/json'}, body:JSON.stringify(data)})
    }
  </script>
</body>
</html>
