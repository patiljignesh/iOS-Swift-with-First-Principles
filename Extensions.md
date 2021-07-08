# Extentions

## Example of UIButton Extension

```
extension UIButton {
    
    func makeCircular() {
        self.clipsToBounds = true
        self.layer.cornerRadius = self.frame.size.width / 2
    }
}

let button = UIButton(frame: CGRect(x: 0, y: 0, width: 50, height: 50))
button.backgroundColor = .red
button.makeCircular()

```

## Extension cab applied to prototocols as well
- Allows the protocol methods to be optional and not as required. 
