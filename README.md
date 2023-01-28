# Fraction-class


class fract: 
   
    def __init__(self):
        pass
    def redfraction(self,x,y):
        for i in range(1,1000):
            try:
                if x%i==0 and y%i==0:
                
                    a = x//i
                    b = y//i
            except ZeroDivisionError:
                    print("Enter valid number ")
                
        return (a,b)
    def addfract(self,a,b,c,d):
        if b==0:
            z = (a*d)+c
            return self.redfraction(z,d)
        elif d==0:
            y = (b*c)+a
            return self.redfraction(y,b)
        elif b==d:
            e=(a+b)
            return self.redfraction(e,b)
        else:
            g=((a*d)+(b*c))
            h=b*d
            return self.redfraction(g,h)
    def subfract(self,a,b,c,d):
        if b==0:
            z = (a*c)-b
            return self.redfraction(z,c)
        elif d==0:
            y = (b*c)-a
            return self.redfraction(y,b)
        elif b==d:
            e=(a-b)
            return self.redfraction(e,b)
        else:
            g=((a*d)-(b*c))
            h=b*d
            return self.redfraction(g,h)
    def mulfract(self,a,b,c,d):
        e = a*c
        f = b*d
        return self.redfraction(e,f)
    def divfract(self,a,b,c,d):
            e = a*d
            f = b*c
            return self.redfraction(e,f)
f = fract()
print("fraction=",f.redfraction(10,25))
print("Addition of fraction=",f.addfract(4,5,3,25))
print("Subtraction of fraction=",f.subfract(10,14,15,10))
print("Multiplication of fraction=",f.mulfract(10,14,15,10))
print("Division of fraction=",f.divfract(15,10,15,25))
