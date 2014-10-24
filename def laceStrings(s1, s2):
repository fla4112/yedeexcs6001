def myLog(x, b):
    '''
    x: a positive integer
    b: a positive integer; b >= 2

    returns: log_b(x), or, the logarithm of x relative to a base b.
    '''
    # Your Code Here
    i = 0
    while True:
        if b**i == x:
            return i
        elif b**i > x:
            return i - 1
        else:
            i += 1

def laceStrings(s1, s2):
    """
    s1 and s2 are strings.

    Returns a new str with elements of s1 and s2 interlaced,
    beginning with s1. If strings are not of same length, 
    then the extra elements should appear at the end.
    """
    # Your Code Here
        
    if len(s1) < len(s2):
        minStr= s1
        maxStr= s2
    else:
        minStr= s2
        maxStr= s1
    txt=''
    n=len(minStr)
    
    i=0
    if len(maxStr)==0:
        return ''
    while i < n:
        txt += s1[i]
        txt += s2[i]        
        i+=1
    txt += maxStr[n:]
    return txt
    
def laceStringsRecur(s1, s2):
    """
    s1 and s2 are strings.

    Returns a new str with elements of s1 and s2 interlaced,
    beginning with s1. If strings are not of same length, 
    then the extra elements should appear at the end.
    """
    def helpLaceStrings(s1, s2, out):
        if s1 == '':
            #PLACE A LINE OF CODE HERE
            return out + s2
        if s2 == '':
            #PLACE A LINE OF CODE HERE
            return out + s1
        else:
            #PLACE A LINE OF CODE HERE
            return helpLaceStrings(s1[1:], s2[1:], out + s1[0] + s2[0]) 
    return helpLaceStrings(s1, s2, '')
    
def McNuggets(n):
    """
    n is an int

    Returns True if some integer combination of 6, 9 and 20 equals n
    Otherwise returns False.
    """
    a=0
    b=0
    c=0
    while (6*a)<=n:
        while (9*b)<=n:
            while (20*c)<= n:
                tot= (6*a) + (9*b) + (20*c)
                if tot==n:
                    # print a,b,c,n
                    return True
                c += 1
            c=0
            b +=1
        c=0
        b=0
        a +=1

    return False 
    
def fixedPoint(f, epsilon):
    """
    f: a function of one argument that returns a float
    epsilon: a small float
  
    returns the best guess when that guess is less than epsilon 
    away from f(guess) or after 100 trials, whichever comes first.
    """
    guess = 1.0
    for i in range(100):
        if abs(f(guess) - guess) < epsilon:
            return guess
        else:
            guess = f(guess)
    return guess
    
def sqrt(a):
    def tryit(x):
        return 0.5 * (a/x + x)
    return fixedPoint(tryit, 0.0001)
    
def babylon(a):
    def test(x):
        return 0.5 * ((a / x) + x)
    return test

def sqrt(a):
    return fixedPoint(babylon(a), 0.0001)    
    
    
    
