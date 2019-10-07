# knConstraints
This is my own Auto layout functions. I tried some libs before and found TinyConstraint from Robert-Hein Hooijmans (https://github.com/roberthein/TinyConstraints). It's really exciting and sweet. Learnt from his code and tried my own one. Now, here it is. 

## Why KNConstraints? 
- Short syntax
- Easily and quickly understand

## Example

### Fill a view to other view
**Old way**

```
    orangeView.topAnchor.constraint(equalTo: view.topAnchor, constant: 68).isActive = true
    orangeView.leftAnchor.constraint(equalTo: view.leftAnchor, constant: 68).isActive = true
    orangeView.rightAnchor.constraint(equalTo: view.rightAnchor, constant: -68).isActive = true
    orangeView.bottomAnchor.constraint(equalTo: view.bottomAnchor, constant: -68).isActive = true
```

**Old way**

```
    orangeView.fill(toView: view, space: UIEdgeInsets(space: 68))
```
or 

```
    orangeView.horizontal(toView: view, space: 68)
    orangeView.vertical(toView: view, space: 68)
```

### Align a view to left/right/top/bottom to other view
**Old way**

```
    yellowView.bottomAnchor.constraint(equalTo: view.bottomAnchor, constant: -8)
    yellowView.rightAnchor.constraint(equalTo: view.rightAnchor, constant: -8)
```
**Old way**
```
    yellowView.bottom(toView: view, space: -8)
    yellowView.right(toView: view, space: -8)
```
**Easier way**
```
    yellowView.bottomLeft(toView: view, bottom: -8, left: -8)
```

### Size 
**Old way**
```
    redView.widthAnchor.constraint(equalToConstant: 100).isActive = true
    redView.heightAnchor.constraint(equalToConstant: 100).isActive = true
```
**Old way**
```
    redView.height(100)
    redView.width(100)
```
**Easier way**
```
    redView.size(CGSize(width: 100, height: 100))
```
or 
```	
    redView.square(edge: 100)
```
### Stack views 
Stack views but don't want to use UIStackView, try this

```
stackHorizontally(views: [orangeView, redView], viewSpaces: 4, leftSpace: 16, rightSpace: nil)
```

`rightSpace` is nil that means the `redView's rightAnchor` is free (not set to the superview)

The `orangeView` has `leftAnchor` align to `superview's leftAnchor` with 16px spacing. 

## Suggestions or feedback?

Feel free to create a pull request, open an issue
