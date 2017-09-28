## Authentication
- Explain why each system fails (hacked), and how to guard against that failure when using the follwoing types of passwords:
- Commit with th comment "passwords"

- Plaintext passwords
	The reson why this sys will fail is: storing a plaintext password in a configuration file  allows anyone who can read the file access to the password-protected resource.
	So we have to find another way to protect our passwords than save them in a plantext file like:
	hash them or encrypted them.

- Encrypted passwords
	The reson why this sys will fail is : Encrypting is a proper (two way) function. It's reversible,
	so this unsafe functionality it's referring to is that if you encrypt the passwords, your application
	has the key stored somewhere and an attacker who gets access to your database (and/or code) can 
	get the original passwords by getting both the key and the encrypted text.
	So we have to use the hash way to improve our security.


- Hashed passwords
    This is the best way of these three, because this guards against the possibility that someone who 
    gains unauthorized access to the database can retrieve the passwords of every user in the system. 
    Hashing performs a one-way transformation on a password, turning the password into another String,
    called the hashed password. 'One-way' means that it is practically impossible to go the other way 
    to turn the hashed password back into the original password.
    And also it uses SALT, this makes the same password hash into a completely different string every time. To check if a password is correct, we need the salt, so it is usually stored in the user account database along with the hash, or as part of the hash string itself.

