# YALLO Logo — Exact SVG Paths

## Complete Icon SVG (copy-paste ready)

```svg
<svg width="52" height="52" viewBox="0 0 300 300" fill="none" xmlns="http://www.w3.org/2000/svg">
  <!-- Top-left petal -->
  <path fill-rule="evenodd"
    d="M19.6,214.3c0-32.4,26.1-58.7,58.3-58.7h58.3v58.7c0,32.4-26.1,58.7-58.3,58.7s-58.3-26.3-58.3-58.7Z"
    fill="#D4A843"/>
  <!-- Top-right petal -->
  <path fill-rule="evenodd"
    d="M272.5,78.9c0,32.4-26.1,58.7-58.3,58.7h-58.3v-58.7c0-32.4,26.1-58.7,58.3-58.7s58.3,26.3,58.3,58.7Z"
    fill="#D4A843"/>
  <!-- Bottom-left petal -->
  <path fill-rule="evenodd"
    d="M19.6,78.9c0,32.4,26.1,58.7,58.3,58.7h58.3v-58.7c0-32.4-26.1-58.7-58.3-58.7s-58.3,26.3-58.3,58.7Z"
    fill="#D4A843"/>
  <!-- Bottom-right petal -->
  <path fill-rule="evenodd"
    d="M272.5,214.3c0-32.4-26.1-58.7-58.3-58.7h-58.3v58.7c0,32.4,26.1,58.7,58.3,58.7s58.3-26.3,58.3-58.7Z"
    fill="#D4A843"/>
</svg>
```

## The four path data strings (standalone, reusable)

```
TOP-LEFT:
M19.6,214.3c0-32.4,26.1-58.7,58.3-58.7h58.3v58.7c0,32.4-26.1,58.7-58.3,58.7s-58.3-26.3-58.3-58.7Z

TOP-RIGHT:
M272.5,78.9c0,32.4-26.1,58.7-58.3,58.7h-58.3v-58.7c0-32.4,26.1-58.7,58.3-58.7s58.3,26.3,58.3,58.7Z

BOTTOM-LEFT:
M19.6,78.9c0,32.4,26.1,58.7,58.3,58.7h58.3v-58.7c0-32.4-26.1-58.7-58.3-58.7s-58.3,26.3-58.3,58.7Z

BOTTOM-RIGHT:
M272.5,214.3c0-32.4-26.1-58.7-58.3-58.7h-58.3v58.7c0,32.4,26.1,58.7,58.3,58.7s58.3-26.3,58.3-58.7Z
```

## Size variants (change width/height only — keep viewBox unchanged)

| Size | Use |
|---|---|
| `width="10" height="10"` | Slide footer, email footer |
| `width="14" height="14"` | Email signature |
| `width="18" height="18"` | Compact nav, small badges |
| `width="20" height="20"` | Navigation bar |
| `width="22" height="22"` | Small horizontal lockup |
| `width="28" height="28"` | Business card back |
| `width="32" height="32"` | Standard lockup |
| `width="36" height="36"` | Logo variations grid |
| `width="40" height="40"` | Presentation content slide |
| `width="48" height="48"` | Presentation cover |
| `width="52" height="52"` | Standard large |
| `width="64" height="64"` | Banner/header |
| `width="72" height="72"` | Primary logo display |
| `width="80" height="80"` | Hero section |
| `width="98" height="98"` | Hero wordmark lockup |

Always keep: `viewBox="0 0 300 300"` — never change this.

## Colour variants (change `fill` on all 4 paths)

| Variant | Fill value |
|---|---|
| Gold (primary) | `fill="#D4A843"` |
| White reversed | `fill="#ffffff"` |
| Black on gold | `fill="#000000"` |
| Black on white | `fill="#111111"` |
| Greyscale | `fill="#666666"` or `fill="#777777"` |
| Disabled | `fill="#777777"` at `opacity="0.5"` |
| Watermark dark | `fill="#D4A843"` with parent `opacity="0.05"` |
| Watermark light | `fill="#000000"` with parent `opacity="0.04"` |

## Primary lockup HTML snippet (horizontal with GROUP)

```html
<div style="display:flex;align-items:center;gap:14px">
  <svg width="52" height="52" viewBox="0 0 300 300" fill="none">
    <path fill-rule="evenodd" d="M19.6,214.3c0-32.4,26.1-58.7,58.3-58.7h58.3v58.7c0,32.4-26.1,58.7-58.3,58.7s-58.3-26.3-58.3-58.7Z" fill="#D4A843"/>
    <path fill-rule="evenodd" d="M272.5,78.9c0,32.4-26.1,58.7-58.3,58.7h-58.3v-58.7c0-32.4,26.1-58.7,58.3-58.7s58.3,26.3,58.3,58.7Z" fill="#D4A843"/>
    <path fill-rule="evenodd" d="M19.6,78.9c0,32.4,26.1,58.7,58.3,58.7h58.3v-58.7c0-32.4-26.1-58.7-58.3-58.7s-58.3,26.3-58.3,58.7Z" fill="#D4A843"/>
    <path fill-rule="evenodd" d="M272.5,214.3c0-32.4-26.1-58.7-58.3-58.7h-58.3v58.7c0,32.4,26.1,58.7,58.3,58.7s58.3-26.3,58.3-58.7Z" fill="#D4A843"/>
  </svg>
  <div style="display:flex;flex-direction:column;align-items:flex-end">
    <div style="font-size:44px;font-weight:800;color:#ffffff;letter-spacing:-.5px;line-height:1;font-family:'Plus Jakarta Sans',sans-serif">YALLO</div>
    <div style="font-size:14px;color:#D4A843;letter-spacing:.22em;text-transform:uppercase;font-family:'DM Mono',monospace;margin-top:2px">GROUP</div>
  </div>
</div>
```

## Slide/presentation footer lockup

```html
<div style="display:flex;align-items:center;gap:6px">
  <svg width="10" height="10" viewBox="0 0 300 300" fill="none">
    <path fill-rule="evenodd" d="M19.6,214.3c0-32.4,26.1-58.7,58.3-58.7h58.3v58.7c0,32.4-26.1,58.7-58.3,58.7s-58.3-26.3-58.3-58.7Z" fill="#D4A843"/>
    <path fill-rule="evenodd" d="M272.5,78.9c0,32.4-26.1,58.7-58.3,58.7h-58.3v-58.7c0-32.4,26.1-58.7,58.3-58.7s58.3,26.3,58.3,58.7Z" fill="#D4A843"/>
    <path fill-rule="evenodd" d="M19.6,78.9c0,32.4,26.1,58.7,58.3,58.7h58.3v-58.7c0-32.4-26.1-58.7-58.3-58.7s-58.3,26.3-58.3,58.7Z" fill="#D4A843"/>
    <path fill-rule="evenodd" d="M272.5,214.3c0-32.4-26.1-58.7-58.3-58.7h-58.3v58.7c0,32.4,26.1,58.7,58.3,58.7s58.3-26.3,58.3-58.7Z" fill="#D4A843"/>
  </svg>
  <span style="font-size:9px;font-weight:800;color:#ffffff;font-family:'Plus Jakarta Sans',sans-serif">YALLO</span>
  <span style="font-size:7px;color:rgba(212,168,67,.5);font-family:'DM Mono',monospace">yallo.co</span>
</div>
```

## Large watermark (presentation/letterhead background)

```html
<div style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);opacity:0.05;pointer-events:none">
  <svg width="260" height="260" viewBox="0 0 300 300" fill="none">
    <path fill-rule="evenodd" d="M19.6,214.3c0-32.4,26.1-58.7,58.3-58.7h58.3v58.7c0,32.4-26.1,58.7-58.3,58.7s-58.3-26.3-58.3-58.7Z" fill="#D4A843"/>
    <path fill-rule="evenodd" d="M272.5,78.9c0,32.4-26.1,58.7-58.3,58.7h-58.3v-58.7c0-32.4,26.1-58.7,58.3-58.7s58.3,26.3,58.3,58.7Z" fill="#D4A843"/>
    <path fill-rule="evenodd" d="M19.6,78.9c0,32.4,26.1,58.7,58.3,58.7h58.3v-58.7c0-32.4-26.1-58.7-58.3-58.7s-58.3,26.3-58.3,58.7Z" fill="#D4A843"/>
    <path fill-rule="evenodd" d="M272.5,214.3c0-32.4-26.1-58.7-58.3-58.7h-58.3v58.7c0,32.4,26.1,58.7,58.3,58.7s58.3-26.3,58.3-58.7Z" fill="#D4A843"/>
  </svg>
</div>
```

## Tiled pattern (background texture)

```html
<div style="position:absolute;inset:0;opacity:.07;
  background-image:url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%2240%22 height=%2240%22 viewBox=%220 0 300 300%22><path fill-rule=%22evenodd%22 d=%22M19.6,214.3c0-32.4,26.1-58.7,58.3-58.7h58.3v58.7c0,32.4-26.1,58.7-58.3,58.7s-58.3-26.3-58.3-58.7Z%22 fill=%22%23D4A843%22/><path fill-rule=%22evenodd%22 d=%22M272.5,78.9c0,32.4-26.1,58.7-58.3,58.7h-58.3v-58.7c0-32.4,26.1-58.7,58.3-58.7s58.3,26.3,58.3,58.7Z%22 fill=%22%23D4A843%22/><path fill-rule=%22evenodd%22 d=%22M19.6,78.9c0,32.4,26.1,58.7,58.3,58.7h58.3v-58.7c0-32.4-26.1-58.7-58.3-58.7s-58.3,26.3-58.3,58.7Z%22 fill=%22%23D4A843%22/><path fill-rule=%22evenodd%22 d=%22M272.5,214.3c0-32.4-26.1-58.7-58.3-58.7h-58.3v58.7c0,32.4,26.1,58.7,58.3,58.7s58.3-26.3,58.3-58.7Z%22 fill=%22%23D4A843%22/></svg>');
  background-size:40px 40px">
</div>
```
