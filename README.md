# Pulse-Rate-Algorithm
Physiological Mechanics of Pulse Rate Estimation

## Code Quality
Scripts have an intuitive, easy-to-follow structure with code separated into logical functions.
Naming for variables and functions follows the PEP8 style guidelines.
Good work. Scripts have easy-to-follow structure and followed the coding standards.
• Overall naming convention following in the codes, except few issues where variables does not comply with standards
• Some of the variables are single letter notations which will be difficult to debug if issues occurs. This can be avoided

#### Further Reading
• PEP 8 standards for naming convention can be incorporated for better traceability https://www.python.org/dev/peps/pep-0008/
• You can use autopep8 to automate the conversion of codes to PEP 8 compliant https://pypi.org/project/autopep8/
 * Comments are used to clearly describe tricky or opaque pieces of code.
 * Each function has a docstring.
 * The module containing the algorithm has a docstring describing the algorithm.
 
 Good work, you have provided DOC STRINGS for most of functions .
I can clearly see
• The argument requirements for a function
• What functions returns
• Overall descriptions of the functions
• Module level DOC STRINGS also provided.
You have added sufficient amount of comments to your code.

**You can also refer to:**
https://www.pythonforbeginners.com/basics/python-docstrings
* Algorithm parameters are passed as function arguments.
* Default values for algorithm parameters should be set.
* Use module constants or function parameters instead of magic numbers.
* Makes use of vectorized operations (e.g., with numpy) when doing so would make the code easier to read or noticeably faster.
* Good job here, passing algorithm parameters as function arguments, default values are set, used module constants and making use of vectorized operations

#### Algorithm Specifics
* Use the 2nd ppg signal in the third column of the troika data matrix. If you are using the provided starter code to parse the data files, then this happens automatically.
* The troika data matrix contains two ppg signals. One of them is much cleaner and you have rightly used the second one.

* The PPG and accelerometer signals should be bandpass filtered using a reasonable passband and filter design.
The accelerometer channels should be aggregated in a meaningful way (e.g., into a magnitude signal).
* Good work. You have used BandPass filter to filter the signal with required frequency limits. Aggregations applied
Band pass filter is an important tool we have to filter the required frequency from a raw signal which may have noise

Good read on the band pass filter theory in case you are interested to explore https://faculty.wcas.northwestern.edu/~lchrist/research/Filter/bandpassfiltertext.pdf
