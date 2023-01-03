# Nimus-Clock
Digital Clock
from tkinter import *
from tkinter.ttk import *

from time import strftime

root = Tk()
root.title("Digital Clock")


def time():
    string = strftime('%H:%M:%S %p %a %e %n')
    label.config(text=string)
    label.after(1000, time)


label = Label(root, font=("ds-digital", 60), background="black", foreground="yellow")
label.pack(anchor='center')
time()

mainloop()
