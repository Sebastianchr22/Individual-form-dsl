# Individual-form-dsl

The following specification BNF will produce a valid web form the validates two properties:
  1. Name field has a input length >= 22 letters
  2. The age field input value is greater than or equal to 21


	form
	shortText 'Enter full name' length >= 10 + 10 / 5 + 20/2
	number 'Enter legal age' is >= 3+6*3


The way simpler option is still supported, where the following BNF will produce an identical form

	form
	shortText 'Enter full name' length >= 22
	number 'Enter legal age' is >= 21

Ofcause options are important and therefore the two options of hardcoding numbers for validation and computing math for input validation is supported.

The language now contains validation for properties not specified (or not possible) in the DSL
This means that one cannot write multiple 'optional' expressions for one input, and that multiple 'focus' expressions for a form gives a warning message.

Validation -> errors:
	A form must have atleast one input field specified
	An input field must have a name string
	An inputs name string must not be empty
	Multiple optional expressions for one input is not allowed
	
Validation -> warnings:
	An inputs name should start with a capital letter
	Multiple focus expressions will overwrite earlier focus expressions
