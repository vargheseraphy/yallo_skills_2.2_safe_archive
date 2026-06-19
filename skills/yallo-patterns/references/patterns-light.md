# YALLO Light Patterns — CSS Reference
Use on: #FFFFFF, #F9F9F7, #F4F4F2 surfaces (print, letterhead, proposals).

---

## Pattern G — Fine grid (light)
Black lines · 24px cell · 5% opacity · Letterhead, formal proposals, A4 print
```css
.pattern-g {
  background-image:
    linear-gradient(rgba(0,0,0,.05) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0,0,0,.05) 1px, transparent 1px);
  background-size: 24px 24px;
}
```

White base variant:
```css
.pattern-g-white {
  background-color: #ffffff;
  background-image:
    linear-gradient(rgba(0,0,0,.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0,0,0,.04) 1px, transparent 1px);
  background-size: 24px 24px;
}
```

Large 44px variant for full A4 page:
```css
.pattern-g-large {
  background-image:
    linear-gradient(rgba(0,0,0,.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0,0,0,.04) 1px, transparent 1px);
  background-size: 44px 44px;
}
```

---

## Pattern H — Dot grid (light)
Black dot matrix · 20px · 12% dot opacity · Proposals, client reports
```css
.pattern-h {
  background-image: radial-gradient(
    circle, rgba(0,0,0,.12) 1px, transparent 1px
  );
  background-size: 20px 20px;
}
```

Off-white base variant:
```css
.pattern-h-offwhite {
  background-color: #f4f4f2;
  background-image: radial-gradient(
    circle, rgba(0,0,0,.10) 1px, transparent 1px
  );
  background-size: 20px 20px;
}
```

Subtle 8% variant for busy layouts:
```css
.pattern-h-subtle {
  background-image: radial-gradient(
    circle, rgba(0,0,0,.08) 1px, transparent 1px
  );
  background-size: 24px 24px;
}
```

---

## Pattern I — Gold glow (light)
Subtle gold radial corner accent · 8% · Print letterhead, formal documents
```css
/* Bottom-right corner (default) */
.pattern-i {
  background-image: radial-gradient(
    ellipse 80% 60% at 100% 100%, rgba(212,168,67,.08) 0%, transparent 60%
  );
}
```

Top-left corner variant:
```css
.pattern-i-topleft {
  background-image: radial-gradient(
    ellipse 60% 50% at 0% 0%, rgba(212,168,67,.07) 0%, transparent 55%
  );
}
```

Dual corner — top-right + bottom-left:
```css
.pattern-i-dual {
  background-image:
    radial-gradient(ellipse 50% 50% at 100% 0%, rgba(212,168,67,.06) 0%, transparent 55%),
    radial-gradient(ellipse 50% 50% at 0% 100%, rgba(212,168,67,.06) 0%, transparent 55%);
}
```

---

## Pattern J — Large watermark (light)
Single YALLO icon · centred · 4% black opacity · Letterhead body, formal A4 docs
```css
.pattern-j-wrapper { position: relative; }
.pattern-j-icon {
  position: absolute;
  inset: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0.04;
  pointer-events: none;
}
/* Place the YALLO SVG icon inside .pattern-j-icon at width="60%" height="60%" */
/* Icon fill: #000000 for light backgrounds */
```
