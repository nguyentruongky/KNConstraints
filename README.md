# knConstraints
This is my own Auto layout lib. I tried some libs before and found TinyConstraint from Robert-Hein Hooijmans (https://github.com/roberthein/TinyConstraints). It's really exciting and sweet. I learnt from his code and tried my own lib. Now, here it is. 

## Why knConstraints? 
- Short syntax
- Easily and quickly understand
## Example

### Fill 
Old way

	orangeView.topAnchor.constraint(equalTo: view.topAnchor, constant: 68).isActive = true
    orangeView.leftAnchor.constraint(equalTo: view.leftAnchor, constant: 68).isActive = true
    orangeView.rightAnchor.constraint(equalTo: view.rightAnchor, constant: -68).isActive = true
    orangeView.bottomAnchor.constraint(equalTo: view.bottomAnchor, constant: -68).isActive = true

New way 

	orangeView.fill(toView: view, space: UIEdgeInsets(space: 68))

or 

	orangeView.horizontal(toView: view, space: 68)
    orangeView.vertical(toView: view, space: 68)

### Side 
Old way 

	yellowView.bottomAnchor.constraint(equalTo: view.bottomAnchor, constant: -8)
    yellowView.rightAnchor.constraint(equalTo: view.rightAnchor, constant: -8)

New way 

	yellowView.bottom(toView: view, space: -8)
	yellowView.right(toView: view, space: -8)

Easier way

	yellowView.bottomLeft(toView: view, bottom: -8, left: -8)

### Size 
Old way 

	redView.widthAnchor.constraint(equalToConstant: 100).isActive = true
    redView.heightAnchor.constraint(equalToConstant: 100).isActive = true

New way

	redView.height(100)
    redView.width(100)

More easier ways: 

	redView.size(CGSize(width: 100, height: 100))

or 
	
	redView.square(edge: 100)
  
## Suggestions or feedback?

Feel free to create a pull request, open an issue
