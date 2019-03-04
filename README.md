# Vue CLI with PWA using a CDN

Began with `vue create demo` and chose defaults (with PWA plugin).

Added `vue.config.js` with a URL for publicPath.

```
module.exports = {
  publicPath: process.env.NODE_ENV === 'production'
    ? 'https://cdn.example.com/'
    : '/',
}
```

Then run `npm run build`.

I'd like a way to produce the index.html with all assets on the CDN URL. Except, I'd like to link with /manifest.json (or /path/manifest.json).
