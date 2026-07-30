# GREMLIN — Performer Manual

Gremlin is a magic webapp. The spectator sees a toy: a small pixel gremlin
that finds a playing card. The performer controls the card.

> **CAUTION**
> This document shows the secret method. Do not let a spectator see this
> document. Do not open this document during a performance.

---

## 1. General

The app is one HTML file. It has no server calls and no assets. It operates
from a local file or from the web at `https://gremlin.oddpaq.com`.

The spectator sees this sequence:

1. A gremlin is selected.
2. A colour is selected.
3. **START** is pressed.
4. The gremlin walks, thinks, does a performance, and shows one playing card.

The gremlin choice and the colour choice look like customisation. They are
not. They are the secret input. They set the card.

Sound is on by default. Tap the speaker icon (bottom right) to set the sound
to off.

---

## 2. The secret input

### 2.1 The gremlin sets the suit

The picker shows 4 gremlins. Read them left to right. The order is CHaSeD.

| Position | Gremlin | Suit       |
| -------- | ------- | ---------- |
| 1        | Bramble | ♣ Clubs    |
| 2        | Pip     | ♥ Hearts   |
| 3        | Spike   | ♠ Spades   |
| 4        | Gem     | ♦ Diamonds |

### 2.2 The colour sets the value

The picker shows 12 swatches in a grid. Read them left to right, top to
bottom. The **RANDOM** button is the King.

| Column 1     | Column 2      | Column 3      | Column 4       |
| ------------ | ------------- | ------------- | -------------- |
| **A** red    | **2** orange  | **3** yellow  | **4** lime     |
| **5** green  | **6** teal    | **7** sky     | **8** blue     |
| **9** violet | **10** lavender | **J** pink  | **Q** brown    |

> **NOTE**
> For the King, the gremlin gets a random colour on stage. The value is
> always King.

---

## 3. Do a performance

Do the steps that follow:

1. Get the identity of the force card. Use a glimpse, a peek, or a deck in
   Si Stebbins order.
2. Open the app.
3. Tap the gremlin that agrees with the suit. Tap **CONFIRM**.
4. Tap the swatch that agrees with the value. Tap **CONFIRM**.
5. If you want to, give the phone to the spectator.
6. Press **START**.
7. The gremlin does a performance and shows the force card.

After the reveal, the gremlin refuses more performances. The refusal
continues after **BACK** and a new selection. This is a safety. The
spectator cannot make the app do the reveal again.

---

## 4. The repeat reveal (the secret gesture)

The secret gesture permits one more reveal. The new card is the next card
in the Si Stebbins stack. Do the steps that follow:

1. Push and hold one finger on the screen for approximately 0.7 seconds.
   The position of the finger is not important.
2. Look at the info button (bottom left). When the "i" symbol goes out of
   view, the gesture is armed.
3. Lift the finger. The "i" symbol comes back. The app stays armed.
4. Press **AGAIN** (or **START**). The gremlin shows the next card.

The next card obeys the stack rule: value +3, next suit in CHaSeD order
(♣ → ♥ → ♠ → ♦).

Example chain: 4♥ → 7♠ → 10♦ → K♣ → 3♥ → …

> **NOTE**
> The armed state is used one time. After each reveal, the app locks
> again. Do the gesture again for each new reveal.

> **NOTE**
> Do not move the finger during the hold. Movement cancels the gesture.
> A long press on a button is safe. The button does not operate.

> **NOTE**
> After **BACK**, a new gremlin and colour change only the look. The stack
> chain continues from the last card shown. To start a new chain, do a
> refresh of the page.

---

## 5. The URL force

You can put the first card and the first performance in the URL. The app
removes the parameters from the address bar immediately, before the page
shows. The spectator cannot see them.

| You want                    | URL                                          |
| --------------------------- | -------------------------------------------- |
| Force the card              | `https://gremlin.oddpaq.com/?card=4H`        |
| Force the card and the show | `https://gremlin.oddpaq.com/?card=4H&v=3`    |
| Set only the show           | `https://gremlin.oddpaq.com/?v=3`            |

### 5.1 The card code

The code is the value and then the suit letter. The case is not important.

- Values: `A`, `2` … `10` (`T` is also permitted), `J`, `Q`, `K`
- Suits: `C`, `H`, `S`, `D`
- Examples: `4H` = 4♥ · `QS` = Q♠ · `10D` and `TD` = 10♦

When a URL card is set, the picker choices do not change the card. The
spectator can select each gremlin and each colour freely. The reveal shows
the URL card.

### 5.2 The show code (`v`)

The `v` parameter looks like a version number. It is not. It selects the
performance for the first reveal.

| `v` | Performance  | The spectator sees                                      |
| --- | ------------ | ------------------------------------------------------- |
| 1   | Conjure      | Magic charge. The card turns in and flips face up.      |
| 2   | Pull         | Magic charge. The card comes up out of the glow.        |
| 3   | Deck         | "Aha!" — runs off, comes back with a deck on its head, riffles it, tosses it. The card bursts out. |
| 4   | Sneeze       | Nose twitch, large inhale, ACHOO. The card flies out and flutters down. |
| 5   | Falling star | The magic goes up into the sky. A star falls back. The catch shows the card. |

Each performance is approximately 11 to 13 seconds.

> **NOTE**
> The URL force applies to the first reveal only. Reveals unlocked with
> the secret gesture use the stack rule and a random performance.

> **NOTE**
> An incorrect code is ignored. The app then operates as usual.

> **NOTE**
> A refresh removes the force. To force again, open the full URL again.
> A bookmark, a QR code, or a home-screen shortcut keeps the URL ready.

---

## 6. The cheat sheet

Tap the footer text 3 times quickly. A performer panel opens. It shows:

- The suit and value maps.
- The gesture and URL reminders.
- The armed line. `Armed:` shows the card of the next reveal. `Hold to
  arm:` shows the next stack card when the app is locked.

Close the panel before you give the phone to the spectator.

---

## 7. States and resets

| Action                        | Effect                                        |
| ----------------------------- | --------------------------------------------- |
| **START** (first time)        | Reveal. Then the app locks.                   |
| **AGAIN** without the gesture | The gremlin refuses ("No more!").             |
| **BACK**                      | Selection screens. The lock stays on.         |
| Long press                    | The app is armed for one reveal.              |
| Page refresh                  | Full reset. Chain, lock, and URL force clear. |

---

## 8. Troubleshooting

| Condition                        | Possible cause                       | Action                                   |
| -------------------------------- | ------------------------------------ | ---------------------------------------- |
| The gremlin always refuses       | The gesture was not armed            | Do the long press. Then press **AGAIN**. |
| The "i" symbol does not go away  | The hold was too short, or the finger moved | Hold for a full second. Keep the finger stationary. |
| The URL card did not show        | Incorrect code, or a reveal already occurred | Check the code. Open the full URL again. |
| The shown value is wrong by one  | Colour read in the wrong order       | Read the swatches left to right, top to bottom. |
| No sound                         | The mute is on, or the browser blocks audio | Tap the speaker icon. Tap the screen one time. |
