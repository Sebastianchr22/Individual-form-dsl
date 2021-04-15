# Individual-form-dsl

The following specification BNF will produce a valid web form the validates two properties:
  1. Name field has a input length >= 22 letters
  2. The age field input value is greater than or equal to 21


  form
  shortText 'Enter full name' length >= 10 + 10 / 5 + 20/2
  number 'Enter legal age' is >= 3+6*3
