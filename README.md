# Widgets

HTML/CSS/JS embed widgets for Hostinger drag-and-drop sites (silvea.tech).
Each file in `widgets/` is one self-contained block. Paste the entire file into a Hostinger **Embed code** element.

## Demo

`demo.html` previews every widget in its own frame, with a 380px phone toggle and copy buttons.
It loads the widget files with `fetch`, so run it from a local server:

```sh
python3 -m http.server 8000
# open http://localhost:8000/demo.html
```

## Widgets

| File | Prefix | What it does | Before going live |
| --- | --- | --- | --- |
| `widgets/plan-finder.html` | `spq-` | Quiz that recommends a service and links to its intake form | Check the URLs in `SPQ_PLANS` |
| `widgets/plan-compare.html` | `scp-` | Basic vs Advanced website plan table | Keep in sync with `Web-inquiry.html` |
| `widgets/process-timeline.html` | `stl-` | Six-step project process, inquiry to handoff | Check the CTA URL |
| `widgets/faq-accordion.html` | `sfq-` | FAQ with FAQPage JSON-LD | Keep the JSON-LD in sync with the visible answers |
| `widgets/quick-contact.html` | `scq-` | Web3Forms contact form | Replace `YOUR_WEB3FORMS_ACCESS_KEY` |
| `widgets/domain-ideas.html` | `sdn-` | Domain name idea generator | Check `SDN_REQUEST_URL` |
| `widgets/before-after.html` | `sba-` | Before/after redesign slider | Replace the placeholder illustrations with real screenshots |

Existing full-page forms: `Web-inquiry.html`, `dev-inquiry.html`, `ticket.html`.

## Conventions

- Every class and custom property is namespaced with the widget's prefix.
- No background on the outer wrapper; widgets inherit the section background.
- Internal links are absolute URLs with `target="_top"` (embeds render in an iframe).
- Animations stop under `prefers-reduced-motion`.
- No headings or section titles inside a widget; add those with Hostinger's own text elements.
