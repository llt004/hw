# hw5
1-r = range(5)
ff = []
k = 10
for d in r:
    ff.append(k)
    k -= 5  

print(ff)
x = range (6)
tt=[]
for t in x:
    tt.append(t)
print(tt)
y = range(6)
rr = []
for p in y:
    if 2 <= p <= 5:
        rr.append(4)
print(rr)

z = range(6)
uu = []
for w in z:
    g = w +4
    uu.append(g)
uu.reverse()
print(uu)  

         
           
2-[(1, 2, 0), (2, 4, -1), (3, 6, -2), (4, 8, -3), (5, 10, -4)]
zip function returns an iretable of tuples,the first elements of the tuples are joined together and the second and so on,any excess of elements in any tuples are ignored
3-[2,3,4]
def apply(lst, fn):
    result = []
    for elem in lst:
        result.append(fn(elem))
    return result

x= lambda num:num+1

r = list(map(lambda lst: apply(lst, x), [[1,2,3]]))
print(r)
4-def apply(lst, fn):
    result = []
    for elem in lst:
        result.append(fn(elem))
    return result

x= lambda num:num+1

r = apply([1, 2, 3], x)
print(r)
5-[10,20,30]
0
6-x = [1, 2, 10, 13, 1]
lst=[]
for i in x:
    
    if i%2==0:
        lst.append('true')
    else:
        lst.append('false')
print(lst)
7-output will be (5,0)
4.472 (2root5)
__init is the constructor,__str__ returns the x y points between brackets, the add function adds the x compentent of the object that has been set to the x component that called the object and 
likewise the y component, and the distance function calculates the distance by subtracting the components of the object sent to the object calling the function
then it calculates the square root of the sum of the square of those differences of the components
class Point3D:
    def __init__(self, x=0, y=0, z=0):
        self.x = x
        self.y = y
        self.z = z

    def __str__(self):
        return f"({self.x}, {self.y}, {self.z})"

    def add(self, p):
        self.x += p.x
        self.y += p.y
        self.z += p.z

    def distance(self, p):
        delta_x = self.x - p.x
        delta_y = self.y - p.y
        delta_z = self.z - p.z

        dist = (delta_x ** 2 + delta_y ** 2 + delta_z ** 2) ** 0.5
        return dist
    def subtract(self,p):
        self.x-=p.x
        self.y-=p.y
        self.z-=p.z
  


p1 = Point3D(1, 2, 3)
p2 = Point3D(4, -2, -6)

p2.add(p1)
p1.subtract(p2)
print(p1)
print(p2)
print(p1.distance(p2))
