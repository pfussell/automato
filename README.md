### automato.rb

automato uses native LDAP libraries to automate the collection and enumeration of various directory objects. This is incredibly useful during an internal penetration test.

automato can also conduct password spraying attacks, and identify if a user is a local administrator against any number of systems.

By adding the ability to cycle through a list of target servers we can do things like conduct password guessing against AD without tripping alarms. 

If you provide automato credentails it will compare the users bad password count against the provided lockout threshold. 

Output files are automatically created for evidence preservation.

#### Usage
~~~
$ ruby automato.rb
automato v2.0
Written by: Sanjiv Kawa
Twitter: @kawabungah

Commands:
  automato.rb all                                          # Run the most popular features. (computers, users, groups, priv, attributes)
  automato.rb attr                                         # Get the account attributes for all domain users.
  automato.rb bad                                          # Get the bad password count for all domain users.
  automato.rb computers                                    # Get all domain computers.
  automato.rb groups                                       # Get all domain groups.
  automato.rb help [COMMAND]                               # Describe available commands or one specific command
  automato.rb laps                                         # Get the laps password for systems in the network
  automato.rb localadmin DOMAIN USERNAME PASSWORD IP_FILE  # Identify if a user is a local admin against a list of IP's with SMB open
  automato.rb member GROUP                                 # List all users in a supplied domain GROUP.
  automato.rb priv                                         # Recurse through administrative groups and get users from all nested groups.
  automato.rb spray USER_FILE PASSWORD                     # Conduct a password spraying attack against the domain using a USER_FILE and common PASSWORD
  automato.rb user USER                                    # Get the group memberships for a supplied USER
  automato.rb users                                        # Get all domain users.

$
~~~

