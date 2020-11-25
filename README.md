# Youtube-video-downloader-using-python-pytube-
//Using pytube library of python you can download youtube videos,i have used try and exception here.

from pytube import YouTube 

link = input("please provide link:\n")
print("Title:",YouTube(link).title)
print("Duration:",YouTube(link).length)
print("Description:",YouTube(link).description)

try:
    yt = YouTube(link)
except:
    print("Unknown error")

try:
    yt.streams.filter().get_lowest_resolution().download('D:/')
    print("Downloaded successfully")
except:
    print("Try again")

print("Thank you")
