# task 3
## the aim was to learn *how to run a python script* and *create a cloud function*
1.  first, I opened the terminal in Cloud Shell and wrote:
```
vim hello.py
```
2. after that, I pressed: **ESC** then **SHIFT+I**, thanks to that, it will allow VIM to enter the *INSERT* mode. In the INSERT mode, I am able to edit the file (which is empty for now)
3. in the *INSERT* mode I typed:
```
print('Hello DareIT')
```
4. pressed **ESC**, then typed **:wq** end pressed **Enter** to go out
5. mini info: ![dareITminiinfopic](https://user-images.githubusercontent.com/125319277/231571490-13b3a440-5b5c-4740-a52a-691cb69cb15e.jpg)
6. that, what I've done was creating the first python script, the script is stored in our [hello.py](<http://hello.py>) file. In order to run it, I can type in the terminal:
 ```
 python hello.py
 ```
7. after this, **Hello DareIT** is printed in the terminal :smiley:
8. the second step of the task is to create a **Cloud Function**
9. to do that, I went in Google Console, in the *Navigation Menu* (or by writing it search field), I chose **Cloud Function** --> then **CREATE FUNCTION**
10. after enabling APIs (*Cloud logging API*), the next thing to choose was the *trigger type*, in this case: **HTTP**
11. in *Runtime and Build section* (where are the settings for RAM), I left the default 256 MB
12. then I pressed **save**, after that appeard an Editor in which I Choose **Python3.7** from the Runtime dropdown
13. I changed the ***Hello World*** in the *main.py* to other text --> ***I am learning and this is fun*** and pressed **Save**
14. and I have triggered the *execution of the Cloud Function*
15. after that, I copied the url from the *Trigger tab* and pasted it into my browser
16. the result: ![dareITcloudfunctionpic](https://user-images.githubusercontent.com/125319277/231577840-6dd289e6-814a-4f43-a94f-11d3e7f1b7a3.jpg)
17. that what I've done was activation an execution of a piece of code run using Cloud Function :smile:
