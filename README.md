# Logic Parser
A simple CLI parser and evaluator for boolean expressions, written in C99.
Prints the truth table of arbitrary propositional propositional formulas to your terminal.

### Syntax
##### Operators
| Operator | Syntax |
| -- | -- |
| TRUE | 1 |
| FALSE | 0 |
| NEGATION | ! |
| AND | && |
| OR | \|\| |
| IMPLICATION | -> |
| EQUIVALENCE | = |

With precedence as the table suggests.
Note that the implication operator is right associative, but for clarity's sake it is best not to rely on that and use parenthesis instead.

##### Variables
The program can handle up to 64 arbitrary length variables. Variable names must be alphabetic and are case sensitive. 


### Usage

Upon executing the program, you will be greeted with a prompt. Simply enter your formula and you will receive a truth table.

An example:

		Enter your expression:
		(b && a) -> c


		 a | b | c |
		---------------
		 0 | 0 | 0 | 1
		 1 | 0 | 0 | 1
		 0 | 1 | 0 | 1
		 1 | 1 | 0 | 0
		 0 | 0 | 1 | 1
		 1 | 0 | 1 | 1
		 0 | 1 | 1 | 1
		 1 | 1 | 1 | 1

### Building
Quite straight forward, move into the root directory of the project and do:

		make build
		cd build
		cmake ..

Then build with your chosen build system. No external dependencies beyond libc required.
