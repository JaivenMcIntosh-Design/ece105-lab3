# AI log: Lab 3, fit_zipf

Your name: JAIVEN MCINTOSH

Tool: GOOGLE ARGON 4 

## The prompt I gave it

def fit_zipf (c, kmin , kmax):
""" Fit c_k = C * k**m to the counts of ranks kmin to kmax.
c: numpy array of word counts , largest first; c[0] is rank 1.
kmin , kmax: the first and last rank to fit; both are included .
Fits a straight line , log10(c_k) = m * log10(k) + b, by least
squares (np. polyfit ) to the ranks k = kmin , kmin + 1, ..., kmax.
Returns (m, C), where C = 10**b.
Examples ( rounded to 6 decimal places):
fit_zipf (np.array ([600 , 300 , 200 , 150 ]), 1, 4)
returns (-1.0, 600.0)
fit_zipf (np.array ([5000 , 900 , 400 , 1]), 2, 3)
returns (-2.0, 3600.0)
"""
return 0, 0

"’m learning Python and numpy. Write the body of this function,
using numpy (np.arange, np.log10, np.polyfit). Keep the def line
and the docstring exactly as they are. Then explain which elements
of c your code fits, and why."

## The code it gave me

def fit_zipf(c, kmin, kmax):
    """Fit c_k = C * k**m to the counts of ranks kmin to kmax.
    c: numpy array of word counts , largest first; c[0] is rank 1.
    kmin , kmax: the first and last rank to fit; both are included .
    Fits a straight line , log10(c_k) = m * log10(k) + b, by least
    squares (np. polyfit ) to the ranks k = kmin , kmin + 1, ..., kmax.
    Returns (m, C), where C = 10**b.
    Examples ( rounded to 6 decimal places):
    fit_zipf (np.array ([600 , 300 , 200 , 150 ]), 1, 4)
    returns (-1.0, 600.0)
    fit_zipf (np.array ([5000 , 900 , 400 , 1]), 2, 3)
    returns (-2.0, 3600.0)
    """
    k = np.arange(kmin, kmax + 1)
    c_k = c[kmin - 1 : kmax]
    m, b = np.polyfit(np.log10(k), np.log10(c_k), 1)
    return m, 10**b
## What I checked

- Example 1, `fit_zipf(np.array([600, 300, 200, 150]), 1, 4)`: I got
- Example 2, `fit_zipf(np.array([5000, 900, 400, 1]), 2, 3)`: I got
- Anything else I checked:

checked and verified it was correct.

## What I changed, and why

Gemini Argon replaced the return function at the end. as specified.
