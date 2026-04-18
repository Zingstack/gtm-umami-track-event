# Umami Analytics - Track Event

A Google Tag Manager tag template for sending custom events to [Umami Analytics](https://umami.is).

> Built by [Zingstack](https://zingstack.com) · Not an official Umami product

---

## Requirements

- Umami Analytics installed on your website (v2.0.0 or later)
- The Umami tracker script must be loaded **before** this tag fires

## Installation

1. Download `template.tpl`
2. In GTM go to **Templates** → **Tag Templates** → **New**
3. Click `···` → **Import**
4. Select the `template.tpl` file
5. Save the template

## Usage

Create a new tag using the **Umami Analytics - Track Event** template:

| Field | Required | Description |
|-------|----------|-------------|
| Event name | ✓ | The event name shown in your Umami dashboard (e.g. `cta_click`) |
| Properties | — | Optional key/value pairs sent with the event |

### Example

| Key | Value |
|-----|-------|
| `location` | `pricing_hero` |
| `label` | `Get started` |

## Recommended Setup

Use the dataLayer to send events from your website scripts:

```javascript
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: 'cta_click',
  cta_location: 'pricing_hero',
  cta_label: 'Get started'
});
```

Then in GTM create a Custom Event trigger for `cta_click` and map the dataLayer variables to the Properties table.

## Related Templates

- [Umami Analytics - Identify](https://github.com/Zingstack/gtm-umami-identify)

## License

Apache 2.0
