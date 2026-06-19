# YALLO Dark Patterns — CSS Reference
Use on: #000000, #111111, #1F1F1F surfaces only.

---

## Pattern A — Petal tile
Icon tiled · 40px · 7% opacity · Social posts, presentations
```css
/* Recommended: use ::before pseudo-element so opacity doesn't affect content */
.pattern-a-wrapper { position: relative; }
.pattern-a-wrapper::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url('pattern-A-petal-tile.svg');
  background-size: 40px 40px;
  background-repeat: repeat;
  opacity: 0.07;
  pointer-events: none;
}
```

---

## Pattern B — Fine grid
Horizontal + vertical gold lines · 24px cell · 4% opacity · All dark surfaces
```css
.pattern-b {
  background-image:
    linear-gradient(rgba(212,168,67,.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(212,168,67,.04) 1px, transparent 1px);
  background-size: 24px 24px;
}
```

Larger 44px variant for full-page backgrounds:
```css
.pattern-b-large {
  background-image:
    linear-gradient(rgba(212,168,67,.025) 1px, transparent 1px),
    linear-gradient(90deg, rgba(212,168,67,.025) 1px, transparent 1px);
  background-size: 44px 44px;
}
```

---

## Pattern C — Gradient glow
Dual radial gold glow · 20%/8% · Hero sections, cover slides only
```css
.pattern-c {
  background-image:
    radial-gradient(ellipse 100% 80% at 0% 100%, rgba(212,168,67,.20) 0%, transparent 55%),
    radial-gradient(ellipse 60% 60% at 100% 0%, rgba(212,168,67,.08) 0%, transparent 55%);
}
```

Centre glow variant:
```css
.pattern-c-centre {
  background-image:
    radial-gradient(ellipse 80% 60% at 50% 50%, rgba(212,168,67,.12) 0%, transparent 60%);
}
```

Corner only — subtle:
```css
.pattern-c-corner {
  background-image:
    radial-gradient(ellipse 50% 50% at 0% 100%, rgba(212,168,67,.15) 0%, transparent 55%);
}
```

---

## Pattern D — Diagonal lines (architectural/technical)
45° lines · 20px spacing · 3% opacity · CTO/CIO context
```css
.pattern-d {
  background-image: repeating-linear-gradient(
    45deg,
    rgba(212,168,67,.03) 0px,
    rgba(212,168,67,.03) 1px,
    transparent 1px,
    transparent 20px
  );
  background-size: 20px 20px;
}
```

Tight 12px variant:
```css
.pattern-d-tight {
  background-image: repeating-linear-gradient(
    45deg,
    rgba(212,168,67,.025) 0px,
    rgba(212,168,67,.025) 1px,
    transparent 1px,
    transparent 12px
  );
  background-size: 12px 12px;
}
```

---

## Pattern E — Dot grid (dark)
Gold dot matrix · 20px spacing · 18% dot opacity · Precision/data context
```css
.pattern-e {
  background-image: radial-gradient(
    circle, rgba(212,168,67,.18) 1px, transparent 1px
  );
  background-size: 20px 20px;
}
```

Subtle variant · 10% dot · 24px:
```css
.pattern-e-subtle {
  background-image: radial-gradient(
    circle, rgba(212,168,67,.10) 1px, transparent 1px
  );
  background-size: 24px 24px;
}
```

---

## Pattern F — Large watermark (dark)
Single oversized YALLO icon · centred · 5% opacity · Letterhead digital, covers
```css
.pattern-f-wrapper { position: relative; }
.pattern-f-icon {
  position: absolute;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0.05;
  pointer-events: none;
}
/* Place the YALLO SVG icon inside .pattern-f-icon at width="60%" height="60%" */
/* Icon fill: #D4A843 */
```
