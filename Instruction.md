# Інструкція по підключенню до системи SkyHunter (Skymap, ZeroTier)

1. **Реєструємо аккаунт Skyhunter** та [входимо в систему](https://app.skyhuntertech.com/login) до особистого кабінету.  
![Login](/assets/dashboard-login.png "Title")
  >Повідомлення зверху інформує про те, що **немає підключення до радару**.
![no connection](/assets/notification.png "notification")

2. Для  **підключення радару** переходимо в налаштування, натискаємо кнопку "Підключити" та вводимо порт (наприклад `1142`).
![connect](/assets/connect.png "connect")
![port](/assets/port.png "port")
![connected](/assets/connected.png "connected")

-----

3. **Встановлюємо VPN**, до якого підключено сервіс **Skymap** (наприклад, [**ZeroTier**](https://www.zerotier.com/)). 
- Адміністратор VPN-мережі **ZeroTier** повинен надати вам **Network ID** (наприклад `ab000c1def23g4hi`) для підключення. 
- Ви повідомляєте цей **Network ID** (`ab000c1def23g4hi`) команді **SkyHunter**. 
- Команда **SkyHunter** підключається до мережі VPN і надає вам свою адресу (наприклад `z987654yx3`)
- Ви передаєте  цю адресу (`z987654yx3`) адміністратору VPN-мережі **ZeroTier**, щоб адміністратор авторизував **SkyHunter** в своїй системі. 
- Після авторизації адміністратор VPN-мережі **ZeroTier** надає вам **IP-адресу SkyHunter-а** (наприклад `78.193.54.121`).

-----

4. **Переходимо в Skymap**.
- Входимо до системи **Skymap** за раніше отриманими даними доступу. (Якщо доступу немає - зверніться до адміністратора Skymap-осередка).
![Skymap](/assets/skymap.png "Skymap")

5. **Налаштовуємо наш бойовий розрахунок**.
- Обираємо точку на картi, подвійним кліком мишки додаємо розрахунок на мапу і копіюємо широту та довготу з маркера.
![marker](/assets/marker.png "marker")

- Натискаємо на значок шестерні, обираємо пункт меню **Адмін панель** і переходимо в **Розрахунки**.
![crews](/assets/crews.png "crews")
  
- Натискаємо на **Створити розрахунок** і заповнюємо всі обовʼязкові поля та зберігаємо. (Тип вказуємо **Повітряний**, а в координати додаємо ті, що скопіювали з маркеру)
![crew](/assets/crew.png "crew")

- Далі нам потрібно створити засоби ураження і для цього ми переходимо в **Засоби ураження** і додаємо новий.
![means-of-destruction](/assets/means-of-destruction-01.png "means-of-destruction")

- В полі **IP-адреса** вказуєму ту, що отримали від адміністратору VPN-мережі **ZeroTier** - `78.193.54.121`, а **порт** вказуємо той, що вказали при підключенні радару в **SkyHunter** - `1142`
![means-of-destruction](/assets/means-of-destruction-02.png "means-of-destruction")

> **Для перевірки інтеграції** призначте трек на новий розрахунок. (Військові знають, як це робиться.)

> За замовчанням розрахунок неактивний. Для активації увімкніть режим **«На чергуванні»**.
![on-duty-disabled](/assets/on-duty-disabled.png "on-duty-disabled")
![on-duty](/assets/on-duty.png "on-duty")
---

## Створення цілей та прив'язка до розрахунку

1. Натискаємо на значок шестерні, обираємо пункт меню "Відладка". Можна залишити все, як є тільки координати додаємо ті, що скопіювали раніше з маркеру. Натискаємо на **Запустити**.
![add-planes](/assets/add-planes.png "add-planes")
![add-planes-1](/assets/add-planes-1.png "add-planes-1")
2. Обираємо ціль, яку призначемо своєю. Для цього клікаємо на обраний літак і натискаємо на **Свій**. На наступному кроці привʼязуємо ціль до нашого розрахунку. (Аналогічно робимо для ворожого літака)
![define-my-plane](/assets/define-my-plane.png "define-my-plane")
![define-target](/assets/define-target.png "define-target")
3. Аналогічно створюємо та прив'язуємо інші цілі. Як тільки цілі прив'язані до розрахунку, вони повинні відразу з'явитися в інтерфейсі **SkyHunter**.
![skyhunter-targets](/assets/skyhunter-targets.png "skyhunter-targets")

-----

## Інтерфейс симулятора в SkyHunter

1. Клікаємо на мапі в тому місці, де хочемо створити дрон-перехоплювач, та натискаємо **Створити симулятор**. Процес може зайняти близько **2-x хвилин**.
![skyhunter-create-mission](/assets/skyhunter-create-mission.png "skyhunter-create-mission")
![skyhunter-mission](/assets/skyhunter-mission.png "skyhunter-mission")

2. **Прив'язуємо БПЛА до цілі**. Клікаємо на цілі та у списку обираємо наш БПЛА.
![skyhunter-define-target](/assets/skyhunter-define-target.png "skyhunter-define-target")

3. **Запуск місії**. Клікаємо на БПЛА та вибираємо пункт **«Почати місію»**.
![skyhunter-start-mission](/assets/skyhunter-start-mission.png "skyhunter-start-mission")

Після старта місіїї дрон-перехоплючач почне набирати висоту та полетить у бік цілі в автоматичному режимі.

