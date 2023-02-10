# Referring-to-enum-cases-with-associated-values-as-closures

Just like you can refer to a Swift function as a closure, you can do the same thing with enum cases with associated values:

```swift
import Foundation

enum UnboxPath {
    case key(String)
    case keyPath(String)
}

struct UserSchema {
    static let name = key("name")
    static let age = key("age")
    static let posts = key("posts")
    
    // Closure
    private static let key = UnboxPath.key
}

print(UserSchema.name) // key("name")

```
