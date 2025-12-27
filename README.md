# Orpheus Theme Template

A starter template for creating [Orpheus](https://github.com/collectif-pixel/orpheus) themes.

## Quick Start

1. Use this template to create your theme repository
2. Customize `theme.html` with your design
3. Update `package.json` with your theme info
4. Push to GitHub as `your-username/your-theme-name`

## Installation

```bash
orpheus add @your-username/your-theme-name
orpheus use @your-username/your-theme-name
```

## API

Your theme receives track data via Server-Sent Events:

```javascript
// Connect to SSE stream
const eventSource = new EventSource('/api/stream');

eventSource.addEventListener('track', (event) => {
  const track = JSON.parse(event.data);
  // track.title    - Song title
  // track.artist   - Artist name
  // track.album    - Album name (optional)
  // track.coverUrl - Album artwork URL (optional)
  // track.playing  - Boolean, true if playing
});
```

## Structure

```
your-theme/
├── package.json    # Theme metadata
├── theme.html      # Your theme (required)
└── README.md       # Documentation
```

## License

MIT
