# LibertuSQL
C/C++ database and memory manager

<strong style="color:red; font-size: 24px;">THIS PROJECT IS PUT ON HOLD AD VITAM AETERNAM BECAUSE MOST OF ITS SOURCE CODE HAVE BEEN LOST, AND BECAUSE I DEPRECATED IT IN FAVOR OF ANOTHER DATABASE PROJECT WHICH MAY NOT BE MADE AVAILABLE AS AN OPEN SOURCE PROJECT !</strong>

Distribution of the source code will be done exactly when it will be done and not a second before. For now I'll provide information about the software:

## Memory Management

You will be able to manage an *Object-Oriented* on disk memory system. It will be basic bu will allow you to easily modify huge bunches of data that won't fit in the RAM.

The syntax will look like this:

	FSRAM mem = new FSRAM(); // Initializes the storage directory
	STORAGE* ipstorage = mem.new("ip",1); // Creates the collection of IP v4 adresses
	ipstorage->set(0,192,168,1,15); // Stores the adress 192.168.1.15
	ipstorage->renew("ip",2); // Resizes the collection to fit another IP
	ipstorage->set(1,8,8,8,8); // Stores the IP 8.8.8.8 after the first IP
	DH row = ipstorage->dh(0); // Creates a DataHandler (which is between the pointer and the cursor)
	printf("%i",(int)row.field(1)); // Prints 168
	row.next(); // Go to the second row
	printf("%i",(int)row.field(1)); // Prints 8
	
## Database

TODO
