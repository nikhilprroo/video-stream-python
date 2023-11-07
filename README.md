import cv2
cap = cv2.VideoCapture(0)
while True:
    status,photo=cap.read()
    a=photo[100:300,250:450]
    b=photo[100:300,250:450]
    photo[0:200,0:200]=a


    photo[280:480,440:640]=b
    cv2.imshow("My window",photo)
    if cv2.waitKey(100)==13:
        break
    cv2.destroyAllWindows()
    cap.release()
