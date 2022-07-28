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
* Reference values and estimates are appropriately paired (eg. using nearest neighbor or interpolation technique).
* Mean absolute error is computed correctly.
* The reference heart rate produces a value every 2 seconds except for the last 8 seconds of the dataset. Nicely done here
* The mean absolute error at 90% availability is less than 10 BPM.
* Your mean absolute error at 90% availability is less than the required BPM. Great job!
* The algorithm should run on the test subject without errors.
* The algorithm should produce a pulse rate estimate and a confidence value at least every 2 seconds.
* Great work👏, your algorithm run on the test subject without errors and algorithm produce both an estimate and a confidence value at least every 2 seconds.
 ### Project Write-up
 * The Project Write-up describes how to run the code.
The writeup explains all the steps required to run the code, which includes the following:
* Import modules and libraries dependencies to run your code
* Arguments that can be set for your functions and which ones are the recommended ones
* Brief explanation of the workflow of your algorithm. i.e. which functions should someone running your code for the first time run.
* The Project Write-up describes: 
   * what activities were performed in the dataset. 
   * features of the sensor that was used.
   * the quantity of data in the dataset.
   * short-comings of the dataset.

The Project Write-up includes the activities were performed in the dataset., features of the sensor that was used., the quantity of data in the dataset and the short-comings of the datasets. Your write-up is clean and straight forward
Highlights:

* The activities were rest, jog, and run at various speeds on a treadmill.
* The data came from a wrist-wearable that included two PPG signals and a 3-axis accelerometer all sampled at 125 Hz.
* There were 12 sessions of data from 11 subjects. Each session was 5 minutes long.
* Common short-comings of the dataset would be that the subjects in this dataset were performing a set of fixed actions, under supervised study staff, and were not in a free-living context. It is a small dataset with only 11 subjects and the leave-one-subject-out error variance is high.

I would recommend you to explore more on the dataset https://ieeexplore.ieee.org/document/6905737
https://arxiv.org/ftp/arxiv/papers/1504/1504.04785.pdf


**The Project Write-up describes:**

how the algorithm works, including a description of the physiology.
an intuitive explanation of why the confidence algorithm produces a higher number for better estimates.
insightful caveats and failure-modes of the algorithm.

Great job describing all the algorithm's flow. The confidence calculation is very clever as getting the magnitude proportion of the harmonic relative to the magnitude of the entire spectrum neatly represents how confident the prediction is. Well done! 🙂
You are right, wrist movement can affect the algorithm performance. Another issue could arise due to noise, noise is always a problem that we need to handle, that is why we use filters. In this case, we use a basic filter. However, for more robust systems you can find Kalman filters or even particle filters. For instance, you can check [this paper](https://ieeexplore.ieee.org/document/6162034) where a particle-filter approach is recommended to reduce ppg signal noise.








