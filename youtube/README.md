## download video or playlist from youtube

```python

from pytube import YouTube
from pytube import Playlist

# # FOR VIDEO
# yt = YouTube("https://www.youtube.com/watch?v=Yh5Lil03tpI")
# stream = yt.streams.get_by_itag(22)
#
# stream.download()
# print("the end")

# FOR PLAYLIST
node_js ="https://www.youtube.com/watch?v=Oe421EPjeBE"
async_javascript="https://www.youtube.com/watch?v=iWOYAxlnaww&list=PL4cUxeGkcC9haFPT7J25Q9GRB_ZkFrQAc"
jwt_2="https://www.youtube.com/watch?v=mbsmsi7l3r4"
jwt="https://www.youtube.com/watch?v=SnoAwLP1a-0&list=PL4cUxeGkcC9iqqESP8335DA5cRFp8loyp"
django = "https://www.youtube.com/watch?v=UmljXZIypDc&list=PL-osiE80TeTtoQCKZ03TU5fNfx2UY6U4p"
p = Playlist(node_js)

print(f'Downloading: {p.title}')
for video in p.videos:
    stream = video.streams.get_by_itag(22)
    print(stream)
    stream.download()

print("THe End")

```
