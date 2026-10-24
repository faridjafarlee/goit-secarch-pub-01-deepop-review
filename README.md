# Наукова публікація 1: рев'ю DeepOP

Завдання: `../notes/tasks/pub1-spec.md` (300-500 слів, 5 розділів, Google Doc + PDF, дедлайн 4 Oct 23:45).

| Файл | Що це |
|---|---|
| `Джафарлі_Рев’ю_DeepOP_A_Hybrid_Framework.pdf` | PDF для прикріплення (2 стор. A4) |
| `Джафарлі_Рев’ю_DeepOP_A_Hybrid_Framework.docx` | Той самий текст. Завантажити в Google Drive, відкрити через «Відкрити в Google Docs», назвати `Джафарлі. Рев`ю “DeepOP: A Hybrid Framework”` і дати доступ «Усі, хто має посилання» |
| `content.js` | Єдине джерело тексту |
| `build_docx.js`, `build_html.js` | Збірка .docx і review.html, з якого друкується PDF |

Обсяг: 448 слів основного тексту в розділах, 475 разом із назвою, рядком автора і заголовками розділів. Це в межах 300-500.

Перезбірка:
```bash
NODE_PATH=<scratchpad>/docxjs/node_modules node build_docx.js
node build_html.js
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --user-data-dir="$(mktemp -d)" \
  --no-pdf-header-footer --print-to-pdf="Джафарлі_Рев’ю_DeepOP_A_Hybrid_Framework.pdf" "file://$PWD/review.html"
```
Headless Chrome записує PDF, але може не завершитися сам. Коли файл з'явився і перестав рости, процес треба зупинити.

Нічого не здано, подає користувач.
