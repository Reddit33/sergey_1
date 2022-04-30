# sergey_1 RI1-01 Яковлев Сергей
print ("hello")
from tkinter import *
from tkinter import messagebox

def login():
    user = username.get()
    code = password.get()



    if user == "u1" and code == "password1":
        root = Toplevel(screen)
        root.geometry("1160x500")
        root.title("Travel&CO")
        root.resizable(False, False)

        def Total():
            try:
                a1 = int(Radisson_Blu_Hotel.get())
            except:
                a1 = 0
            try:
                a2 = int(Hyatt_Regency_Tashkent.get())
            except:
                a2 = 0
            try:
                a3 = int(Palace_Hotel_Tashkent.get())
            except:
                a3 = 0
            try:
                a4 = int(Cobalt.get())
            except:
                a4 = 0
            try:
                a5 = int(Captiva.get())
            except:
                a5 = 0
            try:
                a6 = int(Tracker.get())
            except:
                a6 = 0
            try:
                a7 = int(Central_Park.get())
            except:
                a7 = 0
            try:
                a8 = int(ECO_Park.get())
            except:
                a8 = 0
            try:
                a9 = int(Tashkent_City_Park.get())
            except:
                a9 = 0

            c1 = 25 * a1
            c2 = 23 * a2
            c3 = 20 * a3
            c4 = 50 * a4
            c5 = 70 * a5
            c6 = 65 * a6
            c7 = 3 * a7
            c8 = 1 * a8
            c9 = 2 * a9

            lbl_total = Label(f2, font=("arial", 20, "bold"), text="Итого", width=16, fg="lightyellow", bg="black")
            lbl_total.place(x=10, y=50)

            entry_total = Entry(f2, font=("ariial", 20, "bold"), textvariable=Total_bill, bd=6, width=15,
                                bg="lightgreen")
            entry_total.place(x=20, y=100)

            totalcost = c1 + c2 + c3 + c4 + c5 + c6 + c7 + c8 + c9
            string_bill = "$", str("%.2f" % totalcost)
            Total_bill.set(string_bill)

        def Reset():
            entry_Radisson_Blu_Hotel.delete(0, END)
            entry_Hyatt_Regency_Tashkent.delete(0, END)
            entry_Palace_Hotel_Tashkent.delete(0, END)
            entry_Cobalt.delete(0, END)
            entry_Captiva.delete(0, END)
            entry_Tracker.delete(0, END)
            entry_Central_Park.delete(0, END)
            entry_ECO_Park.delete(0, END)
            entry_Tashkent_City_Park.delete(0, END)

        Label(text="Travel&CO", bg="black", fg="white", font=("calibri", 33), width="300", height="2").pack()

        f = Frame(root, bg="lightblue", highlightbackground="black", highlightthickness=1, width=450, height=480)
        f.place(x=10, y=5)

        Label(f, text="Цены за услуги", font=("Gabriola", 40, "bold"), fg="black", bg="lightblue").place(x=80, y=0)

        Label(f, font=("comic sans", 15, "bold"), text="Radisson_Blu_Hotel 1.....25$/day", fg="black",
              bg="lightblue").place(x=10, y=80)
        Label(f, font=("comic sans", 15, "bold"), text="Hyatt_Regency_Tashkent.....23$/day", fg="black",
              bg="lightblue").place(x=10, y=110)
        Label(f, font=("comic sans", 15, "bold"), text="Palace_Hotel_Tashkent.....20$/day", fg="black",
              bg="lightblue").place(x=10, y=140)
        Label(f, font=("comic sans", 15, "bold"), text="Cobalt.....50$/day", fg="black", bg="lightblue").place(x=10,
                                                                                                               y=170)
        Label(f, font=("comic sans", 15, "bold"), text="Captiva.....70$/day", fg="black", bg="lightblue").place(x=10,
                                                                                                                y=200)
        Label(f, font=("comic sans", 15, "bold"), text="Tracker.....65$/day", fg="black", bg="lightblue").place(x=10,
                                                                                                                y=230)
        Label(f, font=("comic sans", 15, "bold"), text="Tashkent_City_Park.....2$/ticket", fg="black",
              bg="lightblue").place(x=10, y=260)
        Label(f, font=("comic sans", 15, "bold"), text="ECO_Park.....1$/ticket", fg="black", bg="lightblue").place(x=10,
                                                                                                                   y=290)
        Label(f, font=("comic sans", 15, "bold"), text="Central_Park.....3$/ticket", fg="black", bg="lightblue").place(
            x=10, y=320)

        f2 = Frame(root, bg="lightyellow", highlightbackground="black", highlightthickness=1, width=300, height=480)
        f2.place(x=855, y=5)

        Bill = Label(f2, text="Счет", font=("calibri", 20), bg="lightyellow")
        Bill.place(x=120, y=10)

        f1 = Frame(root, bd=5, height=370, width=300, relief=RAISED)
        f1.place(x=460, y=5)

        Radisson_Blu_Hotel = StringVar()
        Hyatt_Regency_Tashkent = StringVar()
        Palace_Hotel_Tashkent = StringVar()
        Captiva = StringVar()
        Cobalt = StringVar()
        Tracker = StringVar()
        Tashkent_City_Park = StringVar()
        ECO_Park = StringVar()
        Central_Park = StringVar()
        Total_bill = StringVar()

        lbl_Radisson_Blu_Hotel = Label(f1, font=("aria", 15, "bold"), text="Radisson Blu Hotel", width=19, fg="Black")
        lbl_Hyatt_Regency_Tashkent = Label(f1, font=("aria", 15, "bold"), text="Hyatt Regency Tashkent", width=19,
                                           fg="Black")
        lbl_Palace_Hotel_Tashkent = Label(f1, font=("aria", 15, "bold"), text="Palace Hotel Tashkent", width=19,
                                          fg="Black")
        lbl_Captiva = Label(f1, font=("aria", 15, "bold"), text="Captiva", width=19, fg="Black")
        lbl_Cobalt = Label(f1, font=("aria", 15, "bold"), text="Cobalt", width=19, fg="Black")
        lbl_Tracker = Label(f1, font=("aria", 15, "bold"), text="Tracker", width=19, fg="Black")
        lbl_Tashkent_City_Park = Label(f1, font=("aria", 15, "bold"), text="Tashkent City Park", width=19, fg="Black")
        lbl_ECO_Park = Label(f1, font=("aria", 15, "bold"), text="ECO Park", width=19, fg="Black")
        lbl_Central_Park = Label(f1, font=("aria", 15, "bold"), text="Central Park", width=19, fg="Black")

        lbl_Radisson_Blu_Hotel.grid(row=1, column=0)
        lbl_Hyatt_Regency_Tashkent.grid(row=2, column=0)
        lbl_Palace_Hotel_Tashkent.grid(row=3, column=0)
        lbl_Captiva.grid(row=4, column=0)
        lbl_Cobalt.grid(row=5, column=0)
        lbl_Tracker.grid(row=6, column=0)
        lbl_Tashkent_City_Park.grid(row=7, column=0)
        lbl_ECO_Park.grid(row=8, column=0)
        lbl_Central_Park.grid(row=9, column=0)

        entry_Radisson_Blu_Hotel = Entry(f1, font=("aria", 20, "bold"), textvariable=Radisson_Blu_Hotel, bd=6, width=8,
                                         bg="lightgreen")
        entry_Hyatt_Regency_Tashkent = Entry(f1, font=("aria", 20, "bold"), textvariable=Hyatt_Regency_Tashkent, bd=6,
                                             width=8, bg="lightgreen")
        entry_Palace_Hotel_Tashkent = Entry(f1, font=("aria", 20, "bold"), textvariable=Palace_Hotel_Tashkent, bd=6,
                                            width=8, bg="lightgreen")
        entry_Captiva = Entry(f1, font=("aria", 20, "bold"), textvariable=Captiva, bd=6, width=8, bg="lightgreen")
        entry_Cobalt = Entry(f1, font=("aria", 20, "bold"), textvariable=Cobalt, bd=6, width=8, bg="lightgreen")
        entry_Tracker = Entry(f1, font=("aria", 20, "bold"), textvariable=Tracker, bd=6, width=8, bg="lightgreen")
        entry_Tashkent_City_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=Tashkent_City_Park, bd=6, width=8,
                                         bg="lightgreen")
        entry_ECO_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=ECO_Park, bd=6, width=8, bg="lightgreen")
        entry_Central_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=Central_Park, bd=6, width=8,
                                   bg="lightgreen")

        entry_Radisson_Blu_Hotel.grid(row=1, column=1)
        entry_Hyatt_Regency_Tashkent.grid(row=2, column=1)
        entry_Palace_Hotel_Tashkent.grid(row=3, column=1)
        entry_Captiva.grid(row=4, column=1)
        entry_Cobalt.grid(row=5, column=1)
        entry_Tracker.grid(row=6, column=1)
        entry_Tashkent_City_Park.grid(row=7, column=1)
        entry_ECO_Park.grid(row=8, column=1)
        entry_Central_Park.grid(row=9, column=1)
        btn_reset = Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, "bold"), width=10, text="Очистить",
                           command=Reset)
        btn_reset.grid(row=10, column=0)

        btn_total = Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, "bold"), width=10, text="Итого",
                           command=Total)
        btn_total.grid(row=10, column=1)
    elif user == "u1" and code == "admin":
        root = Toplevel(screen)
        root.geometry("1160x500")
        root.title("Travel&CO")
        root.resizable(False, False)

        def Total():
            try:
                a1 = int(Radisson_Blu_Hotel.get())
            except:
                a1 = 0
            try:
                a2 = int(Hyatt_Regency_Tashkent.get())
            except:
                a2 = 0
            try:
                a3 = int(Palace_Hotel_Tashkent.get())
            except:
                a3 = 0
            try:
                a4 = int(Cobalt.get())
            except:
                a4 = 0
            try:
                a5 = int(Captiva.get())
            except:
                a5 = 0
            try:
                a6 = int(Tracker.get())
            except:
                a6 = 0
            try:
                a7 = int(Central_Park.get())
            except:
                a7 = 0
            try:
                a8 = int(ECO_Park.get())
            except:
                a8 = 0
            try:
                a9 = int(Tashkent_City_Park.get())
            except:
                a9 = 0

            c1 = 25 * a1
            c2 = 23 * a2
            c3 = 20 * a3
            c4 = 50 * a4
            c5 = 70 * a5
            c6 = 65 * a6
            c7 = 3 * a7
            c8 = 1 * a8
            c9 = 2 * a9

            lbl_total = Label(f2, font=("arial", 20, "bold"), text="Итого", width=16, fg="lightyellow", bg="black")
            lbl_total.place(x=10, y=50)

            entry_total = Entry(f2, font=("ariial", 20, "bold"), textvariable=Total_bill, bd=6, width=15,
                                bg="lightgreen")
            entry_total.place(x=20, y=100)

            totalcost = c1 + c2 + c3 + c4 + c5 + c6 + c7 + c8 + c9
            string_bill = "$", str("%.2f" % totalcost)
            Total_bill.set(string_bill)

        def Reset():
            entry_Radisson_Blu_Hotel.delete(0, END)
            entry_Hyatt_Regency_Tashkent.delete(0, END)
            entry_Palace_Hotel_Tashkent.delete(0, END)
            entry_Cobalt.delete(0, END)
            entry_Captiva.delete(0, END)
            entry_Tracker.delete(0, END)
            entry_Central_Park.delete(0, END)
            entry_ECO_Park.delete(0, END)
            entry_Tashkent_City_Park.delete(0, END)

        Label(text="Travel&CO", bg="black", fg="white", font=("calibri", 33), width="300", height="2").pack()

        f = Frame(root, bg="lightblue", highlightbackground="black", highlightthickness=1, width=450, height=480)
        f.place(x=10, y=5)

        Label(f, text="Цены за услуги", font=("Gabriola", 40, "bold"), fg="black", bg="lightblue").place(x=80, y=0)

        Label(f, font=("comic sans", 15, "bold"), text="Radisson_Blu_Hotel 1.....25$/day", fg="black",
              bg="lightblue").place(x=10, y=80)
        Label(f, font=("comic sans", 15, "bold"), text="Hyatt_Regency_Tashkent.....23$/day", fg="black",
              bg="lightblue").place(x=10, y=110)
        Label(f, font=("comic sans", 15, "bold"), text="Palace_Hotel_Tashkent.....20$/day", fg="black",
              bg="lightblue").place(x=10, y=140)
        Label(f, font=("comic sans", 15, "bold"), text="Cobalt.....50$/day", fg="black", bg="lightblue").place(x=10,
                                                                                                               y=170)
        Label(f, font=("comic sans", 15, "bold"), text="Captiva.....70$/day", fg="black", bg="lightblue").place(x=10,
                                                                                                                y=200)
        Label(f, font=("comic sans", 15, "bold"), text="Tracker.....65$/day", fg="black", bg="lightblue").place(x=10,
                                                                                                                y=230)
        Label(f, font=("comic sans", 15, "bold"), text="Tashkent_City_Park.....2$/ticket", fg="black",
              bg="lightblue").place(x=10, y=260)
        Label(f, font=("comic sans", 15, "bold"), text="ECO_Park.....1$/ticket", fg="black", bg="lightblue").place(x=10,
                                                                                                                   y=290)
        Label(f, font=("comic sans", 15, "bold"), text="Central_Park.....3$/ticket", fg="black", bg="lightblue").place(
            x=10, y=320)

        f2 = Frame(root, bg="lightyellow", highlightbackground="black", highlightthickness=1, width=300, height=480)
        f2.place(x=855, y=5)

        Bill = Label(f2, text="Счет", font=("calibri", 20), bg="lightyellow")
        Bill.place(x=120, y=10)

        f1 = Frame(root, bd=5, height=370, width=300, relief=RAISED)
        f1.place(x=460, y=5)

        Radisson_Blu_Hotel = StringVar()
        Hyatt_Regency_Tashkent = StringVar()
        Palace_Hotel_Tashkent = StringVar()
        Captiva = StringVar()
        Cobalt = StringVar()
        Tracker = StringVar()
        Tashkent_City_Park = StringVar()
        ECO_Park = StringVar()
        Central_Park = StringVar()
        Total_bill = StringVar()

        lbl_Radisson_Blu_Hotel = Label(f1, font=("aria", 15, "bold"), text="Radisson Blu Hotel", width=19, fg="Black")
        lbl_Hyatt_Regency_Tashkent = Label(f1, font=("aria", 15, "bold"), text="Hyatt Regency Tashkent", width=19,
                                           fg="Black")
        lbl_Palace_Hotel_Tashkent = Label(f1, font=("aria", 15, "bold"), text="Palace Hotel Tashkent", width=19,
                                          fg="Black")
        lbl_Captiva = Label(f1, font=("aria", 15, "bold"), text="Captiva", width=19, fg="Black")
        lbl_Cobalt = Label(f1, font=("aria", 15, "bold"), text="Cobalt", width=19, fg="Black")
        lbl_Tracker = Label(f1, font=("aria", 15, "bold"), text="Tracker", width=19, fg="Black")
        lbl_Tashkent_City_Park = Label(f1, font=("aria", 15, "bold"), text="Tashkent City Park", width=19, fg="Black")
        lbl_ECO_Park = Label(f1, font=("aria", 15, "bold"), text="ECO Park", width=19, fg="Black")
        lbl_Central_Park = Label(f1, font=("aria", 15, "bold"), text="Central Park", width=19, fg="Black")

        lbl_Radisson_Blu_Hotel.grid(row=1, column=0)
        lbl_Hyatt_Regency_Tashkent.grid(row=2, column=0)
        lbl_Palace_Hotel_Tashkent.grid(row=3, column=0)
        lbl_Captiva.grid(row=4, column=0)
        lbl_Cobalt.grid(row=5, column=0)
        lbl_Tracker.grid(row=6, column=0)
        lbl_Tashkent_City_Park.grid(row=7, column=0)
        lbl_ECO_Park.grid(row=8, column=0)
        lbl_Central_Park.grid(row=9, column=0)

        entry_Radisson_Blu_Hotel = Entry(f1, font=("aria", 20, "bold"), textvariable=Radisson_Blu_Hotel, bd=6, width=8,
                                         bg="lightgreen")
        entry_Hyatt_Regency_Tashkent = Entry(f1, font=("aria", 20, "bold"), textvariable=Hyatt_Regency_Tashkent, bd=6,
                                             width=8, bg="lightgreen")
        entry_Palace_Hotel_Tashkent = Entry(f1, font=("aria", 20, "bold"), textvariable=Palace_Hotel_Tashkent, bd=6,
                                            width=8, bg="lightgreen")
        entry_Captiva = Entry(f1, font=("aria", 20, "bold"), textvariable=Captiva, bd=6, width=8, bg="lightgreen")
        entry_Cobalt = Entry(f1, font=("aria", 20, "bold"), textvariable=Cobalt, bd=6, width=8, bg="lightgreen")
        entry_Tracker = Entry(f1, font=("aria", 20, "bold"), textvariable=Tracker, bd=6, width=8, bg="lightgreen")
        entry_Tashkent_City_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=Tashkent_City_Park, bd=6, width=8,
                                         bg="lightgreen")
        entry_ECO_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=ECO_Park, bd=6, width=8, bg="lightgreen")
        entry_Central_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=Central_Park, bd=6, width=8,
                                   bg="lightgreen")

        entry_Radisson_Blu_Hotel.grid(row=1, column=1)
        entry_Hyatt_Regency_Tashkent.grid(row=2, column=1)
        entry_Palace_Hotel_Tashkent.grid(row=3, column=1)
        entry_Captiva.grid(row=4, column=1)
        entry_Cobalt.grid(row=5, column=1)
        entry_Tracker.grid(row=6, column=1)
        entry_Tashkent_City_Park.grid(row=7, column=1)
        entry_ECO_Park.grid(row=8, column=1)
        entry_Central_Park.grid(row=9, column=1)
        btn_reset = Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, "bold"), width=10, text="Очистить",
                           command=Reset)
        btn_reset.grid(row=10, column=0)

        btn_total = Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, "bold"), width=10, text="Итого",
                           command=Total)
        btn_total.grid(row=10, column=1)

    elif user == "u2" and code == "password2":
            root = Toplevel(screen)
            root.geometry("1160x500")
            root.title("Travel&CO")
            root.resizable(False, False)

            def Total():
                try:
                    a1 = int(Radisson_Blu_Hotel.get())
                except:
                    a1 = 0
                try:
                    a2 = int(Hyatt_Regency_Tashkent.get())
                except:
                    a2 = 0
                try:
                    a3 = int(Palace_Hotel_Tashkent.get())
                except:
                    a3 = 0
                try:
                    a4 = int(Cobalt.get())
                except:
                    a4 = 0
                try:
                    a5 = int(Captiva.get())
                except:
                    a5 = 0
                try:
                    a6 = int(Tracker.get())
                except:
                    a6 = 0
                try:
                    a7 = int(Central_Park.get())
                except:
                    a7 = 0
                try:
                    a8 = int(ECO_Park.get())
                except:
                    a8 = 0
                try:
                    a9 = int(Tashkent_City_Park.get())
                except:
                    a9 = 0

                c1 = 25 * a1
                c2 = 23 * a2
                c3 = 20 * a3
                c4 = 50 * a4
                c5 = 70 * a5
                c6 = 65 * a6
                c7 = 3 * a7
                c8 = 1 * a8
                c9 = 2 * a9

                lbl_total = Label(f2, font=("arial", 20, "bold"), text="Итого", width=16, fg="lightyellow", bg="black")
                lbl_total.place(x=10, y=50)

                entry_total = Entry(f2, font=("ariial", 20, "bold"), textvariable=Total_bill, bd=6, width=15,
                                    bg="lightgreen")
                entry_total.place(x=20, y=100)

                totalcost = c1 + c2 + c3 + c4 + c5 + c6 + c7 + c8 + c9
                string_bill = "$", str("%.2f" % totalcost)
                Total_bill.set(string_bill)

            def Reset():
                entry_Radisson_Blu_Hotel.delete(0, END)
                entry_Hyatt_Regency_Tashkent.delete(0, END)
                entry_Palace_Hotel_Tashkent.delete(0, END)
                entry_Cobalt.delete(0, END)
                entry_Captiva.delete(0, END)
                entry_Tracker.delete(0, END)
                entry_Central_Park.delete(0, END)
                entry_ECO_Park.delete(0, END)
                entry_Tashkent_City_Park.delete(0, END)

            Label(text="Travel&CO", bg="black", fg="white", font=("calibri", 33), width="300", height="2").pack()

            f = Frame(root, bg="lightblue", highlightbackground="black", highlightthickness=1, width=450, height=480)
            f.place(x=10, y=5)

            Label(f, text="Цены за услуги", font=("Gabriola", 40, "bold"), fg="black", bg="lightblue").place(x=80, y=0)

            Label(f, font=("comic sans", 15, "bold"), text="Radisson_Blu_Hotel 1.....25$/day", fg="black",
                  bg="lightblue").place(x=10, y=80)
            Label(f, font=("comic sans", 15, "bold"), text="Hyatt_Regency_Tashkent.....23$/day", fg="black",
                  bg="lightblue").place(x=10, y=110)
            Label(f, font=("comic sans", 15, "bold"), text="Palace_Hotel_Tashkent.....20$/day", fg="black",
                  bg="lightblue").place(x=10, y=140)
            Label(f, font=("comic sans", 15, "bold"), text="Cobalt.....50$/day", fg="black", bg="lightblue").place(x=10,
                                                                                                                   y=170)
            Label(f, font=("comic sans", 15, "bold"), text="Captiva.....70$/day", fg="black", bg="lightblue").place(
                x=10,
                y=200)
            Label(f, font=("comic sans", 15, "bold"), text="Tracker.....65$/day", fg="black", bg="lightblue").place(
                x=10,
                y=230)
            Label(f, font=("comic sans", 15, "bold"), text="Tashkent_City_Park.....2$/ticket", fg="black",
                  bg="lightblue").place(x=10, y=260)
            Label(f, font=("comic sans", 15, "bold"), text="ECO_Park.....1$/ticket", fg="black", bg="lightblue").place(
                x=10,
                y=290)
            Label(f, font=("comic sans", 15, "bold"), text="Central_Park.....3$/ticket", fg="black",
                  bg="lightblue").place(
                x=10, y=320)

            f2 = Frame(root, bg="lightyellow", highlightbackground="black", highlightthickness=1, width=300, height=480)
            f2.place(x=855, y=5)

            Bill = Label(f2, text="Счет", font=("calibri", 20), bg="lightyellow")
            Bill.place(x=120, y=10)

            f1 = Frame(root, bd=5, height=370, width=300, relief=RAISED)
            f1.place(x=460, y=5)

            Radisson_Blu_Hotel = StringVar()
            Hyatt_Regency_Tashkent = StringVar()
            Palace_Hotel_Tashkent = StringVar()
            Captiva = StringVar()
            Cobalt = StringVar()
            Tracker = StringVar()
            Tashkent_City_Park = StringVar()
            ECO_Park = StringVar()
            Central_Park = StringVar()
            Total_bill = StringVar()

            lbl_Radisson_Blu_Hotel = Label(f1, font=("aria", 15, "bold"), text="Radisson Blu Hotel", width=19,
                                           fg="Black")
            lbl_Hyatt_Regency_Tashkent = Label(f1, font=("aria", 15, "bold"), text="Hyatt Regency Tashkent", width=19,
                                               fg="Black")
            lbl_Palace_Hotel_Tashkent = Label(f1, font=("aria", 15, "bold"), text="Palace Hotel Tashkent", width=19,
                                              fg="Black")
            lbl_Captiva = Label(f1, font=("aria", 15, "bold"), text="Captiva", width=19, fg="Black")
            lbl_Cobalt = Label(f1, font=("aria", 15, "bold"), text="Cobalt", width=19, fg="Black")
            lbl_Tracker = Label(f1, font=("aria", 15, "bold"), text="Tracker", width=19, fg="Black")
            lbl_Tashkent_City_Park = Label(f1, font=("aria", 15, "bold"), text="Tashkent City Park", width=19,
                                           fg="Black")
            lbl_ECO_Park = Label(f1, font=("aria", 15, "bold"), text="ECO Park", width=19, fg="Black")
            lbl_Central_Park = Label(f1, font=("aria", 15, "bold"), text="Central Park", width=19, fg="Black")

            lbl_Radisson_Blu_Hotel.grid(row=1, column=0)
            lbl_Hyatt_Regency_Tashkent.grid(row=2, column=0)
            lbl_Palace_Hotel_Tashkent.grid(row=3, column=0)
            lbl_Captiva.grid(row=4, column=0)
            lbl_Cobalt.grid(row=5, column=0)
            lbl_Tracker.grid(row=6, column=0)
            lbl_Tashkent_City_Park.grid(row=7, column=0)
            lbl_ECO_Park.grid(row=8, column=0)
            lbl_Central_Park.grid(row=9, column=0)

            entry_Radisson_Blu_Hotel = Entry(f1, font=("aria", 20, "bold"), textvariable=Radisson_Blu_Hotel, bd=6,
                                             width=8,
                                             bg="lightgreen")
            entry_Hyatt_Regency_Tashkent = Entry(f1, font=("aria", 20, "bold"), textvariable=Hyatt_Regency_Tashkent,
                                                 bd=6,
                                                 width=8, bg="lightgreen")
            entry_Palace_Hotel_Tashkent = Entry(f1, font=("aria", 20, "bold"), textvariable=Palace_Hotel_Tashkent, bd=6,
                                                width=8, bg="lightgreen")
            entry_Captiva = Entry(f1, font=("aria", 20, "bold"), textvariable=Captiva, bd=6, width=8, bg="lightgreen")
            entry_Cobalt = Entry(f1, font=("aria", 20, "bold"), textvariable=Cobalt, bd=6, width=8, bg="lightgreen")
            entry_Tracker = Entry(f1, font=("aria", 20, "bold"), textvariable=Tracker, bd=6, width=8, bg="lightgreen")
            entry_Tashkent_City_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=Tashkent_City_Park, bd=6,
                                             width=8,
                                             bg="lightgreen")
            entry_ECO_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=ECO_Park, bd=6, width=8, bg="lightgreen")
            entry_Central_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=Central_Park, bd=6, width=8,
                                       bg="lightgreen")

            entry_Radisson_Blu_Hotel.grid(row=1, column=1)
            entry_Hyatt_Regency_Tashkent.grid(row=2, column=1)
            entry_Palace_Hotel_Tashkent.grid(row=3, column=1)
            entry_Captiva.grid(row=4, column=1)
            entry_Cobalt.grid(row=5, column=1)
            entry_Tracker.grid(row=6, column=1)
            entry_Tashkent_City_Park.grid(row=7, column=1)
            entry_ECO_Park.grid(row=8, column=1)
            entry_Central_Park.grid(row=9, column=1)
            btn_reset = Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, "bold"), width=10,
                               text="Очистить",
                               command=Reset)
            btn_reset.grid(row=10, column=0)

            btn_total = Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, "bold"), width=10, text="Итого",
                               command=Total)
            btn_total.grid(row=10, column=1)

    elif user == "u2" and code == "admin":
            root = Toplevel(screen)
            root.geometry("1160x500")
            root.title("Travel&CO")
            root.resizable(False, False)

            def Total():
                try:
                    a1 = int(Radisson_Blu_Hotel.get())
                except:
                    a1 = 0
                try:
                    a2 = int(Hyatt_Regency_Tashkent.get())
                except:
                    a2 = 0
                try:
                    a3 = int(Palace_Hotel_Tashkent.get())
                except:
                    a3 = 0
                try:
                    a4 = int(Cobalt.get())
                except:
                    a4 = 0
                try:
                    a5 = int(Captiva.get())
                except:
                    a5 = 0
                try:
                    a6 = int(Tracker.get())
                except:
                    a6 = 0
                try:
                    a7 = int(Central_Park.get())
                except:
                    a7 = 0
                try:
                    a8 = int(ECO_Park.get())
                except:
                    a8 = 0
                try:
                    a9 = int(Tashkent_City_Park.get())
                except:
                    a9 = 0

                c1 = 25 * a1
                c2 = 23 * a2
                c3 = 20 * a3
                c4 = 50 * a4
                c5 = 70 * a5
                c6 = 65 * a6
                c7 = 3 * a7
                c8 = 1 * a8
                c9 = 2 * a9

                lbl_total = Label(f2, font=("arial", 20, "bold"), text="Итого", width=16, fg="lightyellow", bg="black")
                lbl_total.place(x=10, y=50)

                entry_total = Entry(f2, font=("ariial", 20, "bold"), textvariable=Total_bill, bd=6, width=15,
                                    bg="lightgreen")
                entry_total.place(x=20, y=100)

                totalcost = c1 + c2 + c3 + c4 + c5 + c6 + c7 + c8 + c9
                string_bill = "$", str("%.2f" % totalcost)
                Total_bill.set(string_bill)

            def Reset():
                entry_Radisson_Blu_Hotel.delete(0, END)
                entry_Hyatt_Regency_Tashkent.delete(0, END)
                entry_Palace_Hotel_Tashkent.delete(0, END)
                entry_Cobalt.delete(0, END)
                entry_Captiva.delete(0, END)
                entry_Tracker.delete(0, END)
                entry_Central_Park.delete(0, END)
                entry_ECO_Park.delete(0, END)
                entry_Tashkent_City_Park.delete(0, END)

            Label(text="Travel&CO", bg="black", fg="white", font=("calibri", 33), width="300", height="2").pack()

            f = Frame(root, bg="lightblue", highlightbackground="black", highlightthickness=1, width=450, height=480)
            f.place(x=10, y=5)

            Label(f, text="Цены за услуги", font=("Gabriola", 40, "bold"), fg="black", bg="lightblue").place(x=80, y=0)

            Label(f, font=("comic sans", 15, "bold"), text="Radisson_Blu_Hotel 1.....25$/day", fg="black",
                  bg="lightblue").place(x=10, y=80)
            Label(f, font=("comic sans", 15, "bold"), text="Hyatt_Regency_Tashkent.....23$/day", fg="black",
                  bg="lightblue").place(x=10, y=110)
            Label(f, font=("comic sans", 15, "bold"), text="Palace_Hotel_Tashkent.....20$/day", fg="black",
                  bg="lightblue").place(x=10, y=140)
            Label(f, font=("comic sans", 15, "bold"), text="Cobalt.....50$/day", fg="black", bg="lightblue").place(x=10,
                                                                                                                   y=170)
            Label(f, font=("comic sans", 15, "bold"), text="Captiva.....70$/day", fg="black", bg="lightblue").place(
                x=10,
                y=200)
            Label(f, font=("comic sans", 15, "bold"), text="Tracker.....65$/day", fg="black", bg="lightblue").place(
                x=10,
                y=230)
            Label(f, font=("comic sans", 15, "bold"), text="Tashkent_City_Park.....2$/ticket", fg="black",
                  bg="lightblue").place(x=10, y=260)
            Label(f, font=("comic sans", 15, "bold"), text="ECO_Park.....1$/ticket", fg="black", bg="lightblue").place(
                x=10,
                y=290)
            Label(f, font=("comic sans", 15, "bold"), text="Central_Park.....3$/ticket", fg="black",
                  bg="lightblue").place(
                x=10, y=320)

            f2 = Frame(root, bg="lightyellow", highlightbackground="black", highlightthickness=1, width=300, height=480)
            f2.place(x=855, y=5)

            Bill = Label(f2, text="Счет", font=("calibri", 20), bg="lightyellow")
            Bill.place(x=120, y=10)

            f1 = Frame(root, bd=5, height=370, width=300, relief=RAISED)
            f1.place(x=460, y=5)

            Radisson_Blu_Hotel = StringVar()
            Hyatt_Regency_Tashkent = StringVar()
            Palace_Hotel_Tashkent = StringVar()
            Captiva = StringVar()
            Cobalt = StringVar()
            Tracker = StringVar()
            Tashkent_City_Park = StringVar()
            ECO_Park = StringVar()
            Central_Park = StringVar()
            Total_bill = StringVar()

            lbl_Radisson_Blu_Hotel = Label(f1, font=("aria", 15, "bold"), text="Radisson Blu Hotel", width=19,
                                           fg="Black")
            lbl_Hyatt_Regency_Tashkent = Label(f1, font=("aria", 15, "bold"), text="Hyatt Regency Tashkent", width=19,
                                               fg="Black")
            lbl_Palace_Hotel_Tashkent = Label(f1, font=("aria", 15, "bold"), text="Palace Hotel Tashkent", width=19,
                                              fg="Black")
            lbl_Captiva = Label(f1, font=("aria", 15, "bold"), text="Captiva", width=19, fg="Black")
            lbl_Cobalt = Label(f1, font=("aria", 15, "bold"), text="Cobalt", width=19, fg="Black")
            lbl_Tracker = Label(f1, font=("aria", 15, "bold"), text="Tracker", width=19, fg="Black")
            lbl_Tashkent_City_Park = Label(f1, font=("aria", 15, "bold"), text="Tashkent City Park", width=19,
                                           fg="Black")
            lbl_ECO_Park = Label(f1, font=("aria", 15, "bold"), text="ECO Park", width=19, fg="Black")
            lbl_Central_Park = Label(f1, font=("aria", 15, "bold"), text="Central Park", width=19, fg="Black")

            lbl_Radisson_Blu_Hotel.grid(row=1, column=0)
            lbl_Hyatt_Regency_Tashkent.grid(row=2, column=0)
            lbl_Palace_Hotel_Tashkent.grid(row=3, column=0)
            lbl_Captiva.grid(row=4, column=0)
            lbl_Cobalt.grid(row=5, column=0)
            lbl_Tracker.grid(row=6, column=0)
            lbl_Tashkent_City_Park.grid(row=7, column=0)
            lbl_ECO_Park.grid(row=8, column=0)
            lbl_Central_Park.grid(row=9, column=0)

            entry_Radisson_Blu_Hotel = Entry(f1, font=("aria", 20, "bold"), textvariable=Radisson_Blu_Hotel, bd=6,
                                             width=8,
                                             bg="lightgreen")
            entry_Hyatt_Regency_Tashkent = Entry(f1, font=("aria", 20, "bold"), textvariable=Hyatt_Regency_Tashkent,
                                                 bd=6,
                                                 width=8, bg="lightgreen")
            entry_Palace_Hotel_Tashkent = Entry(f1, font=("aria", 20, "bold"), textvariable=Palace_Hotel_Tashkent, bd=6,
                                                width=8, bg="lightgreen")
            entry_Captiva = Entry(f1, font=("aria", 20, "bold"), textvariable=Captiva, bd=6, width=8, bg="lightgreen")
            entry_Cobalt = Entry(f1, font=("aria", 20, "bold"), textvariable=Cobalt, bd=6, width=8, bg="lightgreen")
            entry_Tracker = Entry(f1, font=("aria", 20, "bold"), textvariable=Tracker, bd=6, width=8, bg="lightgreen")
            entry_Tashkent_City_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=Tashkent_City_Park, bd=6,
                                             width=8,
                                             bg="lightgreen")
            entry_ECO_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=ECO_Park, bd=6, width=8, bg="lightgreen")
            entry_Central_Park = Entry(f1, font=("aria", 20, "bold"), textvariable=Central_Park, bd=6, width=8,
                                       bg="lightgreen")

            entry_Radisson_Blu_Hotel.grid(row=1, column=1)
            entry_Hyatt_Regency_Tashkent.grid(row=2, column=1)
            entry_Palace_Hotel_Tashkent.grid(row=3, column=1)
            entry_Captiva.grid(row=4, column=1)
            entry_Cobalt.grid(row=5, column=1)
            entry_Tracker.grid(row=6, column=1)
            entry_Tashkent_City_Park.grid(row=7, column=1)
            entry_ECO_Park.grid(row=8, column=1)
            entry_Central_Park.grid(row=9, column=1)
            btn_reset = Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, "bold"), width=10,
                               text="Очистить",
                               command=Reset)
            btn_reset.grid(row=10, column=0)

            btn_total = Button(f1, bd=5, fg="black", bg="lightblue", font=("ariel", 16, "bold"), width=10, text="Итого",
                               command=Total)
            btn_total.grid(row=10, column=1)

    elif user == "" and code == "":
        messagebox.showerror("Error", "Please enter Username and Password")
    elif user == "":
        messagebox.showerror("Error", "Username is required")
    elif code == "":
        messagebox.showerror("Error", "Password field is required")
    elif user != "u1" or "u2":
        messagebox.showerror("Error", "Wrong user")
    elif code != "user1" or "user2" or "admin":
        messagebox.showerror("Error", "Wrong Password")
    elif user == "" and code == "":
        messagebox.showerror()
    elif user == "" and code == "":
        messagebox.showerror()


def main_screen():
    global screen
    global username
    global password


screen = Tk()
screen.geometry("1280x720+150+150")
screen.configure(bg="#ffffff")

image_icon = PhotoImage(file="icon.png")
screen.iconphoto(False, image_icon)
screen.title("Login system")

lblTitle = Label(text="Login system", font=("arial", 50, "bold"), fg="black", bg="#ffffff")
lblTitle.pack(pady=50)

bordercolor = Frame(screen, bg="black", width=800, height=400)
bordercolor.pack()

mainframe = Frame(bordercolor, bg="#ffffff", width=800, height=400)
mainframe.pack(padx=20, pady=20)

Label(mainframe, text="Username", font=("arial", 30, "bold"), bg='#ffffff').place(x=100, y=50)
Label(mainframe, text="Password", font=("arial", 30, "bold"), bg='#ffffff').place(x=100, y=150)

username = StringVar()
password = StringVar()

entry_username = Entry(mainframe, textvariable=username, width=12, bd=2, font=("arial,30"))
entry_username.place(x=400, y=50)
entry_password = Entry(mainframe, textvariable=password, width=12, bd=2, font=("arial,30"))
entry_password.place(x=400, y=150)


def clear():
    entry_username.delete(0, END)
    entry_password.delete(0, END)


Button(mainframe, text="Login", height="2", width=23, bg="#ed3833", fg="white", bd=0, command=login).place(x=100, y=250)
Button(mainframe, text="Clear", height="2", width=23, bg="#1089ff", fg="white", bd=0, command=clear).place(x=300, y=250)
Button(mainframe, text="Exit", height="2", width=23, bg="#00bd56", fg="white", bd=0, command=screen.destroy).place(x=500, y=250)

screen.mainloop()
