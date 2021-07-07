# Assignment-5

import pytube

import tkinter as tk
from pytube import YouTube

#to display the window
win=tk.Tk()
win.geometry('500x300')
win.resizable(0,0)
win.title("YouTube Video Downloader By:-DIKSHA MAHALE")
tk.Label(win,text="YouTube Video Downloader",font="Calibri 20 bold").pack()

#to enter the URL
link=to.StringVar()
tk.Label(win,text="PASTE THE LINK BELOW",font="Cambria 15 bold").place(X=140,y=60)
link_error=tk.Entry(win, width=70, textvariable=link).place(X=34,y=90)

#function to download the video
def Video_Downloader():
    url=YouTube (str(link.get()))
    video=url.streams.first()
    video.download()
    tk.Label(win,text="Your video has been successfully downloaded",font="arial 15").place(X=180,y=200)

#to display the download button
tk.Label(win,text="DOWNLOAD",font="Cochin 15 bold",bf="light blue",padx=2, command=Video_Downloader).place(X=180,y=150)

win.mainloop()
