
## Content hugging priority & Content compression resistance priority
#### Content hugging priority
Setting a larger value to this priority indicates that we don’t want the view to grow larger than its content.

#### Content compression resistance priority
Setting a higher value means that we don’t want the view to shrink smaller than the intrinsic content size.

[link to the blog](https://medium.com/@abhimuralidharan/ios-content-hugging-and-content-compression-resistance-priorities-476fb5828ef)


## Cool way to declare constants

```swift
fileprivate extension String {
    static let const01 = "Howdy!"
    static let const02 = "Hello!"
}

nameLabel.text = .const01
```
## map for optional
```swift
extension Optional {
    func map<U>(transform: (Wrapped) -> U) -> U? {
        guard let value = self else { return nil }
        return transform(value) 
    }
}
```

## flatmap for optional
```swift
extension Optional {
    func flatMap<U>(transform: (Wrapped) -> U?) -> U? {
        if let value = self, let transformed = transform(value) { 
            return transformed
        }
        return nil
    } 
}
```
