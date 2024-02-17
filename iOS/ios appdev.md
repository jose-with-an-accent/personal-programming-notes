- `tag`: numeric value, you can also use accessibility ids and other stuff
- Alert controller code:
```swift
let alertController = UIAlertController(title: title, message: message, preferredStyle: .alert);

let cancelAction = UIAlertAction(title: "OK", style: .cancel, handler: nil);

alertController.addAction(cancelAction);

present(alertController, animation: true, completion: nil);
```
- `uiControl`: convert the view into a `UiControl`, attach touch element into background
- `UiStackView`: simplifies making views a lot, think of it like a flexbox-style layout