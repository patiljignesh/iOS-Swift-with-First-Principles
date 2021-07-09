# Basic Animation 
## Using String and code

```
	titleLabel.text = ""
	let titleText = "⚡️FlashChat"
	var charIndex = 0.0
	for letter in titleText {
		Timer.scheduledTimer(withTimeInterval: 0.1 * charIndex, repeats: false) { timer in
			self.titleLabel.text?.append(letter)
		}
		charIndex += 1
	}
	// charIndex is to create 0.1, 0.2, 0.3, ... for every character
```
