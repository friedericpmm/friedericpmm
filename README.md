import tkinter
from tkinter import ttk

window = tkinter.Tk()
# (0,0) (1,0) (2,0)
# (0,1) (1,1) (2,1)
# (0,2) (1,2) (2,2)
window.columnconfigure(0, weight=1)

window.columnconfigure(1, weight=3)
seleccionado = tkinter.StringVar()

def salir(event):
    print("Adios")
    window.quit()
r1 = ttk.Radiobutton(window, text="Lista1", value="1", variable=seleccionado)
r2 = ttk.Radiobutton(window, text="Lista2", value="2", variable=seleccionado)
r3 = ttk.Radiobutton(window, text="Lista3", value="3", variable=seleccionado)
r1.grid(column=0, row=1, pady=5, sticky=tkinter.W, padx=5)
r2.grid(column=0, row=2, pady=5, sticky=tkinter.W, padx=5)
r3.grid(column=0, row=3, pady=5, sticky=tkinter.W, padx=5)

botonSalir = tkinter.Button(window, text="Salir")
botonSalir.grid(column=2, row=4)
botonSalir.bind("<Button-1>", salir)


def reinicio():
    print("Reinicio")
    botonReinicio.config(comand=reset)
    


botonReinicio = tkinter.Button(window, text="Reinicio")
botonReinicio.grid(column=0, row=4, sticky=tkinter.W, padx=5, pady=5)
botonReinicio.bind("<Button-1>", reinicio)


window.mainloop()
