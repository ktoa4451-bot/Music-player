# Music Player (Fabric 1.21.11)

Клиентский мод: красивый музыкальный плеер на кастомном GUI. Клавиша **M**.

## Сборка
1. Нужна **JDK 21** (`java -version` -> 21).
2. Gradle wrapper (бинарный jar) в архив не входит. Самый надёжный путь:
   - сгенерируй шаблон на https://fabricmc.net/develop/template (Minecraft 1.21.11, Yarn, без datagen/split sources, Java 21);
   - скопируй из этого архива в шаблон: `src/` (целиком), `build.gradle`, `gradle.properties`, `settings.gradle` (с заменой);
   - либо просто положи в эту папку `gradlew`, `gradlew.bat`, `gradle/` из шаблона.
3. `./gradlew build` (Windows: `gradlew.bat build`). Мод: `build/libs/music-player-1.0.0.jar`.
4. Тест в IDE: `./gradlew runClient`.

Версии Fabric Loader / Fabric API / Yarn при необходимости обнови в `gradle.properties` по https://fabricmc.net/develop

## Установка
`music-player-1.0.0.jar` + Fabric API в `.minecraft/mods`.

## Использование
- Папка: `.minecraft/config/music-player/music/` (создаётся сама). Форматы: **MP3, WAV, AIFF, AU**.
- Имя файла `Исполнитель - Название.mp3` -> исполнитель и название определятся автоматически.
- **M** открыть/закрыть, **Space** пауза, **← →** трек, **↑ ↓** громкость, **R** обновить список, колесо — прокрутка / громкость.
- Конфиг: `config/music-player/config.json` (последний трек и громкость).

## Сборка без установки (через GitHub, можно с планшета)
1. Создай репозиторий на github.com и загрузи в него содержимое этого архива (включая папку `.github`).
2. Вкладка **Actions** -> workflow **build** -> дождись зелёной галочки.
3. Внутри запуска скачай артефакт **music-player-jar** — это готовый `.jar`.
