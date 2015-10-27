# GUI-Code"


from tkinter import *
from tkinter.messagebox import showinfo
import random


standaard_window = Tk()

def achtergrond():
    standaard_window
    photo=PhotoImage(file='rsz.gif')
    label = Label(standaard_window,image=photo)
    label.pack()
    standaard_window.mainloop()

topframe= Frame(standaard_window)
topframe.pack()

bottomframe=Frame(standaard_window)
bottomframe.pack(side=BOTTOM)

sideframe= Frame(standaard_window)
sideframe.pack(side=LEFT)

sideframe1=Frame(standaard_window)
sideframe1.pack(side=RIGHT)


label = Label(topframe,text='Raad de volgende Marvel-held!',bg='red',fg='white',font=('impact',35))
label.pack()


def random_hint():
    showinfo(title='Klik hier voor een hint',message='Hier komt de "random" hint')

button2 = Button(standaard_window, text= 'Hints!',font=('courier',15),bg='red', command=random_hint)
button2.pack(padx=50,pady=15)
button2.config(height=2,width=15)


invoer_antwoord = Entry(bottomframe)
invoer_antwoord.pack(pady=5)


list=['incorrect! -1','correct!']
def antwoord_goed_fout():
    showinfo(message=random.choice(list))

button_antwoord = Button(bottomframe,text = 'OK',font=('courier',15),command=antwoord_goed_fout)
button_antwoord.pack(pady=15)
button_antwoord.config(height=1,width=5)

achtergrond()
standaard_window.mainloop()


