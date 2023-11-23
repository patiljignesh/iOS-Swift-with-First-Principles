# Auto Layout

## Three known types

1. Interface Builder
2. Using Visual Format Language
3. Anchors

## Summary 
- Create user interfaces that automatically adjust size and position based on the screen size and orientation.
- Stack views are a convenient way to manage a collection of views in either horizontal or vertical stacks, reducing the complexity of constraints.
- Not all constraints are equal. You can set priority levels to dictate which constraints should be considered more important if conflicts arise.
- Dynamic Layout:
  - Auto Layout can adjust to different screen sizes and orientations, making your app look good on any device.
- Size Classes:
  - These allow for more granular control, enabling different layouts for different device types (like compact width on an iPhone vs. regular width on an iPad).
  - 

Auto Layout in UIKit is a system that allows developers to create flexible and responsive user interfaces for iOS apps. It uses constraints to define relationships between UI elements, making the layout adapt to different screen sizes and orientations. Here’s an explanation from simple to complex concepts:

Simple Concepts

	1.	Constraints: The basic building blocks of Auto Layout. They define the size and position of UI elements relative to each other or to their parent views.
	•	Types of Constraints: Include constraints for size (width and height), position (leading, trailing, top, bottom), and relationships (equal width, aspect ratio).
	•	Creating Constraints: Can be done in Interface Builder (a visual tool in Xcode) or programmatically in Swift.
	2.	Interface Builder: Allows visually setting up constraints, making it easier to design UIs without writing code. You can control-drag between elements to create constraints and edit their properties in the inspector panel.
	3.	Stack Views: Simplify layout by arranging views in a linear stack, either horizontally or vertically. You add views to the stack and define the stack’s properties, and it manages the layout of its children.

Intermediate Concepts

	1.	Priority: Constraints have priorities ranging from 1 to 1000. Higher priority constraints are satisfied first. This is useful when constraints might conflict under certain conditions.
	2.	Content Hugging and Compression Resistance:
	•	Content Hugging: Determines how closely a view should fit to its content. Higher values mean the view prefers to be as close to its content size as possible.
	•	Compression Resistance: Indicates how strongly a view resists being made smaller than its intrinsic content size.
	3.	Intrinsic Content Size: Some views have a natural size based on their content (like a button’s size based on its title). Auto Layout uses this to determine appropriate sizes.

Advanced Concepts

	1.	Dynamic Layouts: Auto Layout works with dynamic content, like table views with variable row heights. Constraints can be recalculated as content changes.
	2.	Animating Constraints: You can animate the changes in constraints to create smooth transitions in the layout.
	3.	Safe Area and Layout Guides:
	•	Safe Area: Ensures content is not obscured by notches, status bars, or other interface elements.
	•	Layout Guides: Objects that represent a space in a view. Useful for managing spacing without adding invisible views.
	4.	Programmatic Constraint Creation: Writing constraints in code using NSLayoutConstraint or layout anchors provides more control and dynamic capabilities.
	5.	Debugging Auto Layout: Xcode provides tools to debug Auto Layout issues, like conflicting or unsatisfied constraints. The console logs and Xcode’s visual debugging tools are invaluable here.

Complex Scenarios

	•	Nested Stack Views: Using stack views within stack views can create complex UIs with less effort.
	•	Responsive Design: Using size classes and trait collections to create different layouts for various device types and orientations.
	•	Custom Constraints: Creating your own NSLayoutConstraint subclasses for custom layout behaviors.

Auto Layout is powerful but can be complex. It’s important to start with simple layouts and progressively tackle more advanced features as you become comfortable.

###### References
1. https://www.raywenderlich.com/811496-auto-layout-tutorial-in-ios-getting-started
2. https://uxdesign.cc/the-why-what-and-how-of-swift-auto-layout-9530a60eedf4
