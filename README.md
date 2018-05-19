N=int(input())
array_damages = []
for i in range(0,N):
    x=input()
    array_damages.append(x)
sort = sorted(array_damages,key=int)

health = 2000
injuries = 1

count=0

for i in range(1,len(sort)+1):
    if health<=0 or injuries >=1000000:
        count = i-1
        break
    injuries = injuries*int(sort[i-1])
    health = health-int(sort[i-1])
    print(injuries,health)
    if health<=0 or injuries >=1000000:
        count = i-1
        break
if count<0:
    count=0
print(count)
