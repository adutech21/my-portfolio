# my-portfolio
# HOW TO DOWNLOAD YOUTUBE VIDEO USING PYTHON
#INSTALL PYTUBE
pip install pytube


#HERE IS THE CODE TO DOWNLOAD ANY VIDEO
from pytube import YouTube

yt = YouTube(" INPUT YOUR YOUTUBE URL HERE!!! ")
streams = yt.streams.filter(progressive=True, file_extension='mp4').order_by('resolution').desc()
video = streams.first()
video.download()
