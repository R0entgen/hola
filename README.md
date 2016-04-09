def qsort(arreglo):
    
    pivote=0
    i=len(arreglo)-1
    
    if (len(arreglo)-1<=0):
        return arreglo
    print arreglo
    
    while i>pivote:
    
        if (arreglo[pivote]<arreglo[i]):
            elem=arreglo[pivote]
            del arreglo[pivote]
            arreglo.append(elem)
            pivote=pivote+1
            
        else:
            i=i-1
            
        	
    a1=qsort(arreglo[pivote+1:])
    a2=qsort(arreglo[:pivote])
    
    return a1+[arreglo[pivote]]+a2

arreglo=[4,8,6,1,2,7,5,3]
print arreglo
a=qsort(arreglo)
print a
