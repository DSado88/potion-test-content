# Special Characters & Edge Cases

## HTML Entities

&amp; &lt; &gt; &quot; &apos; &copy; &reg; &trade;

## Raw HTML

<details>
<summary>Click to expand</summary>

This is hidden content inside a details/summary block.

- Item 1
- Item 2

</details>

<div style="color: red;">
This div has inline styles (should be sanitized or rendered).
</div>

<kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.

## Unicode

### Emoji
🎉 🚀 ✨ 🐛 🔥 💡 ⚡ 🎯 🔒 📊 🤖 🌺 🔵 🟢 🔴 ⭐

### International
日本語テスト (Japanese)
中文测试 (Chinese)
한국어 테스트 (Korean)
Тест на русском (Russian)
اختبار عربي (Arabic - RTL)
עברית בדיקה (Hebrew - RTL)

### Math Symbols
∑ ∏ ∫ ∂ ∇ √ ∞ ≈ ≠ ≤ ≥ ± × ÷ α β γ δ ε θ λ μ π σ φ ω

### Box Drawing
┌──────┬──────┐
│ Cell │ Cell │
├──────┼──────┤
│ Cell │ Cell │
└──────┴──────┘

## Escape Characters

\*not italic\*

\*\*not bold\*\*

\# not a heading

\- not a list

\[not a link\](https://example.com)

\`not code\`

## Zero-Width Characters

Here is a zero-width space: [​] (between the brackets)

Here is a zero-width non-joiner: [‌] (between the brackets)

## Very Long Word

Supercalifragilisticexpialidociousantidisestablishmentarianismelectroencephalographicallypneumonoultramicroscopicsilicovolcanoconiosis

## Consecutive Blank Lines




Three blank lines above (should collapse).
