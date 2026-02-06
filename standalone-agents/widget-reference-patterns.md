# Widget Reference Patterns — Production Standards

These patterns are extracted from production Uplimit widgets. The Widget Designer MUST follow these patterns exactly.

---

## 1. MANDATORY CSS VARIABLES

Every widget must include this EXACT color palette:

```css
:root {
    /* Neutral Color Scale - USE THESE EXACT VALUES */
    --color-neutral-50: #fafafa;
    --color-neutral-100: #f5f5f5;
    --color-neutral-200: #e5e5e5;
    --color-neutral-300: #d4d4d4;
    --color-neutral-400: #a3a3a3;
    --color-neutral-500: #737373;
    --color-neutral-600: #525252;
    --color-neutral-700: #404040;
    --color-neutral-800: #262626;
    --color-neutral-900: #171717;

    /* MANDATORY Accent Color - DO NOT CHANGE */
    --color-accent: #6b9085;
    --color-accent-light: #c0d1cd;

    /* Pastel Backgrounds (for cards, highlights) */
    --color-success: #c0d1cd;
    --color-turquoise: #bfe5e7;
    --color-sand: #f0ede0;
    --color-purple: #d5cae0;

    /* Border Radius */
    --border-radius: 8px;
    --border-radius-sm: 4px;
}
```

**CRITICAL:** Never use arbitrary grays like `#374151` or `#1f2937`. Always use the `--color-neutral-XXX` scale.

---

## 2. MANDATORY ACCESSIBILITY

### Focus Styles
```css
*:focus {
    outline: 2px solid #3182ce;
    outline-offset: 2px;
}
```

### Reduced Motion
```css
@media (prefers-reduced-motion: reduce) {
    * { transition: none !important; }
}
```

### ARIA Requirements
- `role="region"` with `aria-label` on main containers
- `aria-live="polite"` on result displays
- `role="img"` and `aria-label` on charts/canvas
- `tabindex="0"` on interactive non-button elements
- Keyboard handlers for Enter and Space on clickable divs

---

## 3. HORIZONTAL LAYOUT PATTERN

Simulators use two-column horizontal layout, NOT vertical stacking:

```css
.container { max-width: 900px; margin: 0 auto; }

.two-col {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
}

@media (max-width: 640px) {
    .two-col { grid-template-columns: 1fr; }
}
```

---

## 4. SPLASH SCREEN (Interactive Simulators ONLY)

Every Interactive Simulator MUST start with a splash screen:

```html
<div class="splash-screen" id="splash-screen">
    <div class="widget-badge">Interactive Simulator</div>
    <h1 class="widget-title">[Widget Name]</h1>
    <p class="widget-subtitle">[One-line description of what learner will explore]</p>

    <div class="splash-scenario">
        <div class="splash-scenario-label">Your Role</div>
        <p class="splash-scenario-text">You're a <strong>[role]</strong> evaluating [situation]. You'll [what they'll do] to see [what they'll learn].</p>
    </div>

    <div class="splash-simplifications">
        <div class="splash-simplifications-title">Before You Start: What This Model Simplifies</div>
        <div class="splash-simplifications-subtitle">These assumptions make the model explorable but less realistic:</div>
        <ul>
            <li><strong>[Simplification 1]:</strong> [Explanation]</li>
            <li><strong>[Simplification 2]:</strong> [Explanation]</li>
            <li><strong>[Simplification 3]:</strong> [Explanation]</li>
        </ul>
    </div>

    <p class="splash-disclaimer">The numbers are illustrative, not forecasts.</p>

    <button class="start-btn" id="start-btn">I Understand — Start Exploring</button>
    <p class="start-btn-hint">You can adjust all assumptions once inside the simulator.</p>
</div>

<div class="simulator-screen" id="simulator-screen" style="display: none;">
    <!-- Actual simulator content -->
</div>
```

### Splash Screen CSS
```css
.splash-screen { text-align: center; }

.splash-scenario {
    background: white;
    border: 1px solid var(--color-neutral-200);
    border-left: 3px solid var(--color-neutral-800);
    padding: 1.25rem;
    border-radius: var(--border-radius-sm);
    margin-bottom: 1.25rem;
    text-align: left;
}

.splash-scenario-label {
    font-size: 0.7rem;
    font-weight: 600;
    color: var(--color-neutral-500);
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin-bottom: 0.5rem;
}

.splash-simplifications {
    background: var(--color-neutral-100);
    border-radius: var(--border-radius-sm);
    padding: 1.25rem;
    margin-bottom: 1.5rem;
    text-align: left;
}

.start-btn {
    background: var(--color-neutral-800);
    color: white;
    border: none;
    padding: 0.875rem 2rem;
    font-size: 0.95rem;
    font-weight: 600;
    border-radius: var(--border-radius-sm);
    cursor: pointer;
}

.start-btn:hover { background: var(--color-neutral-700); }
```

### Splash Screen JavaScript
```javascript
document.getElementById('start-btn').addEventListener('click', () => {
    document.getElementById('splash-screen').style.display = 'none';
    document.getElementById('simulator-screen').style.display = 'block';
});
```

---

## 5. TOOLTIP PATTERN

Input labels should have explanatory tooltips:

```html
<div class="form-label">
    <span class="tooltip-wrapper">
        [Label Text]
        <span class="tooltip-icon" tabindex="0" role="button" aria-label="More info">?</span>
        <span class="tooltip-content">[Explanation of what this input means and why it matters]</span>
    </span>
    <span class="form-value" id="[id]-value">[Current Value]</span>
</div>
```

### Tooltip CSS
```css
.tooltip-wrapper {
    position: relative;
    display: inline-flex;
    align-items: center;
    gap: 0.25rem;
}

.tooltip-icon {
    width: 14px;
    height: 14px;
    border-radius: 50%;
    background: var(--color-neutral-300);
    color: var(--color-neutral-600);
    font-size: 0.65rem;
    font-weight: 700;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    cursor: help;
}

.tooltip-content {
    position: absolute;
    bottom: calc(100% + 8px);
    left: 50%;
    transform: translateX(-50%);
    background: var(--color-neutral-800);
    color: white;
    padding: 0.5rem 0.75rem;
    border-radius: var(--border-radius-sm);
    font-size: 0.75rem;
    width: 220px;
    text-align: left;
    opacity: 0;
    visibility: hidden;
    transition: opacity 0.2s;
    z-index: 100;
}

.tooltip-wrapper:hover .tooltip-content {
    opacity: 1;
    visibility: visible;
}
```

---

## 6. PRESET BUTTONS

Simulators should have named scenario presets:

```html
<div class="presets-row" role="group" aria-label="Load example scenario">
    <button class="preset-btn active" data-preset="scenario1">[Real Company/Scenario Name]</button>
    <button class="preset-btn" data-preset="scenario2">[Alternative Scenario]</button>
    <button class="preset-btn" data-preset="scenario3">[Third Option]</button>
</div>
```

### Preset CSS
```css
.presets-row {
    display: flex;
    gap: 0.5rem;
    flex-wrap: wrap;
    margin-bottom: 1rem;
    justify-content: center;
}

.preset-btn {
    background: var(--color-neutral-200);
    color: var(--color-neutral-700);
    border: none;
    border-radius: var(--border-radius-sm);
    padding: 0.375rem 0.75rem;
    font-size: 0.75rem;
    font-weight: 600;
    cursor: pointer;
}

.preset-btn:hover { background: var(--color-neutral-300); }
.preset-btn.active { background: var(--color-accent); color: white; }
```

---

## 7. DYNAMIC INSIGHT TEXT

Results should include a dynamic insight box with highlighted metrics:

```html
<div class="insight-box">
    <div class="insight-label">Strategic Insight</div>
    <div class="insight-text" id="insight-text"></div>
</div>
```

### Insight CSS
```css
.insight-box {
    background: white;
    border: 1px solid var(--color-neutral-200);
    border-left: 3px solid var(--color-accent);
    padding: 1rem;
    border-radius: var(--border-radius-sm);
}

.insight-label {
    font-size: 0.75rem;
    font-weight: 600;
    color: var(--color-accent);
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin-bottom: 0.5rem;
}

.insight-text {
    font-size: 0.85rem;
    color: var(--color-neutral-600);
    line-height: 1.6;
}

/* Inline highlighted metrics */
.insight-metric {
    display: inline-block;
    background: var(--color-neutral-100);
    padding: 0.125rem 0.375rem;
    border-radius: 2px;
    font-weight: 600;
    color: var(--color-neutral-800);
}

.insight-metric.insight-warning {
    background: #fef3c7;
    color: #92400e;
}

.insight-metric.insight-positive {
    background: var(--color-accent-light);
    color: #2d5a4e;
}
```

### Dynamic Insight JavaScript Pattern
```javascript
function updateInsight(data) {
    let text = '';

    if (condition1) {
        text = `<span class="insight-metric insight-warning">Warning message.</span> Explanation with <span class="insight-metric">$${value}</span> highlighted.`;
    } else if (condition2) {
        text = `<span class="insight-metric insight-positive">Positive outcome!</span> Details here.`;
    } else {
        text = `Neutral insight with <span class="insight-metric">${metric}</span> inline.`;
    }

    document.getElementById('insight-text').innerHTML = text;
}
```

---

## 8. CSV EXPORT (Not .txt!)

Export must produce actual CSV files:

```javascript
function exportCSV() {
    const rows = ['Column1,Column2,Column3,Column4'];

    data.forEach(d => {
        rows.push(`${d.field1},${d.field2},${d.field3},${d.field4}`);
    });

    const blob = new Blob([rows.join('\n')], { type: 'text/csv' });
    const a = document.createElement('a');
    a.href = URL.createObjectURL(blob);
    a.download = `${widgetName}-${Date.now()}.csv`;
    a.click();
}
```

---

## 9. LEARNING OUTCOMES WIDGET PATTERN

Learning Outcomes widgets use a specific two-column interactive pattern:

```html
<div class="outcomes-grid">
    <div class="outcomes-section">
        <h3>Week Learning Outcomes</h3>
        <div id="wlo-list">
            <!-- WLO cards generated by JS -->
        </div>
    </div>

    <div class="clo-section">
        <h3>Course Learning Outcomes</h3>
        <div id="clo-list">
            <!-- CLO cards, dimmed until WLO clicked -->
        </div>
    </div>
</div>

<div class="help-text">
    <p><strong>How to use:</strong> Click any week outcome to see how it connects to the broader course goals.</p>
</div>
```

Key behaviors:
- Click WLO card → highlights connected CLO cards
- Unselected CLOs are dimmed (opacity: 0.5)
- Selected WLO shows "Contributes to: CLO X, CLO Y" text
- Keyboard accessible (tabindex, Enter/Space handlers)

---

## 10. RESULT PANEL WITH LEFT ACCENT

```css
.results-panel {
    background: white;
    border: 1px solid var(--color-neutral-200);
    border-left: 3px solid var(--color-accent);
    border-radius: var(--border-radius-sm);
    padding: 1rem;
}

.result-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.5rem 0;
    border-bottom: 1px solid var(--color-neutral-100);
}

.result-value.positive { color: var(--color-accent); }
.result-value.negative { color: #b45555; }
```

---

## CHECKLIST BEFORE OUTPUTTING WIDGET

- [ ] Uses EXACT `--color-accent: #6b9085`
- [ ] Uses `--color-neutral-50` through `--color-neutral-900` scale
- [ ] Includes `prefers-reduced-motion` media query
- [ ] Includes focus styles (`outline: 2px solid #3182ce`)
- [ ] Interactive Simulator has splash screen with simplifications
- [ ] Horizontal two-column layout (not vertical)
- [ ] Tooltips on input labels
- [ ] Named preset buttons (not generic)
- [ ] Dynamic insight text with highlighted metrics
- [ ] CSV export (not .txt)
- [ ] No emojis anywhere
- [ ] All ARIA labels present
- [ ] Keyboard navigation works
