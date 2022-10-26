# Revolt Desktop (but better)

literally just adds a "url" option to the config.json for custom clients

exactly the same as the original, go read their readme

edit config.json found in AppData/Roaming/revolt-desktop or whatever OS you're using

add "url": "https://example.com" to the config file json

adds a `customOpener` config option, its a string containing JSON to use for opening URLs in custom ways

`{$}` will be replaced with the url

example:

```js
window.native.set(
    "customOpener",
    JSON.stringify({ file: "/path/to/firefox", args: ["-new-tab", "{$}"] }),
);
```

also adds an isMaximized check `window.native.isMaximized()` to test if the window is maximized
