import random
o=random.randint (0,3000)
gh=0
l = dat[o]
s=len(l)
x=['_']*s
if s<=5:
    print('Hi, I am very sorry but that word was too easy. Try again.')
else:
    while (gh<6):
        print(x)
        f=input()
        if f == 'hint':
            v=random.randint(0,s-1)
            while (l[v] in x):
                v=random.randint(0,s-1)
            print(l[v])
        else:
            if f in l:
                for a in range(len(l)):
                    if f==l[a]:
                        x[a]=f
                        print(x)
                        print(True)
                        continue
            else:
                print(False)
                gh=gh+1
            if '_' not in x:
                            print('you won')
                            print('hope you enjoyed')
                            print('copyright ben prodoction inc')
                            break
            if gh == (5):
                        print('you have one life remaining')
            if gh ==(6):
                print('you lost')
                print('try again')
                print('the word was %s'%l)
                print('copyright ben production inc')
                print('to play again. Play rock,paper,scissors')
