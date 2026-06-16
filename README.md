<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./Assets/banner.png">
    <img src="./Assets/banner.png" alt="Banner">
  </picture>
</p>

<div id="header" align="center">
  <div id="badges">
    <img alt="GitHub License" src="https://img.shields.io/github/license/yourusername/voice-assistant?style=for-the-badge">
    <img alt="GitHub watchers" src="https://img.shields.io/github/watchers/yourusername/voice-assistant?style=for-the-badge">
    <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/yourusername/voice-assistant?style=for-the-badge">
  </div>
</div>

<h1> Описание </h1>
<p>
Голосовой помощник для Windows с открытой архитектурой. Работает полностью локально, без интернета. 
Распознаёт речь с помощью Whisper Small, понимает команды через DistilBERT (дообучен на 250 интентов), 
отвечает синтезированной речью через VITS Lite. Управляет файлами, окнами и системными настройками 
через WinAPI и COM-интерфейсы.
</p>

<h1> Ключевые особенности </h1>
<ul>
  <li><b>Полностью локальная работа</b> — не требует интернета, данные не покидают ваш компьютер</li>
  <li><b>Глубокое управление системой</b> — открывает папки, управляет окнами, меняет настройки</li>
  <li><b>Открытая архитектура</b> — любой разработчик может добавить свои команды</li>
  <li><b>Простота для новичков</b> — команды на естественном языке, голосовые подсказки</li>
</ul>

<h1> Технологии </h1>
<ul>
  <li><a href="https://github.com/openai/whisper">Whisper Small</a> — распознавание речи</li>
  <li><a href="https://huggingface.co/docs/transformers/index">DistilBERT</a> — понимание интентов (дообучен на 250 классов)</li>
  <li><a href="https://github.com/jaywalnut310/vits">VITS Lite</a> — синтез речи</li>
  <li>WinAPI / COM — интеграция с операционной системой Windows</li>
</ul>

<h1> Скриншоты приложения </h1>
<picture>
    <img width="816" height="446" alt="image" src="https://github.com/user-attachments/assets/dd5d8bf8-22e0-461f-b6e5-c4870074f7db" />

</picture>

<h1> Голосовые команды </h1>
<p>
Активация ассистента происходит автоматически — он постоянно слушает микрофон и ждёт команды.
</p>

<h2> Что он может: </h2>

<h3> Запускать приложения: </h3>
<ul>
    <li><code>Открой браузер</code> — Запускает Google Chrome</li>
    <li><code>Открой Яндекс Музыку</code> — Открывает приложение Яндекс Музыка</li>
    <li><code>Открой ВКонтакте</code> — Открывает сайт ВКонтакте в браузере</li>
</ul>

<h3> Управлять системой: </h3>
<ul>
    <li><code>Сделай громче</code> — Увеличивает громкость на 5%</li>
    <li><code>Сделай тише</code> — Уменьшает громкость на 5%</li>
    <li><code>Покажи мои документы</code> — Открывает папку «Документы»</li>
    <li><code>Поставь на паузу</code> — Ставит текущий медиаплеер на паузу</li>
    <li><code>Помощь</code> — Зачитывает список доступных команд</li>
</ul>

<h1> Установка </h1>

<h3> 1. Клонирование репозитория </h3>
<pre><code>git clone https://github.com/yourusername/voice-assistant.git
cd voice-assistant</code></pre>

<h3> 2. Создание и активация виртуального окружения </h3>
<pre><code>python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # macOS/Linux</code></pre>

<h3> 3. Установка зависимостей </h3>
<pre><code>pip install -r requirements.txt</code></pre>

<h3> 4. Запуск </h3>
<pre><code>python main.py</code></pre>

<h1> Добавление своей команды </h1>
<p>
Откройте файл <code>intents.py</code>, напишите функцию-обработчик и добавьте её в словарь <code>INTENT_HANDLERS</code>:
</p>

<pre><code>def execute_my_command(command_text: str) -> str:
    # Ваш код здесь
    return "Команда выполнена"

INTENT_HANDLERS = {
    12: execute_my_command,  # 12 — номер вашего интента
}</code></pre>

<h1> Системные требования </h1>
<ul>
  <li>Python 3.8 или новее</li>
  <li>Windows 10 или Windows 11</li>
  <li>Микрофон (рекомендуется USB-микрофон)</li>
  <li>Видеокарта NVIDIA (опционально, для ускорения)</li>
</ul>

<h1> Лицензия </h1>
<p>
Проект распространяется под лицензией MIT. Вы можете свободно использовать, модифицировать и распространять код.
</p>

<h1> Связаться со мной </h1>
<ul>
  <li>Telegram: @bozuko</li>
</ul>

<i>В проекте используются иконки с сайта <a href="https://icons8.ru/">Icons8.ru</a></i>
