# assignment_7_databasesrepEmail


**Exercise 1**


First normal form - We found a violation which is caused by some of the columns being concated hence they are not in the single domain

Second normal form - There are no violations of the second normal form as all the columns seem to
be dependant on the primary key(customerNumber)

Third normal form - There are several occurances where the third normal form is broken:
		1) ```custCity``` depends on ```custZip``` and vice versa 
		2) ```repAddress``` depends on ```repCity```
		3) ```repName``` and ```repPhone``` depend on ```repEmail```


**Exercise 2**


We agreed upon having a composite key of ```customerName``` and ```repEmail``` as the new primary key. With this new composite key we get a violation of second normal form because ```custCity```,
```custZip```, ```custCountry``` don't depend on the ```repEmail``` part of the composite key
as well as ```repName```, ```repPhone```, ```repZip```, ```repCity```, ```repAddress```, ```repCountry``` don't depend on ```customerName``` part of the composite key.


**Exercise 3**


safe update statement:

```
Update CustomerOverview
Set contactPhone = 87654321, repPhone = 87654321
where contactPhone = 12345678, repPhone = 12345678
```

unsafe update statement:

```
Update CustomerOverview Set repPhone=87654321
```


**Exercise 4**


![alt text](https://raw.githubusercontent.com/lovrobiljeskovic/assignment_7_databases/master/assignment_7.png)

Comparing on the root level - Checking the three initial elements which are
D, E and G. Since "Handji Gifts& Co" Starts with the letter H, it is a value
which is higher than all three initial values we have at the root level so we create
a child node from the G element towards the right. That child node will hold all the letters which
come after G in the alphabet.
	




