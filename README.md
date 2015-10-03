# jQuery Editable
Asynchronous jQuery in-place edit plugin

```js
$('.editable').editable('http://example.com/save.php');
```

## Sync

```js
$('.editable').editable(function(value) {
  return value;
});
```

## Custom AJAX call

```js
$('.editable').editable(function(value) {
  return $.post('http://example.com/save.php', { value: value });
});
```

## Custom promise

```js
$('.editable').editable(function(value) {
  var d = $.Deferred();
  setTimeout(function() {
    d.resolve(value);
  }, 2000);
  return d.promise();
});
```

## Callback styled

```js
$('.editable').editable(function(value, done) {
  setTimeout(function() {
    done(null, value);
  }, 2000);
});
```
