# emotion-design-tokens

**A open source design token system for emotionally-aware interfaces.**

Emotion is one of the strongest drivers of human memory, decision-making, and experience — yet most digital design systems treat it as decoration rather than structure. `emotion-design-tokens` is a research-grounded dataset that maps human emotional states to concrete, usable design tokens: color, typography, animation, sound texture, haptic pattern, and cross-cultural context.

Built by a UX researcher as part of an HCI thesis at NYU Tisch, and expanded as an open source resource for designers and developers building interfaces that respond to how people actually feel.

---

## What's inside

Each emotion entry contains:

| Field | Description |
|---|---|
| `emotion` | The emotional state |
| `color_hex` | Primary color in HEX |
| `color_rgb` | Primary color in RGB |
| `design_token` | CSS variable name (e.g. `emotion-joy`) |
| `valence` | Positive / negative / mixed |
| `arousal` | High / medium / low |
| `ux_context` | When to use this emotion in a product |
| `associated_interactions` | Motion and interaction patterns |
| `typography` | Weight, style, and reasoning |
| `animation` | Timing, easing, movement, duration |
| `sound_texture` | Qualitative description of sonic character |
| `haptic_pattern` | Vibration pattern description |
| `cultural_notes` | How this emotion's color varies across cultures |

---

## Emotions included

| Emotion | Token | Color |
|---|---|---|
| Joy | `emotion-joy` | `#F6C443` |
| Calm | `emotion-calm` | `#7ECEC1` |
| Love | `emotion-love` | `#E88B9C` |
| Wonder | `emotion-wonder` | `#D4A76A` |
| Melancholy | `emotion-melancholy` | `#8BA4C4` |
| Nostalgia | `emotion-nostalgia` | `#C4A1D7` |
| Awe | `emotion-awe` | `#4A6FA5` |
| Grief | `emotion-grief` | `#5A5A6E` |
| Pride | `emotion-pride` | `#C0392B` |
| Anxiety | `emotion-anxiety` | `#E8A87C` |
| Contentment | `emotion-contentment` | `#A8C5A0` |
| Longing | `emotion-longing` | `#B0A8C8` |

---

## How to use it

### As a JSON dataset

```js
fetch('data/emotion-tokens.json')
  .then(res => res.json())
  .then(tokens => {
    const joy = tokens.find(t => t.emotion === 'Joy');
    console.log(joy.color_hex); // #F6C443
    console.log(joy.animation.duration_ms); // 300
  });
```

### As CSS variables

```css
:root {
  --emotion-joy: #F6C443;
  --emotion-calm: #7ECEC1;
  --emotion-love: #E88B9C;
  --emotion-wonder: #D4A76A;
  --emotion-melancholy: #8BA4C4;
  --emotion-nostalgia: #C4A1D7;
  --emotion-awe: #4A6FA5;
  --emotion-grief: #5A5A6E;
  --emotion-pride: #C0392B;
  --emotion-anxiety: #E8A87C;
  --emotion-contentment: #A8C5A0;
  --emotion-longing: #B0A8C8;
}
```

### In a design system

Use `design_token` as your variable name, `ux_context` to decide when to apply each emotion, and `animation` fields to drive motion design decisions.

---

## Research background

This dataset is grounded in:

- **Baddeley (2000)** — Episodic memory as multisensory and emotionally encoded
- **Norman (2004)** — Emotional design: visceral, behavioural, and reflective levels
- **Hassenzahl (2010)** — Experience-centred design and hedonic quality
- **Gayler et al. (2022)** — Multisensory UX and memory recall at CHI
- **Russell (1980)** — Circumplex model of affect (valence × arousal axes)

The original 6-emotion dataset was contributed to [dariusk/corpora](https://github.com/dariusk/corpora/pull/440) in April 2026. This repository expands that work into a full design token system.

---

## How to contribute

Contributions are welcome! You can:

- **Add a new emotion** — follow the existing JSON structure exactly
- **Improve cultural notes** — especially for cultures underrepresented in the current dataset
- **Add usage examples** — code snippets, p5.js sketches, React components
- **Translate the README** — into other languages

Please open a Pull Request with your changes and a brief description of what you added and why.

---

## License

MIT License — free to use, modify, and distribute with attribution.

See [LICENSE](LICENSE) for full terms.

---

## Author

**Rajeshwari Ranjeet Kotwal**
HCI Master's Student, NYU Tisch ITP
[behance.net/rajeshwkotwal1](https://behance.net/rajeshwkotwal1)

*Memora thesis project — designing emotional memory through multisensory interaction.*
