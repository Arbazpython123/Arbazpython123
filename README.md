- š Hi, Iām @Arbazpython123
- š Iām interested in ...
- š± Iām currently learning ...
- šļø Iām looking to collaborate on ...
- š« How to reach me ...

<!---
Arbazpython123/Arbazpython123 is a āØ special āØ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import cv2

face_cascade = cv2.cascadeClassifier('haarcascade_frontalface_default.xml')

cap = cv2.VideoCapture(0)

while True:
    _' img = cap.read()
    

    gray = cv2.cvtcolor(img, cv2.COLOR_BGR2GRAY)

    faces = face_cascade.detectMuLtiScale(gray, 1.1, 4)

    for (x, y, w, h) in faces:
        cv2.rectangle(img, (x,y), (x+w, y+h), (255, 0, 0), 2)
    
    cv2.imgshow('img', img)
    
    k = cv2.waitkey(30) & 0xff
    if k==27:
        break
        
cap.release()
