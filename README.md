Ссылка для розыгрышей можно записать на NFC метку 
<!-- Гайд: как записать ссылку на NFC-метку (HTML для README.md) -->
<div style="max-width: 900px; margin: 0 auto; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; line-height: 1.5; color: #24292f;">
  <h1>📱 Гайд: как записать ссылку на NFC‑метку</h1>
  <p>Полное руководство, чтобы ссылка гарантированно открывалась на любом смартфоне (Android и iPhone) без установки дополнительных приложений. В качестве инструмента используется <strong>NFC Tools</strong> (доступно в Play Market и App Store).</p>

  <hr />

  <h2>1. Подготовка</h2>
  <ul>
    <li><strong>Тип метки:</strong> Используйте метки <code>NTAG 21x</code> (NTAG213, NTAG215, NTAG216). Старые метки Mifare Classic (ключи от домофонов, транспортные карты) для записи ссылок <strong>не подходят</strong>.</li>
    <li><strong>Объем памяти:</strong>
      <ul>
        <li><code>NTAG213</code> (144 байта) — для короткой ссылки.</li>
        <li><code>NTAG215</code> (504 байта) или <code>NTAG216</code> (888 байт) — для длинных ссылок с UTM‑метками или дополнительной информацией.</li>
      </ul>
    </li>
    <li><strong>Приложение:</strong> Установите <strong>NFC Tools</strong> (разработчик — <em>wakdev</em>).</li>
  </ul>

  <h2>2. Два способа записи ссылки</h2>

  <h3>🔹 Способ 1: «сырая» ссылка (URL/URI)</h3>
  <p>Этот способ подходит для Android или если на iPhone пользователь готов нажать лишнее уведомление.</p>
  <ol>
    <li>Откройте <strong>NFC Tools</strong>.</li>
    <li>Нажмите <strong>«Запись»</strong> (Write).</li>
    <li>Выберите <strong>«Добавить запись»</strong> → категория <strong>«Изменение данных»</strong> → тип <strong>URL / URI</strong>.</li>
    <li>Вставьте ссылку → <strong>OK</strong> → <strong>«Записать»</strong>.</li>
    <li>Поднесите метку к задней крышке телефона.</li>
  </ol>
  <p><strong>⚠️ Минус для iPhone:</strong> потребуется дополнительное подтверждение (разблокировка, нажатие на уведомление).</p>

  <h3>🔸 Способ 2: через запись контакта (VCard + URL) — <strong>рекомендуемый</strong></h3>
  <p>Ссылка выглядит как системное уведомление с кнопкой «Открыть», работает чище на iOS и привычнее на Android.</p>
  <ol>
    <li>В <strong>NFC Tools</strong> нажмите <strong>«Запись»</strong> → <strong>«Добавить запись»</strong> → категория <strong>«Контакты»</strong> (VCard).</li>
    <li>Заполните поля:
      <ul>
        <li><strong>Имя (Name):</strong> заголовок уведомления (например, «Меню ресторана», «Сайт компании»).</li>
        <li><strong>URL:</strong> вставьте нужную ссылку. Остальные поля оставьте пустыми.</li>
      </ul>
    </li>
    <li>Нажмите <strong>OK</strong> → <strong>«Записать»</strong> и приложите метку.</li>
  </ol>
  <p><strong>Как это работает:</strong><br />
  На <strong>iPhone</strong> появляется системное уведомление с вашим заголовком и кнопкой «Открыть контакт» → внутри карточки ссылка кликабельна.<br />
  На <strong>Android</strong> часто сразу отображается ссылка или предлагается добавить контакт (в современных версиях это также работает как быстрый доступ).</p>

  <hr />

  <h2>3. Нюансы и «золотые правила»</h2>
  <ul>
    <li><strong>Сокращайте ссылки</strong> — используйте <code>bit.ly</code>, <code>clck.ru</code> или свой короткий домен. Это экономит память метки и повышает доверие.</li>
    <li><strong>Тестируйте на обоих телефонах</strong> — обязательно проверьте работу на <strong>iPhone (в том числе с заблокированным экраном)</strong> и на <strong>Android</strong>. Если ссылка открывается не так, как нужно, перезапишите метку способом VCard.</li>
    <li><strong>Защита от перезаписи (Lock)</strong> — когда всё настроено, в NFC Tools поставьте галочку <strong>«Защитить от записи»</strong>. <em>Внимание: это действие необратимо.</em></li>
    <li><strong>Оформление</strong> — используйте стикеры с печатью (логотип, текст) или пластиковые NFC-карты, чтобы пользователь понимал, куда прикладывать телефон.</li>
  </ul>

  <h2>4. Итоговая шпаргалка</h2>
  <table style="width: 100%; border-collapse: collapse; background: #f6f8fa; border: 1px solid #d0d7de;">
    <thead>
      <tr style="background: #eaeef2;">
        <th style="padding: 10px; border: 1px solid #d0d7de;">Шаг</th>
        <th style="padding: 10px; border: 1px solid #d0d7de;">Действие</th>
        <th style="padding: 10px; border: 1px solid #d0d7de;">Инструмент / Примечание</th>
      </tr>
    </thead>
    <tbody>
      <tr><td style="padding: 8px; border: 1px solid #d0d7de;">1</td><td style="padding: 8px; border: 1px solid #d0d7de;">Купить метку</td><td style="padding: 8px; border: 1px solid #d0d7de;">NTAG213 (короткая ссылка) или NTAG215/216 (длинная)</td></tr>
      <tr><td style="padding: 8px; border: 1px solid #d0d7de;">2</td><td style="padding: 8px; border: 1px solid #d0d7de;">Скачать приложение</td><td style="padding: 8px; border: 1px solid #d0d7de;">NFC Tools (wakdev)</td></tr>
      <tr><td style="padding: 8px; border: 1px solid #d0d7de;">3</td><td style="padding: 8px; border: 1px solid #d0d7de;">Сократить ссылку</td><td style="padding: 8px; border: 1px solid #d0d7de;">Bitly, Clck.ru или свой домен</td></tr>
      <tr><td style="padding: 8px; border: 1px solid #d0d7de;">4</td><td style="padding: 8px; border: 1px solid #d0d7de;">Выбрать тип записи</td><td style="padding: 8px; border: 1px solid #d0d7de;"><strong>VCard (контакт)</strong> — самый надёжный для iOS и Android</td></tr>
      <tr><td style="padding: 8px; border: 1px solid #d0d7de;">5</td><td style="padding: 8px; border: 1px solid #d0d7de;">Записать данные</td><td style="padding: 8px; border: 1px solid #d0d7de;">Приложить телефон к метке</td></tr>
      <tr><td style="padding: 8px; border: 1px solid #d0d7de;">6</td><td style="padding: 8px; border: 1px solid #d0d7de;">Протестировать</td><td style="padding: 8px; border: 1px solid #d0d7de;">iPhone (заблокирован) + Android</td></tr>
      <tr><td style="padding: 8px; border: 1px solid #d0d7de;">7</td><td style="padding: 8px; border: 1px solid #d0d7de;">Защитить от записи</td><td style="padding: 8px; border: 1px solid #d0d7de;">(опционально) NFC Tools → Lock, после финального теста</td></tr>
    </tbody>
  </table>

  <hr />
  <p>Теперь вы можете записать любую ссылку на NFC-метку так, чтобы она работала корректно и выглядела профессионально. Если возникнут вопросы — перепроверьте тип метки и используйте способ <strong>VCard</strong> для максимальной совместимости.</p>
</div>
