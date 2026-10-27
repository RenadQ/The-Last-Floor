# 👻 The Last Floor

A mobile horror-maze game built with **React Native (Expo)**. You are trapped in a haunted building and must escape floor by floor, dodging ghosts, collecting coins and power-ups, and riding the elevator up to the last floor.

> Team project for **CS 526: Mobile Application Programming**, Imam Abdulrahman Bin Faisal University (IAU).
> Project lead: **Renad Alkahtani**

<p align="center">
  <img src="src/assets/splash-icon.png" width="160" alt="The Last Floor icon">
</p>

---

## 🎮 Gameplay

- **Escape the maze:** each floor is a maze with its own theme, and ghosts patrol their own zones. Cross into a ghost's zone and it will alert, then chase you.
- **Survive with hearts:** you start with 3 hearts, and bandages can raise the maximum to 5.
- **Use power-ups:** freeze guns stop ghosts, push charges knock them back, and a sprint boost (double-tap) lasts 30 seconds.
- **Dark Mode + microphone:** the lights randomly go out. If microphone mode is on and you make a loud noise, nearby ghosts hear you and rush to your position.
- **Panic Mode:** stay on a floor too long and extra ghosts appear.
- **Elevator questions:** answer a riddle in the elevator to earn bonus coins on the way up.
- **Progress:** coins, achievements, character skins, a player profile and stats are saved on the device.

## 📱 Screens

Intro video → Home (hub) → Profile & name setup → Character selection → Achievements → Settings → Rules → Floors (maze) → Elevator transition → Win / Defeat

The full UI/UX design, with every screen, the navigation flow and the style guide, is in [`docs/cs526_milestone2_ui_ux_design.pdf`](docs/cs526_milestone2_ui_ux_design.pdf).

## 🛠️ Tech stack

| Area | Used |
|---|---|
| Framework | React Native + Expo SDK 54 |
| Navigation | React Navigation (native stack) |
| State | React Context |
| Storage | AsyncStorage (profile, coins, stats, achievements) |
| Media | `expo-av` (intro video, ambience, ghost sounds, microphone) |
| Graphics | `react-native-svg` |
| Device | `expo-location`, `expo-screen-orientation`, vibration |

## 📁 Project structure

```
.
├── App.js                    # App entry: context provider + navigation
├── index.js                  # Registers the root component with Expo
├── app.json                  # Expo config (name, icons, splash)
├── package.json
├── babel.config.js
├── src/
│   ├── navigation/
│   │   └── AppNavigator.js   # Game, Achievements and Settings screens
│   ├── context/
│   │   └── GameContext.js    # Shared session state
│   ├── screens/
│   │   └── GameScreen.js     # Main game: maze, ghosts, power-ups, UI
│   ├── utils/
│   │   ├── storage.js        # AsyncStorage keys and helpers
│   │   └── questions.js      # Elevator riddles
│   ├── components/
│   ├── styles/
│   └── assets/               # Characters, ghosts, items, icons, intro video
└── docs/
    └── cs526_milestone2_ui_ux_design.pdf
```

## ▶️ How to run

```bash
git clone https://github.com/RenadQ/The-Last-Floor.git
cd The-Last-Floor
npm install
npx expo start
```

Then scan the QR code with the **Expo Go** app on your phone, or press `a` for an Android emulator or `i` for the iOS simulator.

---

<details>
<summary>🇸🇦 ملخص بالعربي</summary>

**The Last Floor** لعبة رعب للجوال مبنية بـ React Native (Expo). اللاعب محبوس في مبنى مسكون ولازم يهرب دور بعد دور، يتفادى الأشباح ويجمع العملات والقدرات (التجميد، الدفع، السرعة)، ويطلع بالمصعد لين يوصل آخر دور.

من مميزاتها: وضع الظلام مع المايكروفون، اللي فيه الأشباح تسمع صوتك وتلحقك. ووضع الذعر لو طوّلت في الدور. وأسئلة المصعد اللي تعطيك عملات إضافية. وكمان الإنجازات والشخصيات، وحفظ التقدم على الجهاز.

مشروع مادة CS 526 برمجة تطبيقات الجوال، جامعة الإمام عبدالرحمن بن فيصل.
</details>
