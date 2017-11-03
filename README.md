<p align="center">
	<img src=".github/swift-style-guide-logo.png" alt="Rosberry Swift Style Guide" />
</p>

Based on [Ray Wenderlich Swift Style Guide](https://github.com/raywenderlich/swift-style-guide) with changes and additions. Make sure to read [Swift API Design Guidelines](https://swift.org/documentation/api-design-guidelines).

## Questions:

- [Use Type Inferred Context](https://github.com/raywenderlich/swift-style-guide#use-type-inferred-context)? В блоках как хотим, в проперти явно указываем тип, для цвета как хотим, в остальных случаях опускаем
- [Spacing](https://github.com/raywenderlich/swift-style-guide#spacing) - 4
- Elses on newline, except guard
- [Closure  anonymous arguments](https://github.com/raywenderlich/swift-style-guide#closure-expressions) - never
- [Extending object lifetime](https://github.com/raywenderlich/swift-style-guide#extending-object-lifetime) optional
- [Access Control](https://github.com/raywenderlich/swift-style-guide#access-control)  explicitly use `open`, `public`, and `internal`
- [Failing Guards](https://github.com/raywenderlich/swift-style-guide#failing-guards) - on newline
- 

## Our rules:
- `guard`, `set`, `get` body on newline

```swift
guard let token = token else {
    return
}
```
- Setting properties with lazy closures:

```swift
private lazy var tableView: UITableView = {
    let tableView = UITableView()
    tableView.tableFooterView = UIView()
    return tableView
}()
```
- Accessors order - `get set`

```swift
var name: String {
    get {
        return "unknown"
    }
    set {
        name = newValue
    }
}
```
- Deinit below init

```swift
init() {
    // initialization logic
}
	
deinit() {
    // deinitialization logic
}
```
- Names of actions in view controllers: `...buttonPressed`, `...viewTapped`

```swift
@objc private func nameButtonPressed() {
    // calling of view model events
}
```
- Names of actions in view models: `...EventTriggered`
 
```swift
func loginEventTriggered() {
    // event logic
}
```
- Closure naming - success/failure, completion, handler in other cases
- Enum cases on newline
 
```swift
enum Colors {
    case red
    case green
    case blue
}
```
- Nested types and type aliases should be at the top of classes.

## Links:
- [Swiftlint configuration file](https://github.com/rosberry/Foundation/blob/master/.swiftlint.yml) 
- [Github Swift Style Guide](https://github.com/github/swift-style-guide)
- [Linkedin Swift Style Guide](https://github.com/linkedin/swift-style-guide)

## About

<img src="https://github.com/rosberry/Foundation/blob/master/Assets/full_logo.png?raw=true" height="100" />

This project is owned and maintained by [Rosberry](http://rosberry.com). We build mobile apps for users worldwide 🌏.

Check out our [open source projects](https://github.com/rosberry), read [our blog](https://medium.com/@Rosberry) or give us a high-five on 🐦 [@rosberryapps](http://twitter.com/RosberryApps).

## License

Rosberry Swift Style Guide is available under the MIT license. See the LICENSE file for more info.
