import tkinter as tk
ventana = tk.Tk()
ventana.title("Lista despeable")

ventana.geometry('380x300+100+100')
#ventana.configure(background='dark turqoise')
var = tk.StringVar(ventana)
var.set("Rojo")
opciones = ["Azul", "Rosa", "Amarillo", "Verde", "Blanco", "Morando"]
opcion = tk.OptionMenu(ventana, var, *opciones)
opcion.config(width=20)
opcion.pack(side="left", padx=30, pady=30)
el = tk.Label(ventana, text="Color seleccionado:", bg="pink", fg="white")
el.pack(padx=5, pady=5, ipadx=5, ipady=5, fill=tk.X)
color = tk.Label(ventana, bg='plum', textvariable=var, padx=5, pady=5, width=50)
color.pack()

ventana.mainloop()
