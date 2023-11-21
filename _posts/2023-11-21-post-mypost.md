---
layout: posts
title: working with turtle library
---
# explanation

<h4 style= "text-align:right;">
در مورد کار کردن با فرکتال ها چیزی که مشهوده تکرار شدنه یک شکل است برای کشیدن یک فرکتال باید درک کنی شکلی که میخواهی بکشی از چه مراحلی تولید شده و به ترتیب آن را اجرا کنی
 برای کار کردن درخت نیز همینطور باید به ترتیب مشخص کنید سمت راست و چپ چگونه باشد و سر کدام شاخه ها برگ بکشد
برای کشیدن جنگل مکان ها و رنگ هارو رندوم انتخاب کرده و سعی میکنیم جنگلی که میخواهیم را با جابه جا کردن دستور هایی که نوشتیم بدست بیاریم




## they are my triangle codes:
<pre style="font-size: 25; text-align:left;"> 
import turtle as t


def triangle(d):
    if d<10:
        return
    t.pencolor("blue")
    t.tracer(0)
    for _ in range(3):
        t.fd(d)
        t.lt(120)
        triangle(d/2)
    t.update()

triangle(200)
t.mainloop()
</pre>

![alt text](../assets/images/Screenshot%20(7).png "triangle Picture")


## they are my tree codes:
<pre style="font-size: 25; text-align:left;">
import turtle as t

def setare(n,d):
    for _ in range(n):
        t.pencolor("gold")
        t.fd(d)
        t.rt(180-180/n)
        
def tree(d,r,w):
    t.pencolor("chocolate4")
    if d<10 or r<10:
        return
    t.pensize(w)
    t.fd(d)
    t.lt(r)
    tree(d*0.7,r, 0.5*w)
    t.rt(2*r)
    if d>=10 and d<15 :
        setare(7,15)
    tree(d*0.7,r, 0.5*w)
    t.lt(r)
    t.backward(d)

t.speed(0)
t.lt(90)
tree(100 ,30,15)
t.rt(90)
t.penup()
t.fd(100)
t.pendown()
setare(7,15)
t.penup()
t.fd(20)
t.pendown()
setare(7,15)
t.penup()
t.fd(20)
t.pendown()
setare(7,15)
t.penup()
t.update()
t.backward(140)
t.mainloop()
</pre>

![alt text](../assets/images/Screenshot%20(351).png "tree Picture")

My jungle code is very long, but the result is this image:

![alt text](../assets/images/Screenshot%20(9).png "gungle Picture")


[my favorite website about turtle library color](https://suherfe.blog.ir/post/color-turtle)


