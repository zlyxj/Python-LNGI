from rich import print;
from math import floor;
import time
f=open('storage.txt','r')
tm=float(f.read());
f.close()
def getString(t):
    if(t<=20):
        return str(round(t,1));
    elif(1.1**(t-20)*20<10**10):
        formatnum="{:,.1f}".format(round(1.1**(t-20)*20,1));
        return str(formatnum);
    elif(t<450):
        return ("10[red]^[/red]"+getString(t-220));
    else:
        arrows=int(floor((t/450)**2)+3);
        farrows=((t/450)**2+2)%1.0
        return ("10[#FF7F00]^^[/#FF7F00]"*(arrows//10)+"10[red]^[/red]"*(arrows%10)+"{:,.1f}".format(10**(farrows*9+1)))
while(1):
    tm+=0.05;
    print("[white]"+getString(tm)+"[/]"+' '*999,end='\r');
    if(abs(tm%5)<0.05):
        f=open('storage.txt','w');
        f.write(str(tm));
        f.close()
    time.sleep(0.05)
