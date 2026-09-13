# primes-between
gives the total number of primes in an interval [x,y], including x and y 
 def primesbet(x,y):
...     P = [2]
...     c = int((x+y)/3)
...     o = int((2/3)*(x+y))
...     for i in range(3,c+1):
...         p=0
...         for j in range(len(P)):
...             if i%P[j] == 0:
...                 p = p + 1
...         if p == 0:
...             P.append(i)
...     for q in range(c+1,o):
...         z=0
...         for m in range(len(P)):
...             if q%P[m] == 0 :
...                z = z + 1
...
...         if z == 0 :
...             P.append(q)
...
...     for f in range(o,y+1):
...         e=0
...         for l in range(len(P)):
...             if f%P[l] == 0 :
...                e = e +1
...
...         if e == 0:
...             P.append(f)
...     return len(P)
