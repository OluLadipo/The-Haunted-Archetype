[README (5).md](https://github.com/user-attachments/files/34596672/README.5.md)
# The Haunted Archetype

Six spirits are waiting. One of them already knows your name.

### 🔮 [Draw your card](https://the-haunted-archetype.netlify.app/)

*8 questions. 2 minutes. Zero data saved.*

---

## The deck

Answer on instinct and the cards deal you one of six:

**I. The Haunted Strategist**
**II. The Chaos Witch**
**III. The Phantom Creative**
**IV. The Final Girl**
**V. The Midnight Oracle**
**VI. The Mad Scientist**

Which one you are stays face down until you play.

## What you walk away with

- **Your tarot card,** dealt with your archetype's sigil and a one-line tagline that's a little too accurate
- **Your reading,** the version of you that shows up when the lights cut out
- **Signature strengths,** three of them
- **Your AI ritual,** how your archetype actually uses AI
- **A copy button,** so you can drop your result in the group chat and make everyone else take it

It went around the office before. Some people liked their card so much they had AI paint a portrait of their archetype.

## Behind the scenes

A few crumbs from the code. The rest stays in the deck.

**Every answer feeds two spirits.** Your first pick gets 2 points, and a second archetype gets 1:

```js
const [, p, s] = QUESTIONS[qi].o[ai];
pts[p] += 2; prim[p] += 1; pts[s] += 1;
```

**Ties never break randomly.** Same answers, same card, every time:

```js
const TIEBREAK = ["F","M","P","W","O","S"];
```

So if you and a friend tie, look at that list and see who got lucky.

**The ambience is made live.** Wind, slow chords and little bells with an echo, all generated in your browser with the Web Audio API. It stays off until you turn it on.

```js
const CHORDS = [[45,57,60,64,67],[41,53,57,60,64],[43,55,59,62,67],[40,52,55,59,64]]; // Am7 Fmaj7 G Em7
```

All eight questions, the full readings and what each AI ritual says... you'll have to draw.

## Built with

One HTML file. Vanilla JavaScript, CSS, hand-drawn SVG sigils and the Web Audio API. No frameworks, no audio files, no build step. Nothing you answer is stored or sent anywhere.

## Made by

**Olu Ladipo**
I wrote the concept, questions and scoring, then used AI tools to prototype and build it.
[Portfolio](https://oluladportfolio.netlify.app/) · [LinkedIn](https://www.linkedin.com/in/oluladipoinsights)

*These archetypes are playful fiction, not a psychological assessment.*

### 🔮 [The cards are waiting](https://the-haunted-archetype.netlify.app/)
