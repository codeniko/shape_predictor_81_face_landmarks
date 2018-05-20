81 Facial Landmarks Shape Predictor
===============
This is a custom shape predictor model trained to find 81 facial feature landmarks given any image.

It's trained similar to dlib's 68 facial landmark shape predictor. In addition to the original 68 facial landmarks, I added an additional 13 landmarks to cover the forehead area. This allows for precise head detection and for image operations that require points along the top of the head, for example when [placing a hat on someone's head.](https://github.com/codeniko/shape_predictor_81_face_landmarks/raw/master/transformation_example.bmp)

The additional 13 points were extract using my fork of eos by patrikhuber: https://github.com/codeniko/eos. I continued to use the Surrey Face Model and made note of 13 points that I thought were the perfect fit for my use case. I made the modifications here, then ran it on the entire ibug large database of images to overwrite each image's 68 landmark coordinates with my 81 landmark coordinates. From here, the training for the shape predictor model can proceed using http://dlib.net/train_shape_predictor.py.html

Check out this live example video of 81 landmark detection in action: [https://www.youtube.com/watch?v=mDJrASIB1T0](https://www.youtube.com/watch?v=mDJrASIB1T0)

81 landmarks reference
----------------
<img src="https://github.com/codeniko/shape_predictor_81_face_landmarks/raw/master/81_facial_landmarks_reference.jpg" alt="81 landmarks reference image"></img>
