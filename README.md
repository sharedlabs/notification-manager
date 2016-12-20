# notification-manager

A notification manager used to create notifications to be shown to the user.

### How it works

Append the <notify-manager> element anywhere in the dom.
By default it will listen to all notify events up to the document.

```html
<notify-manager></notify-manager>
```

Then in the javascript you can dispatch notify events.

```js
const notifyEvent = new CustomEvent('notify-error', {
  bubbles: true,
  detail: {
    text: 'Error message',
    duration: Infinity
  }
});

this.dispatchEvent(notifyEvent);
```

### Events listen

`notify-error`
`notify-warning`
`notify-info`
`notify-success`