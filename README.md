# A2ATextField

[![CI Status](https://img.shields.io/travis/Ferrick90/A2ATextField.svg?style=flat)](https://travis-ci.org/Ferrick90/A2ATextField)
[![Version](https://img.shields.io/cocoapods/v/A2ATextField.svg?style=flat)](https://cocoapods.org/pods/A2ATextField)
[![License](https://img.shields.io/cocoapods/l/A2ATextField.svg?style=flat)](https://cocoapods.org/pods/A2ATextField)
[![Platform](https://img.shields.io/cocoapods/p/A2ATextField.svg?style=flat)](https://cocoapods.org/pods/A2ATextField)

A2ATextField class to float the Placeholder and validate the text while editing.

## Features
- [x] Floating effect in placeholder
- [x] Change border style to bottom line
- [x] Change placeholder active and inactive text color
- [x] Mandatory option
- [x] Change mandatory error text
- [x] Show error text
- [x] Validate the text while editing

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements

## Installation

A2ATextField is available through [CocoaPods](https://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'A2ATextField'
```

## How to use
####  Set placeholder
```
self.textField.placeholder = @"Name*"; // Default is nil
```

#### Change border style to bottom line
```
self.textField.bottomBorderOnly = YES; // Default is NO
```

#### Change the placeholder active color
```
self.textField.placeholderActiveColor = [UIColor colorWithRed:38/255.0 green:108/255.0 blue:194/255.0 alpha:1.0];
```

#### Change the placeholder inactive color
```
self.textField.placeholderInactiveColor = [[UIColor grayColor] colorWithAlphaComponent:0.7];
```

#### Set mandatory
```
self.textField.isMandatory = YES; // Default value is NO
```

#### Change mandatory error message
```
self.textField.mandatoryText = @"Please input a valid name"; // Default value is Error
```

#### Show error text
```
[self.textField errorMessage:@"Please input a valid name"];
```

#### Validate the text while editing
##### 1) Set delegate
```
self.textField.delegate = self;
```

##### 2) Set validationBlock
```
- (void) validationBlock:(UITextField *)textField {
	if (textField.text.length < 6 && textField.tag == 1) {
		[self.textField errorMessage:@"Passwords must be at least 8 characters in length"];
	}
}
```

## Author

Ferrick90, ferrick1990@hotmail.com

## License

A2ATextField is available under the MIT license. See the LICENSE file for more info.
