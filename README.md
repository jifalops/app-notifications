[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/jifalops/app-notifications)

# app-notifications
Web component for using the notifications API.

## Installation
```
bower install --save app-notifications
```

## Usage
* Give it an `id` and call the `show()` method.
* Pass event handlers to `show()` or as attributes like `on-show="..."`.

## Demo
<!--
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="app-notifications.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->

```html
<app-notifications id="notifications"></app-notifications>
Title:<br/>
<input id="title" value="title"/><br/>
Options:<br/>
<textarea id="options" rows="3" cols="30">
{"tag": "app", "body": "body", "icon": "icon.png"}
</textarea><br/>
Duration (ms):<br/>
<input id="duration" value="0"/><br/>
<button onclick="_showNotification();">Show Notification</button>
Last event: <span id="feedback"></span>
<script>
  var notifications = document.getElementById('notifications');
  var title = document.getElementById('title');
  var options = document.getElementById('options');
  var duration = document.getElementById('duration');
  var feedback = document.getElementById('feedback');
  _showNotification = function() {
    notifications.show(
      title.value,
      JSON.parse(options.value),
      duration.value,
      function(e, n) { feedback.innerHTML = 'Notification shown'; },
      function(e, n) { feedback.innerHTML = 'Notification clicked'; },
      function(e, n) { feedback.innerHTML = 'Notification closed'; },
      function(e, n) { feedback.innerHTML = 'Notification error'; });
  }
</script>
```

Full demo:
[webcomponents.org](https://www.webcomponents.org/element/jifalops/app-notifications/demo/demo/index.html)
| [github](https://jifalops.github.io/app-notifications/components/app-notifications/demo/).

API: [webcomponents.org](https://www.webcomponents.org/element/jifalops/app-notifications/app-notifications)
| [github](https://jifalops.github.io/app-notifications).

## Contributing

1. Fork it on Github.
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## License

[MIT](https://opensource.org/licenses/MIT)
