The following language specification will produce a legal set of forms linked by name, with property validation via JS.
	
	form
	shortText 'Full name' length >= (4*6)-12 focus 
	number 'Age' is >= 3*2+18-6
	
	leadsTo
	form
	shortText 'Housemate name' focus
	number 'Housemate age' is >= 12+6
	longText 'Tell us what happened?'
	date 'When did the damage occur' optional  
	
	leadsTo
	form
	email 'Email address' optional
	number 'Telephone number' length == 8 focus 

The math expression are computed by recursive dispatch functions, these distribute the call to a suitable function.
The JS will navigate to another web page on submit of a form, this is what defines the "flow" feature of the DSL.
