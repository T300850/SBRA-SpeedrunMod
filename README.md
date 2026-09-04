# SchoolboyMod (SchoolBoy Runaway) — Speedrun Mod

<div align="center">

# 🏁 SchoolBoy Runaway — Speedrun Mod

### v2.0.0

**A speedrunning & practice toolkit for _SchoolBoy Runaway_ (Linked Squad)**

[![Platform](https://img.shields.io/badge/Platform-Unity-black?logo=unity)](https://unity.com/)
[![Loader](https://img.shields.io/badge/Loader-MelonLoader-orange)](https://melonwiki.xyz/)
[![Version](https://img.shields.io/badge/Version-2.0.0-blue)]()
[![License](https://img.shields.io/badge/License-Unofficial%20Mod-lightgrey)]()

**Made by:** `TL12 Mods`

</div>

---

## 🌐 Language / Язык

- [🇬🇧 English](#-english)
- [🇷🇺 Русский](#-русский)

---

<a name="-english"></a>
## 🇬🇧 ENGLISH

A modification for **SchoolBoy Runaway** created for **speedrunning, practice, and run analysis**.

| | |
|---|---|
| **Made by** | TL12 Mods |
| **Platform / Loader** | [MelonLoader](https://melonwiki.xyz/) (Unity) |
| **Mod Version** | 2.0.0 |

---

## 📥 Installation

1. Install **MelonLoader** into the game directory.
2. Put `SchoolboyMod.dll` into:  
   `...\SchoolBoy Runaway\Mods\`
3. Launch the game.

Logs: `...\MelonLoader\Latest.log`

---

## ⌨️ Hotkeys (Binds)

Default binds (can be changed in the mod menu):

| Key | Action |
|:---:|:---|
| `F1` | Open / close overlay menu |
| `F2` | Restart run (calls `GameManager.RestartGame()`) |
| `F3` | Toggle **LowFPS** mode (5–15 FPS) |

✅ Rebind is available in **General** tab.  
Allowed keys: `A–Z`, `0–9`, `F1–F12` (Escape/Enter are blocked).

---

## 🖥️ On-Screen HUD

**⏱️ Speedrun Timer** *(top center)*  
Shows run time `HH:MM:SS.mmm`.  
Uses a “main GameTimer filter” so **mini-games (PC timer)** do not pause/reset the speedrun timer.

**📊 Item Splits Notifications** *(left side)*  
When you pick an item, it shows a quick split line and compares to PB:
- First time / New PB / Behind PB (delta)

**🎮 Input Overlay** *(bottom right)*  
Displays keyboard (`WASD`, `Shift`, `Space`) and mouse buttons (LMB/RMB).

**✍️ Watermark** *(bottom left)*  
`by TL12 Mods`

---

## 🗂️ Mod Menu Tabs (`F1`)

### 1️⃣ General
- FPS limiter (slider)
- LowFPS value input **(5–15)** + toggle via hotkey
- Speedrun info
- Keybind rebind (F1/F2/F3 by default)

### 2️⃣ Items
- PB list for item pickups
- Clear item PB records

### 3️⃣ Endings
**All Endings Challenge**
- RTA (real time)
- IGT (sum) — uses **actual run times**, not your historical PBs
- Checklist:
  - `Belt`, `GateA`, `GateB`, `Roof`, `Door`, `Drowned`, `Cheat`, `Bug`
- Restart challenge / reset progress

**PB (single-run best times)**
- Shows PB per ending and allows clearing PB records

### 4️⃣ Location
- Spawn/randomization presets (some require restart with `F2`)

### 5️⃣ Code
- Custom 4-digit code mode (optional)
- **Important:** code is applied only to the **Control_Panel** CodeLock to avoid affecting other locks.

---

## 💾 Saves / Files

**MelonPreferences** (settings, binds, PB endings):  
`...\UserData\MelonPreferences.cfg` (category: `SchoolboyMod`)

**Persistent mod files** (`Application.persistentDataPath/SchoolboyMod/`):
- `itemsplits.txt` — PB splits by items
- `endings_challenge.txt` — All Endings Challenge progress + IGT per ending

---

## ⚙️ Technical Notes

### ✅ Main GameTimer Filtering
The game has extra timers (e.g. PC/mini-games).  
The mod captures the “main” game timer from `GameManager.gameTimer` and ignores other `GameTimer` instances so your run timer is stable.

### 🔐 Why custom code can affect other locks (game behavior)
In the original game, CodeLock saves password using:
`PlayerPrefs.SetString(saveName + "_password", password)`  
If `saveName` is empty, the key becomes `"_password"` (global).  
This mod prevents side effects by applying the custom code only to **Control_Panel**.

---

<a name="-русский"></a>
## 🇷🇺 РУССКИЙ

Модификация для **SchoolBoy Runaway**, созданная для **спидрана, тренировок и анализа забегов**.

| | |
|---|---|
| **Сделано** | TL12 Mods |
| **Платформа / Загрузчик** | [MelonLoader](https://melonwiki.xyz/) (Unity) |
| **Версия мода** | 2.0.0 |

---

## 📥 Установка

1. Установите **MelonLoader** в папку игры.
2. Поместите `SchoolboyMod.dll` в:  
   `...\SchoolBoy Runaway\Mods\`
3. Запустите игру.

Логи: `...\MelonLoader\Latest.log`

---

## ⌨️ Горячие клавиши (Binds)

Бинды по умолчанию (можно изменить в меню):

| Клавиша | Действие |
|:---:|:---|
| `F1` | Открыть / закрыть оверлей |
| `F2` | Рестарт забега (вызывает `GameManager.RestartGame()`) |
| `F3` | Вкл/Выкл **LowFPS** (5–15 FPS) |

✅ Ребинд доступен во вкладке **Общее**.  
Разрешены: `A–Z`, `0–9`, `F1–F12` (Escape/Enter запрещены).

---

## 🖥️ HUD (на экране)

**⏱️ Таймер спидрана** *(сверху по центру)*  
Формат `ЧЧ:ММ:СС.мс`.  
Есть защита от “левых таймеров” (например таймеров мини-игр в ПК), чтобы они **не останавливали** спидран-таймер.

**📊 Уведомления сплитов по предметам** *(слева)*  
При подборе предмета показывает сплит и сравнение с PB.

**🎮 Оверлей ввода** *(справа внизу)*  
Показывает `WASD`, `Shift`, `Space`, ЛКМ/ПКМ.

**✍️ Водяной знак** *(слева внизу)*  
`by TL12 Mods`

---

## 🗂️ Вкладки меню (`F1`)

### 1️⃣ Общее
- Лимитер FPS
- LowFPS 5–15 + переключение горячей клавишей
- Информация по спидрану
- Ребинд клавиш (F1/F2/F3)

### 2️⃣ Предметы
- PB по предметам
- Сброс PB по предметам

### 3️⃣ Концовки
**Челлендж “Все концовки”**
- RTA
- IGT (сумма) — считается по реальным времени забегов, а не по старым PB
- Чеклист:
  - `Belt`, `GateA`, `GateB`, `Roof`, `Door`, `Drowned`, `Cheat`, `Bug`
- Сброс челленджа

**PB (лучшее время одиночного забега)**
- Отображение PB по каждой концовке + кнопка очистки

### 4️⃣ Расположение
- Пресеты случайного спавна/вариаций (для применения иногда нужен рестарт `F2`)

### 5️⃣ Код
- Режим “свой код” (4 цифры)
- Код применяется **только к `Control_Panel`**, чтобы не менять другие замки.

---

## 💾 Сохранения / файлы

**Настройки MelonPreferences (включая бинды и PB концовок):**  
`...\UserData\MelonPreferences.cfg` (категория: `SchoolboyMod`)

**Файлы мода** (`Application.persistentDataPath/SchoolboyMod/`):
- `itemsplits.txt` — PB по предметам
- `endings_challenge.txt` — прогресс челленджа + IGT по концовкам

---

## ⚙️ Технические детали

### ✅ Фильтрация главного таймера
В игре есть дополнительные таймеры (например в ПК/мини-играх).  
Мод фиксирует “главный” таймер из `GameManager.gameTimer` и игнорирует остальные, чтобы спидран-таймер не ломался.

### 🔐 Почему код мог менять другие замки (поведение игры)
В игре `CodeLock` сохраняет пароль как:
`PlayerPrefs.SetString(saveName + "_password", password)`  
Если `saveName` пустой, ключ становится `"_password"` (общий).  
Мод избегает побочек: применяет кастомный код только к `Control_Panel`.

---

<div align="center">

### 💬 Feedback & Support

Found a bug or have a suggestion? Contact TL12 Mods.  
Нашли баг или есть предложение? Свяжитесь с TL12 Mods.

---

**Made by TL12 Mods**

*This is an unofficial fan-made modification. Not affiliated with Linked Squad.*  
*Это неофициальная модификация, созданная фанатами. Не связана с Linked Squad.*

</div>
