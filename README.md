# zxcvbn
A command-line implementation of the open-source zxcvbn password-strength tool

This command-line implemtation is written in perl, and uses 2 perl modules.  So you must have perl installed with modules:

- Data::Password::zxcvbn
- Data::Dumper

To install with Perl CPAN:

    sudo perl -MCPAN -e 'CPAN::Shell->force(qw(install Data::Password::zxcvbn))'
    sudo perl -MCPAN -e 'CPAN::Shell->force(qw(install Data::Dumper))'
    
Then, run this script.  Paste in your password, or pipe your password into it.

Option 1:

    ./zxcvbn
    # press enter, and type or paste your entire password. Press enter.
    # returns a score from 0 to 4, and estimated time to crack
    
Option 2:

    echo "my secret password" | ./zxcvbn
    # returns a score from 0 to 4, and estimated time to crack

Password comes from standard input (STDIN) because it can contain any character, including special characters that could break if done as a command-line argument.
