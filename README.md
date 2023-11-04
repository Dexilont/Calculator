# Calculator
from tkinter import *

def plus():
    lbl3.configure(text=int(txt1.get())+int(txt2.get()))
def minus():
    lbl3.configure(text=int(txt1.get())-int(txt2.get()))
def division():
    lbl3.configure(text=int(txt1.get())/int(txt2.get()))
def multiply():
    lbl3.configure(text=int(txt1.get())*int(txt2.get()))

window = Tk()
window.title('Калькулятор для лютых')
window.geometry('250x350')

lbl1 = Label(window,text='Первое число')
lbl1.pack()
txt1=Entry(window,width=50,bg='grey')
txt1.pack()

lbl2 = Label(window,text='Второе число')
lbl2.pack()
txt2=Entry(window,width=50,bg='grey')
txt2.pack()

btn1 = Button(window,text='+',command=plus)
btn1.pack()
btn2 = Button(window,text='-',command=minus)
btn2.pack()
btn3 = Button(window,text='/',command=division)
btn3.pack()
btn3 = Button(window,text='*',command=multiply)
btn3.pack()

lbl3=Label(window,text='Ответ:')
lbl3.pack()

window.mainloop()
